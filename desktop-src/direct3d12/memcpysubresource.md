---
title: Função MemcpySubresource (D3dx12. h)
description: Copia uma linha de subrecurso por linha.
ms.assetid: 33A9F99D-FD85-4FD6-AFD6-7A10F16C3D9B
keywords:
- Função MemcpySubresource
topic_type:
- apiref
api_name:
- MemcpySubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b955211a490927033186442480b3449773b4ebcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781143"
---
# <a name="memcpysubresource-function"></a>Função MemcpySubresource

Copia uma linha de subrecurso por linha.

## <a name="syntax"></a>Sintaxe


```C++
void inline MemcpySubresource(
  _In_ const D3D12_MEMCPY_DEST      *pDest,
  _In_ const D3D12_SUBRESOURCE_DATA *pSrc,
             SIZE_T                 RowSizeInBytes,
             UINT                   NumRows,
             UINT                   NumSlices
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDest* \[ no\]
</dt> <dd>

Tipo: **const [**D3D12 \_ MEMCPY \_ dest**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) \***

Um ponteiro para uma estrutura de [**\_ \_ dest D3D12 MEMCPY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) que descreve o destino da operação de cópia de memória.

</dd> <dt>

*pSrc* \[ no\]
</dt> <dd>

Tipo: **const [**D3D12 \_ subresource \_ Data**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) \***

Um ponteiro para uma estrutura de [**\_ \_ dados de subrecurso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) que descreve a origem da operação de cópia de memória.

</dd> <dt>

*RowSizeInBytes* 
</dt> <dd>

Tipo: **[ **tamanho \_ T**](/windows/desktop/WinProg/windows-data-types)**

O tamanho, em bytes, de cada linha.

</dd> <dt>

*NumRows* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O número de linhas.

</dd> <dt>

*NumSlices* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O número de fatias.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Considere também os seguintes métodos:

-   [**ID3D12Resource::WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource)
-   [**ID3D12Resource::ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource)
-   [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)

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

 

