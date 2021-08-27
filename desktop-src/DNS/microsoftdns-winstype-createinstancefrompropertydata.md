---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_WINSType
description: o método CreateInstanceFromPropertyData instancia um registro de recurso Windows WINS (serviço de cadastramento na Internet).
ms.assetid: 0b41a6a5-0bb1-467b-9089-2c721d521887
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_WINSType
- MicrosoftDNS_WINSType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92f39b360c29ca859c0d0fd0188f0b065dec58293207c27e0a0267572472aabe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077046"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_winstype-class"></a>Método CreateInstanceFromPropertyData da \_ classe winstype MicrosoftDNS

o método **CreateInstanceFromPropertyData** instancia um registro de recurso Windows WINS (serviço de cadastramento na Internet).

## <a name="syntax"></a>Sintaxe


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint32                MappingFlag,
  [in]           uint32                LookupTimeout,
  [in]           uint32                CacheTimeout,
  [in]           string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
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

*MappingFlag* \[ no\]
</dt> <dd>

Sinalizador de mapeamento WINS que especifica se o registro deve ser incluído na replicação de zona. Ele pode ter apenas dois valores: 0x80000000 e 0x00010000 correspondentes aos sinalizadores de replicação e sem replicação (registro local), respectivamente. Os valores a seguir são válidos.



| Valor                                                                                                                                               | Significado                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <dt>**0x80000000**</dt> </dl> | Sinalizador de replicação<br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <dt>**0x00010000**</dt> </dl> | Sinalizador sem replicação (registro local)<br/> |



 

</dd> <dt>

*LookupTimeout* \[ no\]
</dt> <dd>

Tempo, em segundos, que um servidor DNS tenta resolução usando a pesquisa WINS.

</dd> <dt>

*CacheTimeout* \[ no\]
</dt> <dd>

Tempo, em segundos, que um servidor DNS que usa a pesquisa WINS pode armazenar em cache a resposta do servidor WINS.

</dd> <dt>

*WinsServers* \[ no\]
</dt> <dd>

Lista de endereços IP separados por vírgulas de servidores WINS usados na pesquisa WINS.

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

[**MicrosoftDNS \_ winstype**](microsoftdns-winstype.md)
</dt> <dt>

[**Método Modify da \_ classe winstype MicrosoftDNS**](microsoftdns-winstype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





