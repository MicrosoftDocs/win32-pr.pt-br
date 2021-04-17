---
description: A \_ estrutura do item KSMULTIPLE descreve o tamanho e a contagem de propriedades de comprimento variável em Pins do modo kernel.
ms.assetid: aedbf7bc-393d-4ab5-afcd-d8822b925f07
title: Estrutura de KSMULTIPLE_ITEM (KS. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSMULTIPLE_ITEM
api_type:
- HeaderDef
api_location:
- ks.h
ms.openlocfilehash: 62e26b1aa8804514588e66c1d02e1f0643e97bcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759495"
---
# <a name="ksmultiple_item-structure"></a>\_Estrutura de item KSMULTIPLE

A `KSMULTIPLE_ITEM` estrutura descreve o tamanho e a contagem de propriedades de comprimento variável em Pins do modo kernel.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  ULONG Size;
  ULONG Count;
} KSMULTIPLE_ITEM, *PKSMULTIPLE_ITEM;
```



## <a name="members"></a>Membros

<dl> <dt>

**Tamanho**
</dt> <dd>

Tamanho do bloco de memória retornado, em bytes. O tamanho inclui a estrutura do **\_ Item KSMULTIPLE** e os itens que o seguem.

</dd> <dt>

**Count**
</dt> <dd>

Especifica o número total de itens que seguem essa estrutura.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>KS. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do DirectShow](directshow-structures.md)
</dt> <dt>

[**IKsPin::KsQueryMediums**](ikspin-ksquerymediums.md)
</dt> <dt>

[**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium)
</dt> </dl>

 

 




