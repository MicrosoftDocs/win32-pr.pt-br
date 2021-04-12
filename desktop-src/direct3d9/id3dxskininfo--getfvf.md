---
description: Obtém o valor de vértice da função fixa.
ms.assetid: 9b80c4b9-2e5b-4965-99b9-ad6c459ef413
title: 'Método ID3DXSkinInfo:: GetFVF (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6d48cd9cea6efd6cb43e6da6877a7aaf42909c71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298463"
---
# <a name="id3dxskininfogetfvf-method"></a>Método ID3DXSkinInfo:: GetFVF

Obtém o valor de vértice da função fixa.

## <a name="syntax"></a>Sintaxe


```C++
DWORD GetFVF();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Retorna os códigos de formato de vértice flexível (FVF).

## <a name="remarks"></a>Comentários

Esse método pode retornar 0 se o formato de vértice não puder ser mapeado diretamente para um código FVF. Isso ocorrerá para uma malha criada a partir de uma declaração de vértice que não tenha a mesma ordem e elementos suportados pelos códigos FVF.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetFVF**](id3dxskininfo--setfvf.md)
</dt> </dl>

 

 
