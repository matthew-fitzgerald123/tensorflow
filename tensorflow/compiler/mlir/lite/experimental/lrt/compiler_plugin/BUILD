# Copyright 2024 Google LLC.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#      http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

package(
    # copybara:uncomment default_applicable_licenses = ["//tensorflow:license"],
    default_visibility = ["//tensorflow/compiler/mlir/lite/experimental/lrt:__subpackages__"],
)

cc_library(
    name = "lite_rt_compiler_plugin",
    hdrs = ["lite_rt_compiler_plugin.h"],
    visibility = ["//visibility:public"],
    deps = [
        "//tensorflow/compiler/mlir/lite/experimental/lrt:lite_rt_common",
        "//tensorflow/compiler/mlir/lite/experimental/lrt/api:lite_rt_model_api",
    ],
)

cc_library(
    name = "algo",
    hdrs = ["algo.h"],
    deps = [
        "//tensorflow/compiler/mlir/lite/experimental/lrt:lite_rt_op_code",
        "//tensorflow/compiler/mlir/lite/experimental/lrt/api:lite_rt_model_api",
        "//tensorflow/compiler/mlir/lite/experimental/lrt/model:lite_rt_model",
    ],
)

cc_test(
    name = "algo_test",
    srcs = ["algo_test.cc"],
    tags = ["no_oss"],
    deps = [
        ":algo",
        "//tensorflow/compiler/mlir/lite/experimental/lrt:lite_rt_op_code",
        "//tensorflow/compiler/mlir/lite/experimental/lrt/api:graph_tools",
        "//tensorflow/compiler/mlir/lite/experimental/lrt/api:lite_rt_model_api",
        "//tensorflow/compiler/mlir/lite/experimental/lrt/model:lite_rt_model",
        "//tensorflow/compiler/mlir/lite/experimental/lrt/test_data:test_data_util",
        "@com_google_googletest//:gtest_main",
    ],
)
