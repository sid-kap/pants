target(
  name='all',
  dependencies=[
    ':integration',
    ':unit',
  ]
)

target(
  name='unit',
  dependencies=[
    ':go_compile',
    ':go_fetch',
    ':go_workspace_task',
  ]
)

target(
  name='integration',
  dependencies=[
    ':go_compile_integration',
    ':go_fetch_integration',
    ':go_run_integration',
    ':go_test_integration',
  ]
)

python_tests(
  name='go_workspace_task',
  sources=['test_go_workspace_task.py'],
  dependencies=[
    'contrib/go/src/python/pants/contrib/go/targets:go_library',
    'contrib/go/src/python/pants/contrib/go/targets:go_remote_library',
    'contrib/go/src/python/pants/contrib/go/tasks:go_workspace_task',
    'src/python/pants/base:source_root',
    'src/python/pants/util:contextutil',
    'src/python/pants/util:dirutil',
    'tests/python/pants_test/tasks:task_test_base',
  ]
)

python_tests(
  name='go_compile',
  sources=['test_go_compile.py'],
  dependencies=[
    'contrib/go/src/python/pants/contrib/go/targets:go_library',
    'contrib/go/src/python/pants/contrib/go/tasks:go_compile',
    'src/python/pants/util:dirutil',
    'tests/python/pants_test/tasks:task_test_base',
  ]
)

python_tests(
  name='go_fetch',
  sources=['test_go_fetch.py'],
  dependencies=[
    'contrib/go/src/python/pants/contrib/go/subsystems:fetchers',
    'contrib/go/src/python/pants/contrib/go/targets:go_remote_library',
    'contrib/go/src/python/pants/contrib/go/tasks:go_fetch',
    'src/python/pants/base:address',
    'src/python/pants/base:source_root',
    'src/python/pants/util:contextutil',
    'tests/python/pants_test/tasks:task_test_base',
  ]
)

python_tests(
  name='go_compile_integration',
  sources=['test_go_compile_integration.py'],
  dependencies=[
    'contrib/go/src/python/pants/contrib/go/subsystems:go_distribution',
    'src/python/pants/util:contextutil',
    'tests/python/pants_test/subsystem:subsystem_utils',
    'tests/python/pants_test:int-test',
  ]
)

python_tests(
  name='go_test_integration',
  sources=['test_go_test_integration.py'],
  dependencies=[
    'tests/python/pants_test:int-test',
  ]
)

python_tests(
  name='go_run_integration',
  sources=['test_go_run_integration.py'],
  dependencies=[
    'tests/python/pants_test:int-test',
  ]
)

python_tests(
  name='go_fetch_integration',
  sources=['test_go_fetch_integration.py'],
  dependencies=[
    'tests/python/pants_test:int-test',
  ]
)
