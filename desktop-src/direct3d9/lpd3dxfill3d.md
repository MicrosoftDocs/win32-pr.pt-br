---
description: LPD3DXFILL3D – tipo de função usado pelas funções de preenchimento de textura.
ms.assetid: ab2f3005-150f-46e1-b75b-75c39e7feed1
title: LPD3DXFILL3D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399c711b550124cf93889640277d86b8669e20b1dfc33b2d3865f73b29e85e4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799428"
---
# <a name="lpd3dxfill3d"></a>LPD3DXFILL3D

Tipo de função usado pelas funções de preenchimento de textura.

## <a name="syntax"></a>Sintaxe


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR3* pTexCoord, 
    CONST D3DXVECTOR3* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a>Parâmetros

pOut – ponteiro para um vetor, que a função usa para retornar seu resultado. X, Y, Z e W serão mapeados para R, G, B e A, respectivamente.

pTexCoord – ponteiro para um vetor que contém as coordenadas do texel que está sendo avaliado no momento. Os componentes de coordenadas de textura para textura e texturas de volume variam de 0 a 1. Os componentes de coordenadas de textura para texturas de cubo variam de -1 a 1.

pTexelSize – ponteiro para um vetor que contém as dimensões do texel atual.

pData – ponteiro para dados do usuário.

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Especifique a convenção [**de chamada Windows tipos**](../winprog/windows-data-types.md) de dados ao declarar a função de retorno de chamada. Caso contrário, podem ocorrer estouros de pilha.



| Requisito                         | Valor           |
|--------------------------|------------|
| parâmetro                   | d3dx9tex.h |
| Bibliotecas de importação           | d3dx9.lib  |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de retorno de chamada](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[LPD3DXFILL2D](lpd3dxfill2d.md)
</dt> </dl>

 

 
