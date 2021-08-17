---
title: Função MemcpySubresource (D3dx12.h)
description: Copia uma sub-fonte linha por linha.
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
ms.openlocfilehash: 8c27e8cf9ffda237c2dad017b3a981ff71498a22c1c7b54ede032d6bf8c012a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733358"
---
# <a name="memcpysubresource-function"></a>Função MemcpySubresource

Copia uma sub-fonte linha por linha.

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

*pDest* \[ Em\]
</dt> <dd>

Tipo: **const [**D3D12 \_ MEMCPY \_ DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) \***

Um ponteiro para uma [**estrutura D3D12 \_ MEMCPY \_ DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) que descreve o destino da operação de cópia de memória.

</dd> <dt>

*pSrc* \[ Em\]
</dt> <dd>

Tipo: **const [**D3D12 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) \***

Um ponteiro para uma [**estrutura D3D12 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) que descreve a origem da operação de cópia de memória.

</dd> <dt>

*RowSizeInBytes* 
</dt> <dd>

Tipo: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)**

O tamanho, em bytes, de cada linha.

</dd> <dt>

*NumRows* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

O número de linhas.

</dd> <dt>

*NumSlices* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

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
| parâmetro<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções auxiliares do D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Sub-recursos](subresources.md)
</dt> </dl>

 

