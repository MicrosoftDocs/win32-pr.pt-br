---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_SRVType dados
description: O método CreateInstanceFromPropertyData cria uma instanância de um Registro de Recurso de Serviço (SRV).
ms.assetid: ef55faa8-1109-4c96-98ac-2b01b940fa5c
keywords:
- Método CREATEInstanceFromPropertyData DNS
- Classe DNS MicrosoftDNS_SRVType método CreateInstanceFromPropertyData
- MicrosoftDNS_SRVType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92519a3dcd383fca9297323c5217cfdefa997752ede62435b8002af5e151114f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669084"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_srvtype-class"></a>Método CreateInstanceFromPropertyData da classe SRVType do MicrosoftDNS \_

O **método CreateInstanceFromPropertyData** cria uma instanância de um Registro de Recurso de Serviço (SRV).

## <a name="syntax"></a>Sintaxe


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               Priority,
  [in]           uint16               Weight,
  [in]           uint16               Port,
  [in]           string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
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

Nome do contêiner para a instância Zone, Cache ou RootHints que contém esse RR.

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

*Prioridade* \[ Em\]
</dt> <dd>

Prioridade do host de destino especificado no nome do proprietário. Números menores implicam prioridades mais altas.

</dd> <dt>

*Peso* \[ Em\]
</dt> <dd>

Peso do host de destino. Isso é útil ao selecionar entre hosts que têm a mesma prioridade. As chances de usar esse host devem ser proporcionais ao seu peso.

</dd> <dt>

*Porta* \[ Em\]
</dt> <dd>

Porta usada no host de destino de um serviço de protocolo.

</dd> <dt>

*SRVDomainName* \[ Em\]
</dt> <dd>

FQDN do host de destino. Um destino de \\ . significa que o serviço não está disponível nesse \\ domínio.

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

[**MicrosoftDNS \_ SRVType**](microsoftdns-srvtype.md)
</dt> <dt>

[**Método Modify da classe SRVType do MicrosoftDNS \_**](microsoftdns-srvtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





