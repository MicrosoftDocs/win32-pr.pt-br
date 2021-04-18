---
title: Função D3D12IsLayoutOpaque (D3dx12. h)
description: Indica se o layout é opaco.
ms.assetid: 43B46A18-A725-4999-BD97-108032793A95
keywords:
- Função D3D12IsLayoutOpaque
topic_type:
- apiref
api_name:
- D3D12IsLayoutOpaque
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971c44688e57dd1081d33a4a077a8dcadcb89abf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807335"
---
# <a name="d3d12islayoutopaque-function"></a>Função D3D12IsLayoutOpaque

Indica se o layout é opaco.

## <a name="syntax"></a>Sintaxe


```C++
bool inline D3D12IsLayoutOpaque(
   D3D12_TEXTURE_LAYOUT Layout
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Layout* 
</dt> <dd>

Tipo: **[ **\_ \_ layout de textura D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)**

O layout a ser verificado, como [**um \_ \_ layout de textura D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **bool**

Um **bool** que indica se o layout é opaco. Um layout será opaco se for um \_ layout de textura D3D12 \_ \_ desconhecido ou D3D12 do \_ layout de textura \_ \_ 64 KB \_ indefinido \_ SWIZZLE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções auxiliares do D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





