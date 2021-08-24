---
description: LPD3DXFILL2D – tipo de função usado pelas funções de preenchimento de textura.
ms.assetid: faa2d610-cf85-42d0-833c-a46fb7fe3dbf
title: LPD3DXFILL2D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b6d1407d5b6ebad18f748d5e4ba78953ad6ca543aa6df7b798aa242658a0512
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846478"
---
# <a name="lpd3dxfill2d"></a>LPD3DXFILL2D

Tipo de função usado pelas funções de preenchimento de textura.

## <a name="syntax"></a>Sintaxe


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR2* pTexCoord, 
    CONST D3DXVECTOR2* pTexelSize, 
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

[LPD3DXFILL3D](lpd3dxfill3d.md)
</dt> </dl>

 

 
