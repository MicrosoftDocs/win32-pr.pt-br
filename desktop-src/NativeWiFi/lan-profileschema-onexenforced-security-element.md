---
description: Especifica se o serviço de configuração automática para redes com fio requer o uso do 802.1 X para autenticação de porta.
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
ms.openlocfilehash: e6656238b0745f8bfef9aff5bcb0b80775dd1da2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789748"
---
# <a name="onexenforced-security-element"></a>Elemento OneXEnforced (segurança)

O elemento **OneXEnforced** (Security) especifica se o serviço de configuração automática para redes com fio requer o uso do 802.1 x para autenticação de porta. Quando **OneXEnforced** é true, o serviço de configuração automática deve usar 802.1 x para autenticação de porta. Quando **OneXEnforced** for false, o serviço de configuração automática tentará usar 802.1 x para autenticação de porta, mas o serviço fará o fallback para sem autenticação se a autenticação 802.1 x falhar por qualquer motivo.

Esse elemento é opcional. O valor padrão é FALSE.

Esse elemento tem apenas um valor significativo se [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md) for true. Se **OneXEnabled** for false, o valor desse elemento será ignorado.

``` syntax
<xs:element name="OneXEnforced"
    type="boolean"
 />
```

O elemento **OneXEnforced** é definido pelo elemento [**Security**](lan-profileschema-security-msm-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**segurança**](lan-profileschema-security-msm-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**segurança (MSM)**](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




