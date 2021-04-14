---
description: Especifica se as redes negadas aparecem no assistente conectar-se a uma rede.
ms.assetid: d0a13a80-2532-4383-8946-2536cc1f5e12
title: Elemento showDeniedNetwork (globalFlags)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- showDeniedNetwork
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33049dad00e5fda22e3f739d3dc200a282481a8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502238"
---
# <a name="showdeniednetwork-globalflags-element"></a>Elemento showDeniedNetwork (globalFlags)

O elemento **showDeniedNetwork** (globalFlags) especifica se as redes negadas aparecem no assistente **conectar a uma rede** . As redes podem ser negadas pela política de grupo ou pelas configurações do usuário. Quando **showDeniedNetwork** tem um valor de true, redes negadas aparecem no assistente **conectar-se a uma rede** ; caso contrário, as redes negadas não aparecerão no assistente.

Esse elemento é obrigatório. Quando um perfil é criado pelo serviço de configuração automática, esse elemento assumirá o valor padrão de FALSE.

``` syntax
<xs:element name="showDeniedNetwork"
    type="boolean"
 />
```

O elemento **showDeniedNetwork** é definido pelo elemento [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**globalFlags (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




