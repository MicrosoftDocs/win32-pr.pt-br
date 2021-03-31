---
description: Define padrões de bit que habilitam planos de recorte definidos pelo usuário. Essas macros são definidas como uma conveniência ao definir valores para o \_ estado de RENDERIZAÇÃO D3DRS CLIPPLANEENABLE.
ms.assetid: 5bca2401-a3fb-4b1c-bb59-621b15da10f1
title: Macro D3DCLIPPLANEn (D3D9Types. h)
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
ms.openlocfilehash: 4508f1654a357eb80b3847b7562e230c6a9be4d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370934"
---
# <a name="d3dclipplanen-macro"></a>Macro D3DCLIPPLANEn

Define padrões de bit que habilitam planos de recorte definidos pelo usuário. Essas macros são definidas como uma conveniência ao definir valores para o \_ estado de RENDERIZAÇÃO D3DRS CLIPPLANEENABLE.

## <a name="syntax"></a>Sintaxe


```C++
void D3DCLIPPLANEn(void);
```



## <a name="parameters"></a>Parâmetros

Esta macro não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Essa macro não retorna um valor.

## <a name="remarks"></a>Comentários

Os planos de recorte definidos pelo usuário são habilitados quando o valor definido no \_ estado de RENDERIZAÇÃO D3DRS CLIPPLANEENABLE contém um ou mais conjuntos de bits (ou seja, não é 0). O valor do estado render não é importante; o sistema não interpreta o valor como um número. Em vez disso, o valor habilita o plano de recorte cujo bit correspondente está definido. O bit 0 controla o estado do primeiro plano de recorte (no índice 0), bit 1 o segundo plano e assim por diante.

Os padrões de bits criados por essas macros podem ser combinados usando uma operação OR lógica para habilitar simultaneamente vários planos de recorte. Omitir uma dessas macros da combinação efetivamente desabilita o plano de recorte nesse índice.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




