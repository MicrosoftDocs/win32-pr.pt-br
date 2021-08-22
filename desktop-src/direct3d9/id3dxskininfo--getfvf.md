---
description: Método ID3DXSkinInfo::GetFVF – Obtém o valor de vértice de função fixa.
ms.assetid: 9b80c4b9-2e5b-4965-99b9-ad6c459ef413
title: Método ID3DXSkinInfo::GetFVF (D3DX9Mesh.h)
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
ms.openlocfilehash: e7419e116cddd20aebfc61d7813ea2bd403ce04b897aa821f03a2ad48eae6965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492286"
---
# <a name="id3dxskininfogetfvf-method"></a>Método ID3DXSkinInfo::GetFVF

Obtém o valor de vértice de função fixa.

## <a name="syntax"></a>Sintaxe


```C++
DWORD GetFVF();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Retorna os códigos FVF (formato de vértice flexível).

## <a name="remarks"></a>Comentários

Esse método poderá retornar 0 se o formato de vértice não puder ser mapeado diretamente para um código FVF. Isso ocorrerá para uma malha criada de uma declaração de vértice que não tem a mesma ordem e elementos com suporte pelos códigos FVF.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetFVF**](id3dxskininfo--setfvf.md)
</dt> </dl>

 

 
