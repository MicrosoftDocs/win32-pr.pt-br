---
title: Método ResetSecondaries da MicrosoftDNS_Zone classe
description: O método ResetSecondaries redefine os endereços IP para servidores DNS secundários na zona.
ms.assetid: b9a47714-f180-40cf-831a-f59e804a4ca2
keywords:
- Método RESETSecondaries DNS
- Classe dns do método ResetSecondaries, MicrosoftDNS_Zone dados
- MicrosoftDNS_Zone classe DNS , método ResetSecondaries
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ResetSecondaries
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ab3737bc8143f712560e5ea253237c97da4e2401b98886428642210805ca586
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957285"
---
# <a name="resetsecondaries-method-of-the-microsoftdns_zone-class"></a>Método ResetSecondaries da classe Zona \_ MicrosoftDNS

O **método ResetSecondaries** redefine os endereços IP para servidores DNS secundários na zona.

## <a name="syntax"></a>Sintaxe


```mof
void ResetSecondaries(
  [in]       string            SecondaryServers[],
  [in]       uint32            SecureSecondaries,
  [in]       string            NotifyServers[],
  [in]       uint32            Notify,
  [out, ref] MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SecondaryServers* \[ Em\]
</dt> <dd>

Matriz de endereços IP para servidores DNS secundários.

</dd> <dt>

*SecureSecondaries* \[ Em\]
</dt> <dd>

Especifica a segurança a ser aplicada e deve ser uma das seguintes:

-   ZONE \_ SECSECURE \_ SEM \_ SEGURANÇA
-   SOMENTE \_ NS DA ZONA SECSECURE \_ \_
-   ZONE \_ SECSECURE \_ LIST \_ ONLY
-   ZONE \_ SECSECURE \_ NO \_ XFR

</dd> <dt>

*NotifyServers* \[ Em\]
</dt> <dd>

Endereço IP dos Servidores DNS a serem notificados quando a zona for mudada.

</dd> <dt>

*Notificar* \[ Em\]
</dt> <dd>

Configuração de notificação e deve ser uma das seguintes:

-   NOTIFICAÇÃO \_ DE \_ ZONA OFF
-   NOTIFICAR \_ \_ TODAS AS \_ SECUNDÁRIAS DE ZONA
-   SOMENTE \_ LISTA DE \_ NOTIFICAÇÃO DE \_ ZONA

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

RR do tipo [**Zona MicrosoftDNS. \_**](microsoftdns-zone.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Zona \_ MicrosoftDNS**](microsoftdns-zone.md)
</dt> <dt>

[**Método AgeAllRecords da classe de zona \_ MicrosoftDNS**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**Método ChangeZoneType da classe de zona \_ MicrosoftDNS**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**Método CreateZone da classe de zona \_ MicrosoftDNS**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**Método ForceRefresh da classe de zona \_ MicrosoftDNS**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Método GetDistinguishedName da classe de zona \_ MicrosoftDNS**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Método PauseZone da classe zone \_ MicrosoftDNS**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Método ReloadZone da classe de zona \_ MicrosoftDNS**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Método ResumeZone da classe de zona \_ MicrosoftDNS**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Método UpdateFromDS da classe de zona \_ MicrosoftDNS**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Método WriteBackZone da classe de zona \_ MicrosoftDNS**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





