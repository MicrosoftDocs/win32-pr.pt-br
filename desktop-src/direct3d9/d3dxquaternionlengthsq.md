---
description: Retorna o quadrado do comprimento de um quaterão.
ms.assetid: 358d2a2b-7baf-4ae9-9b92-7a7f01ca843b
title: Função D3DXQuaternionLengthSq (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLengthSq
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 062339144a182d0ceeec27d34dd0d572d470ef10fcc1722375f89156b6b55874
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631076"
---
# <a name="d3dxquaternionlengthsq-function"></a>Função D3DXQuaternionLengthSq

Retorna o quadrado do comprimento de um quaterão.

## <a name="syntax"></a>Sintaxe


```C++
FLOAT D3DXQuaternionLengthSq(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pQ* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Ponteiro para a estrutura [**D3DXQUATERNION de origem.**](d3dxquaternion.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

O comprimento quadrado do quatrion.

## <a name="remarks"></a>Comentários

Use [**D3DXQuaternionNormalize para**](d3dxquaternionnormalize.md) qualquer entrada de quatérnion que ainda não tenha sido normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionLength**](d3dxquaternionlength.md)
</dt> </dl>

 

 
