# Copyright (C) 2018-2020 - DevSH Graphics Programming Sp. z O.O.
# This file is part of the "Nabla Engine".
# For conditions of distribution and use, see copyright notice in nabla.h

# PCH & CommonAPI library for Nabla framework examples
add_subdirectory(common EXCLUDE_FROM_ALL)

if(NBL_BUILD_EXAMPLES)
	if(NBL_BUILD_ANDROID)
		nbl_android_create_media_storage_apk()
	endif()

	# showcase the use of `nbl::core`,`nbl::system` and `nbl::asset`
	add_subdirectory(01_HelloCoreSystemAsset EXCLUDE_FROM_ALL)
	# showcase the use of `system::IApplicationFramework` and `nbl::video`
	add_subdirectory(02_HelloCompute EXCLUDE_FROM_ALL)
	# showcase physical device selection, resource embedding and the use of identical headers in HLSL and C++
	add_subdirectory(03_DeviceSelectionAndSharedSources EXCLUDE_FROM_ALL)
	# showcase the creation of windows and polling for input
	add_subdirectory(04_HelloUI EXCLUDE_FROM_ALL)
	# showcase the semi-advanced use of Nabla's Streaming Buffers and BDA
	add_subdirectory(05_StreamingAndBufferDeviceAddressApp EXCLUDE_FROM_ALL)
	# showcase the use of a graphics queue
	add_subdirectory(06_HelloGraphicsQueue EXCLUDE_FROM_ALL)
	# showcase the set-up of multiple queues
	add_subdirectory(07_StagingAndMultipleQueues EXCLUDE_FROM_ALL)
	# showcase the set-up of a swapchain and picking of a matching device
	add_subdirectory(08_HelloSwapchain EXCLUDE_FROM_ALL)
	# showcase the use of a depth buffer and rudimentary camera
	add_subdirectory(09_DepthBufferAndCamera EXCLUDE_FROM_ALL)
  # demonstrate the counting sort utility
	add_subdirectory(10_CountingSort EXCLUDE_FROM_ALL)
	add_subdirectory(13_BitonicSort EXCLUDE_FROM_ALL)


	# Waiting for a refactor
	#add_subdirectory(27_PLYSTLDemo EXCLUDE_FROM_ALL)
	#add_subdirectory(29_SpecializationConstants EXCLUDE_FROM_ALL)
	#add_subdirectory(33_Draw3DLine EXCLUDE_FROM_ALL)
	add_subdirectory(35_GeometryCreator EXCLUDE_FROM_ALL)

	# Unit Test Examples
	add_subdirectory(20_AllocatorTest EXCLUDE_FROM_ALL)
	add_subdirectory(21_LRUCacheUnitTest EXCLUDE_FROM_ALL)
	add_subdirectory(22_CppCompat EXCLUDE_FROM_ALL)
	add_subdirectory(23_ArithmeticUnitTest EXCLUDE_FROM_ALL)
	add_subdirectory(24_ColorSpaceTest EXCLUDE_FROM_ALL)
	add_subdirectory(25_FilterTest EXCLUDE_FROM_ALL)
	# add_subdirectory(36_CUDAInterop EXCLUDE_FROM_ALL)

	add_subdirectory(38_EXRSplit EXCLUDE_FROM_ALL)
	# if (NBL_BUILD_MITSUBA_LOADER AND NBL_BUILD_OPTIX)
	#	add_subdirectory(39_DenoiserTonemapper EXCLUDE_FROM_ALL)
	# endif()

	add_subdirectory(42_FragmentShaderPathTracer EXCLUDE_FROM_ALL)
	#add_subdirectory(43_SumAndCDFFilters EXCLUDE_FROM_ALL)
	#add_subdirectory(45_BRDFEvalTest EXCLUDE_FROM_ALL)
	#add_subdirectory(46_SamplingValidation EXCLUDE_FROM_ALL)
	add_subdirectory(47_DerivMapTest EXCLUDE_FROM_ALL)
	add_subdirectory(53_ComputeShaders EXCLUDE_FROM_ALL)
	add_subdirectory(54_Transformations EXCLUDE_FROM_ALL)
	add_subdirectory(55_RGB18E7S3 EXCLUDE_FROM_ALL)
	add_subdirectory(56_RayQuery EXCLUDE_FROM_ALL)
	add_subdirectory(60_ClusteredRendering EXCLUDE_FROM_ALL)
	add_subdirectory(61_UI EXCLUDE_FROM_ALL)
	add_subdirectory(62_CAD EXCLUDE_FROM_ALL)
	add_subdirectory(62_SchusslerTest EXCLUDE_FROM_ALL)
	add_subdirectory(0_ImportanceSamplingEnvMaps EXCLUDE_FROM_ALL) #TODO: integrate back into 42
endif()
