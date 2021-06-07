---
UID: NS:directml.DML_ADAM_OPTIMIZER_OPERATOR_DESC
title: DML_ADAM_OPTIMIZER_OPERATOR_DESC
description: Computa pesos atualizados (parâmetros) usando os gradientes fornecidos, com base no algoritmo Adam (ptive de Oment de **Ada**= **M** estimativa). Esse operador é um otimizador e normalmente é usado na etapa de atualização de peso de um loop de treinamento para executar descendente de gradiente.
helpviewer_keywords:
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
- DML_ADAM_OPTIMIZER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ADAM_OPTIMIZER_OPERATOR_DESC, DML_ADAM_OPTIMIZER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
- directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
ms.openlocfilehash: 9943f70bd3d62faf57f4eca83f9f09ce0119881a
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417001"
---
# <a name="dml_adam_optimizer_operator_desc-structure-directmlh"></a>Estrutura de DML_ADAM_OPTIMIZER_OPERATOR_DESC (directml. h)

Computa pesos atualizados (parâmetros) usando os gradientes fornecidos, com base no algoritmo Adam (ptive de Oment de **Ada**= **M** estimativa). Esse operador é um otimizador e normalmente é usado na etapa de atualização de peso de um loop de treinamento para executar descendente de gradiente.

Esse operador executa a seguinte computação:

```
X = InputParametersTensor
M = InputFirstMomentTensor
V = InputSecondMomentTensor
G = GradientTensor
T = TrainingStepTensor

// Compute updated first and second moment estimates.
M = Beta1 * M + (1.0 - Beta1) * G
V = Beta2 * V + (1.0 - Beta2) * G * G

// Compute bias correction factor for first and second moment estimates.
Alpha = sqrt(1.0 - pow(Beta2, T)) / (1.0 - pow(Beta1, T))

X -= LearningRate * Alpha * M / (sqrt(V) + Epsilon)

OutputParametersTensor = X
OutputFirstMomentTensor = M
OutputSecondMomentTensor = V
```

Além de computar os parâmetros de peso atualizados (retornados em *OutputParametersTensor*), esse operador também retorna as estimativas atualizadas do primeiro e do segundo momento em *OutputFirstMomentTensor* e *OutputSecondMomentTensor*, respectivamente. Normalmente, você deve armazenar essas estimativas de primeiro e segundo momento e fornecê-las como entradas durante a etapa de treinamento subsequente.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior. Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe
```cpp
struct DML_ADAM_OPTIMIZER_OPERATOR_DESC
{ 
  const DML_TENSOR_DESC* InputParametersTensor;
  const DML_TENSOR_DESC* InputFirstMomentTensor;
  const DML_TENSOR_DESC* InputSecondMomentTensor;
  const DML_TENSOR_DESC* GradientTensor;
  const DML_TENSOR_DESC* TrainingStepTensor;
  const DML_TENSOR_DESC* OutputParametersTensor;
  const DML_TENSOR_DESC* OutputFirstMomentTensor;
  const DML_TENSOR_DESC* OutputSecondMomentTensor;
  FLOAT LearningRate;
  FLOAT Beta1;
  FLOAT Beta2;
  FLOAT Epsilon;
};
```

## <a name="members"></a>Membros

`InputParametersTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os parâmetros (pesos) para aplicar esse otimizador a. As estimativas de gradiente, primeiro e segundo momento, a etapa de treinamento atual, bem como hiperparâmetros *LearningRate*, *beta1* e *beta2*, são usadas por esse operador para executar gradiente descendente nos valores de peso fornecidos neste tensor.

`InputFirstMomentTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém a primeira estimativa de tempo do gradiente para cada valor de peso. Esses valores normalmente são obtidos como resultado de uma execução anterior desse operador, por meio de *OutputFirstMomentTensor*.

Ao aplicar esse otimizador a um conjunto de pesos pela primeira vez (por exemplo, durante a etapa de treinamento inicial), os valores desse tensor normalmente devem ser inicializados como zero. As execuções subsequentes devem usar os valores retornados em *OutputFirstMomentTensor*.

Os *tamanhos* e o *tipo de dados* desse tensor devem corresponder exatamente aos do *InputParametersTensor*.

`InputSecondMomentTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém a segunda estimativa de tempo do gradiente para cada valor de peso. Esses valores normalmente são obtidos como resultado de uma execução anterior desse operador, por meio de *OutputSecondMomentTensor*.

Ao aplicar esse otimizador a um conjunto de pesos pela primeira vez (por exemplo, durante a etapa de treinamento inicial), os valores desse tensor normalmente devem ser inicializados como zero. As execuções subsequentes devem usar os valores retornados em *OutputSecondMomentTensor*.

Os *tamanhos* e o *tipo de dados* desse tensor devem corresponder exatamente aos do *InputParametersTensor*.

`GradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Os gradientes a serem aplicados aos parâmetros de entrada (pesos) para descendente de gradiente. Os gradientes normalmente são obtidos em uma passagem de repropagação durante o treinamento.

Os *tamanhos* e o *tipo de dados* desse tensor devem corresponder exatamente aos do *InputParametersTensor*.

`TrainingStepTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor escalar que contém um único valor inteiro que representa a contagem de etapas de treinamento atual. Esse valor junto com *beta1* e *beta2* é usado para calcular a decaimento exponencial do primeiro e do segundo tempo estimar os tempos.

Normalmente, o valor da etapa de treinamento começa em 0 no início do treinamento e é incrementado em 1 em cada etapa de treinamento sucessiva. Esse operador não atualiza o valor da etapa de treinamento; Você deve fazer isso manualmente, por exemplo, usando [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).

Esse tensor deve ser um escalar (ou seja, todos os *tamanhos* iguais a 1) e ter o tipo de dados [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).

`OutputParametersTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor de saída que contém os valores de parâmetro (peso) atualizados após a aplicação do descendente do gradiente.

Durante a associação, esse tensor é permitido para alias de um tensor de entrada qualificado, que pode ser usado para executar uma atualização in-loco desse tensor. Consulte a seção [comentários](#remarks) para obter mais detalhes.

Os *tamanhos* e o *tipo de dados* desse tensor devem corresponder exatamente aos do *InputParametersTensor*.

`OutputFirstMomentTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Uma tensor de saída que contém estimativas de primeiro momento atualizadas. Você deve armazenar os valores desse tensor e fornecê-los em *InputFirstMomentTensor* durante a etapa de treinamento subsequente.

Durante a associação, esse tensor é permitido para alias de um tensor de entrada qualificado, que pode ser usado para executar uma atualização in-loco desse tensor. Consulte a seção [comentários](#remarks) para obter mais detalhes.

Os *tamanhos* e o *tipo de dados* desse tensor devem corresponder exatamente aos do *InputParametersTensor*.

`OutputSecondMomentTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor de saída que contém estimativas de segundo momento atualizadas. Você deve armazenar os valores desse tensor e fornecê-los em *InputSecondMomentTensor* durante a etapa de treinamento subsequente.

Durante a associação, esse tensor é permitido para alias de um tensor de entrada qualificado, que pode ser usado para executar uma atualização in-loco desse tensor. Consulte a seção [comentários](#remarks) para obter mais detalhes.

Os *tamanhos* e o *tipo de dados* desse tensor devem corresponder exatamente aos do *InputParametersTensor*.

`LearningRate`

Tipo: **float**

A taxa de aprendizagem, também conhecida como o *tamanho da etapa*. A taxa de aprendizagem é um hiperparâmetro que determina a magnitude da atualização de peso ao longo do vetor de gradiente em cada etapa de treinamento.

`Beta1`

Tipo: **float**

Um hiperparâmetro que representa a taxa de decaimento exponencial da primeira estimativa de momento do gradiente. Esse valor deve estar entre 0,0 e 1,0. Um valor de 0,9 f é típico.

`Beta2`

Tipo: **float**

Um hiperparâmetro que representa a taxa de decaimento exponencial da estimativa do segundo tempo do gradiente. Esse valor deve estar entre 0,0 e 1,0. Um valor de 0,999 f é típico.

`Epsilon`

Tipo: **float**

Um valor pequeno usado para ajudar na estabilidade numérica, impedindo a divisão por zero. Para entradas de ponto flutuante de 32 bits, os valores típicos incluem 1e-8 ou `FLT_EPSILON` .

## <a name="remarks"></a>Comentários
Esse operador dá suporte à execução in-loco, o que significa que cada tensor de saída tem permissão para alias de um tensor de entrada qualificado durante a associação. Por exemplo, é possível associar o mesmo recurso para *InputParametersTensor* e *OutputParametersTensor* a fim de alcançar efetivamente uma atualização in-loco dos parâmetros de entrada. Todos os tempos de entrada desse operador, com exceção do *TrainingStepTensor*, estão qualificados para serem alias dessa maneira.

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restrições de tensor
* *GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, *OutputSecondMomentTensor* e *TrainingStepTensor* devem ter o mesmo *tipo de dados*.
* *GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor* e *OutputSecondMomentTensor* devem ter os mesmos *tamanhos*.

## <a name="tensor-support"></a>Suporte do tensor
| Tensor | Tipo | Dimensões | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputParametersTensor | Entrada | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| InputFirstMomentTensor | Entrada | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| InputSecondMomentTensor | Entrada | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| GradientTensor | Entrada | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| TrainingStepTensor | Entrada | {1, 1, 1, 1} | 4 | FLOAT32, FLOAT16 |
| OutputParametersTensor | Saída | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| OutputFirstMomentTensor | Saída | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| OutputSecondMomentTensor | Saída | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml. h |