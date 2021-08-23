---
description: Especifica se o serviço de configuração automática para redes com fio tentará a autenticação de porta usando 802.1X.
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
ms.openlocfilehash: aaaf5344078e4c8da2e5ee2118eed84563ebeb4daa8aebd700a29630b2fe4301
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801086"
---
# <a name="onexenabled-security-element"></a>Elemento OneXEnabled (segurança)

O **elemento OneXEnabled** (segurança) especifica se o serviço de configuração automática para redes com fio tentará a autenticação de porta usando 802.1X. Quando **OneXEnabled** é FALSE, o serviço de configuração automática nunca usa 802.1X para autenticação de porta. Quando **OneXEnabled** é TRUE, o serviço de configuração automática tenta a autenticação de porta usando 802.1X.

Esse elemento é opcional. O valor padrão é TRUE. Quando **OneXEnabled** não for especificado em um perfil, 802.1X poderá ser usado para autenticação de porta.

``` syntax
<xs:element name="OneXEnabled"
    type="boolean"
 />
```

O **elemento OneXEnabled** é definido pelo [**elemento de**](lan-profileschema-security-msm-element.md) segurança.

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

 

 




