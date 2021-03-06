cmake_minimum_required(VERSION 3.10)
project(randballs)

set(CMAKE_CXX_STANDARD 14)

include_directories(.)
include_directories(components)
include_directories(events)
include_directories(external)
include_directories(external/entt)
include_directories(external/entt/config)
include_directories(external/entt/core)
include_directories(external/entt/entity)
include_directories(external/entt/locator)
include_directories(external/entt/process)
include_directories(external/entt/resource)
include_directories(external/entt/signal)
include_directories(scenes)
include_directories(systems)

add_executable(randballs
        components/body.hpp
        components/colorable.hpp
        components/holdable.hpp
        components/lerpable.hpp
        components/portal.hpp
        components/renderable.hpp
        components/teleportable.hpp
        events/escapefromarea.hpp
        events/freearea.hpp
        events/spawnball.hpp
        events/spawnportal.hpp
        events/teleport.hpp
        external/entt/config/config.h
        external/entt/core/algorithm.hpp
        external/entt/core/family.hpp
        external/entt/core/hashed_string.hpp
        external/entt/core/ident.hpp
        external/entt/core/monostate.hpp
        external/entt/entity/actor.hpp
        external/entt/entity/entity.hpp
        external/entt/entity/entt_traits.hpp
        external/entt/entity/helper.hpp
        external/entt/entity/prototype.hpp
        external/entt/entity/registry.hpp
        external/entt/entity/snapshot.hpp
        external/entt/entity/sparse_set.hpp
        external/entt/entity/utility.hpp
        external/entt/entity/view.hpp
        external/entt/locator/locator.hpp
        external/entt/process/process.hpp
        external/entt/process/scheduler.hpp
        external/entt/resource/cache.hpp
        external/entt/resource/handle.hpp
        external/entt/resource/loader.hpp
        external/entt/signal/delegate.hpp
        external/entt/signal/dispatcher.hpp
        external/entt/signal/emitter.hpp
        external/entt/signal/sigh.hpp
        external/entt/entt.hpp
        media/DejaVuSans.ttf
        scenes/gamescene.cpp
        scenes/gamescene.hpp
        systems/basesystem.cpp
        systems/basesystem.hpp
        systems/collisionsystem.cpp
        systems/collisionsystem.hpp
        systems/colorsystem.cpp
        systems/colorsystem.hpp
        systems/movesystem.cpp
        systems/movesystem.hpp
        systems/rendersystem.cpp
        systems/rendersystem.hpp
        systems/teleportsystem.cpp
        systems/teleportsystem.hpp
        systems/usersystem.cpp
        systems/usersystem.hpp
        engine.cpp
        engine.hpp
        entitymanager.cpp
        entitymanager.hpp
        LICENSE
        README.md
        scene.cpp
        scene.hpp
        scenemanager.cpp
        scenemanager.hpp
        texturemanager.cpp
        texturemanager.hpp
        utils.hpp components/sharedstate.h)

target_link_libraries (randballs sfml-graphics sfml-window sfml-system)
file(COPY media DESTINATION ${CMAKE_BINARY_DIR})