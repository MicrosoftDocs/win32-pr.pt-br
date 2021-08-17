---
description: Define padrões de bits que habilitam planos de recorte definidos pelo usuário. Essas macros são definidas como uma conveniência ao definir valores para o estado de \_ renderização CLIPPLANEENABLE D3DRS.
ms.assetid: 5bca2401-a3fb-4b1c-bb59-621b15da10f1
title: Macro D3DCLIPPLANEn (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPPLANEn
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 315f1cdd8f8835b869f04edd9869243f3e05a9c2c9a08a41eeffc014727b3fc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805463"
---
# <a name="d3dclipplanen-macro"></a>Macro D3DCLIPPLANEn

Define padrões de bits que habilitam planos de recorte definidos pelo usuário. Essas macros são definidas como uma conveniência ao definir valores para o estado de \_ renderização CLIPPLANEENABLE D3DRS.

## <a name="syntax"></a>Sintaxe


```C++
void D3DCLIPPLANEn(void);
```



## <a name="parameters"></a>Parâmetros

Essa macro não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Essa macro não retorna um valor.

## <a name="remarks"></a>Comentários

Os planos de recorte definidos pelo usuário são habilitados quando o valor definido no estado de renderização CLIPPLANEENABLE D3DRS contém um ou mais bits definidos \_ (ou seja, não é 0). O valor do estado de renderização não é importante; o sistema não interpreta o valor como um número. Em vez disso, o valor habilita o plano de recorte cujo bit correspondente está definido. O bit 0 controla o estado do primeiro plano de recorte (no índice 0), bit 1 no segundo plano e assim por diante.

Os padrões de bits que essas macros criam podem ser combinados usando uma operação OR lógica para habilitar simultaneamente vários planos de recorte. Omitir uma dessas macros da combinação desabilita efetivamente o plano de recorte nesse índice.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




