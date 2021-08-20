---
title: add sslcert
description: Adiciona uma nova associação de certificado de servidor protocolo SSL (SSL) e as políticas de certificado de cliente correspondentes para um endereço IP e uma porta.
ms.assetid: 4ba3d2cb-050f-46e3-81f9-5f7e360b19fb
keywords:
- Adicionar HTTP sslcert
topic_type:
- apiref
api_name:
- add sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721931bfa05a96ca47fd69f643a02076201bb5f93eff003afa83714f2d14b519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950945"
---
# <a name="add-sslcert"></a>add sslcert

Adiciona uma nova associação de certificado de servidor protocolo SSL (SSL) e as políticas de certificado de cliente correspondentes para um endereço IP e uma porta.

``` syntax
add sslcert [ipport=]IP Address:port
            [certhash=]string
            [appid=]GUID
            [certstorename=]string
            [verifyclientcertrevocation={enable|disable}]
            [verifyrevocationwithcachedclientcertonly={enable|disable}]
            [usagecheck={enable|disable}]
            [revocationfreshnesstime=]u-int
            [urlretrievaltimeout=]u-int
            [sslctlidentifier=]string
            [sslctlstorename=]string
            [dsmapperusage={enable|disable}]
            [clientcertnegotiation={enable|disable}]

 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport = endereço IP: porta\]**
</dt> <dd>

Especifica o endereço IP e a porta para a associação.

</dd> <dt>

<span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>**\[certhash = cadeia de caracteres\]**
</dt> <dd>

Especifica o hash de SHA do certificado. Esse hash tem 20 bytes de comprimento e é especificado como uma cadeia de caracteres hexadecimal.

</dd> <dt>

<span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>**\[AppID = GUID\]**
</dt> <dd>

Especifica o GUID para identificar o aplicativo proprietário.

</dd> <dt>

<span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>**\[certstorename = cadeia de caracteres\]**
</dt> <dd>

Especifica o nome do repositório para o certificado. O padrão é MY. O certificado deve ser armazenado no contexto do computador local.

</dd> <dt>

<span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation = {habilitar \| desabilitar}\]**
</dt> <dd>

Ativa ou turnsoff a verificação de revogação de certificados de cliente.

</dd> <dt>

<span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly = {habilitar \| desabilitar}\]**
</dt> <dd>

Ativa ou desativa o uso apenas do certificado de cliente em cache para verificação de revogação.

</dd> <dt>

<span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck = {habilitar \| desabilitar}\]**
</dt> <dd>

Ativa ou desativa a verificação de uso. O padrão é habilitada.

</dd> <dt>

<span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>**\[RevocationFreshnessTime = u-int\]**
</dt> <dd>

Especifica o intervalo de tempo para verificar se há uma CRL (lista de certificados revogados) atualizada. Se esse valor for 0, a nova CRL será atualizada somente se a anterior expirar (em segundos).

</dd> <dt>

<span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>**\[UrlRetrievalTimeout = u-int\]**
</dt> <dd>

Especifica o intervalo de tempo limite em tentativas de recuperar a lista de certificados revogados para a URL remota (em milissegundos).

</dd> <dt>

<span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>**\[SslCtlIdentifier = cadeia de caracteres\]**
</dt> <dd>

Lista os emissores de certificado que podem ser confiáveis. Essa lista pode ser um subconjunto dos emissores de certificado que são confiáveis para o computador.

</dd> <dt>

<span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>**\[sslctlstorename = cadeia de caracteres\]**
</dt> <dd>

Especifica o nome do repositório no \_ computador local em que SslCtlIdentifier está armazenado.

</dd> <dt>

<span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage = {habilitar \| desabilitar}\]**
</dt> <dd>

Ativa ou desativa os Mapeadores do DS. O padrão é desabilitado.

</dd> <dt>

<span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertnegotiation = {habilitar \| desabilitar}\]**
</dt> <dd>

Ativa ou desativa a negociação do certificado. O padrão é desabilitado.

</dd> </dl>

## <a name="examples"></a>Exemplos

**Adicionar SSLCERT IPPORT = 1.1.1.1:443**

**certhash = 0102030405060708090A0B0C0D0E0F1011121314**

**AppID = {00112233-4455-6677-8899-AABBCCDDEEFF}**

 

 




