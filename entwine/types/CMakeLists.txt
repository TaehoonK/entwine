set(MODULE types)
set(BASE "${CMAKE_CURRENT_SOURCE_DIR}")

set(
    SOURCES
    "${BASE}/bounds.cpp"
    "${BASE}/file-info.cpp"
    "${BASE}/manifest.cpp"
    "${BASE}/metadata.cpp"
    "${BASE}/pooled-point-table.cpp"
    "${BASE}/storage.cpp"
    "${BASE}/structure.cpp"
    "${BASE}/subset.cpp"
    "${BASE}/tube.cpp"
)

set(
    HEADERS
    "${BASE}/binary-point-table.hpp"
    "${BASE}/bounds.hpp"
    "${BASE}/delta.hpp"
    "${BASE}/dim-info.hpp"
    "${BASE}/dir.hpp"
    "${BASE}/file-info.hpp"
    "${BASE}/fixed-point-layout.hpp"
    "${BASE}/manifest.hpp"
    "${BASE}/metadata.hpp"
    "${BASE}/outer-scope.hpp"
    "${BASE}/point.hpp"
    "${BASE}/point-pool.hpp"
    "${BASE}/pooled-point-table.hpp"
    "${BASE}/reprojection.hpp"
    "${BASE}/schema.hpp"
    "${BASE}/stats.hpp"
    "${BASE}/storage.hpp"
    "${BASE}/storage-types.hpp"
    "${BASE}/structure.hpp"
    "${BASE}/subset.hpp"
    "${BASE}/tube.hpp"
    "${BASE}/vector-point-table.hpp"
    "${BASE}/version.hpp"
)

add_subdirectory(chunk-storage)

install(FILES ${HEADERS} DESTINATION include/entwine/${MODULE})
add_library(${MODULE} OBJECT ${SOURCES})

