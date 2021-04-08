---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_MINFOType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de informações de email (MINFO).
ms.assetid: 693b4b19-cbdd-48d5-89e0-a700a60477aa
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_MINFOType
- MicrosoftDNS_MINFOType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a565b1575dc51a59a09faea6fd271d719518f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008896"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_minfotype-class"></a>Método CreateInstanceFromPropertyData da \_ classe MINFOType MicrosoftDNS

O método **CreateInstanceFromPropertyData** instancia um registro de recurso de informações de email (MINFO).

## <a name="syntax"></a>Sintaxe


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           string                 ResponsibleMailbox,
  [in]           string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
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
| <span id="4"></span><dl> <dt>**quatro**</dt> </dl> | HS (Hesiod)<br/>   |



 

</dd> <dt>

*TTL* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*ResponsibleMailbox* \[ no\]
</dt> <dd>

FQDN que especifica uma caixa de correio responsável pela lista de endereçamento ou caixa de correio especificada no nome do proprietário do registro.

</dd> <dt>

*ErrorMailbox* \[ no\]
</dt> <dd>

FQDN que especifica uma caixa de correio para receber mensagens de erro relacionadas à lista de endereçamento ou à caixa de correio especificada pelo nome do proprietário do registro MINFO.

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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MicrosoftDNS \_ MINFOType**](microsoftdns-minfotype.md)
</dt> <dt>

[**Método Modify da classe MicrosoftDNS \_ MINFOType**](microsoftdns-minfotype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





