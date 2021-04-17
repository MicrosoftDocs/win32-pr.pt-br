---
title: Função UpdateSubresources (Stack-Alocation) (D3dx12. h)
description: Atualiza os subrecursos com uma implementação de alocação de pilha.
ms.assetid: 2F30FDF1-4450-473E-AEA8-C5FF54260BCE
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
ms.openlocfilehash: 237e7df26b35b4cb5b1dba7b2a80c1baaac64e8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105782749"
---
# <a name="updatesubresources-stack-allocating-function"></a>Função UpdateSubresources (pilha-alocação)

Atualiza os subrecursos com uma implementação de alocação de pilha.

## <a name="syntax"></a>Sintaxe


```C++
UINT64 inline UpdateSubresources(
  _In_ ID3D12GraphicsCommandList *pCmdList,
  _In_ ID3D12Resource            *pDestinationResource,
  _In_ ID3D12Resource            *pIntermediate,
       UINT64                    IntermediateOffset,
  _In_ UINT                      FirstSubresource,
  _In_ UINT                      NumSubresources,
  _In_ D3D12_SUBRESOURCE_DATA    *pSrcData
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

*IntermediateOffset* 
</dt> <dd>

Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

O deslocamento, em bytes, para o recurso intermediário.

</dd> <dt>

*FirstSubresource* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O índice do primeiro subrecurso no recurso. Os valores válidos variam de 0 a *MaxSubresources*.

</dd> <dt>

*NumSubresources* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O número de subrecursos no recurso. Os valores válidos variam de 1 a (*MaxSubresources*  -  *FirstSubresource*).

</dd> <dt>

*pSrcData* \[ no\]
</dt> <dd>

Tipo: **[ **D3D12 \_ \_ dados de subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***

Ponteiro para uma matriz (de comprimento *NumSubresources*) de ponteiros para D3D12 estruturas de [**\_ \_ dados de subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) que contêm descrições dos dados de subrecurso usados para a atualização.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

O tamanho do buffer, em bytes.

## <a name="remarks"></a>Comentários

A declaração dessa função começa com: `template <UINT MaxSubresources>`

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

 

