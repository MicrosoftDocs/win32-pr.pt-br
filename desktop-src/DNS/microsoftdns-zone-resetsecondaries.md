---
title: Método ResetSecondaries da classe MicrosoftDNS_Zone
description: O método ResetSecondaries redefine os endereços IP para servidores DNS secundários na zona.
ms.assetid: b9a47714-f180-40cf-831a-f59e804a4ca2
keywords:
- DNS do método ResetSecondaries
- Método ResetSecondaries DNS, classe MicrosoftDNS_Zone
- MicrosoftDNS_Zone classe DNS, método ResetSecondaries
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
ms.openlocfilehash: 3a78d65b2153782c38d6d91d34f642860e896ed1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918768"
---
# <a name="resetsecondaries-method-of-the-microsoftdns_zone-class"></a>Método ResetSecondaries da classe de \_ zona MicrosoftDNS

O método **ResetSecondaries** redefine os endereços IP para servidores DNS secundários na zona.

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

*SecondaryServers* \[ no\]
</dt> <dd>

Matriz de endereços IP para servidores DNS secundários.

</dd> <dt>

*SecureSecondaries* \[ no\]
</dt> <dd>

Especifica a segurança a ser aplicada e deve ser uma das seguintes:

-   SECSECURE de zona \_ \_ sem \_ segurança
-   ZONA \_ SECSECURE \_ \_ somente NS
-   lista de SECSECURE de zona \_ \_ \_ somente
-   SECSECURE de zona \_ \_ sem \_ XFR

</dd> <dt>

*NotifyServers* \[ no\]
</dt> <dd>

Endereço IP dos servidores DNS a ser notificado quando a zona for alterada.

</dd> <dt>

*Notificar* \[ no\]
</dt> <dd>

A configuração de notificação e deve ser uma das seguintes:

-   notificação de zona \_ \_ desativada
-   \_notificar \_ todos os \_ SECUNDÁRIOs da zona
-   lista de notificações de zona \_ \_ \_ somente

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

RR do tipo [**MicrosoftDNS \_ Zone**](microsoftdns-zone.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Zona MicrosoftDNS**](microsoftdns-zone.md)
</dt> <dt>

[**Método AgeAllRecords da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**Método ChangeZoneType da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**Método createzone da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**Método ForceRefresh da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Método getdistinguiname da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Método PauseZone da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Método ReloadZone da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Método ResumeZone da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Método UpdateFromDS da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Método WriteBackZone da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





