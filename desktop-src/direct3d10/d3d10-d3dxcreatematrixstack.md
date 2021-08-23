---
description: Criar uma pilha de matriz.
ms.assetid: df0f3564-0226-44b8-b22b-4dd27905c44c
title: Função D3DXCreateMatrixStack (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMatrixStack
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 90436f905c2470fd14b022a1c025737fa78726cf5e46286dec2e13d7392e9b32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498346"
---
# <a name="d3dxcreatematrixstack-function-d3dx10mathh"></a>Função D3DXCreateMatrixStack (D3DX10Math. h)

Criar uma pilha de matriz.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateMatrixStack(
  _In_  UINT              Flags,
  _Out_ LPD3DXMATRIXSTACK *ppStack
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Sinalizadores* \[ de no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Não implementado. Especifique zero.

</dd> <dt>

*ppStack* \[ fora\]
</dt> <dd>

Tipo: **LPD3DXMATRIXSTACK \***

O endereço de um ponteiro para uma pilha de matriz (consulte a [**interface ID3DXMatrixStack**](d3d10-id3dxmatrixstack.md)).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
