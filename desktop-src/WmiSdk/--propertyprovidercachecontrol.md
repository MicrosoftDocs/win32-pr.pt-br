---
description: Controla o cache quando um provedor de propriedades é descarregado.
ms.assetid: 8fc7de7a-889c-4d53-97ea-a676879de1d3
ms.tgt_platform: multiple
title: Classe __PropertyProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderCacheControl
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d153049a9635b4b77a1ad09ca0ee64835b9bcfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169812"
---
# <a name="__propertyprovidercachecontrol-class"></a>\_\_Classe PropertyProviderCacheControl

A classe **\_ \_ PropertyProviderCacheControl** controla o cache quando um provedor de propriedades é descarregado. Essa classe existe somente no \\ namespace raiz.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __PropertyProviderCacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ PropertyProviderCacheControl** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ PropertyProviderCacheControl** tem essas propriedades.

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Intervalo de tempo após o WMI liberar um provedor de propriedades. A hora está no formato de intervalo.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ PropertyProviderCacheControl** é derivada de [**\_ \_ CacheControl**](--cachecontrol.md). Para obter mais informações, consulte [descarregando um provedor](unloading-a-provider.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

 




