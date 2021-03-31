---
description: Serve como uma classe pai para classes que controlam a geração de eventos, como eventos de temporizador.
ms.assetid: 381b06e7-2857-4932-9f52-f1d62efa8b79
ms.tgt_platform: multiple
title: Classe __EventGenerator
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventGenerator
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b40524405c3b284e7ec61414e36448cb37afeab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172145"
---
# <a name="__eventgenerator-class"></a>\_\_Classe EventGenerator

A classe de sistema **\_ \_ EventGenerator** é uma classe base abstrata que serve como uma classe pai para classes que controlam a geração de eventos, como [eventos de temporizador](receiving-a-timed-or-repeating-event.md).

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[abstract]
class __EventGenerator : __IndicationRelated
{
};
```

## <a name="members"></a>Membros

A classe **\_ \_ EventGenerator** não define nenhum membro.

## <a name="remarks"></a>Comentários

A classe **\_ \_ EventGenerator** é derivada de [**\_ \_ IndicationRelated**](--indicationrelated.md), que não tem propriedades.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_IndicationRelated**](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

