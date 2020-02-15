# 於windows安裝完tensorflow 2.1 出現如下錯誤  

原因是因為需要安裝Visual C++語言套件
[下載網址](https://support.microsoft.com/en-us/help/2977003/the-latest-supported-visual-c-downloads)

[x86: vc_redist.x86.exe](https://aka.ms/vs/16/release/vc_redist.x86.exe)
[x64: vc_redist.x64.exe](https://aka.ms/vs/16/release/vc_redist.x64.exe)
[ARM64: vc_redist.arm64.exe](https://aka.ms/vs/16/release/vc_redist.x64.exe)

安裝完成之後可以解決這個問題

```
Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow.py", line 58, in <module>
    from tensorflow.python.pywrap_tensorflow_internal import *
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 28, in <module>
    _pywrap_tensorflow_internal = swig_import_helper()
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 24, in swig_import_helper
    _mod = imp.load_module('_pywrap_tensorflow_internal', fp, pathname, description)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 242, in load_module
    return load_dynamic(name, filename, file)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 342, in load_dynamic
    return _load(spec)
ImportError: DLL load failed: 找不到指定的模組。

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\interactiveshell.py", line 3331, in run_code
    exec(code_obj, self.user_global_ns, self.user_ns)
  File "<ipython-input-1-f79e48826468>", line 1, in <module>
    import tensorflow as tf
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow\__init__.py", line 101, in <module>
    from tensorflow_core import *
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\__init__.py", line 40, in <module>
    from tensorflow.python.tools import module_util as _module_util
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow\__init__.py", line 50, in __getattr__
    module = self._load()
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow\__init__.py", line 44, in _load
    module = _importlib.import_module(self.__name__)
  File "c:\users\aking\.conda\envs\tf21\lib\importlib\__init__.py", line 127, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\__init__.py", line 49, in <module>
    from tensorflow.python import pywrap_tensorflow
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow.py", line 74, in <module>
    raise ImportError(msg)
ImportError: Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow.py", line 58, in <module>
    from tensorflow.python.pywrap_tensorflow_internal import *
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 28, in <module>
    _pywrap_tensorflow_internal = swig_import_helper()
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 24, in swig_import_helper
    _mod = imp.load_module('_pywrap_tensorflow_internal', fp, pathname, description)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 242, in load_module
    return load_dynamic(name, filename, file)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 342, in load_dynamic
    return _load(spec)
ImportError: DLL load failed: 找不到指定的模組。


Failed to load the native TensorFlow runtime.

See https://www.tensorflow.org/install/errors

for some common reasons and solutions.  Include the entire stack trace
above this error message when asking for help.

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\interactiveshell.py", line 2044, in showtraceback
    stb = value._render_traceback_()
AttributeError: 'ImportError' object has no attribute '_render_traceback_'

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow.py", line 58, in <module>
    from tensorflow.python.pywrap_tensorflow_internal import *
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 28, in <module>
    _pywrap_tensorflow_internal = swig_import_helper()
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 24, in swig_import_helper
    _mod = imp.load_module('_pywrap_tensorflow_internal', fp, pathname, description)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 242, in load_module
    return load_dynamic(name, filename, file)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 342, in load_dynamic
    return _load(spec)
ImportError: DLL load failed: 找不到指定的模組。

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\ultratb.py", line 1151, in get_records
    return _fixed_getinnerframes(etb, number_of_lines_of_context, tb_offset)
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\ultratb.py", line 319, in wrapped
    return f(*args, **kwargs)
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\ultratb.py", line 353, in _fixed_getinnerframes
    records = fix_frame_records_filenames(inspect.getinnerframes(etb, context))
  File "c:\users\aking\.conda\envs\tf21\lib\inspect.py", line 1502, in getinnerframes
    frameinfo = (tb.tb_frame,) + getframeinfo(tb, context)
  File "c:\users\aking\.conda\envs\tf21\lib\inspect.py", line 1460, in getframeinfo
    filename = getsourcefile(frame) or getfile(frame)
  File "c:\users\aking\.conda\envs\tf21\lib\inspect.py", line 696, in getsourcefile
    if getattr(getmodule(object, filename), '__loader__', None) is not None:
  File "c:\users\aking\.conda\envs\tf21\lib\inspect.py", line 733, in getmodule
    if ismodule(module) and hasattr(module, '__file__'):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow\__init__.py", line 50, in __getattr__
    module = self._load()
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow\__init__.py", line 44, in _load
    module = _importlib.import_module(self.__name__)
  File "c:\users\aking\.conda\envs\tf21\lib\importlib\__init__.py", line 127, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
  File "<frozen importlib._bootstrap>", line 1006, in _gcd_import
  File "<frozen importlib._bootstrap>", line 983, in _find_and_load
  File "<frozen importlib._bootstrap>", line 953, in _find_and_load_unlocked
  File "<frozen importlib._bootstrap>", line 219, in _call_with_frames_removed
  File "<frozen importlib._bootstrap>", line 1006, in _gcd_import
  File "<frozen importlib._bootstrap>", line 983, in _find_and_load
  File "<frozen importlib._bootstrap>", line 967, in _find_and_load_unlocked
  File "<frozen importlib._bootstrap>", line 677, in _load_unlocked
  File "<frozen importlib._bootstrap_external>", line 728, in exec_module
  File "<frozen importlib._bootstrap>", line 219, in _call_with_frames_removed
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\__init__.py", line 42, in <module>
    from . _api.v2 import audio
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\_api\v2\audio\__init__.py", line 10, in <module>
    from tensorflow.python.ops.gen_audio_ops import decode_wav
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\ops\gen_audio_ops.py", line 9, in <module>
    from tensorflow.python import pywrap_tensorflow as _pywrap_tensorflow
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow\__init__.py", line 50, in __getattr__
    module = self._load()
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow\__init__.py", line 44, in _load
    module = _importlib.import_module(self.__name__)
  File "c:\users\aking\.conda\envs\tf21\lib\importlib\__init__.py", line 127, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\__init__.py", line 49, in <module>
    from tensorflow.python import pywrap_tensorflow
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow.py", line 74, in <module>
    raise ImportError(msg)
ImportError: Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow.py", line 58, in <module>
    from tensorflow.python.pywrap_tensorflow_internal import *
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 28, in <module>
    _pywrap_tensorflow_internal = swig_import_helper()
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 24, in swig_import_helper
    _mod = imp.load_module('_pywrap_tensorflow_internal', fp, pathname, description)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 242, in load_module
    return load_dynamic(name, filename, file)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 342, in load_dynamic
    return _load(spec)
ImportError: DLL load failed: 找不到指定的模組。

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\interactiveshell.py", line 3331, in run_code
    exec(code_obj, self.user_global_ns, self.user_ns)
  File "<ipython-input-1-f79e48826468>", line 1, in <module>
    import tensorflow as tf
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow\__init__.py", line 101, in <module>
    from tensorflow_core import *
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\__init__.py", line 40, in <module>
    from tensorflow.python.tools import module_util as _module_util
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow\__init__.py", line 50, in __getattr__
    module = self._load()
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow\__init__.py", line 44, in _load
    module = _importlib.import_module(self.__name__)
  File "c:\users\aking\.conda\envs\tf21\lib\importlib\__init__.py", line 127, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\__init__.py", line 49, in <module>
    from tensorflow.python import pywrap_tensorflow
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow.py", line 74, in <module>
    raise ImportError(msg)
ImportError: Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow.py", line 58, in <module>
    from tensorflow.python.pywrap_tensorflow_internal import *
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 28, in <module>
    _pywrap_tensorflow_internal = swig_import_helper()
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 24, in swig_import_helper
    _mod = imp.load_module('_pywrap_tensorflow_internal', fp, pathname, description)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 242, in load_module
    return load_dynamic(name, filename, file)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 342, in load_dynamic
    return _load(spec)
ImportError: DLL load failed: 找不到指定的模組。


Failed to load the native TensorFlow runtime.

See https://www.tensorflow.org/install/errors

for some common reasons and solutions.  Include the entire stack trace
above this error message when asking for help.

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\interactiveshell.py", line 2044, in showtraceback
    stb = value._render_traceback_()
AttributeError: 'ImportError' object has no attribute '_render_traceback_'

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow.py", line 58, in <module>
    from tensorflow.python.pywrap_tensorflow_internal import *
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 28, in <module>
    _pywrap_tensorflow_internal = swig_import_helper()
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 24, in swig_import_helper
    _mod = imp.load_module('_pywrap_tensorflow_internal', fp, pathname, description)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 242, in load_module
    return load_dynamic(name, filename, file)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 342, in load_dynamic
    return _load(spec)
ImportError: DLL load failed: 找不到指定的模組。


Failed to load the native TensorFlow runtime.

See https://www.tensorflow.org/install/errors

for some common reasons and solutions.  Include the entire stack trace
above this error message when asking for help.
Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow.py", line 58, in <module>
    from tensorflow.python.pywrap_tensorflow_internal import *
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 28, in <module>
    _pywrap_tensorflow_internal = swig_import_helper()
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 24, in swig_import_helper
    _mod = imp.load_module('_pywrap_tensorflow_internal', fp, pathname, description)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 242, in load_module
    return load_dynamic(name, filename, file)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 342, in load_dynamic
    return _load(spec)
ImportError: DLL load failed: 找不到指定的模組。

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\interactiveshell.py", line 3331, in run_code
    exec(code_obj, self.user_global_ns, self.user_ns)
  File "<ipython-input-1-f79e48826468>", line 1, in <module>
    import tensorflow as tf
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow\__init__.py", line 101, in <module>
    from tensorflow_core import *
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\__init__.py", line 40, in <module>
    from tensorflow.python.tools import module_util as _module_util
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow\__init__.py", line 50, in __getattr__
    module = self._load()
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow\__init__.py", line 44, in _load
    module = _importlib.import_module(self.__name__)
  File "c:\users\aking\.conda\envs\tf21\lib\importlib\__init__.py", line 127, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\__init__.py", line 49, in <module>
    from tensorflow.python import pywrap_tensorflow
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow.py", line 74, in <module>
    raise ImportError(msg)
ImportError: Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow.py", line 58, in <module>
    from tensorflow.python.pywrap_tensorflow_internal import *
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 28, in <module>
    _pywrap_tensorflow_internal = swig_import_helper()
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 24, in swig_import_helper
    _mod = imp.load_module('_pywrap_tensorflow_internal', fp, pathname, description)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 242, in load_module
    return load_dynamic(name, filename, file)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 342, in load_dynamic
    return _load(spec)
ImportError: DLL load failed: 找不到指定的模組。


Failed to load the native TensorFlow runtime.

See https://www.tensorflow.org/install/errors

for some common reasons and solutions.  Include the entire stack trace
above this error message when asking for help.

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\interactiveshell.py", line 2044, in showtraceback
    stb = value._render_traceback_()
AttributeError: 'ImportError' object has no attribute '_render_traceback_'

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\interactiveshell.py", line 3254, in run_ast_nodes
    if (await self.run_code(code, result,  async_=asy)):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\interactiveshell.py", line 3348, in run_code
    self.showtraceback(running_compiled_code=True)
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\interactiveshell.py", line 2047, in showtraceback
    value, tb, tb_offset=tb_offset)
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\ultratb.py", line 1418, in structured_traceback
    self, etype, value, tb, tb_offset, number_of_lines_of_context)
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\ultratb.py", line 1318, in structured_traceback
    self, etype, value, tb, tb_offset, number_of_lines_of_context
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\ultratb.py", line 1186, in structured_traceback
    formatted_exceptions += self.prepare_chained_exception_message(evalue.__cause__)
TypeError: can only concatenate str (not "list") to str

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\interactiveshell.py", line 2044, in showtraceback
    stb = value._render_traceback_()
AttributeError: 'TypeError' object has no attribute '_render_traceback_'

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow.py", line 58, in <module>
    from tensorflow.python.pywrap_tensorflow_internal import *
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 28, in <module>
    _pywrap_tensorflow_internal = swig_import_helper()
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 24, in swig_import_helper
    _mod = imp.load_module('_pywrap_tensorflow_internal', fp, pathname, description)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 242, in load_module
    return load_dynamic(name, filename, file)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 342, in load_dynamic
    return _load(spec)
ImportError: DLL load failed: 找不到指定的模組。

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\ultratb.py", line 1151, in get_records
    return _fixed_getinnerframes(etb, number_of_lines_of_context, tb_offset)
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\ultratb.py", line 319, in wrapped
    return f(*args, **kwargs)
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\ultratb.py", line 353, in _fixed_getinnerframes
    records = fix_frame_records_filenames(inspect.getinnerframes(etb, context))
  File "c:\users\aking\.conda\envs\tf21\lib\inspect.py", line 1502, in getinnerframes
    frameinfo = (tb.tb_frame,) + getframeinfo(tb, context)
  File "c:\users\aking\.conda\envs\tf21\lib\inspect.py", line 1460, in getframeinfo
    filename = getsourcefile(frame) or getfile(frame)
  File "c:\users\aking\.conda\envs\tf21\lib\inspect.py", line 696, in getsourcefile
    if getattr(getmodule(object, filename), '__loader__', None) is not None:
  File "c:\users\aking\.conda\envs\tf21\lib\inspect.py", line 733, in getmodule
    if ismodule(module) and hasattr(module, '__file__'):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow\__init__.py", line 50, in __getattr__
    module = self._load()
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow\__init__.py", line 44, in _load
    module = _importlib.import_module(self.__name__)
  File "c:\users\aking\.conda\envs\tf21\lib\importlib\__init__.py", line 127, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
  File "<frozen importlib._bootstrap>", line 1006, in _gcd_import
  File "<frozen importlib._bootstrap>", line 983, in _find_and_load
  File "<frozen importlib._bootstrap>", line 953, in _find_and_load_unlocked
  File "<frozen importlib._bootstrap>", line 219, in _call_with_frames_removed
  File "<frozen importlib._bootstrap>", line 1006, in _gcd_import
  File "<frozen importlib._bootstrap>", line 983, in _find_and_load
  File "<frozen importlib._bootstrap>", line 967, in _find_and_load_unlocked
  File "<frozen importlib._bootstrap>", line 677, in _load_unlocked
  File "<frozen importlib._bootstrap_external>", line 728, in exec_module
  File "<frozen importlib._bootstrap>", line 219, in _call_with_frames_removed
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\__init__.py", line 42, in <module>
    from . _api.v2 import audio
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\_api\v2\audio\__init__.py", line 10, in <module>
    from tensorflow.python.ops.gen_audio_ops import decode_wav
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\ops\gen_audio_ops.py", line 9, in <module>
    from tensorflow.python import pywrap_tensorflow as _pywrap_tensorflow
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow\__init__.py", line 50, in __getattr__
    module = self._load()
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow\__init__.py", line 44, in _load
    module = _importlib.import_module(self.__name__)
  File "c:\users\aking\.conda\envs\tf21\lib\importlib\__init__.py", line 127, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\__init__.py", line 49, in <module>
    from tensorflow.python import pywrap_tensorflow
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow.py", line 74, in <module>
    raise ImportError(msg)
ImportError: Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow.py", line 58, in <module>
    from tensorflow.python.pywrap_tensorflow_internal import *
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 28, in <module>
    _pywrap_tensorflow_internal = swig_import_helper()
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 24, in swig_import_helper
    _mod = imp.load_module('_pywrap_tensorflow_internal', fp, pathname, description)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 242, in load_module
    return load_dynamic(name, filename, file)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 342, in load_dynamic
    return _load(spec)
ImportError: DLL load failed: 找不到指定的模組。

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\interactiveshell.py", line 3331, in run_code
    exec(code_obj, self.user_global_ns, self.user_ns)
  File "<ipython-input-1-f79e48826468>", line 1, in <module>
    import tensorflow as tf
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow\__init__.py", line 101, in <module>
    from tensorflow_core import *
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\__init__.py", line 40, in <module>
    from tensorflow.python.tools import module_util as _module_util
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow\__init__.py", line 50, in __getattr__
    module = self._load()
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow\__init__.py", line 44, in _load
    module = _importlib.import_module(self.__name__)
  File "c:\users\aking\.conda\envs\tf21\lib\importlib\__init__.py", line 127, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\__init__.py", line 49, in <module>
    from tensorflow.python import pywrap_tensorflow
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow.py", line 74, in <module>
    raise ImportError(msg)
ImportError: Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow.py", line 58, in <module>
    from tensorflow.python.pywrap_tensorflow_internal import *
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 28, in <module>
    _pywrap_tensorflow_internal = swig_import_helper()
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 24, in swig_import_helper
    _mod = imp.load_module('_pywrap_tensorflow_internal', fp, pathname, description)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 242, in load_module
    return load_dynamic(name, filename, file)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 342, in load_dynamic
    return _load(spec)
ImportError: DLL load failed: 找不到指定的模組。


Failed to load the native TensorFlow runtime.

See https://www.tensorflow.org/install/errors

for some common reasons and solutions.  Include the entire stack trace
above this error message when asking for help.

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\interactiveshell.py", line 2044, in showtraceback
    stb = value._render_traceback_()
AttributeError: 'ImportError' object has no attribute '_render_traceback_'

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\interactiveshell.py", line 3254, in run_ast_nodes
    if (await self.run_code(code, result,  async_=asy)):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\interactiveshell.py", line 3348, in run_code
    self.showtraceback(running_compiled_code=True)
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\interactiveshell.py", line 2047, in showtraceback
    value, tb, tb_offset=tb_offset)
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\ultratb.py", line 1418, in structured_traceback
    self, etype, value, tb, tb_offset, number_of_lines_of_context)
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\ultratb.py", line 1318, in structured_traceback
    self, etype, value, tb, tb_offset, number_of_lines_of_context
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\ultratb.py", line 1186, in structured_traceback
    formatted_exceptions += self.prepare_chained_exception_message(evalue.__cause__)
TypeError: can only concatenate str (not "list") to str

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\interactiveshell.py", line 2044, in showtraceback
    stb = value._render_traceback_()
AttributeError: 'TypeError' object has no attribute '_render_traceback_'

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow.py", line 58, in <module>
    from tensorflow.python.pywrap_tensorflow_internal import *
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 28, in <module>
    _pywrap_tensorflow_internal = swig_import_helper()
  File "c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py", line 24, in swig_import_helper
    _mod = imp.load_module('_pywrap_tensorflow_internal', fp, pathname, description)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 242, in load_module
    return load_dynamic(name, filename, file)
  File "c:\users\aking\.conda\envs\tf21\lib\imp.py", line 342, in load_dynamic
    return _load(spec)
ImportError: DLL load failed: 找不到指定的模組。


Failed to load the native TensorFlow runtime.

See https://www.tensorflow.org/install/errors

for some common reasons and solutions.  Include the entire stack trace
above this error message when asking for help.
---------------------------------------------------------------------------
ImportError                               Traceback (most recent call last)
c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow.py in <module>
     57 
---> 58   from tensorflow.python.pywrap_tensorflow_internal import *
     59   from tensorflow.python.pywrap_tensorflow_internal import __version__

c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py in <module>
     27             return _mod
---> 28     _pywrap_tensorflow_internal = swig_import_helper()
     29     del swig_import_helper

c:\users\aking\.conda\envs\tf21\lib\site-packages\tensorflow_core\python\pywrap_tensorflow_internal.py in swig_import_helper()
     23             try:
---> 24                 _mod = imp.load_module('_pywrap_tensorflow_internal', fp, pathname, description)
     25             finally:

c:\users\aking\.conda\envs\tf21\lib\imp.py in load_module(name, file, filename, details)
    241         else:
--> 242             return load_dynamic(name, filename, file)
    243     elif type_ == PKG_DIRECTORY:

c:\users\aking\.conda\envs\tf21\lib\imp.py in load_dynamic(name, path, file)
    341             name=name, loader=loader, origin=path)
--> 342         return _load(spec)
    343 

ImportError: DLL load failed: 找不到指定的模組。

During handling of the above exception, another exception occurred:


During handling of the above exception, another exception occurred:

AttributeError                            Traceback (most recent call last)
c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\interactiveshell.py in showtraceback(self, exc_tuple, filename, tb_offset, exception_only, running_compiled_code)
   2043                         # in the engines. This should return a list of strings.
-> 2044                         stb = value._render_traceback_()
   2045                     except Exception:

AttributeError: 'ImportError' object has no attribute '_render_traceback_'

During handling of the above exception, another exception occurred:

TypeError                                 Traceback (most recent call last)
c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\interactiveshell.py in run_code(self, code_obj, result, async_)
   3346             if result is not None:
   3347                 result.error_in_exec = sys.exc_info()[1]
-> 3348             self.showtraceback(running_compiled_code=True)
   3349         else:
   3350             outflag = False

c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\interactiveshell.py in showtraceback(self, exc_tuple, filename, tb_offset, exception_only, running_compiled_code)
   2045                     except Exception:
   2046                         stb = self.InteractiveTB.structured_traceback(etype,
-> 2047                                             value, tb, tb_offset=tb_offset)
   2048 
   2049                     self._showtraceback(etype, value, stb)

c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\ultratb.py in structured_traceback(self, etype, value, tb, tb_offset, number_of_lines_of_context)
   1416             self.tb = tb
   1417         return FormattedTB.structured_traceback(
-> 1418             self, etype, value, tb, tb_offset, number_of_lines_of_context)
   1419 
   1420 

c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\ultratb.py in structured_traceback(self, etype, value, tb, tb_offset, number_of_lines_of_context)
   1316             # Verbose modes need a full traceback
   1317             return VerboseTB.structured_traceback(
-> 1318                 self, etype, value, tb, tb_offset, number_of_lines_of_context
   1319             )
   1320         elif mode == 'Minimal':

c:\users\aking\.conda\envs\tf21\lib\site-packages\IPython\core\ultratb.py in structured_traceback(self, etype, evalue, etb, tb_offset, number_of_lines_of_context)
   1184         exception = self.get_parts_of_chained_exception(evalue)
   1185         if exception:
-> 1186             formatted_exceptions += self.prepare_chained_exception_message(evalue.__cause__)
   1187             etype, evalue, etb = exception
   1188         else:

TypeError: can only concatenate str (not "list") to str
```
