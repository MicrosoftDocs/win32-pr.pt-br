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
# <a name="directml-feature-level-history"></a>Histórico do nível de recurso do DirectML

Para obter o histórico de versões gerais do DirectML, consulte [histórico de versão do DirectML](./dml-version-history.md).

## <a name="dml_feature_level_4_0"></a>DML_FEATURE_LEVEL_4_0

Introduzido na versão DirectML 1.6.0.

Adicionado suporte para os seguintes tipos de operador, documentados em [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type). Para cada constante de tipo de operador, esse tópico fornece um link para a estrutura correspondente.

* **DML_OPERATOR_ELEMENT_WISE_QUANTIZED_LINEAR_ADD**
* **DML_OPERATOR_DYNAMIC_QUANTIZE_LINEAR**
* **DML_OPERATOR_ROI_ALIGN1**

O tipo de dados estendidos e o suporte de contagem de dimensões para os seguintes operadores, documentados em [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type). Para obter detalhes sobre o suporte específico adicionado no [**DML_FEATURE_LEVEL_4_0**](/windows/win32/api/directml/ne-directml-dml_feature_level), consulte o tópico de estrutura de cada operador.

* **DML_OPERATOR_ACTIVATION_RELU_GRAD**
* **DML_OPERATOR_ADAM_OPTIMIZER**
* **DML_OPERATOR_CONVOLUTION**
* **DML_OPERATOR_CONVOLUTION_INTEGER**
* **DML_OPERATOR_CUMULATIVE_PRODUCT**
* **DML_OPERATOR_CUMULATIVE_SUMMATION**
* **DML_OPERATOR_DIAGONAL_MATRIX**
* **DML_OPERATOR_FILL_VALUE_CONSTANT**
* **DML_OPERATOR_FILL_VALUE_SEQUENCE**
* **DML_OPERATOR_GEMM**
* **DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**
* **DML_OPERATOR_MAX_POOLING_GRAD**
* **DML_OPERATOR_NONZERO_COORDINATES**
* **DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**
* **DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**
* **DML_OPERATOR_RANDOM_GENERATOR**
* **DML_OPERATOR_REVERSE_SUBSEQUENCES**

## <a name="dml_feature_level_3_1"></a>DML_FEATURE_LEVEL_3_1

Introduzido na versão 1.5.0 do DirectML.

Adicionado suporte para os seguintes tipos de operador, documentados em [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type). Para cada constante de tipo de operador, esse tópico fornece um link para a estrutura correspondente.

* **DML_OPERATOR_ELEMENT_WISE_ATAN_YX**
* **DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**
* **DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**
* **DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**
* **DML_OPERATOR_CUMULATIVE_PRODUCT**
* **DML_OPERATOR_BATCH_NORMALIZATION_GRAD**

O número máximo de dimensões com suporte para os seguintes operadores aumentou de 4 para 8.

* **DML_OPERATOR_BATCH_NORMALIZATION**
* **DML_OPERATOR_CAST**
* **DML_OPERATOR_JOIN**
* **DML_OPERATOR_LP_NORMALIZATION**
* **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**
* **DML_OPERATOR_PADDING**
* **DML_OPERATOR_ACTIVATION_RELU_GRAD**
* **DML_OPERATOR_SLICE_GRAD**
* **DML_OPERATOR_TILE**
* **DML_OPERATOR_TOP_K**
* **DML_OPERATOR_TOP_K1**

## <a name="dml_feature_level_3_0"></a>DML_FEATURE_LEVEL_3_0

Introduzido na versão DirectML 1.4.0.

Adicionado suporte para os seguintes tipos de operador, documentados em [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type). Para cada constante de tipo de operador, esse tópico fornece um link para a estrutura correspondente.

* **DML_OPERATOR_ELEMENT_WISE_BIT_AND**
* **DML_OPERATOR_ELEMENT_WISE_BIT_OR**
* **DML_OPERATOR_ELEMENT_WISE_BIT_XOR**
* **DML_OPERATOR_ELEMENT_WISE_BIT_NOT**
* **DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**
* **DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**
* **DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**
* **DML_OPERATOR_ACTIVATION_CELU**
* **DML_OPERATOR_ACTIVATION_RELU_GRAD**
* **DML_OPERATOR_AVERAGE_POOLING_GRAD**
* **DML_OPERATOR_MAX_POOLING_GRAD**
* **DML_OPERATOR_RANDOM_GENERATOR**
* **DML_OPERATOR_NONZERO_COORDINATES**
* **DML_OPERATOR_RESAMPLE_GRAD**
* **DML_OPERATOR_SLICE_GRAD**
* **DML_OPERATOR_ADAM_OPTIMIZER**
* **DML_OPERATOR_ARGMIN**
* **DML_OPERATOR_ARGMAX**
* **DML_OPERATOR_ROI_ALIGN**
* **DML_OPERATOR_GATHER_ND1**

Foram adicionados os seguintes aprimoramentos.

* O número máximo de dimensões de tensor aumentou de 5 para 8. Consulte [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).
* O suporte adicional para tipos de texto inteiros foi adicionado aos operadores a seguir.
  * **DML_OPERATOR_ELEMENT_WISE_POW**
  * **DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**
  * **DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** e **DML_OPERATOR_MAX_POOLING2**
  * **DML_OPERATOR_REDUCE**, ao usar **DML_REDUCE_FUNCTION_ARGMIN** ou **DML_REDUCE_FUNCTION_ARGMAX**
* Os seguintes tipos de dados de 64 bits foram adicionados e têm suporte dos operadores SELECT.
  * **DML_TENSOR_DATA_TYPE_FLOAT64**
  * **DML_TENSOR_DATA_TYPE_UINT64**
  * **DML_TENSOR_DATA_TYPE_INT64**

Funcionalidade preterida.

* **DML_REDUCE_FUNCTION_ARGMAX** e **DML_REDUCE_FUNCTION_ARGMIN** foram preteridos. Você deve preferir usar os operadores autônomos **DML_OPERATOR_ARGMIN** e **DML_OPERATOR_ARGMAX** em seu lugar.

## <a name="dml_feature_level_2_1"></a>DML_FEATURE_LEVEL_2_1

Introduzido na versão DirectML 1.2.0.

Foram adicionadas as seguintes APIs.

* [Interface IDMLDevice1](/windows/win32/api/directml/nn-directml-idmldevice1)
* Suporte ao grafo do operador (consulte [IDMLDevice1:: CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)

Adicionado suporte para os seguintes tipos de operador, documentados em [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type). Para cada constante de tipo de operador, esse tópico fornece um link para a estrutura correspondente.

* **DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**
* **DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**
* **DML_OPERATOR_ELEMENT_WISE_ROUND**
* **DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**
* **DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**
* **DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**
* **DML_OPERATOR_FILL_VALUE_CONSTANT**
* **DML_OPERATOR_FILL_VALUE_SEQUENCE**
* **DML_OPERATOR_CUMULATIVE_SUMMATION**
* **DML_OPERATOR_REVERSE_SUBSEQUENCES**
* **DML_OPERATOR_GATHER_ELEMENTS**
* **DML_OPERATOR_GATHER_ND**
* **DML_OPERATOR_SCATTER_ND**
* **DML_OPERATOR_MAX_POOLING2**
* **DML_OPERATOR_SLICE1**
* **DML_OPERATOR_TOP_K1**
* **DML_OPERATOR_DEPTH_TO_SPACE1**
* **DML_OPERATOR_SPACE_TO_DEPTH1**
* **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**
* **DML_OPERATOR_RESAMPLE1**
* **DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**
* **DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**
* **DML_OPERATOR_CONVOLUTION_INTEGER**
* **DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**

Foram adicionados os seguintes aprimoramentos.

* O suporte adicional para tipos de texto inteiros foi adicionado aos operadores a seguir.
  * **DML_OPERATOR_ELEMENT_WISE_IDENTITY**
  * **DML_OPERATOR_ELEMENT_WISE_ABS**
  * **DML_OPERATOR_ELEMENT_WISE_ADD**
  * **DML_OPERATOR_ELEMENT_WISE_CLIP**
  * **DML_OPERATOR_ELEMENT_WISE_DIVIDE**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_MAX**
  * **DML_OPERATOR_ELEMENT_WISE_MEAN**
  * **DML_OPERATOR_ELEMENT_WISE_MIN**
  * **DML_OPERATOR_ELEMENT_WISE_MULTIPLY**
  * **DML_OPERATOR_ELEMENT_WISE_SUBTRACT**
  * **DML_OPERATOR_ELEMENT_WISE_THRESHOLD**
  * **DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**
  * **DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**
  * **DML_OPERATOR_ELEMENT_WISE_SIGN**
  * **DML_OPERATOR_ELEMENT_WISE_IF**
  * **DML_OPERATOR_ACTIVATION_SHRINK**
  * **DML_OPERATOR_PADDING**
  * **DML_OPERATOR_GATHER**
  * **DML_OPERATOR_SCATTER**
  * **DML_OPERATOR_DEPTH_TO_SPACE**
  * **DML_OPERATOR_SPACE_TO_DEPTH**
  * **DML_OPERATOR_TILE**
  * **DML_OPERATOR_TOP_K** e **DML_OPERATOR_TOP_K1**
  * **DML_OPERATOR_ONE_HOT**
  * **DML_OPERATOR_REDUCE**, ao usar uma das funções de redução a seguir.
    * **DML_REDUCE_FUNCTION_ARGMIN**
    * **DML_REDUCE_FUNCTION_ARGMAX**
    * **DML_REDUCE_FUNCTION_MAX**
    * **DML_REDUCE_FUNCTION_MIN**
    * **DML_REDUCE_FUNCTION_MULTIPLY**
    * **DML_REDUCE_FUNCTION_SUM**
* Restrições de formas tensor reduzidas para **DML_OPERATOR_GATHER**

## <a name="dml_feature_level_2_0"></a>DML_FEATURE_LEVEL_2_0

Introduzido no DirectML versão 1.1.0.

Foram adicionadas as seguintes APIs.
* [Função DMLCreateDevice1](/windows/win32/api/directml/nf-directml-dmlcreatedevice1)
* [Enumeração de DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level)
* Consultas de nível de recurso (consulte [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))

Adicionado suporte para os seguintes tipos de operador, documentados em [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type). Para cada constante de tipo de operador, esse tópico fornece um link para a estrutura correspondente.

* **DML_OPERATOR_ELEMENT_WISE_SIGN**
* **DML_OPERATOR_ELEMENT_WISE_IS_NAN**
* **DML_OPERATOR_ELEMENT_WISE_ERF**
* **DML_OPERATOR_ELEMENT_WISE_SINH**
* **DML_OPERATOR_ELEMENT_WISE_COSH**
* **DML_OPERATOR_ELEMENT_WISE_TANH**
* **DML_OPERATOR_ELEMENT_WISE_ASINH**
* **DML_OPERATOR_ELEMENT_WISE_ACOSH**
* **DML_OPERATOR_ELEMENT_WISE_ATANH**
* **DML_OPERATOR_ELEMENT_WISE_IF**
* **DML_OPERATOR_ELEMENT_WISE_ADD1**
* **DML_OPERATOR_ACTIVATION_SHRINK**
* **DML_OPERATOR_MAX_POOLING1**
* **DML_OPERATOR_MAX_UNPOOLING**
* **DML_OPERATOR_DIAGONAL_MATRIX**
* **DML_OPERATOR_SCATTER_ELEMENTS**
* **DML_OPERATOR_SCATTER**
* **DML_OPERATOR_ONE_HOT**
* **DML_OPERATOR_RESAMPLE**

Foram adicionados os seguintes aprimoramentos.

* Ao ligar um recurso de entrada para expedição de um [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), agora é legal fornecer um recurso com [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (além de **D3D12_HEAP_TYPE_DEFAULT**), desde que as propriedades de heap apropriadas também sejam definidas. Consulte [Binding in DirectML](./dml-binding.md).
* Os seguintes operadores boolianos lógicos agora dão suporte a tempos de saída **UINT8** , além do suporte existente para **UINT32**.
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**
* as funções de ativação de 5D agora dão suporte ao uso de progressos em seus tempos de entrada e de saída.

## <a name="dml_feature_level_1_0"></a>DML_FEATURE_LEVEL_1_0

O nível de recurso no qual o DirectML foi introduzido.

## <a name="see-also"></a>Confira também

* [Histórico de versão do DirectML](./dml-version-history.md)
* [Enumeração de DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [Função DMLCreateDevice1](/windows/win32/api/directml/nf-directml-dmlcreatedevice1.md)
* [Estrutura de DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)
