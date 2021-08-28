---
description: Especifica se os computadores usam o serviço interno de configuração automática (autoconfiguração) para gerenciar conexões sem fio.
ms.assetid: c255e0a0-65ae-44a8-95cb-1a000394109d
title: Elemento enableAutoConfig (globalFlags) (LAN_policy) para WLAN
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
ms.openlocfilehash: 77b09bf046cdbadb58c888a3084d14ed14794064bf9f11c110ccecaff105fceb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684406"
---
# <a name="enableautoconfig-globalflags-element-lan_policy-for-wlan"></a>Elemento enableAutoConfig (globalFlags) (LAN_policy) para WLAN 

O elemento **enableAutoConfig** (globalFlags) especifica se os computadores usam o serviço interno de configuração automática (AutoConfig) para gerenciar conexões sem fio. Quando **enableAutoConfig** tem um valor de false, os computadores não devem usar o autoConfig para gerenciar conexões sem fio e o serviço de configuração automática responde apenas a solicitações para habilitar o serviço. Quando **enableAutoConfig** tem um valor de true, os computadores podem usar o serviço de configuração automática.

Esse elemento é obrigatório. Quando um perfil é criado pelo serviço de configuração automática, esse elemento terá o valor padrão de TRUE.

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

O elemento **enableAutoConfig** é definido pelo elemento [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



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

 

 




