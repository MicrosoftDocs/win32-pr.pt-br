---
description: Define o tipo de animação conjunto de modos de loop usados para reprodução.
ms.assetid: 2ce26bf0-2b33-4193-a58f-03493a051351
title: Enumeração de D3DXPLAYBACK_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLAYBACK_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 642c3e1d49792016ea1d161352d4dda9fc1330aab544880e754659c735d1ecd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044784"
---
# <a name="d3dxplayback_type-enumeration"></a>\_Enumeração de tipo D3DXPLAYBACK

Define o tipo de animação conjunto de modos de loop usados para reprodução.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXPLAYBACK_TYPE { 
  D3DXPLAY_LOOP         = 0,
  D3DXPLAY_ONCE         = 1,
  D3DXPLAY_PINGPONG     = 2,
  D3DXPLAY_FORCE_DWORD  = 0x7fffffff
} D3DXPLAYBACK_TYPE, *LPD3DXPLAYBACK_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXPLAY_LOOP"></span><span id="d3dxplay_loop"></span>**\_Loop D3DXPLAY**
</dt> <dd>

A animação se repete inparadamente.

</dd> <dt>

<span id="D3DXPLAY_ONCE"></span><span id="d3dxplay_once"></span>**D3DXPLAY \_ uma vez**
</dt> <dd>

A animação é reproduzida uma vez e, em seguida, é interrompida no último quadro.

</dd> <dt>

<span id="D3DXPLAY_PINGPONG"></span><span id="d3dxplay_pingpong"></span>**D3DXPLAY \_ PINGPONG**
</dt> <dd>

A animação alterna perversamente entre a reprodução e a reprodução.

</dd> <dt>

<span id="D3DXPLAY_FORCE_DWORD"></span><span id="d3dxplay_force_dword"></span>**D3DXPLAY \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




