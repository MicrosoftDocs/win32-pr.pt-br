---
title: Função UpdateSubresources (D3dx12. h)
description: Atualiza os subrecursos, todas as matrizes de subrecurso devem ser preenchidas, normalmente chamando ID3D12Device GetCopyableFootprints.
ms.assetid: D6885165-095E-452D-8D93-A2C43A215F48
keywords:
- Função UpdateSubresources
topic_type:
- apiref
api_name:
- UpdateSubresources
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 885ee058aacbfca238448830f2b7b1b54a298f89
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791547"
---
# <a name="updatesubresources-function"></a>Função UpdateSubresources

Atualiza os subrecursos, todas as matrizes de subrecurso devem ser preenchidas, normalmente chamando [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).

## <a name="syntax"></a>Sintaxe


```C++
UINT64 inline UpdateSubresources(
  _In_       ID3D12GraphicsCommandList          *pCmdList,
  _In_       ID3D12Resource                     *pDestinationResource,
  _In_       ID3D12Resource                     *pIntermediate,
  _In_       UINT                               FirstSubresource,
  _In_       UINT                               NumSubresources,
             UINT64                             RequiredSize,
  _In_ const D3D12_PLACED_SUBRESOURCE_FOOTPRINT *pLayouts,
  _In_ const UINT                               *pNumRows,
  _In_ const UINT64                             *pRowSizesInBytes,
  _In_ const D3D12_SUBRESOURCE_DATA             *pSrcData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCmdList* \[ no\]
</dt> <dd>

Tipo: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

A lista de comandos, como um ponteiro para um [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).

</dd> <dt>

*pDestinationResource* \[ no\]
</dt> <dd>

Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

O recurso de destino, como um ponteiro para um [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).

</dd> <dt>

*pIntermediate* \[ no\]
</dt> <dd>

Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

O recurso intermediário, como um ponteiro para um [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).

</dd> <dt>

*FirstSubresource* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O índice do primeiro subrecurso no recurso. O intervalo de valores válidos é de 0 a D3D12 \_ req \_ subrecursos.

</dd> <dt>

*NumSubresources* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O número de subrecursos no recurso. O intervalo de valores válidos é de 0 a (D3D12 \_ req \_ subresources- *FirstSubresource*).

</dd> <dt>

*RequiredSize* 
</dt> <dd>

Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

O tamanho necessário, em bytes, para a atualização.

</dd> <dt>

*pLayouts* \[ no\]
</dt> <dd>

Tipo: **\* const [**D3D12 \_ colocou a \_ \_ superfície do subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)**

Ponteiro para uma matriz (de comprimento *NumSubresources*) de ponteiros para as estruturas que contêm a descrição e o posicionamento dos subrecursos do recurso.

</dd> <dt>

*pNumRows* \[ no\]
</dt> <dd>

Tipo: **const [**uint**](/windows/desktop/WinProg/windows-data-types) \***

Ponteiro para uma matriz (de comprimento *NumSubresources*) de UINTs contendo o número de linhas para cada subrecurso.

</dd> <dt>

*pRowSizesInBytes* \[ no\]
</dt> <dd>

Tipo: **const [**UINT64**](/windows/desktop/WinProg/windows-data-types) \***

Ponteiro para uma matriz (de comprimento *NumSubresources*) de UINTs contendo o tamanho, em bytes, de cada linha.

</dd> <dt>

*pSrcData* \[ no\]
</dt> <dd>

Tipo: **const [**D3D12 \_ subresource \_ Data**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) \***

Ponteiro para uma matriz (de comprimento *NumSubresources*) de ponteiros para D3D12 estruturas de [**\_ \_ dados de subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) que contêm descrições dos dados de subrecurso usados para a atualização.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

O tamanho do buffer, em bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções auxiliares do D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Sub-recursos](subresources.md)
</dt> </dl>

 

