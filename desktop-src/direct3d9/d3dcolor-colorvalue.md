---
description: Inicializa uma cor com os valores de ponto flutuante vermelho, verde, azul e alfa fornecidos.
ms.assetid: 61825e33-4150-47cd-97f2-2144434a45e2
title: D3DCOLOR_COLORVALUE macro (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_COLORVALUE
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: f4ee10003e0f4fdeae937d8ac786b4d389a91ec0326c2d6288d10af2a63e2286
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751226"
---
# <a name="d3dcolor_colorvalue-macro"></a>Macro COLORVALUE D3DCOLOR \_

Inicializa uma cor com os valores de ponto flutuante vermelho, verde, azul e alfa fornecidos.

## <a name="syntax"></a>Sintaxe


```C++
D3DCOLOR D3DCOLOR_COLORVALUE(
   float r,
   float g,
   float b,
   float a
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*r* 
</dt> <dd>

Componente vermelho da cor. Esse valor deve ser um valor de ponto flutuante no intervalo de 0,0 a 1,0.

</dd> <dt>

*G* 
</dt> <dd>

Componente verde da cor. Esse valor deve ser um valor de ponto flutuante no intervalo de 0,0 a 1,0.

</dd> <dt>

*b* 
</dt> <dd>

Componente azul da cor. Esse valor deve ser um valor de ponto flutuante no intervalo de 0,0 a 1,0.

</dd> <dt>

*Um* 
</dt> <dd>

Componente alfa da cor. Esse valor deve ser um valor de ponto flutuante no intervalo de 0,0 a 1,0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o [**valor D3DCOLOR**](d3dcolor.md) que corresponde aos valores de RGBA fornecidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




