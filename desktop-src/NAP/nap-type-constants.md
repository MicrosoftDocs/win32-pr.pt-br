---
title: Constantes de tipo NAP (NapTypes. h)
description: As constantes de NAP a seguir são definidas.
ms.assetid: 2727487c-8c6a-4cd9-b6d8-253191a7d7f6
topic_type:
- apiref
api_name:
- maxSoHAttributeCount
- maxSoHAttributeSize
- minNetworkSoHSize
- maxNetworkSoHSize
- maxDwordCountPerSoHAttribute
- maxIpv4CountPerSoHAttribute
- maxIpv6CountPerSoHAttribute
- maxStringLength
- maxStringLengthInBytes
- maxSystemHealthEntityCount
- SystemHealthEntityCount
- maxEnforcerCount
- EnforcementEntityCount
- maxPrivateDataSize
- maxConnectionCountPerEnforcer
- maxCachedSoHCount
- freshSoHRequest
- shaFixup
- failureCategoryCount
- ComponentTypeEnforcementClientSoH
- ComponentTypeEnforcementClientRp
- defaultProtocolMaxSize
- maxProtocolMaxSize
- minProtocolMaxSize
- ProtocolMaxSize
api_location:
- NapTypes.h
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85692a7ccc9cbb602a34da714a5eeb488ea5c4a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766249"
---
# <a name="nap-type-constants"></a>Constantes de tipo NAP

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

As constantes de NAP a seguir são definidas.

As constantes de NAP a seguir são definidas em NapTypes. h:

<dl> <dt>

<span id="maxSoHAttributeCount"></span><span id="maxsohattributecount"></span><span id="MAXSOHATTRIBUTECOUNT"></span>**maxSoHAttributeCount**
</dt> <dd> <dl> <dt>

0x64
</dt> <dt>



O número máximo de objetos TLV (tipo-tamanho-valor) [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) associados a um pacote [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) .


</dt> </dl> </dd> <dt>

<span id="maxSoHAttributeSize"></span><span id="maxsohattributesize"></span><span id="MAXSOHATTRIBUTESIZE"></span>**maxSoHAttributeSize**
</dt> <dd> <dl> <dt>

0xFA0
</dt> <dt>



O tamanho máximo, em bytes, de um objeto [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) associado a um pacote de [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh)(declaração de integridade).


</dt> </dl> </dd> <dt>

<span id="minNetworkSoHSize"></span><span id="minnetworksohsize"></span><span id="MINNETWORKSOHSIZE"></span>**minNetworkSoHSize**
</dt> <dd> <dl> <dt>

0xC
</dt> <dt>



O tamanho mínimo, em bytes, de um pacote [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) .


</dt> </dl> </dd> <dt>

<span id="maxNetworkSoHSize"></span><span id="maxnetworksohsize"></span><span id="MAXNETWORKSOHSIZE"></span>**maxNetworkSoHSize**
</dt> <dd> <dl> <dt>

0xFA0
</dt> <dt>



O tamanho máximo, em bytes, de um pacote [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) .


</dt> </dl> </dd> <dt>

<span id="maxDwordCountPerSoHAttribute"></span><span id="maxdwordcountpersohattribute"></span><span id="MAXDWORDCOUNTPERSOHATTRIBUTE"></span>**maxDwordCountPerSoHAttribute**
</dt> <dd> <dl> <dt>

maxSoHAttributeSize/sizeof (DWORD)
</dt> <dt>



O número máximo de valores DWORD associados a um [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).


</dt> </dl> </dd> <dt>

<span id="maxIpv4CountPerSoHAttribute"></span><span id="maxipv4countpersohattribute"></span><span id="MAXIPV4COUNTPERSOHATTRIBUTE"></span>**maxIpv4CountPerSoHAttribute**
</dt> <dd> <dl> <dt>

maxSoHAttributeSize/0x4
</dt> <dt>



O número máximo de endereços IPv4 associados a um [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).


</dt> </dl> </dd> <dt>

<span id="maxIpv6CountPerSoHAttribute"></span><span id="maxipv6countpersohattribute"></span><span id="MAXIPV6COUNTPERSOHATTRIBUTE"></span>**maxIpv6CountPerSoHAttribute**
</dt> <dd> <dl> <dt>

maxSoHAttributeSize/0x10
</dt> <dt>



O número máximo de endereços IPv6 associados a um [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).


</dt> </dl> </dd> <dt>

<span id="maxStringLength"></span><span id="maxstringlength"></span><span id="MAXSTRINGLENGTH"></span>**maxStringLength**
</dt> <dd> <dl> <dt>

0x400
</dt> <dt>



O comprimento máximo de uma cadeia de caracteres especificada pela estrutura de [**contado**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .


</dt> </dl> </dd> <dt>

<span id="maxStringLengthInBytes"></span><span id="maxstringlengthinbytes"></span><span id="MAXSTRINGLENGTHINBYTES"></span>**maxStringLengthInBytes**
</dt> <dd> <dl> <dt>

(maxStringLength + 1) \* sizeof (WCHAR)
</dt> <dt>



O comprimento máximo, em bytes, de uma cadeia de caracteres especificada pela estrutura de [**contado**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .


</dt> </dl> </dd> <dt>

<span id="maxSystemHealthEntityCount"></span><span id="maxsystemhealthentitycount"></span><span id="MAXSYSTEMHEALTHENTITYCOUNT"></span>**maxSystemHealthEntityCount**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



O número máximo de entidades de integridade do sistema, como SHVs e SHAs.


</dt> </dl> </dd> <dt>

<span id="SystemHealthEntityCount"></span><span id="systemhealthentitycount"></span><span id="SYSTEMHEALTHENTITYCOUNT"></span>**SystemHealthEntityCount**
</dt> <dd> <dl> <dt>

\[intervalo (0, maxSystemHealthEntityCount)\] 
</dt> <dt>



O intervalo de valores possíveis para o número de entidades de integridade do sistema.


</dt> </dl> </dd> <dt>

<span id="maxEnforcerCount"></span><span id="maxenforcercount"></span><span id="MAXENFORCERCOUNT"></span>**maxEnforcerCount**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



O número máximo de entidades de imposição, como QECs.


</dt> </dl> </dd> <dt>

<span id="EnforcementEntityCount"></span><span id="enforcemententitycount"></span><span id="ENFORCEMENTENTITYCOUNT"></span>**EnforcementEntityCount**
</dt> <dd> <dl> <dt>

\[intervalo (0, maxEnforcerCount)\]
</dt> <dt>



O intervalo de valores possíveis para o número de entidades de imposição.


</dt> </dl> </dd> <dt>

<span id="maxPrivateDataSize"></span><span id="maxprivatedatasize"></span><span id="MAXPRIVATEDATASIZE"></span>**maxPrivateDataSize**
</dt> <dd> <dl> <dt>

0xC8
</dt> <dt>



O tamanho máximo, em bytes, de uma estrutura [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) .


</dt> </dl> </dd> <dt>

<span id="maxConnectionCountPerEnforcer"></span><span id="maxconnectioncountperenforcer"></span><span id="MAXCONNECTIONCOUNTPERENFORCER"></span>**maxConnectionCountPerEnforcer**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



O número máximo de objetos [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) associados a uma entidade de imposição.


</dt> </dl> </dd> <dt>

<span id="maxCachedSoHCount"></span><span id="maxcachedsohcount"></span><span id="MAXCACHEDSOHCOUNT"></span>**maxCachedSoHCount**
</dt> <dd> <dl> <dt>

maxSystemHealthEntityCount \* maxEnforcerCount \* maxConnectionCountPerEnforcer
</dt> <dt>



O número máximo de conexões SoH em cache para todas as entidades de integridade do sistema e imposição.


</dt> </dl> </dd> <dt>

<span id="freshSoHRequest"></span><span id="freshsohrequest"></span><span id="FRESHSOHREQUEST"></span>**freshSoHRequest**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Especifica que um [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh)é devido a uma nova solicitação, não a uma solicitação armazenada em cache. Esse sinalizador é usado pelo agente NAP em um objeto [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) .


</dt> </dl> </dd> <dt>

<span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span>**shaFixup**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Especifica que a correção é necessária. Esse sinalizador é usado por um SHA.


</dt> </dl> </dd> <dt>

<span id="failureCategoryCount"></span><span id="failurecategorycount"></span><span id="FAILURECATEGORYCOUNT"></span>**failureCategoryCount**
</dt> <dd> <dl> <dt>

0x5
</dt> <dt>



O número de categorias de falha contidas em uma estrutura [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) .


</dt> </dl> </dd> <dt>

<span id="ComponentTypeEnforcementClientSoH"></span><span id="componenttypeenforcementclientsoh"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTSOH"></span>**ComponentTypeEnforcementClientSoH**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



O componente é um cliente de imposição de quarentena (QEC) que envia um pacote [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) em banda durante a autenticação de conexão.

> [!Note]  
> Esse valor não é usado por SHAs e SHVs.

 


</dt> </dl> </dd> <dt>

<span id="ComponentTypeEnforcementClientRp"></span><span id="componenttypeenforcementclientrp"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTRP"></span>**ComponentTypeEnforcementClientRp**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



O componente é um QEC que implementa o [**INapCertRelyingParty**](inapcertrelyingparty.md) e deve interagir com o HCS (servidor de certificado de integridade) para obter um certificado de integridade.

> [!Note]  
> Esse valor não é usado por SHAs e SHVs.

 


</dt> </dl> </dd> </dl>

As constantes de NAP a seguir são definidas em NapEnforcementClient. h.

<dl> <dt>

<span id="defaultProtocolMaxSize"></span><span id="defaultprotocolmaxsize"></span><span id="DEFAULTPROTOCOLMAXSIZE"></span>**defaultProtocolMaxSize**
</dt> <dd> <dl> <dt>

0x0FA0
</dt> <dt>



O tamanho máximo padrão, em bytes, de um pacote SoH.


</dt> </dl> </dd> <dt>

<span id="maxProtocolMaxSize"></span><span id="maxprotocolmaxsize"></span><span id="MAXPROTOCOLMAXSIZE"></span>**maxProtocolMaxSize**
</dt> <dd> <dl> <dt>

0xFFFF
</dt> <dt>



O tamanho máximo possível, em bytes, de um pacote SoH.


</dt> </dl> </dd> <dt>

<span id="minProtocolMaxSize"></span><span id="minprotocolmaxsize"></span><span id="MINPROTOCOLMAXSIZE"></span>**minProtocolMaxSize**
</dt> <dd> <dl> <dt>

0x012C
</dt> <dt>



O menor tamanho máximo possível, em bytes, de um pacote SoH. O tamanho real do pacote SoH pode ser menor que **minProtocolMaxSize**.


</dt> </dl> </dd> <dt>

<span id="ProtocolMaxSize"></span><span id="protocolmaxsize"></span><span id="PROTOCOLMAXSIZE"></span>**ProtocolMaxSize**
</dt> <dd> <dl> <dt>

intervalo (minProtocolMaxSize, maxProtocolMaxSize)
</dt> <dt>



O intervalo de valores possíveis para o tamanho máximo de um pacote SoH.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                                                                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                                                                                |
| parâmetro<br/>                   | <dl> <dt>NapTypes. h; </dt> <dt>NapEnforcementClient. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Constantes de NAP**](nap-constants.md)
</dt> </dl>

 

 





