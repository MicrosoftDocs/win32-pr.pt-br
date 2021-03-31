---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_WKSType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de serviços de Well-Known (WKS).
ms.assetid: 6d910716-74f9-48a0-b43c-3243f5518caf
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_WKSType
- MicrosoftDNS_WKSType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e27b62bd2008c58d283d0e7564fa7821c452cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824553"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_wkstype-class"></a>Método CreateInstanceFromPropertyData da \_ classe WKSType MicrosoftDNS

O método **CreateInstanceFromPropertyData** instancia um registro de recurso de serviços de Well-Known (WKS).

## <a name="syntax"></a>Sintaxe


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               InternetAddress,
  [in]           string               IPProtocol,
  [in]           string               Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DnsServerName* \[ no\]
</dt> <dd>

FQDN ou endereço IP do servidor DNS que contém este RR.

</dd> <dt>

*ContainerName* \[ no\]
</dt> <dd>

Nome do contêiner para a zona, o cache ou a instância de RootHints que contém esse RR.

</dd> <dt>

*OwnerName* \[ no\]
</dt> <dd>

Nome do proprietário do RR.

</dd> <dt>

*RecordClass* \[ em, opcional\]
</dt> <dd>

Classe do RR. O valor padrão é 1. Os valores a seguir são válidos.



| Valor                                                                                                | Significado                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | NO (Internet)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | CS (CSNET)<br/>    |
| <span id="3"></span><dl> <dt>**Beta**</dt> </dl> | CH (CAOS)<br/>    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | HS (Hesiod)<br/>   |



 

</dd> <dt>

*TTL* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*InternetAddress* \[ no\]
</dt> <dd>

Endereço IP da Internet para o proprietário do registro.

</dd> <dt>

*IPProtocol* \[ no\]
</dt> <dd>

Cadeia de caracteres que representa o protocolo IP para este registro. Os valores válidos são UDP ou TCP.

</dd> <dt>

*Serviços* \[ do no\]
</dt> <dd>

Cadeia de caracteres que contém todos os serviços usados pelo registro WKS (serviço bem conhecido).

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referência ao novo objeto.

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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**MicrosoftDNS \_ WKSType**](microsoftdns-wkstype.md)
</dt> <dt>

[**Método Modify da classe MicrosoftDNS \_ WKSType**](microsoftdns-wkstype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





