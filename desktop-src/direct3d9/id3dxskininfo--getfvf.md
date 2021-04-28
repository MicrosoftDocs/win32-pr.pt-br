---
description: 'Método ID3DXSkinInfo:: GetFVF – Obtém o valor de vértice da função fixa.'
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
ms.openlocfilehash: 3415f86f778fbb6fb3592927277e399584bc49a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107154"
---
# <a name="id3dxskininfogetfvf-method"></a>Método ID3DXSkinInfo:: GetFVF

Obtém o valor de vértice da função fixa.

## <a name="syntax"></a>Sintaxe


```C++
DWORD GetFVF();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Retorna os códigos de formato de vértice flexível (FVF).

## <a name="remarks"></a>Comentários

Esse método pode retornar 0 se o formato de vértice não puder ser mapeado diretamente para um código FVF. Isso ocorrerá para uma malha criada a partir de uma declaração de vértice que não tenha a mesma ordem e elementos suportados pelos códigos FVF.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetFVF**](id3dxskininfo--setfvf.md)
</dt> </dl>

 

 
