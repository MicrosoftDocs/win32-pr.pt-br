---
description: Indica se a autenticação 802.1X é usada.
ms.assetid: dbddaf5a-7574-4282-ab4d-f6f697ed94ab
title: Elemento useOneX (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- useOneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 961f1b6be52da97ada2c230579ac281652a07fcbae67ac32d2399eb2968b1946
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912566"
---
# <a name="useonex-authencryption-element"></a>Elemento useOneX (authEncryption)

O elemento useOneX (authEncryption) indica se a autenticação 802.1X é usada.

``` syntax
<xs:element name="useOneX"
    type="boolean"
    minOccurs="0"
 />
```

O elemento é definido pelo [**elemento authEncryption.**](wlan-profileschema-authencryption-security-element.md)

## <a name="examples"></a>Exemplos

Para exibir perfis de exemplo que usam **o elemento useOneX,** consulte [Exemplos de perfil sem fio.](wireless-profile-samples.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista, Windows XP somente com aplicativos da área de trabalho SP3 \[\]<br/> |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                |
| Redistribuível<br/>          | API de LAN sem fio para Windows XP com SP2<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**authEncryption**](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**authEncryption (segurança)**](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




