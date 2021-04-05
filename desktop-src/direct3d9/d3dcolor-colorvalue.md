---
description: Inicializa uma cor com os valores de ponto flutuante de vermelho, verde, azul e alfa fornecidos.
ms.assetid: 61825e33-4150-47cd-97f2-2144434a45e2
title: Macro D3DCOLOR_COLORVALUE (D3d9types. h)
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
ms.openlocfilehash: 3d5bb780a5999d8931335da1e9f49ad8af88dc12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103663974"
---
# <a name="d3dcolor_colorvalue-macro"></a>\_Macro D3DCOLOR ColorValue

Inicializa uma cor com os valores de ponto flutuante de vermelho, verde, azul e alfa fornecidos.

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

*m* 
</dt> <dd>

Componente verde da cor. Esse valor deve ser um valor de ponto flutuante no intervalo de 0,0 a 1,0.

</dd> <dt>

*b* 
</dt> <dd>

Componente azul da cor. Esse valor deve ser um valor de ponto flutuante no intervalo de 0,0 a 1,0.

</dd> <dt>

*um* 
</dt> <dd>

Componente alfa da cor. Esse valor deve ser um valor de ponto flutuante no intervalo de 0,0 a 1,0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o valor [**D3DCOLOR**](d3dcolor.md) que corresponde aos valores RGBA fornecidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




