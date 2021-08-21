---
description: 'Método ID3DXBaseMesh:: GetFVF – Obtém o valor de vértice da função fixa.'
ms.assetid: ed56ff2d-0366-426c-9f9a-7d1a7c5d1a7c
title: 'Método ID3DXBaseMesh:: GetFVF (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 814f14645e5e7f0aa883f04e689f0774441482b86223bf485fa1fc8a395618c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987616"
---
# <a name="id3dxbasemeshgetfvf-method"></a>Método ID3DXBaseMesh:: GetFVF

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



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
