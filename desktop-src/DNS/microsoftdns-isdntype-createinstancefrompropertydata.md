---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_ISDNType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de ISDN.
ms.assetid: cd3b98e3-a804-473e-8831-5f045d43a54f
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_ISDNType
- MicrosoftDNS_ISDNType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 082bf764c93e19b7829309de62c4ce5ff99650322c5bb4533db7e4c9b5c23bca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433036"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_isdntype-class"></a>Método CreateInstanceFromPropertyData da \_ classe isdntype MicrosoftDNS

O método **CreateInstanceFromPropertyData** instancia um registro de recurso de ISDN.

## <a name="syntax"></a>Sintaxe


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           string                ISDNNumber,
  [in]           string                SubAddress,
  [out, ref]     MicrosoftDNS_ISDNType &RR
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
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | CH (CAOS)<br/>    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | HS (Hesiod)<br/>   |



 

</dd> <dt>

*TTL* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*ISDNNumber* \[ no\]
</dt> <dd>

Número ISDN e DDI do proprietário do registro.

</dd> <dt>

*Subendereço* \[ no\]
</dt> <dd>

Subendereço do proprietário, se definido.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referência ao novo objeto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

[**\_Isdntype MicrosoftDNS**](microsoftdns-isdntype.md)
</dt> <dt>

[**Método Modify da \_ classe isdntype MicrosoftDNS**](microsoftdns-isdntype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





