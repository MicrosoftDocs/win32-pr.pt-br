---
title: Histórico do nível de recurso do DirectML
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 1e5d9f8b0532b809bab617655694af68ba530430
ms.sourcegitcommit: d168355cd7112871f24643b4079c2640b36f4975
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111521199"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="08422-103">Histórico do nível de recurso do DirectML</span><span class="sxs-lookup"><span data-stu-id="08422-103">DirectML feature level history</span></span>

<span data-ttu-id="08422-104">Para o histórico geral da versão do DirectML, consulte [Histórico de versão do DirectML.](./dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="08422-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_3_1"></a><span data-ttu-id="08422-105">DML_FEATURE_LEVEL_3_1</span><span class="sxs-lookup"><span data-stu-id="08422-105">DML_FEATURE_LEVEL_3_1</span></span>

<span data-ttu-id="08422-106">Introduzido na versão 1.5.0 do DirectML.</span><span class="sxs-lookup"><span data-stu-id="08422-106">Introduced in DirectML version 1.5.0.</span></span>

<span data-ttu-id="08422-107">Adicionado suporte para os operadores a [seguir.](/windows/win32/api/directml/ne-directml-dml_operator_type)</span><span class="sxs-lookup"><span data-stu-id="08422-107">Added support for the following [operators](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

* <span data-ttu-id="08422-108">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span><span class="sxs-lookup"><span data-stu-id="08422-108">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span></span>
* <span data-ttu-id="08422-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span><span class="sxs-lookup"><span data-stu-id="08422-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span></span>
* <span data-ttu-id="08422-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span><span class="sxs-lookup"><span data-stu-id="08422-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span></span>
* <span data-ttu-id="08422-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="08422-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span></span>
* <span data-ttu-id="08422-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="08422-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="08422-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="08422-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span></span>

<span data-ttu-id="08422-114">O número máximo de dimensões com suporte para os operadores a seguir aumentou de 4 para 8.</span><span class="sxs-lookup"><span data-stu-id="08422-114">The maximum number of supported dimensions for the following operators has increased from 4 to 8.</span></span>

* <span data-ttu-id="08422-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="08422-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="08422-116">**DML_OPERATOR_CAST**</span><span class="sxs-lookup"><span data-stu-id="08422-116">**DML_OPERATOR_CAST**</span></span>
* <span data-ttu-id="08422-117">**DML_OPERATOR_JOIN**</span><span class="sxs-lookup"><span data-stu-id="08422-117">**DML_OPERATOR_JOIN**</span></span>
* <span data-ttu-id="08422-118">**DML_OPERATOR_LP_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="08422-118">**DML_OPERATOR_LP_NORMALIZATION**</span></span>
* <span data-ttu-id="08422-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="08422-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="08422-120">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="08422-120">**DML_OPERATOR_PADDING**</span></span>
* <span data-ttu-id="08422-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="08422-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="08422-122">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="08422-122">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="08422-123">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="08422-123">**DML_OPERATOR_TILE**</span></span>
* <span data-ttu-id="08422-124">**DML_OPERATOR_TOP_K**</span><span class="sxs-lookup"><span data-stu-id="08422-124">**DML_OPERATOR_TOP_K**</span></span>
* <span data-ttu-id="08422-125">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="08422-125">**DML_OPERATOR_TOP_K1**</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="08422-126">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="08422-126">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="08422-127">Introduzido na versão 1.4.0 do DirectML.</span><span class="sxs-lookup"><span data-stu-id="08422-127">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="08422-128">Adicionado suporte para os operadores a [seguir.](/windows/win32/api/directml/ne-directml-dml_operator_type)</span><span class="sxs-lookup"><span data-stu-id="08422-128">Added support for the following [operators](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

* <span data-ttu-id="08422-129">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span><span class="sxs-lookup"><span data-stu-id="08422-129">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span></span>
* <span data-ttu-id="08422-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="08422-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="08422-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="08422-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="08422-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="08422-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="08422-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="08422-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="08422-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="08422-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="08422-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="08422-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="08422-136">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="08422-136">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="08422-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="08422-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="08422-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="08422-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="08422-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="08422-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="08422-140">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="08422-140">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="08422-141">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="08422-141">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="08422-142">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="08422-142">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="08422-143">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="08422-143">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="08422-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="08422-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="08422-145">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="08422-145">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="08422-146">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="08422-146">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="08422-147">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="08422-147">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="08422-148">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="08422-148">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="08422-149">Foram adicionados os aprimoramentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="08422-149">Added the following enhancements.</span></span>

* <span data-ttu-id="08422-150">O número máximo de dimensões tensores foi aumentado de 5 para 8.</span><span class="sxs-lookup"><span data-stu-id="08422-150">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="08422-151">Consulte [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span><span class="sxs-lookup"><span data-stu-id="08422-151">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="08422-152">Suporte adicional para tipos de dados inteiros foi adicionado aos operadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="08422-152">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="08422-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="08422-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="08422-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="08422-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="08422-155">**DML_OPERATOR_MAX_POOLING,** **DML_OPERATOR_MAX_POOLING1** e **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="08422-155">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="08422-156">**DML_OPERATOR_REDUCE**, ao usar **DML_REDUCE_FUNCTION_ARGMIN** ou **DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="08422-156">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="08422-157">Os seguintes tipos de dados de 64 bits foram adicionados e têm suporte de operadores selecionados.</span><span class="sxs-lookup"><span data-stu-id="08422-157">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="08422-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="08422-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="08422-159">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="08422-159">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="08422-160">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="08422-160">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="08422-161">Funcionalidade preterida.</span><span class="sxs-lookup"><span data-stu-id="08422-161">Deprecated functionality.</span></span>

* <span data-ttu-id="08422-162">**DML_REDUCE_FUNCTION_ARGMAX** e **DML_REDUCE_FUNCTION_ARGMIN** foram preterido.</span><span class="sxs-lookup"><span data-stu-id="08422-162">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="08422-163">Você deve preferir usar os operadores autônomos **DML_OPERATOR_ARGMIN** e **DML_OPERATOR_ARGMAX** em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="08422-163">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="08422-164">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="08422-164">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="08422-165">Introduzido na versão 1.2.0 do DirectML.</span><span class="sxs-lookup"><span data-stu-id="08422-165">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="08422-166">Adicionadas as APIs a seguir.</span><span class="sxs-lookup"><span data-stu-id="08422-166">Added the following APIs.</span></span>

* [<span data-ttu-id="08422-167">Interface IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="08422-167">IDMLDevice1 interface</span></span>](/windows/win32/api/directml/nn-directml-idmldevice1)
* <span data-ttu-id="08422-168">Suporte ao grafo do operador (consulte [IDMLDevice1::CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span><span class="sxs-lookup"><span data-stu-id="08422-168">Operator graph support (see [IDMLDevice1::CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span></span>

<span data-ttu-id="08422-169">Adicionado suporte para os operadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="08422-169">Added support for the following operators.</span></span>

* <span data-ttu-id="08422-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="08422-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="08422-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="08422-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="08422-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="08422-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="08422-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="08422-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="08422-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="08422-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="08422-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="08422-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="08422-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="08422-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="08422-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="08422-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="08422-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="08422-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="08422-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="08422-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="08422-180">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="08422-180">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="08422-181">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="08422-181">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="08422-182">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="08422-182">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="08422-183">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="08422-183">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="08422-184">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="08422-184">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="08422-185">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="08422-185">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="08422-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="08422-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="08422-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="08422-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="08422-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="08422-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="08422-189">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="08422-189">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="08422-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="08422-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="08422-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="08422-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="08422-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="08422-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="08422-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="08422-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="08422-194">Foram adicionados os aprimoramentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="08422-194">Added the following enhancements.</span></span>

* <span data-ttu-id="08422-195">Suporte adicional para tipos de dados inteiros foi adicionado aos operadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="08422-195">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="08422-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="08422-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="08422-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="08422-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="08422-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="08422-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="08422-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="08422-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="08422-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="08422-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="08422-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="08422-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="08422-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="08422-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="08422-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="08422-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="08422-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="08422-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="08422-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="08422-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="08422-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="08422-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="08422-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="08422-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="08422-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="08422-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="08422-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="08422-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="08422-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="08422-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="08422-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="08422-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="08422-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="08422-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="08422-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="08422-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="08422-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="08422-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="08422-215">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="08422-215">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="08422-216">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="08422-216">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="08422-217">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="08422-217">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="08422-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="08422-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="08422-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="08422-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="08422-220">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="08422-220">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="08422-221">**DML_OPERATOR_TOP_K** e **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="08422-221">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="08422-222">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="08422-222">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="08422-223">**DML_OPERATOR_REDUCE**, ao usar uma das funções de redução a seguir.</span><span class="sxs-lookup"><span data-stu-id="08422-223">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="08422-224">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="08422-224">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="08422-225">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="08422-225">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="08422-226">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="08422-226">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="08422-227">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="08422-227">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="08422-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="08422-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="08422-229">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="08422-229">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="08422-230">Restrições de formas tensor reduzidas para **DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="08422-230">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="08422-231">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="08422-231">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="08422-232">Introduzido no DirectML versão 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="08422-232">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="08422-233">Foram adicionadas as seguintes APIs.</span><span class="sxs-lookup"><span data-stu-id="08422-233">Added the following APIs.</span></span>
* [<span data-ttu-id="08422-234">Função DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="08422-234">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1)
* [<span data-ttu-id="08422-235">Enumeração de DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="08422-235">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="08422-236">Consultas de nível de recurso (consulte [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span><span class="sxs-lookup"><span data-stu-id="08422-236">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="08422-237">Adicionado suporte para os seguintes operadores.</span><span class="sxs-lookup"><span data-stu-id="08422-237">Added support for the following operators.</span></span>

* <span data-ttu-id="08422-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="08422-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="08422-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="08422-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="08422-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="08422-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="08422-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="08422-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="08422-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="08422-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="08422-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="08422-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="08422-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="08422-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="08422-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="08422-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="08422-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="08422-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="08422-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="08422-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="08422-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="08422-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="08422-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="08422-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="08422-250">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="08422-250">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="08422-251">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="08422-251">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="08422-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="08422-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="08422-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="08422-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="08422-254">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="08422-254">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="08422-255">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="08422-255">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="08422-256">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="08422-256">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="08422-257">Foram adicionados os seguintes aprimoramentos.</span><span class="sxs-lookup"><span data-stu-id="08422-257">Added the following enhancements.</span></span>

* <span data-ttu-id="08422-258">Ao ligar um recurso de entrada para expedição de um [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), agora é legal fornecer um recurso com [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (além de **D3D12_HEAP_TYPE_DEFAULT**), desde que as propriedades de heap apropriadas também sejam definidas.</span><span class="sxs-lookup"><span data-stu-id="08422-258">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="08422-259">Consulte [Binding in DirectML](./dml-binding.md).</span><span class="sxs-lookup"><span data-stu-id="08422-259">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="08422-260">Os seguintes operadores boolianos lógicos agora dão suporte a tempos de saída **UINT8** , além do suporte existente para **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="08422-260">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="08422-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="08422-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="08422-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="08422-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="08422-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="08422-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="08422-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="08422-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="08422-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="08422-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="08422-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="08422-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="08422-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="08422-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="08422-268">as funções de ativação de 5D agora dão suporte ao uso de progressos em seus tempos de entrada e de saída.</span><span class="sxs-lookup"><span data-stu-id="08422-268">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="08422-269">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="08422-269">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="08422-270">O nível de recurso no qual o DirectML foi introduzido.</span><span class="sxs-lookup"><span data-stu-id="08422-270">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="08422-271">Confira também</span><span class="sxs-lookup"><span data-stu-id="08422-271">See also</span></span>

* [<span data-ttu-id="08422-272">Histórico de versão do DirectML</span><span class="sxs-lookup"><span data-stu-id="08422-272">DirectML version history</span></span>](./dml-version-history.md)
* [<span data-ttu-id="08422-273">Enumeração de DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="08422-273">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="08422-274">Função DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="08422-274">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="08422-275">Estrutura de DML_FEATURE_QUERY_FEATURE_LEVELS</span><span class="sxs-lookup"><span data-stu-id="08422-275">DML_FEATURE_QUERY_FEATURE_LEVELS structure</span></span>](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)
