set( EXECUTABLE_OUTPUT_PATH ${CMAKE_CURRENT_BINARY_DIR} )

include(ECMAddTests)
include(KritaAddBrokenUnitTest)

macro_add_unittest_definitions()

ecm_add_tests(
    TestPosition.cpp
    TestSelection.cpp
    TestPathTool.cpp
    TestShapeAt.cpp
    TestShapePainting.cpp
    TestKoShapeFactory.cpp
    TestKoShapeRegistry.cpp
    TestShapeContainer.cpp
    TestShapeGroupCommand.cpp
    TestShapeReorderCommand.cpp
    TestImageCollection.cpp
    TestResourceManager.cpp
    TestShapeBackgroundCommand.cpp
    TestShapeStrokeCommand.cpp
    TestShapeShadowCommand.cpp
    TestInputDevice.cpp
    TestSnapStrategy.cpp
    NAME_PREFIX "libs-kritaflake-"
    LINK_LIBRARIES kritaflake Qt5::Test)

krita_add_broken_unit_test(TestPathShape.cpp
    TEST_NAME libs-kritaflake-TestPathShape
    LINK_LIBRARIES kritaflake Qt5::Test)

krita_add_broken_unit_test(TestControlPointMoveCommand.cpp
    TEST_NAME libs-kritaflake-TestControlPointMoveCommand
    LINK_LIBRARIES kritaflake Qt5::Test)

krita_add_broken_unit_test(TestPointTypeCommand.cpp
    TEST_NAME libs-kritaflake-TestPointTypeCommand
    LINK_LIBRARIES kritaflake Qt5::Test)

krita_add_broken_unit_test(TestPointRemoveCommand.cpp
    TEST_NAME libs-kritaflake-TestPointRemoveCommand
    LINK_LIBRARIES kritaflake Qt5::Test)

krita_add_broken_unit_test(TestRemoveSubpathCommand.cpp
    TEST_NAME libs-kritaflake-TestRemoveSubpathCommand
    LINK_LIBRARIES kritaflake Qt5::Test)

krita_add_broken_unit_test(TestPathSegment.cpp
    TEST_NAME libs-kritaflake-TestPathSegment
    LINK_LIBRARIES kritaflake Qt5::Test)

krita_add_broken_unit_test(TestSegmentTypeCommand.cpp
    TEST_NAME libs-kritaflake-TestSegmentTypeCommand
    LINK_LIBRARIES kritaflake Qt5::Test)

krita_add_broken_unit_test(TestPointMergeCommand.cpp
    TEST_NAME libs-kritaflake-TestPointMergeCommand
    LINK_LIBRARIES kritaflake Qt5::Test)
