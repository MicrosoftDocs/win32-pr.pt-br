---
description: Controla quando um provedor de eventos é descarregado.
ms.assetid: 7f11e521-d0f6-4c3c-8bfe-ceed2d106ed3
ms.tgt_platform: multiple
title: __EventProviderCacheControl classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderCacheControl
- Root.__EventProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 9d027fec5aea132524924655047c0f0a8aa8605d1972c6f91b2c2315c5834ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557920"
---
# <a name="__eventprovidercachecontrol-class"></a>\_\_Classe EventProviderCacheControl

A **\_ \_ classe de sistema EventProviderCacheControl** controla quando um provedor de eventos é descarregado. Ele está localizado apenas no \\ namespace raiz.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[singleton]
class __EventProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Membros

A **\_ \_ classe EventProviderCacheControl** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **\_ \_ classe EventProviderCacheControl** tem essas propriedades.

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Intervalo de tempo após Windows WMI (Instrumentação de Gerenciamento) libera um provedor de eventos. A hora está no [formato de intervalo](interval-format.md). Pode levar até duas vezes o intervalo especificado para descarregar o provedor.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **\_ \_ classe EventProviderCacheControl** é derivada de [**\_ \_ CacheControl.**](--cachecontrol.md)

Para obter mais informações sobre como usar essa classe, [consulte Descarregando um provedor](unloading-a-provider.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Root<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_Cachecontrol**](/windows/desktop/WmiSdk/--cachecontrol)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

