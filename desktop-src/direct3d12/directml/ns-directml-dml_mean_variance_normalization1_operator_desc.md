---
UID: NS:directml.DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
title: DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
description: Executa uma função de normalização de variância média no tensor de entrada. Esse operador calculará a média e a variação do tensor de entrada para executar a normalização.
helpviewer_keywords:
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure
- direct3d12.dml_mean_variance_normalization1_operator_desc
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
ms.openlocfilehash: ae22b004f1e879eb020ddcfe39a5f26481a508b0
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549771"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a>Estrutura de DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC (directml. h)

Executa uma função de normalização de variância média no tensor de entrada. Esse operador calculará a média e a variação do tensor de entrada para executar a normalização. Esse operador executa a computação a seguir.

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior. Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe
```cpp
struct DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC {
  const DML_TENSOR_DESC   *InputTensor;
  const DML_TENSOR_DESC   *ScaleTensor;
  const DML_TENSOR_DESC   *BiasTensor;
  const DML_TENSOR_DESC   *OutputTensor;
  UINT                    AxisCount;
  const UINT              *Axes;
  BOOL                    NormalizeVariance;
  FLOAT                   Epsilon;
  const DML_OPERATOR_DESC *FusedActivation;
};
```
## <a name="members"></a>Membros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados de entrada. As dimensões deste tensor devem ser `{ BatchCount, ChannelCount, Height, Width }` .

`ScaleTensor`

Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor opcional que contém os dados de escala.

Se **DML_FEATURE_LEVEL** for menor que **DML_FEATURE_LEVEL_4_0**, as dimensões desse tensor deverão ser `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }` . As dimensões ScaleBatchCount, AlturaDaEscala e LarguraDaEscala devem corresponder a *InputTensor* ou ser definidas como 1 para transmitir automaticamente essas dimensões pela entrada.

Se **DML_FEATURE_LEVEL** for maior ou igual a **DML_FEATURE_LEVEL_4_0**, qualquer dimensão poderá ser definida como 1 e será difundida automaticamente para corresponder ao *InputTensor*.

Esse tensor será necessário se o *BiasTensor* for usado.

`BiasTensor`

Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***


Um tensor opcional que contém os dados de tendência.

Se **DML_FEATURE_LEVEL** for menor que **DML_FEATURE_LEVEL_4_0**, as dimensões desse tensor deverão ser `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }` . As dimensões BiasBatchCount, BiasHeight e BiasWidth devem corresponder *a InputTensor* ou ser definidas como 1 para transmitir automaticamente essas dimensões pela entrada.

Se **DML_FEATURE_LEVEL** for maior ou igual **a DML_FEATURE_LEVEL_4_0**, qualquer dimensão poderá ser definida como 1 e ser transmitida automaticamente para corresponder a *InputTensor*.

Esse tensor será necessário se o *ScaleTensor* for usado.

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor no que gravar os resultados. As dimensões desse tensor são `{ BatchCount, ChannelCount, Height, Width }` .

`AxisCount`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b>

O número de eixos. Esse campo determina o tamanho da matriz *Eixos.*

`Axes`

Tipo: \_ Tamanho do campo \_ \_ (AxisCount) **const [UINT](../../winprog/windows-data-types.md) \*** 

Os eixos ao longo dos quais calcular a Média e a Variação.

`NormalizeVariance`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b>

**TRUE** se a camada normalização incluir Variação no cálculo de normalização. Caso contrário, **FALSE.** Se **FALSE**, a equação de normalização será `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .

`Epsilon`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b>

O valor de epsilon a ser usado para evitar a divisão por zero. Um valor de 0,00001 é recomendado como padrão.

`FusedActivation`

Tipo: \_ Maybenull \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***

Uma camada de ativação opcional mesclada a ser aplicada após a normalização.

## <a name="remarks"></a>Comentários
**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** é um superconjunto de funcionalidades do [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc). Aqui, a definição da matriz de **eixos** como `{ 0, 2, 3 }` é o equivalente à definição de *CrossChannel* como **false** em **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; ao definir a matriz de **eixos** como `{ 1, 2, 3 }` equivalente à definição de *CrossChannel* como **true**.

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restrições de tensor

*BiasTensor*, *InputTensor*, *OutputTensor* e *ScaleTensor* devem ter o mesmo *tipo de dados* e *DimensionCount*.

## <a name="tensor-support"></a>Suporte do tensor

### <a name="dml_feature_level_3_1-and-above"></a>DML_FEATURE_LEVEL_3_1 e acima

| Tensor | Tipo | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 1 a 8 | FLOAT32, FLOAT16 |
| ScaleTensor | Entrada opcional | 1 a 8 | FLOAT32, FLOAT16 |
| BiasTensor | Entrada opcional | 1 a 8 | FLOAT32, FLOAT16 |
| OutputTensor | Saída | 1 a 8 | FLOAT32, FLOAT16 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 e superior

| Tensor | Tipo | Contagens de dimensões com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16 |
| ScaleTensor | Entrada opcional | 4 | FLOAT32, FLOAT16 |
| BiasTensor | Entrada opcional | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Saída | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml.h |

## <a name="see-also"></a>Confira também

[Usando operadores mesclados para melhorar o desempenho](../dml-fused-activations.md)