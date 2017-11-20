# -*-python-*-

import os
from SCons.Errors import EnvironmentError

env = Environment(tools = ['prefix'])

VariantDir('build', 'src')
try:
  SConscript(os.path.join('build', 'cpp', 'SConscript'), exports="env")
except EnvironmentError:
  pass
except Exception:
  raise
try:
  SConscript(os.path.join('build', 'py', 'SConscript'), exports="env")
except EnvironmentError:
  pass
except Exception:
  raise
    
Default("install")
