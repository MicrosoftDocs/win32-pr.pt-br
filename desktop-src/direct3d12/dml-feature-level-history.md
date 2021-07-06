---
title: Histórico do nível de recurso do DirectML
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 3ddb2eec80448b8119bf2d990afbb998f212db26
ms.sourcegitcommit: 0b93de98c4afc79a6801a113bc91adbc89e835b9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/03/2021
ms.locfileid: "113282545"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="1010a-103">Histórico do nível de recurso do DirectML</span><span class="sxs-lookup"><span data-stu-id="1010a-103">DirectML feature level history</span></span>

<span data-ttu-id="1010a-104">Para obter o histórico de versões gerais do DirectML, consulte [histórico de versão do DirectML](./dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="1010a-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_4_0"></a><span data-ttu-id="1010a-105">DML_FEATURE_LEVEL_4_0</span><span class="sxs-lookup"><span data-stu-id="1010a-105">DML_FEATURE_LEVEL_4_0</span></span>

<span data-ttu-id="1010a-106">Introduzido na versão DirectML 1.6.0.</span><span class="sxs-lookup"><span data-stu-id="1010a-106">Introduced in DirectML version 1.6.0.</span></span>

<span data-ttu-id="1010a-107">Adicionado suporte para os seguintes tipos de operador, documentados em [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="1010a-107">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="1010a-108">Para cada constante de tipo de operador, esse tópico fornece um link para a estrutura correspondente.</span><span class="sxs-lookup"><span data-stu-id="1010a-108">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="1010a-109">**DML_OPERATOR_ELEMENT_WISE_QUANTIZED_LINEAR_ADD**</span><span class="sxs-lookup"><span data-stu-id="1010a-109">**DML_OPERATOR_ELEMENT_WISE_QUANTIZED_LINEAR_ADD**</span></span>
* <span data-ttu-id="1010a-110">**DML_OPERATOR_DYNAMIC_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="1010a-110">**DML_OPERATOR_DYNAMIC_QUANTIZE_LINEAR**</span></span>
* <span data-ttu-id="1010a-111">**DML_OPERATOR_ROI_ALIGN1**</span><span class="sxs-lookup"><span data-stu-id="1010a-111">**DML_OPERATOR_ROI_ALIGN1**</span></span>

<span data-ttu-id="1010a-112">O tipo de dados estendidos e o suporte de contagem de dimensões para os seguintes operadores, documentados em [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="1010a-112">Extended data type and dimension count support for the following operators, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="1010a-113">Para obter detalhes sobre o suporte específico adicionado no [**DML_FEATURE_LEVEL_4_0**](/windows/win32/api/directml/ne-directml-dml_feature_level), consulte o tópico de estrutura de cada operador.</span><span class="sxs-lookup"><span data-stu-id="1010a-113">For details on the specific support added in [**DML_FEATURE_LEVEL_4_0**](/windows/win32/api/directml/ne-directml-dml_feature_level), see each operator's structure topic.</span></span>

* <span data-ttu-id="1010a-114">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1010a-114">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="1010a-115">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="1010a-115">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="1010a-116">**DML_OPERATOR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="1010a-116">**DML_OPERATOR_CONVOLUTION**</span></span>
* <span data-ttu-id="1010a-117">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="1010a-117">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="1010a-118">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="1010a-118">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="1010a-119">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="1010a-119">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="1010a-120">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="1010a-120">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="1010a-121">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="1010a-121">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="1010a-122">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="1010a-122">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="1010a-123">**DML_OPERATOR_GEMM**</span><span class="sxs-lookup"><span data-stu-id="1010a-123">**DML_OPERATOR_GEMM**</span></span>
* <span data-ttu-id="1010a-124">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="1010a-124">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="1010a-125">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1010a-125">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="1010a-126">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="1010a-126">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="1010a-127">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="1010a-127">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>
* <span data-ttu-id="1010a-128">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="1010a-128">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="1010a-129">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="1010a-129">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="1010a-130">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="1010a-130">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>

## <a name="dml_feature_level_3_1"></a><span data-ttu-id="1010a-131">DML_FEATURE_LEVEL_3_1</span><span class="sxs-lookup"><span data-stu-id="1010a-131">DML_FEATURE_LEVEL_3_1</span></span>

<span data-ttu-id="1010a-132">Introduzido na versão 1.5.0 do DirectML.</span><span class="sxs-lookup"><span data-stu-id="1010a-132">Introduced in DirectML version 1.5.0.</span></span>

<span data-ttu-id="1010a-133">Adicionado suporte para os seguintes tipos de operador, documentados em [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="1010a-133">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="1010a-134">Para cada constante de tipo de operador, esse tópico fornece um link para a estrutura correspondente.</span><span class="sxs-lookup"><span data-stu-id="1010a-134">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="1010a-135">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span><span class="sxs-lookup"><span data-stu-id="1010a-135">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span></span>
* <span data-ttu-id="1010a-136">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1010a-136">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span></span>
* <span data-ttu-id="1010a-137">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span><span class="sxs-lookup"><span data-stu-id="1010a-137">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span></span>
* <span data-ttu-id="1010a-138">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1010a-138">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span></span>
* <span data-ttu-id="1010a-139">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="1010a-139">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="1010a-140">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1010a-140">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span></span>

<span data-ttu-id="1010a-141">O número máximo de dimensões com suporte para os seguintes operadores aumentou de 4 para 8.</span><span class="sxs-lookup"><span data-stu-id="1010a-141">The maximum number of supported dimensions for the following operators has increased from 4 to 8.</span></span>

* <span data-ttu-id="1010a-142">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="1010a-142">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="1010a-143">**DML_OPERATOR_CAST**</span><span class="sxs-lookup"><span data-stu-id="1010a-143">**DML_OPERATOR_CAST**</span></span>
* <span data-ttu-id="1010a-144">**DML_OPERATOR_JOIN**</span><span class="sxs-lookup"><span data-stu-id="1010a-144">**DML_OPERATOR_JOIN**</span></span>
* <span data-ttu-id="1010a-145">**DML_OPERATOR_LP_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="1010a-145">**DML_OPERATOR_LP_NORMALIZATION**</span></span>
* <span data-ttu-id="1010a-146">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="1010a-146">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="1010a-147">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="1010a-147">**DML_OPERATOR_PADDING**</span></span>
* <span data-ttu-id="1010a-148">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1010a-148">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="1010a-149">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1010a-149">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="1010a-150">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="1010a-150">**DML_OPERATOR_TILE**</span></span>
* <span data-ttu-id="1010a-151">**DML_OPERATOR_TOP_K**</span><span class="sxs-lookup"><span data-stu-id="1010a-151">**DML_OPERATOR_TOP_K**</span></span>
* <span data-ttu-id="1010a-152">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="1010a-152">**DML_OPERATOR_TOP_K1**</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="1010a-153">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="1010a-153">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="1010a-154">Introduzido na versão DirectML 1.4.0.</span><span class="sxs-lookup"><span data-stu-id="1010a-154">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="1010a-155">Adicionado suporte para os seguintes tipos de operador, documentados em [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="1010a-155">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="1010a-156">Para cada constante de tipo de operador, esse tópico fornece um link para a estrutura correspondente.</span><span class="sxs-lookup"><span data-stu-id="1010a-156">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="1010a-157">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span><span class="sxs-lookup"><span data-stu-id="1010a-157">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span></span>
* <span data-ttu-id="1010a-158">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="1010a-158">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="1010a-159">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="1010a-159">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="1010a-160">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="1010a-160">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="1010a-161">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="1010a-161">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="1010a-162">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="1010a-162">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="1010a-163">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="1010a-163">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="1010a-164">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="1010a-164">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="1010a-165">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1010a-165">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="1010a-166">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1010a-166">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="1010a-167">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1010a-167">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="1010a-168">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="1010a-168">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="1010a-169">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="1010a-169">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="1010a-170">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1010a-170">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="1010a-171">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1010a-171">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="1010a-172">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="1010a-172">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="1010a-173">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="1010a-173">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="1010a-174">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="1010a-174">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="1010a-175">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="1010a-175">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="1010a-176">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="1010a-176">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="1010a-177">Foram adicionados os seguintes aprimoramentos.</span><span class="sxs-lookup"><span data-stu-id="1010a-177">Added the following enhancements.</span></span>

* <span data-ttu-id="1010a-178">O número máximo de dimensões de tensor aumentou de 5 para 8.</span><span class="sxs-lookup"><span data-stu-id="1010a-178">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="1010a-179">Consulte [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1010a-179">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="1010a-180">O suporte adicional para tipos de texto inteiros foi adicionado aos operadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1010a-180">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="1010a-181">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="1010a-181">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="1010a-182">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="1010a-182">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="1010a-183">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** e **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="1010a-183">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="1010a-184">**DML_OPERATOR_REDUCE**, ao usar **DML_REDUCE_FUNCTION_ARGMIN** ou **DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="1010a-184">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="1010a-185">Os seguintes tipos de dados de 64 bits foram adicionados e têm suporte dos operadores SELECT.</span><span class="sxs-lookup"><span data-stu-id="1010a-185">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="1010a-186">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="1010a-186">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="1010a-187">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="1010a-187">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="1010a-188">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="1010a-188">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="1010a-189">Funcionalidade preterida.</span><span class="sxs-lookup"><span data-stu-id="1010a-189">Deprecated functionality.</span></span>

* <span data-ttu-id="1010a-190">**DML_REDUCE_FUNCTION_ARGMAX** e **DML_REDUCE_FUNCTION_ARGMIN** foram preteridos.</span><span class="sxs-lookup"><span data-stu-id="1010a-190">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="1010a-191">Você deve preferir usar os operadores autônomos **DML_OPERATOR_ARGMIN** e **DML_OPERATOR_ARGMAX** em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="1010a-191">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="1010a-192">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="1010a-192">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="1010a-193">Introduzido na versão DirectML 1.2.0.</span><span class="sxs-lookup"><span data-stu-id="1010a-193">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="1010a-194">Foram adicionadas as seguintes APIs.</span><span class="sxs-lookup"><span data-stu-id="1010a-194">Added the following APIs.</span></span>

* [<span data-ttu-id="1010a-195">Interface IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="1010a-195">IDMLDevice1 interface</span></span>](/windows/win32/api/directml/nn-directml-idmldevice1)
* <span data-ttu-id="1010a-196">Suporte ao grafo do operador (consulte [IDMLDevice1:: CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span><span class="sxs-lookup"><span data-stu-id="1010a-196">Operator graph support (see [IDMLDevice1::CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span></span>

<span data-ttu-id="1010a-197">Adicionado suporte para os seguintes tipos de operador, documentados em [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="1010a-197">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="1010a-198">Para cada constante de tipo de operador, esse tópico fornece um link para a estrutura correspondente.</span><span class="sxs-lookup"><span data-stu-id="1010a-198">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="1010a-199">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="1010a-199">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="1010a-200">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="1010a-200">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="1010a-201">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="1010a-201">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="1010a-202">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="1010a-202">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="1010a-203">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="1010a-203">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="1010a-204">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="1010a-204">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="1010a-205">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="1010a-205">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="1010a-206">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="1010a-206">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="1010a-207">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="1010a-207">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="1010a-208">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="1010a-208">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="1010a-209">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="1010a-209">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="1010a-210">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="1010a-210">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="1010a-211">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="1010a-211">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="1010a-212">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="1010a-212">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="1010a-213">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="1010a-213">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="1010a-214">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="1010a-214">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="1010a-215">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="1010a-215">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="1010a-216">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="1010a-216">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="1010a-217">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="1010a-217">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="1010a-218">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="1010a-218">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="1010a-219">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="1010a-219">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="1010a-220">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="1010a-220">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="1010a-221">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="1010a-221">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="1010a-222">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="1010a-222">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="1010a-223">Foram adicionados os seguintes aprimoramentos.</span><span class="sxs-lookup"><span data-stu-id="1010a-223">Added the following enhancements.</span></span>

* <span data-ttu-id="1010a-224">O suporte adicional para tipos de texto inteiros foi adicionado aos operadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1010a-224">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="1010a-225">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="1010a-225">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="1010a-226">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="1010a-226">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="1010a-227">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="1010a-227">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="1010a-228">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="1010a-228">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="1010a-229">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="1010a-229">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="1010a-230">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="1010a-230">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="1010a-231">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="1010a-231">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="1010a-232">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="1010a-232">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="1010a-233">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="1010a-233">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="1010a-234">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="1010a-234">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="1010a-235">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="1010a-235">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="1010a-236">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="1010a-236">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="1010a-237">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="1010a-237">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="1010a-238">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="1010a-238">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="1010a-239">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="1010a-239">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="1010a-240">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="1010a-240">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="1010a-241">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="1010a-241">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="1010a-242">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="1010a-242">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="1010a-243">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="1010a-243">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="1010a-244">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="1010a-244">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="1010a-245">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="1010a-245">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="1010a-246">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="1010a-246">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="1010a-247">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="1010a-247">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="1010a-248">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="1010a-248">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="1010a-249">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="1010a-249">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="1010a-250">**DML_OPERATOR_TOP_K** e **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="1010a-250">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="1010a-251">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="1010a-251">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="1010a-252">**DML_OPERATOR_REDUCE**, ao usar uma das funções de redução a seguir.</span><span class="sxs-lookup"><span data-stu-id="1010a-252">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="1010a-253">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="1010a-253">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="1010a-254">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="1010a-254">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="1010a-255">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="1010a-255">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="1010a-256">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="1010a-256">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="1010a-257">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="1010a-257">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="1010a-258">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="1010a-258">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="1010a-259">Restrições de formas tensor reduzidas para **DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="1010a-259">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="1010a-260">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="1010a-260">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="1010a-261">Introduzido no DirectML versão 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="1010a-261">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="1010a-262">Foram adicionadas as seguintes APIs.</span><span class="sxs-lookup"><span data-stu-id="1010a-262">Added the following APIs.</span></span>
* [<span data-ttu-id="1010a-263">Função DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="1010a-263">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1)
* [<span data-ttu-id="1010a-264">Enumeração de DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="1010a-264">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="1010a-265">Consultas de nível de recurso (consulte [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span><span class="sxs-lookup"><span data-stu-id="1010a-265">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="1010a-266">Adicionado suporte para os seguintes tipos de operador, documentados em [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="1010a-266">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="1010a-267">Para cada constante de tipo de operador, esse tópico fornece um link para a estrutura correspondente.</span><span class="sxs-lookup"><span data-stu-id="1010a-267">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="1010a-268">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="1010a-268">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="1010a-269">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="1010a-269">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="1010a-270">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="1010a-270">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="1010a-271">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="1010a-271">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="1010a-272">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="1010a-272">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="1010a-273">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="1010a-273">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="1010a-274">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="1010a-274">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="1010a-275">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="1010a-275">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="1010a-276">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="1010a-276">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="1010a-277">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="1010a-277">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="1010a-278">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="1010a-278">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="1010a-279">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="1010a-279">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="1010a-280">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="1010a-280">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="1010a-281">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="1010a-281">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="1010a-282">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="1010a-282">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="1010a-283">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="1010a-283">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="1010a-284">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="1010a-284">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="1010a-285">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="1010a-285">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="1010a-286">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="1010a-286">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="1010a-287">Foram adicionados os seguintes aprimoramentos.</span><span class="sxs-lookup"><span data-stu-id="1010a-287">Added the following enhancements.</span></span>

* <span data-ttu-id="1010a-288">Ao ligar um recurso de entrada para expedição de um [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), agora é legal fornecer um recurso com [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (além de **D3D12_HEAP_TYPE_DEFAULT**), desde que as propriedades de heap apropriadas também sejam definidas.</span><span class="sxs-lookup"><span data-stu-id="1010a-288">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="1010a-289">Consulte [Binding in DirectML](./dml-binding.md).</span><span class="sxs-lookup"><span data-stu-id="1010a-289">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="1010a-290">Os seguintes operadores boolianos lógicos agora dão suporte a tempos de saída **UINT8** , além do suporte existente para **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="1010a-290">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="1010a-291">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="1010a-291">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="1010a-292">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="1010a-292">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="1010a-293">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="1010a-293">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="1010a-294">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="1010a-294">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="1010a-295">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="1010a-295">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="1010a-296">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="1010a-296">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="1010a-297">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="1010a-297">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="1010a-298">as funções de ativação de 5D agora dão suporte ao uso de progressos em seus tempos de entrada e de saída.</span><span class="sxs-lookup"><span data-stu-id="1010a-298">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="1010a-299">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="1010a-299">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="1010a-300">O nível de recurso no qual o DirectML foi introduzido.</span><span class="sxs-lookup"><span data-stu-id="1010a-300">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="1010a-301">Confira também</span><span class="sxs-lookup"><span data-stu-id="1010a-301">See also</span></span>

* [<span data-ttu-id="1010a-302">Histórico de versão do DirectML</span><span class="sxs-lookup"><span data-stu-id="1010a-302">DirectML version history</span></span>](./dml-version-history.md)
* [<span data-ttu-id="1010a-303">Enumeração de DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="1010a-303">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="1010a-304">Função DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="1010a-304">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="1010a-305">Estrutura de DML_FEATURE_QUERY_FEATURE_LEVELS</span><span class="sxs-lookup"><span data-stu-id="1010a-305">DML_FEATURE_QUERY_FEATURE_LEVELS structure</span></span>](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)
