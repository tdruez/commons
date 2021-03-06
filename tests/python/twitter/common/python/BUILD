# ==================================================================================================
# Copyright 2011 Twitter, Inc.
# --------------------------------------------------------------------------------------------------
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this work except in compliance with the License.
# You may obtain a copy of the License in the LICENSE file, or at:
#
#  http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
# ==================================================================================================


python_library(
  name = 'test_common',
  sources = ['test_common.py'],
  dependencies = [
    pants('3rdparty/python:setuptools'),
    pants('src/python/twitter/common/contextutil'),
    pants('src/python/twitter/common/dirutil'),
    pants('src/python/twitter/common/lang'),
    pants('src/python/twitter/common/python'),
  ],
)


python_test_suite(name = 'all',
  dependencies = [
    pants('tests/python/twitter/common/python/http:all'),
    pants(':test_environment'),
    pants(':test_obtainer'),
    pants(':test_platform'),
    pants(':test_pex_builder'),
    pants(':test_util'),
  ]
)

python_tests(name = 'test_environment',
  sources = ['test_environment.py'],
  dependencies = [
    pants(':test_common'),
    pants('src/python/twitter/common/contextutil'),
    pants('src/python/twitter/common/python')
  ]
)

python_tests(name = 'test_obtainer',
  sources = ['test_obtainer.py'],
  dependencies = [
    pants('src/python/twitter/common/python')
  ]
)

python_tests(name = 'test_platform',
  sources = ['test_platform.py'],
  dependencies = [
    pants('src/python/twitter/common/python')
  ]
)

python_tests(name = 'test_pex_builder',
  sources = ['test_pex_builder.py'],
  dependencies = [
    pants(':test_common'),
    pants('src/python/twitter/common/python'),
  ]
)

python_tests(name = 'test_util',
  sources = ['test_util.py'],
  dependencies = [
    pants(':test_common'),
    pants('src/python/twitter/common/python'),
  ]
)
