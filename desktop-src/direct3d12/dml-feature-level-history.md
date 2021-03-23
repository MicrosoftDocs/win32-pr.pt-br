---
title: Histórico de nível de recurso do DirectML
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 92f5a004b73d608a3958ae0edfa8c6d6b6a523d6
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104548338"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="87f4f-103">Histórico de nível de recurso do DirectML</span><span class="sxs-lookup"><span data-stu-id="87f4f-103">DirectML feature level history</span></span>

<span data-ttu-id="87f4f-104">Para obter o histórico de versões gerais do DirectML, consulte [histórico de versão do DirectML](./dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="87f4f-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="87f4f-105">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="87f4f-105">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="87f4f-106">Introduzido na versão DirectML 1.4.0.</span><span class="sxs-lookup"><span data-stu-id="87f4f-106">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="87f4f-107">Adicionado suporte para os seguintes operadores.</span><span class="sxs-lookup"><span data-stu-id="87f4f-107">Added support for the following operators.</span></span>

* [<span data-ttu-id="87f4f-108">DML_OPERATOR_ELEMENT_WISE_BIT_AND</span><span class="sxs-lookup"><span data-stu-id="87f4f-108">DML_OPERATOR_ELEMENT_WISE_BIT_AND</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="87f4f-109">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="87f4f-109">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="87f4f-110">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="87f4f-110">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="87f4f-111">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="87f4f-111">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="87f4f-112">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="87f4f-112">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="87f4f-113">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="87f4f-113">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="87f4f-114">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="87f4f-114">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="87f4f-115">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="87f4f-115">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="87f4f-116">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="87f4f-116">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="87f4f-117">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="87f4f-117">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="87f4f-118">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="87f4f-118">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="87f4f-119">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="87f4f-119">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="87f4f-120">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="87f4f-120">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="87f4f-121">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="87f4f-121">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="87f4f-122">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="87f4f-122">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="87f4f-123">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="87f4f-123">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="87f4f-124">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="87f4f-124">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="87f4f-125">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="87f4f-125">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="87f4f-126">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="87f4f-126">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="87f4f-127">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="87f4f-127">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="87f4f-128">Foram adicionados os seguintes aprimoramentos.</span><span class="sxs-lookup"><span data-stu-id="87f4f-128">Added the following enhancements.</span></span>

* <span data-ttu-id="87f4f-129">O número máximo de dimensões de tensor aumentou de 5 para 8.</span><span class="sxs-lookup"><span data-stu-id="87f4f-129">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="87f4f-130">Consulte [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span><span class="sxs-lookup"><span data-stu-id="87f4f-130">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="87f4f-131">O suporte adicional para tipos de texto inteiros foi adicionado aos operadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="87f4f-131">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="87f4f-132">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="87f4f-132">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="87f4f-133">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="87f4f-133">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="87f4f-134">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** e **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="87f4f-134">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="87f4f-135">**DML_OPERATOR_REDUCE**, ao usar **DML_REDUCE_FUNCTION_ARGMIN** ou **DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="87f4f-135">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="87f4f-136">Os seguintes tipos de dados de 64 bits foram adicionados e têm suporte dos operadores SELECT.</span><span class="sxs-lookup"><span data-stu-id="87f4f-136">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="87f4f-137">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="87f4f-137">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="87f4f-138">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="87f4f-138">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="87f4f-139">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="87f4f-139">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="87f4f-140">Funcionalidade preterida.</span><span class="sxs-lookup"><span data-stu-id="87f4f-140">Deprecated functionality.</span></span>

* <span data-ttu-id="87f4f-141">**DML_REDUCE_FUNCTION_ARGMAX** e **DML_REDUCE_FUNCTION_ARGMIN** foram preteridos.</span><span class="sxs-lookup"><span data-stu-id="87f4f-141">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="87f4f-142">Você deve preferir usar os operadores autônomos **DML_OPERATOR_ARGMIN** e **DML_OPERATOR_ARGMAX** em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="87f4f-142">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="87f4f-143">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="87f4f-143">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="87f4f-144">Introduzido na versão DirectML 1.2.0.</span><span class="sxs-lookup"><span data-stu-id="87f4f-144">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="87f4f-145">Foram adicionadas as seguintes APIs.</span><span class="sxs-lookup"><span data-stu-id="87f4f-145">Added the following APIs.</span></span>

* [<span data-ttu-id="87f4f-146">Interface IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="87f4f-146">IDMLDevice1 interface</span></span>](./directml/nn-directml-idmldevice1.md)
* <span data-ttu-id="87f4f-147">Suporte ao grafo do operador (consulte [IDMLDevice1:: CompileGraph](./directml/nf-directml-idmldevice1-compilegraph.md)</span><span class="sxs-lookup"><span data-stu-id="87f4f-147">Operator graph support (see [IDMLDevice1::CompileGraph](./directml/nf-directml-idmldevice1-compilegraph.md)</span></span>

<span data-ttu-id="87f4f-148">Adicionado suporte para os seguintes operadores.</span><span class="sxs-lookup"><span data-stu-id="87f4f-148">Added support for the following operators.</span></span>

* <span data-ttu-id="87f4f-149">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="87f4f-149">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="87f4f-150">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="87f4f-150">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="87f4f-151">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="87f4f-151">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="87f4f-152">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="87f4f-152">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="87f4f-153">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="87f4f-153">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="87f4f-154">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="87f4f-154">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="87f4f-155">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="87f4f-155">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="87f4f-156">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="87f4f-156">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="87f4f-157">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="87f4f-157">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="87f4f-158">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="87f4f-158">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="87f4f-159">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="87f4f-159">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="87f4f-160">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="87f4f-160">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="87f4f-161">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="87f4f-161">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="87f4f-162">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="87f4f-162">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="87f4f-163">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="87f4f-163">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="87f4f-164">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="87f4f-164">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="87f4f-165">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="87f4f-165">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="87f4f-166">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="87f4f-166">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="87f4f-167">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="87f4f-167">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="87f4f-168">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="87f4f-168">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="87f4f-169">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="87f4f-169">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="87f4f-170">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="87f4f-170">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="87f4f-171">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="87f4f-171">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="87f4f-172">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="87f4f-172">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="87f4f-173">Foram adicionados os seguintes aprimoramentos.</span><span class="sxs-lookup"><span data-stu-id="87f4f-173">Added the following enhancements.</span></span>

* <span data-ttu-id="87f4f-174">O suporte adicional para tipos de texto inteiros foi adicionado aos operadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="87f4f-174">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="87f4f-175">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="87f4f-175">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="87f4f-176">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="87f4f-176">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="87f4f-177">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="87f4f-177">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="87f4f-178">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="87f4f-178">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="87f4f-179">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="87f4f-179">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="87f4f-180">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="87f4f-180">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="87f4f-181">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="87f4f-181">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="87f4f-182">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="87f4f-182">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="87f4f-183">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="87f4f-183">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="87f4f-184">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="87f4f-184">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="87f4f-185">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="87f4f-185">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="87f4f-186">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="87f4f-186">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="87f4f-187">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="87f4f-187">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="87f4f-188">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="87f4f-188">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="87f4f-189">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="87f4f-189">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="87f4f-190">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="87f4f-190">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="87f4f-191">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="87f4f-191">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="87f4f-192">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="87f4f-192">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="87f4f-193">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="87f4f-193">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="87f4f-194">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="87f4f-194">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="87f4f-195">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="87f4f-195">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="87f4f-196">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="87f4f-196">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="87f4f-197">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="87f4f-197">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="87f4f-198">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="87f4f-198">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="87f4f-199">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="87f4f-199">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="87f4f-200">**DML_OPERATOR_TOP_K** e **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="87f4f-200">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="87f4f-201">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="87f4f-201">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="87f4f-202">**DML_OPERATOR_REDUCE**, ao usar uma das funções de redução a seguir.</span><span class="sxs-lookup"><span data-stu-id="87f4f-202">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="87f4f-203">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="87f4f-203">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="87f4f-204">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="87f4f-204">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="87f4f-205">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="87f4f-205">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="87f4f-206">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="87f4f-206">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="87f4f-207">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="87f4f-207">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="87f4f-208">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="87f4f-208">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="87f4f-209">Restrições de formas tensor reduzidas para **DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="87f4f-209">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="87f4f-210">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="87f4f-210">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="87f4f-211">Introduzido no DirectML versão 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="87f4f-211">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="87f4f-212">Foram adicionadas as seguintes APIs.</span><span class="sxs-lookup"><span data-stu-id="87f4f-212">Added the following APIs.</span></span>
* [<span data-ttu-id="87f4f-213">Função DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="87f4f-213">DMLCreateDevice1 function</span></span>](./directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="87f4f-214">Enumeração de DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="87f4f-214">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="87f4f-215">Consultas de nível de recurso (consulte [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span><span class="sxs-lookup"><span data-stu-id="87f4f-215">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="87f4f-216">Adicionado suporte para os seguintes operadores.</span><span class="sxs-lookup"><span data-stu-id="87f4f-216">Added support for the following operators.</span></span>

* <span data-ttu-id="87f4f-217">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="87f4f-217">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="87f4f-218">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="87f4f-218">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="87f4f-219">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="87f4f-219">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="87f4f-220">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="87f4f-220">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="87f4f-221">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="87f4f-221">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="87f4f-222">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="87f4f-222">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="87f4f-223">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="87f4f-223">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="87f4f-224">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="87f4f-224">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="87f4f-225">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="87f4f-225">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="87f4f-226">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="87f4f-226">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="87f4f-227">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="87f4f-227">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="87f4f-228">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="87f4f-228">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="87f4f-229">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="87f4f-229">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="87f4f-230">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="87f4f-230">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="87f4f-231">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="87f4f-231">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="87f4f-232">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="87f4f-232">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="87f4f-233">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="87f4f-233">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="87f4f-234">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="87f4f-234">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="87f4f-235">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="87f4f-235">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="87f4f-236">Foram adicionados os seguintes aprimoramentos.</span><span class="sxs-lookup"><span data-stu-id="87f4f-236">Added the following enhancements.</span></span>

* <span data-ttu-id="87f4f-237">Ao ligar um recurso de entrada para expedição de um [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), agora é legal fornecer um recurso com [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (além de **D3D12_HEAP_TYPE_DEFAULT**), desde que as propriedades de heap apropriadas também sejam definidas.</span><span class="sxs-lookup"><span data-stu-id="87f4f-237">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="87f4f-238">Consulte [Binding in DirectML](./dml-binding.md).</span><span class="sxs-lookup"><span data-stu-id="87f4f-238">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="87f4f-239">Os seguintes operadores boolianos lógicos agora dão suporte a tempos de saída **UINT8** , além do suporte existente para **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="87f4f-239">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="87f4f-240">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="87f4f-240">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="87f4f-241">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="87f4f-241">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="87f4f-242">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="87f4f-242">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="87f4f-243">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="87f4f-243">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="87f4f-244">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="87f4f-244">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="87f4f-245">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="87f4f-245">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="87f4f-246">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="87f4f-246">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="87f4f-247">as funções de ativação de 5D agora dão suporte ao uso de progressos em seus tempos de entrada e de saída.</span><span class="sxs-lookup"><span data-stu-id="87f4f-247">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="87f4f-248">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="87f4f-248">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="87f4f-249">O nível de recurso no qual o DirectML foi introduzido.</span><span class="sxs-lookup"><span data-stu-id="87f4f-249">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="87f4f-250">Confira também</span><span class="sxs-lookup"><span data-stu-id="87f4f-250">See also</span></span>

<span data-ttu-id="87f4f-251">Histórico de versão do [DirectML](./dml-version-history.md) 
 [Enumeração](/windows/win32/api/directml/ne-directml-dml_feature_level) 
 de DML_FEATURE_LEVEL [Função DMLCreateDevice1](./directml/nf-directml-dmlcreatedevice1.md) 
 [Estrutura de DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)</span><span class="sxs-lookup"><span data-stu-id="87f4f-251">[DirectML version history](./dml-version-history.md)
[DML_FEATURE_LEVEL enumeration](/windows/win32/api/directml/ne-directml-dml_feature_level)
[DMLCreateDevice1 function](./directml/nf-directml-dmlcreatedevice1.md)
[DML_FEATURE_QUERY_FEATURE_LEVELS structure](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)</span></span>