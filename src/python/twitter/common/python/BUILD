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
  name = 'python-source',
  sources = globs('*.py') + globs('http/*.py'),
  dependencies = [
    pants('3rdparty/python:setuptools'),
  ],
)

python_library(
  name = 'python',
  dependencies = [
    pants(':python-source'),
  ],
  provides = setup_py(
    name = 'twitter.common.python',
    version = '0.3.0',
    description = "Twitter's Python packaging toolchain.",
    long_description = """
Twitter's Python packaging toolchain.  Includes support for package
fetching, building, installing, "distillation" into eggs and
Twitter's "PEX" standalone Python virtual environment.
""",
    url = 'https://github.com/twitter/commons/tree/master/src/python/twitter/common/python',
    license = 'Apache License, Version 2.0',
    zip_safe = True,
    classifiers = [
      'Intended Audience :: Developers',
      'License :: OSI Approved :: Apache Software License',
      'Operating System :: OS Independent',
      'Programming Language :: Python',
    ]
  ).with_binaries(
    pex = pants('src/python/twitter/common/python/bin:pex'),
  )
)

page(name = 'pexreadme',
  source = 'README.md',
  dependencies = [
    pants(':pexinstall')
  ]
)

page(name = 'pexinstall',
  source = 'INSTALL.md',
)
