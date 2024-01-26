include(CetTest)

cet_enable_asserts()
cet_test_env("FHICL_FILE_PATH=.")
cet_transitive_paths(LIBRARY_DIR BINARY IN_TREE)
cet_test_env_prepend(CET_PLUGIN_PATH ${TRANSITIVE_PATHS_WITH_LIBRARY_DIR})

add_subdirectory(RandomUtils)
add_subdirectory(GeneratedEventTimestamp)
