---
title: Enumerações do DirectML
description: As enumerações a seguir são declaradas em DirectML.h.
ms.localizationpriority: low
ms.topic: article
ms.date: 11/06/2020
ms.custom: 19H1
ms.openlocfilehash: a74ce2fc3b5bcf94a97d7f51cec20d5f9f0d8e9837a7b59d2f1bdea80328db90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953096"
---
# <a name="directml-enumerations"></a>Enumerações do DirectML

As enumerações a seguir são declaradas em DirectML.h.

## <a name="in-this-section"></a>Nesta seção

| Tópico e descrição |
|-|
| [**DML_AXIS_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_axis_direction). Define constantes que especificam a direção de uma operação ao longo do eixo especificado para o operador (por exemplo, soma, selecionando os elementos top-k, selecionando o elemento mínimo). |
| [**DML_BINDING_TYPE**](/windows/desktop/api/directml/ne-directml-dml_binding_type). Define constantes que especificam a natureza dos recursos referenciados por uma descrição de associação [DML_BINDING_DESC estrutura](/windows/desktop/api/directml/ns-directml-dml_binding_desc). |
| [**DML_CONVOLUTION_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_convolution_direction). Define constantes que especificam uma direção para o operador de convolução DirectML (conforme descrito pela [estrutura DML_CONVOLUTION_OPERATOR_DESC ).](/windows/desktop/api/directml/ns-directml-dml_convolution_operator_desc) |
| [**DML_CONVOLUTION_MODE**](/windows/desktop/api/directml/ne-directml-dml_convolution_mode). Define constantes que especificam um modo para o operador de convolução DirectML (conforme descrito pela [estrutura DML_CONVOLUTION_OPERATOR_DESC ).](/windows/desktop/api/directml/ns-directml-dml_convolution_operator_desc) |
| [**DML_CREATE_DEVICE_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_create_device_flags). Fornece opções de criação de dispositivo adicionais [para DMLCreateDevice.](/windows/desktop/api/directml/nf-directml-dmlcreatedevice) |
| [**DML_DEPTH_SPACE_ORDER**](/windows/desktop/api/directml/ne-directml-dml_depth_space_order). Define constantes que controlam a transformação aplicada nos operadores DirectML [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) e **DML_OPERATOR_SPACE_TO_DEPTH1**. |
| [**DML_EXECUTION_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_execution_flags). Fornece opções ao DirectML para controlar a execução de operadores. |
| [**DML_FEATURE**](/windows/desktop/api/directml/ne-directml-dml_feature). Define um conjunto de recursos opcionais e recursos que podem ser consultados do dispositivo DirectML. |
| [**DML_GRAPH_EDGE_TYPE**](/windows/desktop/api/directml/ne-directml-dml_graph_edge_type). Define constantes que especificam um tipo de borda de grafo. Consulte [DML_GRAPH_EDGE_DESC](/windows/win32/api/directml/ns-directml-dml_graph_edge_desc) para saber o uso dessa enumeração. |
| [**DML_GRAPH_NODE_TYPE**](/windows/desktop/api/directml/ne-directml-dml_graph_node_type). Define constantes que especificam um tipo de nó de grafo. Consulte [DML_GRAPH_NODE_DESC](/windows/win32/api/directml/ns-directml-dml_graph_node_desc) para saber o uso dessa enumeração. |
| [**DML_INTERPOLATION_MODE**](/windows/desktop/api/directml/ne-directml-dml_interpolation_mode). Define constantes que especificam um modo para o operador directML upsample 2D (conforme descrito pela [estrutura DML_UPSAMPLE_2D_OPERATOR_DESC ).](/windows/desktop/api/directml/ns-directml-dml_upsample_2d_operator_desc) |
| [**DML_MATRIX_TRANSFORM**](/windows/desktop/api/directml/ne-directml-dml_matrix_transform). Define constantes que especificam uma transformação de matriz a ser aplicada a um tensor DirectML. |
| [**DML_OPERATOR_TYPE**](/windows/desktop/api/directml/ne-directml-dml_operator_type). Define o tipo de uma descrição do operador. |
| [**DML_PADDING_MODE**](/windows/desktop/api/directml/ne-directml-dml_padding_mode). Define constantes que especificam um modo para o operador de painel DirectML (conforme descrito pela [estrutura DML_PADDING_OPERATOR_DESC ).](/windows/desktop/api/directml/ns-directml-dml_padding_operator_desc) |
| [**DML_RANDOM_GENERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_random_generator_type). Define constantes que especificam tipos de gerador de número aleatório aleatório. |
| [**DML_RECURRENT_NETWORK_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_recurrent_network_direction). Define constantes que especificam uma direção para um operador DirectML recorrente. |
| [**DML_REDUCE_FUNCTION**](/windows/desktop/api/directml/ne-directml-dml_reduce_function). Define constantes que especificam o algoritmo de redução específico a ser usado para o operador de redução DirectML (conforme descrito pela [estrutura DML_REDUCE_OPERATOR_DESC ).](/windows/desktop/api/directml/ns-directml-dml_reduce_operator_desc) |
| [**DML_TENSOR_DATA_TYPE**](/windows/desktop/api/directml/ne-directml-dml_tensor_data_type). Especifica o tipo de dados dos valores em um tensor. |
| [**DML_TENSOR_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_tensor_flags). Especifica opções adicionais em uma descrição de tensor. |
| [**DML_TENSOR_TYPE**](/windows/desktop/api/directml/ne-directml-dml_tensor_type). Identifica um tipo de descrição do tensor. |

## <a name="related-topics"></a>Tópicos relacionados

* [Referência do DirectML](direct3d-directml-reference.md)
* [Referência de núcleo](direct3d-12-core-reference.md)
* [Referência do Direct3D 12](direct3d-12-reference.md)