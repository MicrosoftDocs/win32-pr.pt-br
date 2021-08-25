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
ms.openlocfilehash: 2e1cdf3d8edcea88fbcfb260d87d3e79d62eb2aebc57144ae38defb018065f1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823306"
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

[DirectShow Estruturas](directshow-structures.md)
</dt> <dt>

[**IKsPin::KsQueryMediums**](ikspin-ksquerymediums.md)
</dt> <dt>

[**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium)
</dt> </dl>

 

 




