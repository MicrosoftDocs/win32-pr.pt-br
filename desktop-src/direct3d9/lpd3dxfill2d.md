---
description: Tipo de função usado pelas funções de preenchimento de textura.
ms.assetid: faa2d610-cf85-42d0-833c-a46fb7fe3dbf
title: LPD3DXFILL2D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c8c9d9ef610ee10faa069841a05f43c17b0885c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163735"
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

pOut-ponteiro para um vetor, que a função usa para retornar seu resultado. X, Y, Z e W serão mapeados para R, G, B e A, respectivamente.

pTexCoord-ponteiro para um vetor que contém as coordenadas do Texel que está sendo avaliado no momento. Os componentes de coordenadas de textura para textura e texturas de volume variam de 0 a 1. Os componentes da coordenada de textura para texturas de cubo variam de-1 a 1.

pTexelSize-ponteiro para um vetor que contém as dimensões do Texel atual.

pData-ponteiro para dados do usuário.

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Certifique-se de especificar a Convenção de chamada de [**tipos de dados do Windows**](../winprog/windows-data-types.md) ao declarar a função de retorno de chamada. Caso contrário, podem ocorrer estouros de pilha.



|                          |            |
|--------------------------|------------|
| parâmetro                   | d3dx9tex. h |
| Bibliotecas de importação           | d3dx9. lib  |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de retorno de chamada](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[LPD3DXFILL3D](lpd3dxfill3d.md)
</dt> </dl>

 

 
