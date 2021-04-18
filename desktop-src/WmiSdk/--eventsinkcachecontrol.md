---
description: Usado para determinar quando o WMI libera um ponteiro IWbemUnboundObjectSink de provedores de consumidor de eventos.
ms.assetid: f7b14efc-a2f7-4e99-8ec8-5b5af0743139
ms.tgt_platform: multiple
title: Classe __EventSinkCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventSinkCacheControl
- Root.__EventSinkCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 9d20e64fed1ee6ba5622d5e6a342a60485f53d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810728"
---
# <a name="__eventsinkcachecontrol-class"></a>\_\_Classe EventSinkCacheControl

A classe de sistema **\_ \_ EventSinkCacheControl** é usada para determinar quando o WMI libera o ponteiro [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) de um provedor de consumidor de evento. A classe **\_ \_ EventSinkCacheControl** é uma classe singleton. Ele está localizado somente no \\ namespace raiz.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[singleton]
class __EventSinkCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ EventSinkCacheControl** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ EventSinkCacheControl** tem essas propriedades.

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Intervalo de tempo após o qual o WMI libera um provedor de eventos. Pode levar até duas vezes o intervalo especificado para descarregar o provedor. A hora está no [formato de intervalo](interval-format.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ EventSinkCacheControl** é derivada de [**\_ \_ CacheControl**](--cachecontrol.md). Para obter mais informações sobre como usar essa classe, consulte [descarregando um provedor](unloading-a-provider.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Root<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

 




