---
title: Função UpdateSubresources (heap-alocação) (D3dx12. h)
description: Atualiza os subrecursos com uma implementação de alocação de heap.
ms.assetid: 328D8755-D328-471D-AAF4-9771CBFF7539
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
ms.openlocfilehash: bc4e476501c91c3e7508c0aefdc1d9d6c99a057840b5a126879c8b4ff3608f68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460746"
---
# <a name="updatesubresources-heap-allocating-function"></a>Função UpdateSubresources (heap-alocando)

Atualiza os subrecursos com uma implementação de alocação de heap.

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

Um ponteiro para a interface [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) da lista de comandos.

</dd> <dt>

*pDestinationResource* \[ no\]
</dt> <dd>

Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Um ponteiro para a interface [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) que representa o recurso de destino.

</dd> <dt>

*pIntermediate* \[ no\]
</dt> <dd>

Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Um ponteiro para a interface [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) que representa o recurso intermediário.

</dd> <dt>

*IntermediateOffset* 
</dt> <dd>

Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

O deslocamento, em bytes, para o recurso intermediário.

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

*pSrcData* \[ no\]
</dt> <dd>

Tipo: **[ **D3D12 \_ \_ dados de subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***

Ponteiro para uma matriz (de comprimento *NumSubresources*) de ponteiros para D3D12 estruturas de [**\_ \_ dados de subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) que contêm descrições dos dados de subrecurso usados para a atualização.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

 

