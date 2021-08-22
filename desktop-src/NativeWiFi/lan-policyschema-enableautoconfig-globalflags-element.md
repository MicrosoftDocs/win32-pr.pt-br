---
description: Especifica se os máquinas usam o serviço de configuração automática interna para gerenciar conexões com redes com fio que exigem autenticação de camada 2 (como 802.1X).
ms.assetid: c7a0f6bc-4d42-4d95-8483-2c480f4d8db9
title: Elemento enableAutoConfig (globalFlags) (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- enableAutoConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 2842da69b07136df80d15ea84553aecdf2c62d417c73f7ec85d9c315b819a397
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780196"
---
# <a name="enableautoconfig-globalflags-element-lan_policy"></a>Elemento enableAutoConfig (globalFlags) (LAN_policy)

O **elemento enableAutoConfig** (globalFlags) especifica se os máquinas usam o serviço de configuração automática interna para gerenciar conexões com redes com fio que exigem autenticação de camada 2 (como 802.1X).

Quando **enableAutoConfig** tem um valor FALSE, os máquinas não devem usar o serviço de configuração automática interna para gerenciar conexões que exigem autenticação de camada 2. Em vez disso, a rede especificada no [**elemento profileList**](lan-policyschema-profilelist-lanpolicy-element.md) é a única rede disponível para conexão. O serviço de configuração automática responderá apenas às solicitações para habilitar o serviço.

Quando **enableAutoConfig** tem um valor TRUE, os máquinas podem usar o serviço de configuração automática interna para se conectar a redes com fio que exigem autenticação de camada 2.

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

O **elemento enableAutoConfig** é definido pelo [**elemento globalFlags.**](lan-policyschema-globalflags-lanpolicy-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**globalFlags (LANPolicy)**](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> </dl>

 

 




