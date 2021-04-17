---
description: Especifica o valor que uma propriedade assume em um determinado momento.
ms.assetid: 117868b7-65e5-4b3b-9e50-4106ee6a65d0
title: Estrutura de DEXTER_PARAM (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_PARAM
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 22b0f6ef0a91f9a6d9163a03c17f6e86ee8b5f4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748614"
---
# <a name="dexter_param-structure"></a>\_Estrutura de parâmetro Dexter

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

Especifica o valor que uma propriedade assume em um determinado momento.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  BSTR   Name;
  DISPID dispID;
  LONG   nValues;
} DEXTER_PARAM;
```



## <a name="members"></a>Membros

<dl> <dt>

**Nome**
</dt> <dd>

Nome da propriedade.

</dd> <dt>

**dispID**
</dt> <dd>

Reservado. Definido como zero.

</dd> <dt>

**nValores**
</dt> <dd>

Número de valores que a propriedade assume.

</dd> </dl>

## <a name="remarks"></a>Comentários

O objeto deve dar suporte à interface **IDispatch** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>QEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[**valor de DEXTER \_**](dexter-value.md)
</dt> </dl>

 

 




