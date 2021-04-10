---
description: Especifica se o serviço de configuração automática para redes com fio tentará a autenticação de porta usando 802.1 X.
ms.assetid: ab6cfc59-9cfd-45d3-ad27-306ad4f6d4e1
title: Elemento OneXEnabled (segurança)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnabled
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9c76fce3b42cff648d03f520ddeb569a39e99f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170411"
---
# <a name="onexenabled-security-element"></a>Elemento OneXEnabled (segurança)

O elemento **OneXEnabled** (Security) especifica se o serviço de configuração automática para redes com fio tentará a autenticação de porta usando 802.1 x. Quando **OneXEnabled** é false, o serviço de configuração automática nunca usa 802.1 x para autenticação de porta. Quando **OneXEnabled** é true, o serviço de configuração automática tenta a autenticação de porta usando 802.1 x.

Esse elemento é opcional. O valor padrão é TRUE. Quando **OneXEnabled** não é especificado em um perfil, o 802.1 x pode ser usado para autenticação de porta.

``` syntax
<xs:element name="OneXEnabled"
    type="boolean"
 />
```

O elemento **OneXEnabled** é definido pelo elemento [**Security**](lan-profileschema-security-msm-element.md) .

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

 

 




