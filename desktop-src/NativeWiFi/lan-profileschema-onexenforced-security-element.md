---
description: Especifica se o serviço de configuração automática para redes com fio requer o uso de 802.1X para autenticação de porta.
ms.assetid: fb01be74-46ad-4d8c-be4c-50ae05a0c33b
title: Elemento OneXEnforced (segurança)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnforced
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bcaa8604fb8b813417299725133e9c6e51f7d7510b540cf8495ff9009b9d1c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798436"
---
# <a name="onexenforced-security-element"></a>Elemento OneXEnforced (segurança)

O **elemento OneXEnforced** (segurança) especifica se o serviço de configuração automática para redes com fio requer o uso de 802.1X para autenticação de porta. Quando **OneXEnforced** é TRUE, o serviço de configuração automática deve usar 802.1X para autenticação de porta. Quando **OneXEnforced** for FALSE, o serviço de configuração automática tentará usar 802.1X para autenticação de porta, mas o serviço retornará para nenhuma autenticação se a autenticação 802.1X falhar por qualquer motivo.

Esse elemento é opcional. O valor padrão é FALSE.

Esse elemento só terá um valor significativo se [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md) for TRUE. Se **OneXEnabled** for FALSE, o valor desse elemento será ignorado.

``` syntax
<xs:element name="OneXEnforced"
    type="boolean"
 />
```

O **elemento OneXEnforced** é definido pelo [**elemento de**](lan-profileschema-security-msm-element.md) segurança.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**Segurança**](lan-profileschema-security-msm-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**security (MSM)**](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




