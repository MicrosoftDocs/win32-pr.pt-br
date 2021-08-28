---
description: Sinalizadores usados para obter informações de retorno de chamada.
ms.assetid: e8126ff0-db23-4da6-a999-0efb8c2647da
title: D3DXCALLBACK_SEARCH_FLAGS enumeração (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCALLBACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0a050263934684f766bb9b7d58b83665a31a5edbd099a43ad1947eba74ca25bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676376"
---
# <a name="d3dxcallback_search_flags-enumeration"></a>Enumeração DE SINALIZADORES DE PESQUISA D3DXCALLBACK \_ \_

Sinalizadores usados para obter informações de retorno de chamada.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXCALLBACK_SEARCH_FLAGS { 
  D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION  = 1,
  D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION     = 2,
  D3DXCALLBACK_SEARCH_FORCE_DWORD                 = 0x7fffffff
} D3DXCALLBACK_SEARCH_FLAGS, *LPD3DXCALLBACK_SEARCH_FLAGS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION"></span><span id="d3dxcallback_search_excluding_initial_position"></span>**PESQUISA D3DXCALLBACK \_ \_ EXCLUINDO A \_ POSIÇÃO \_ INICIAL**
</dt> <dd>

Exclua retornos de chamada localizados na posição inicial da pesquisa.

</dd> <dt>

<span id="D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION"></span><span id="d3dxcallback_search_behind_initial_position"></span>**D3DXCALLBACK \_ SEARCH POR TRÁS DA POSIÇÃO \_ \_ \_ INICIAL**
</dt> <dd>

Inverta a direção da pesquisa de retorno de chamada.

</dd> <dt>

<span id="D3DXCALLBACK_SEARCH_FORCE_DWORD"></span><span id="d3dxcallback_search_force_dword"></span>**D3DXCALLBACK \_ SEARCH \_ FORCE \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar para 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada para um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




