---
description: Contém o nome de um perfil de LAN sem fio.
ms.assetid: b8977183-7b5d-4c79-9065-ade85ed45716
title: Elemento Name (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 79174d1cb24fff1841b3022fa06e201794415ce5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502234"
---
# <a name="name-wlanprofile-element"></a>Elemento Name (WLANProfile)

O elemento Name (WLANProfile) contém o nome de um perfil de LAN sem fio.

``` syntax
<xs:element name="name"
    type="nameType"
 />
```

O elemento **Name** é definido pelo elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="remarks"></a>Comentários

Os nomes diferenciam maiúsculas de minúsculas.

Para o Windows XP com Service Pack 3 (SP3) e a API de LAN sem fio para Windows XP com Service Pack 2 (SP2), o elemento Name é ignorado quando o perfil é salvo no repositório de perfis. O nome do perfil é derivado do SSID da rede. Para perfis de rede de infraestrutura, o nome do perfil é o SSID da rede. Para perfis de rede ad hoc, o nome do perfil é o SSID da rede ad hoc seguida por `-adhoc` . Os caracteres de escape XML, como &, não são exibidos. Evite usar caracteres de escape XML em nomes SSID para perfis implantados no Windows XP com SP3 ou API de LAN sem fio para Windows XP com SP2.

Para qualquer perfil de rede destinado a uso somente no Windows Vista ou no Windows Server 2008, o nome pode ser qualquer cadeia de caracteres.

## <a name="examples"></a>Exemplos

Para exibir perfis de exemplo que usam o elemento **Name** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).

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

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




