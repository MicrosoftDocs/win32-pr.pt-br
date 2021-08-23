---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_MINFOType dados
description: O método CreateInstanceFromPropertyData cria uma instanância de um registro de recurso MINFO (Informações de Email).
ms.assetid: 693b4b19-cbdd-48d5-89e0-a700a60477aa
keywords:
- Método CREATEInstanceFromPropertyData DNS
- Classe DNS MicrosoftDNS_MINFOType método CreateInstanceFromPropertyData
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
ms.openlocfilehash: ce72838382dd5276a4a0b9b660b67f1d7f8cb04cb894c72f245e908a916ae8f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573926"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_minfotype-class"></a>Método CreateInstanceFromPropertyData da classe MINFOType do MicrosoftDNS \_

O **método CreateInstanceFromPropertyData** cria uma instanância de um registro de recurso MINFO (Informações de Email).

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

*DnsServerName* \[ Em\]
</dt> <dd>

FQDN ou endereço IP do Servidor DNS que contém esse RR.

</dd> <dt>

*ContainerName* \[ Em\]
</dt> <dd>

Nome do Contêiner para a instância Zone, Cache ou RootHints que contém esse RR.

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

*ResponsibleMailbox* \[ Em\]
</dt> <dd>

FQDN especificando uma caixa de correio responsável pela lista de correspondência ou caixa de correio especificada no Nome do Proprietário do registro.

</dd> <dt>

*ErrorMailbox* \[ Em\]
</dt> <dd>

FQDN especificando uma caixa de correio para receber mensagens de erro relacionadas à lista de correspondência ou à caixa de correio especificada pelo nome do proprietário do registro MINFO.

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

[**MicrosoftDNS \_ MINFOType**](microsoftdns-minfotype.md)
</dt> <dt>

[**Método Modify da classe MINFOType do MicrosoftDNS \_**](microsoftdns-minfotype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





