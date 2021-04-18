---
UID: NS:directml.DML_ROI_ALIGN_OPERATOR_DESC
title: DML_ROI_ALIGN_OPERATOR_DESC
description: Executa uma operação de alinhamento de ROI, conforme descrito no [papel de máscara R-CNN](https://arxiv.org/abs/1703.06870). Em suma, a operação extrai aparas da imagem de entrada tensor e as redimensiona para um tamanho de saída comum especificado pelas duas últimas dimensões de *OutputTensor* usando o *interpolamode* especificado.
helpviewer_keywords:
- DML_ROI_ALIGN_OPERATOR_DESC
- DML_ROI_ALIGN_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ROI_ALIGN_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ROI_ALIGN_OPERATOR_DESC, DML_ROI_ALIGN_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
- directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
ms.openlocfilehash: 987aef7d7002892b8af3167fb8da2b74dc80a12e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105793770"
---
# <a name="dml_roi_align_operator_desc-structure-directmlh"></a>Estrutura de DML_ROI_ALIGN_OPERATOR_DESC (directml. h)

Executa uma operação de alinhamento de ROI, conforme descrito no [papel de máscara R-CNN](https://arxiv.org/abs/1703.06870). Em suma, a operação extrai aparas da imagem de entrada tensor e as redimensiona para um tamanho de saída comum especificado pelas duas últimas dimensões de *OutputTensor* usando o *interpolamode* especificado.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe

```cpp
struct DML_ROI_ALIGN_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* ROITensor;
  const DML_TENSOR_DESC* BatchIndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  DML_REDUCE_FUNCTION ReductionFunction;
  DML_INTERPOLATION_MODE InterpolationMode;
  FLOAT SpatialScaleX;
  FLOAT SpatialScaleY;
  FLOAT OutOfBoundsInputValue;
  UINT MinimumSamplesPerOutput;
  UINT MaximumSamplesPerOutput;
};
```

## <a name="members"></a>Membros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados de entrada com dimensões `{ BatchCount, ChannelCount, InputHeight, InputWidth }` .

`ROITensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados de ROI (regiões de interesse). As dimensões permitidas do `ROITensor` são `{ NumROIs, 4 }` , `{ 1, NumROIs, 4 }` , ou `{ 1, 1, NumROIs, 4 }` . Para cada ROI, os valores serão as coordenadas de seus cantos superior esquerdo e inferior direito na ordem `[x1, y1, x2, y2]` .

`BatchIndicesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os índices de lote para extrair o ROIs. As dimensões permitidas `BatchIndicesTensor` são `{ NumROIs }` , `{ 1, NumROIs }` , `{ 1, 1, NumROIs }` ou `{ 1, 1, 1, NumROIs }` . Cada valor é o índice de um lote de *InputTensor*. O comportamento será indefinido se os valores não estiverem no intervalo [0, BatchCount).

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados de saída. As dimensões esperadas de *OutputTensor* são `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }` .

`ReductionFunction`

Tipo: **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**

A função de redução a ser usada ao reduzir em todos os exemplos de entrada que contribuem para um elemento de saída ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) ou **DML_REDUCE_FUNCTION_MAX**). O número de amostras de entrada para reduzir em é limitado por *MinimumSamplesPerOutput* e *MaximumSamplesPerOutput*.

`InterpolationMode`

Tipo: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**

O modo de interpolação a ser usado ao redimensionar as regiões.

- [DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode). Usa o algoritmo de *vizinho mais próximo* , que escolhe o elemento de entrada mais próximo ao pixel Center correspondente para cada elemento de saída.
- **DML_INTERPOLATION_MODE_LINEAR**. Usa o algoritmo *biline* , que computa o elemento Output, fazendo a média ponderada dos 2 elementos de entrada vizinhos mais próximos por dimensão. Como apenas 2 dimensões são redimensionadas, a média ponderada é calculada em um total de 4 elementos de entrada para cada elemento de saída.

`SpatialScaleX`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b>

O componente X (ou largura) do fator de dimensionamento para multiplicar as coordenadas *ROITensor* por a fim de torná-las proporcionais a *InputHeight* e *InputWidth*. Por exemplo, se *ROITensor* contiver coordenadas normalizadas (valores no intervalo [0.. 1]), *SpatialScaleX* normalmente teria o mesmo valor que *InputWidth*.

`SpatialScaleY`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b>

O componente Y (ou Height) do fator de dimensionamento para multiplicar as coordenadas *ROITensor* por a fim de torná-las proporcionais a *InputHeight* e *InputWidth*. Por exemplo, se *ROITensor* contiver coordenadas normalizadas (valores no intervalo [0.. 1]), *SpatialScaleY* normalmente teria o mesmo valor que *InputHeight*.

`OutOfBoundsInputValue`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b>

O valor a ser lido de *InputTensor* quando Rois estão fora dos limites de *InputTensor*. Isso pode acontecer quando os valores obtidos após o dimensionamento de *ROITensor* por *SpatialScaleX* e *SpatialScaleY* são maiores que *InputWidth* e *InputHeight*.

`MinimumSamplesPerOutput`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b>

O número mínimo de amostras de entrada a serem usadas para cada elemento de saída. O operador calculará o número de exemplos de entrada fazendo `ScaledCropSize / OutputSize` e, em seguida, fixe-o para *MinimumSamplesPerOutput* e *MaximumSamplesPerOutput*.

`MaximumSamplesPerOutput`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b>

O número máximo de amostras de entrada a serem usadas para cada elemento de saída. O operador calculará o número de exemplos de entrada fazendo `ScaledCropSize / OutputSize` e, em seguida, fixe-o para *MinimumSamplesPerOutput* e *MaximumSamplesPerOutput*.

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restrições de tensor
*InputTensor*, *OutputTensor* e *ROITensor* devem ter o mesmo *tipo de dados*.

## <a name="tensor-support"></a>Suporte do tensor
| Tensor | Tipo | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16 |
| ROITensor | Entrada | 2 a 4 | FLOAT32, FLOAT16 |
| BatchIndicesTensor | Entrada | 1 a 4 | UINT32 |
| OutputTensor | Saída | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml. h |