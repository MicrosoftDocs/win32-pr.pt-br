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
ms.openlocfilehash: f3302f8081ed4bf64fa858ac3e303519089d01fb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105812140"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a>Estrutura de DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC (directml. h)
Executa uma função de normalização de variância média no tensor de entrada. Esse operador calculará a média e a variação do tensor de entrada para executar a normalização. Esse operador executa a computação a seguir.

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

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

Um tensor opcional que contém os dados de escala. As dimensões deste tensor devem ser `{ BatchCount, ChannelCount, Height, Width }` . Qualquer dimensão pode ser substituída por 1 para difundir nessa dimensão. Esse tensor será necessário se o *BiasTensor* for usado.


`BiasTensor`

Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor opcional que contém os dados de tendência. As dimensões deste tensor devem ser `{ BatchCount, ChannelCount, Height, Width }` . Qualquer dimensão pode ser substituída por 1 para difundir nessa dimensão. Esse tensor será necessário se o *ScaleTensor* for usado.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor para gravar os resultados. As dimensões de tensor são `{ BatchCount, ChannelCount, Height, Width }` .


`AxisCount`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b>

O número de eixos. Este campo determina o tamanho da matriz de *eixos* .


`Axes`

Tipo: \_ \_ tamanho \_ do campo (AxisCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \*** 

Os eixos ao longo do qual calcular a média e a variância.


`NormalizeVariance`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">bool</a></b>

**True** se a camada de normalização incluir variância no cálculo de normalização. Caso contrário, **false**. Se for **false**, a equação de normalização será `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .


`Epsilon`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b>

O valor de Épsilon a ser usado para evitar a divisão por zero. Um valor de 0, 1 é recomendado como padrão.


`FusedActivation`

Tipo: \_ Maybenull \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***

Uma camada de ativação com fusível opcional a ser aplicada após a normalização.


## <a name="remarks"></a>Comentários
**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** é um superconjunto de funcionalidades do [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc). Aqui, a definição da matriz de **eixos** como `{ 0, 2, 3 }` é o equivalente à definição de *CrossChannel* como **false** em **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; ao definir a matriz de **eixos** como `{ 1, 2, 3 }` equivalente à definição de *CrossChannel* como **true**.

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restrições de tensor
* *InputTensor* e *OutputTensor* devem ter os mesmos *tamanhos*.
* *BiasTensor*, *InputTensor*, *OutputTensor* e *ScaleTensor* devem ter o mesmo *tipo de dados*.

## <a name="tensor-support"></a>Suporte do tensor
| Tensor | Tipo | Dimensões | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Entrada | {BatchCount, ChannelCount, altura, largura} | 4 | FLOAT32, FLOAT16 |
| ScaleTensor | Entrada opcional | {ScaleBatchCount, ScaleChannelCount, AlturaDaEscala, LarguraDaEscala} | 4 | FLOAT32, FLOAT16 |
| BiasTensor | Entrada opcional | { BiasBatchCount, BiasChannelCount, BiasHeight, BiasWidth } | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Saída | {BatchCount, ChannelCount, altura, largura} | 4 | FLOAT32, FLOAT16 |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml. h |

## <a name="see-also"></a>Confira também

[Usando operadores com fusível para melhorar o desempenho](../dml-fused-activations.md)