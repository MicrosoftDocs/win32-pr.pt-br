---
description: Indica se é para se conectar a uma rede oculta.
ms.assetid: 31b859e9-adc7-49e2-91d9-4fb63a35addb
title: Elemento nonBroadcast (SSIDConfig)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nonBroadcast
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 695bede631b19c028a55a2f3ca82ba994ca12ada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766368"
---
# <a name="nonbroadcast-ssidconfig-element"></a>Elemento nonBroadcast (SSIDConfig)

O elemento nonBroadcast (SSIDConfig) indica se uma rede oculta deve ser conectada. Se uma rede não difundir seu SSID, ela é conhecida como rede oculta. Se vários SSIDs forem definidos dentro do perfil, eles deverão ter o mesmo valor de não-difusão.

Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) for definido como **ESS**, esse valor poderá ser "true" ou "false". Se esse elemento não estiver presente, o valor padrão será "false".

Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) for definido como **IBSS**, esse valor deverá ser "false". Se esse elemento não estiver presente, o valor padrão será "false".

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.

``` syntax
<xs:element name="nonBroadcast"
    type="boolean"
    minOccurs="0"
 />
```

O elemento é definido pelo elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) .

## <a name="examples"></a>Exemplos

Para exibir um perfil de exemplo que usa o elemento **nonBroadcast** , consulte [exemplo de perfil sem difusão](non-broadcast-profile-sample.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




