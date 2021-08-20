---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_AAAAType dados
description: O método CreateInstanceFromPropertyData cria uma instanância de um registro de recurso de endereço IPv6 (AAAA).
ms.assetid: 3f2774d8-1eb6-4300-95e2-f918fc6612e0
keywords:
- Método CREATEInstanceFromPropertyData DNS
- Classe MicrosoftDNS_AAAAType DNS do método CreateInstanceFromPropertyData
- MicrosoftDNS_AAAAType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0df2c76b9289cb710de4e82e3cbc3dfc0b482ea63448b90a02fa37b7965fd931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163764"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_aaaatype-class"></a>Método CreateInstanceFromPropertyData da classe \_ MicrosoftDNS AAAAType

O **método CreateInstanceFromPropertyData** cria uma instanância de um registro de recurso de endereço IPv6 (AAAA).

## <a name="syntax"></a>Sintaxe


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           string                IPv6Address,
  [out, ref]     MicrosoftDNS_AAAAType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DnsServerName* \[ Em\]
</dt> <dd>

FQDN ou endereço IP do Servidor DNS que contém esse RR.

</dd> <dt>

*ContainerName* \[ Em\]
</dt> <dd>

Nome do Contêiner para a instância zone, cache ou RootHints que contém esse RR.

</dd> <dt>

*OwnerName* \[ Em\]
</dt> <dd>

Nome do proprietário para a RR.

</dd> <dt>

*RecordClass* \[ in, opcional\]
</dt> <dd>

Classe do RR. O valor padrão é 1. Os valores a seguir são válidos.



| Valor                                                                                                | Significado                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | IN (Internet)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | CS (CSNET)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | CH (CHAOS)<br/>    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | HS (Hesiod)<br/>   |



 

</dd> <dt>

*TTL* \[ in, opcional\]
</dt> <dd>

Tempo, em segundos, em que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*IPv6Address* \[ Em\]
</dt> <dd>

Endereço IPv6 para o host.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referência ao novo objeto .

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

[**MicrosoftDNS \_ AAAAType**](microsoftdns-aaaatype.md)
</dt> <dt>

[**Método Modify da classe \_ MicrosoftDNS AAAAType**](microsoftdns-aaaatype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





