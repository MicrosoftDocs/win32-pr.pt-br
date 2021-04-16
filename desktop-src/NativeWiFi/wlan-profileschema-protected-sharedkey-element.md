---
description: Indica se uma chave compartilhada é criptografada.
ms.assetid: 9206ef74-cd3e-4374-bea9-0c10505d10bf
title: Elemento protected (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- protected
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0b48ef0e07e5502ea8577904facc52f9f7e69838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758744"
---
# <a name="protected-sharedkey-element"></a>Elemento protected (sharedKey)

O elemento protected (sharedKey) indica se uma chave compartilhada é criptografada.

``` syntax
<xs:element name="protected"
    type="boolean"
 />
```

O elemento é definido pelo elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .

## <a name="remarks"></a>Comentários

Para o Windows Vista e o Windows Server 2008, o **protegido** sempre terá um valor de true se o perfil tiver sido recuperado do repositório de perfis (por exemplo, chamando [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)).

Para perfis destinados a uso no Windows XP com Service Pack 3 (SP3) ou API de LAN sem fio para Windows XP com Service Pack 2 (SP2), **protegido** deve ter um valor de false.

## <a name="examples"></a>Exemplos

Para exibir perfis de exemplo que usam o elemento **protegido** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                |
| Redistribuível<br/>          | API de LAN sem fio para Windows XP com SP2<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**sharedKey**](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**sharedKey (segurança)**](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




