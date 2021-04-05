---
description: Especifica se os computadores usam o serviço de configuração automática interno para gerenciar conexões com redes com fio que exigem autenticação de camada 2 (como 802.1 X).
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
ms.openlocfilehash: af1ca32f177140bbfc6563f74df5afc519ee0c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662588"
---
# <a name="enableautoconfig-globalflags-element-lan_policy"></a>Elemento enableAutoConfig (globalFlags) (LAN_policy)

O elemento **enableAutoConfig** (globalFlags) especifica se os computadores usam o serviço de configuração automática interno para gerenciar conexões com redes com fio que exigem autenticação de camada 2 (como 802.1 x).

Quando **enableAutoConfig** tem um valor de false, os computadores não devem usar o serviço de configuração automática interno para gerenciar conexões que exigem autenticação de camada 2. Em vez disso, a rede especificada no elemento [**ProfileList**](lan-policyschema-profilelist-lanpolicy-element.md) é a única rede disponível para conexão. O serviço de configuração automática responderá apenas às solicitações para habilitar o serviço.

Quando **enableAutoConfig** tem um valor de true, os computadores podem usar o serviço de configuração automática interno para se conectar a redes com fio que exigem autenticação de camada 2.

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

O elemento **enableAutoConfig** é definido pelo elemento [**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



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

 

 




