---
description: Determina quando o WMI deve liberar um provedor de consumidor de eventos.
ms.assetid: 93246826-8070-4e05-96f0-f773041ed1d4
ms.tgt_platform: multiple
title: Classe __EventConsumerProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderCacheControl
- Root.__EventConsumerProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: f769427c77f6efdf9a521a63f7334d5d27416c04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765708"
---
# <a name="__eventconsumerprovidercachecontrol-class"></a>\_\_Classe EventConsumerProviderCacheControl

A classe de sistema **\_ \_ EventConsumerProviderCacheControl** determina quando o WMI deve liberar um provedor de consumidor de eventos. A classe **\_ \_ EventConsumerProviderCacheControl** é uma classe singleton. Ele está localizado somente no \\ namespace raiz.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[singleton]
class __EventConsumerProviderCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ EventConsumerProviderCacheControl** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ EventConsumerProviderCacheControl** tem essas propriedades.

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Intervalo de tempo após o qual o WMI libera um provedor de consumidor de eventos. Pode levar até duas vezes o intervalo especificado para descarregar o provedor. A hora está no [formato de intervalo](interval-format.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ EventConsumerProviderCacheControl** é derivada de [**\_ \_ CacheControl**](--cachecontrol.md). Para obter mais informações sobre como usar essa classe, consulte [descarregando um provedor](unloading-a-provider.md).

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

 

 




