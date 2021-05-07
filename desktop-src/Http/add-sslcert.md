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
ms.openlocfilehash: 309050be35748f39eefc8b40b8e590f8f6889fde
ms.sourcegitcommit: 07ba02719c9779e082b108ae74f9699fb0236c34
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/06/2021
ms.locfileid: "108644188"
---
# <a name="add-sslcert"></a><span data-ttu-id="17f98-104">add sslcert</span><span class="sxs-lookup"><span data-stu-id="17f98-104">add sslcert</span></span>

<span data-ttu-id="17f98-105">Adiciona uma nova associação de certificado de servidor protocolo SSL (SSL) e as políticas de certificado de cliente correspondentes para um endereço IP e uma porta.</span><span class="sxs-lookup"><span data-stu-id="17f98-105">Adds a new Secure Sockets Layer (SSL) server certificate binding and the corresponding client certificate policies for an IP address and port.</span></span>

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

## <a name="parameters"></a><span data-ttu-id="17f98-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17f98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17f98-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport = endereço IP: porta\]**</span><span class="sxs-lookup"><span data-stu-id="17f98-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport=IP Address:port\]**</span></span>
</dt> <dd>

<span data-ttu-id="17f98-108">Especifica o endereço IP e a porta para a associação.</span><span class="sxs-lookup"><span data-stu-id="17f98-108">Specifies the IP address and port for the binding.</span></span>

</dd> <dt>

<span data-ttu-id="17f98-109"><span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>**\[certhash = cadeia de caracteres\]**</span><span class="sxs-lookup"><span data-stu-id="17f98-109"><span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>**\[certhash=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="17f98-110">Especifica o hash de SHA do certificado.</span><span class="sxs-lookup"><span data-stu-id="17f98-110">Specifies the SHA hash of the certificate.</span></span> <span data-ttu-id="17f98-111">Esse hash tem 20 bytes de comprimento e é especificado como uma cadeia de caracteres hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="17f98-111">This hash is 20 bytes long and specified as a hexadecimal string.</span></span>

</dd> <dt>

<span data-ttu-id="17f98-112"><span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>**\[AppID = GUID\]**</span><span class="sxs-lookup"><span data-stu-id="17f98-112"><span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>**\[appid=GUID\]**</span></span>
</dt> <dd>

<span data-ttu-id="17f98-113">Especifica o GUID para identificar o aplicativo proprietário.</span><span class="sxs-lookup"><span data-stu-id="17f98-113">Specifies the GUID to identify the owning application.</span></span>

</dd> <dt>

<span data-ttu-id="17f98-114"><span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>**\[certstorename = cadeia de caracteres\]**</span><span class="sxs-lookup"><span data-stu-id="17f98-114"><span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>**\[certstorename=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="17f98-115">Especifica o nome do repositório para o certificado.</span><span class="sxs-lookup"><span data-stu-id="17f98-115">Specifies the store name for the certificate.</span></span> <span data-ttu-id="17f98-116">O padrão é MY.</span><span class="sxs-lookup"><span data-stu-id="17f98-116">Defaults to MY.</span></span> <span data-ttu-id="17f98-117">O certificado deve ser armazenado no contexto do computador local.</span><span class="sxs-lookup"><span data-stu-id="17f98-117">Certificate must be stored in the local computer context.</span></span>

</dd> <dt>

<span data-ttu-id="17f98-118"><span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation = {habilitar \| desabilitar}\]**</span><span class="sxs-lookup"><span data-stu-id="17f98-118"><span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="17f98-119">Ativa ou turnsoff a verificação de revogação de certificados de cliente.</span><span class="sxs-lookup"><span data-stu-id="17f98-119">Turns on or turnsoff verification of revocation of client certificates.</span></span>

</dd> <dt>

<span data-ttu-id="17f98-120"><span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly = {habilitar \| desabilitar}\]**</span><span class="sxs-lookup"><span data-stu-id="17f98-120"><span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="17f98-121">Ativa ou desativa o uso apenas do certificado de cliente em cache para verificação de revogação.</span><span class="sxs-lookup"><span data-stu-id="17f98-121">Turns on or turns off usage of only cached client certificate for revocation checking.</span></span>

</dd> <dt>

<span data-ttu-id="17f98-122"><span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck = {habilitar \| desabilitar}\]**</span><span class="sxs-lookup"><span data-stu-id="17f98-122"><span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="17f98-123">Ativa ou desativa a verificação de uso.</span><span class="sxs-lookup"><span data-stu-id="17f98-123">Turns on or turns off usage check.</span></span> <span data-ttu-id="17f98-124">O padrão é habilitada.</span><span class="sxs-lookup"><span data-stu-id="17f98-124">Default is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="17f98-125"><span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>**\[RevocationFreshnessTime = u-int\]**</span><span class="sxs-lookup"><span data-stu-id="17f98-125"><span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>**\[revocationfreshnesstime=u-int\]**</span></span>
</dt> <dd>

<span data-ttu-id="17f98-126">Especifica o intervalo de tempo para verificar se há uma CRL (lista de certificados revogados) atualizada.</span><span class="sxs-lookup"><span data-stu-id="17f98-126">Specifies the time interval to check for an updated certificate revocation list (CRL).</span></span> <span data-ttu-id="17f98-127">Se esse valor for 0, a nova CRL será atualizada somente se a anterior expirar (em segundos).</span><span class="sxs-lookup"><span data-stu-id="17f98-127">If this value is 0, then the new CRL is updated only if the previous one expires (in seconds).</span></span>

</dd> <dt>

<span data-ttu-id="17f98-128"><span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>**\[UrlRetrievalTimeout = u-int\]**</span><span class="sxs-lookup"><span data-stu-id="17f98-128"><span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>**\[urlretrievaltimeout=u-int\]**</span></span>
</dt> <dd>

<span data-ttu-id="17f98-129">Especifica o intervalo de tempo limite em tentativas de recuperar a lista de certificados revogados para a URL remota (em milissegundos).</span><span class="sxs-lookup"><span data-stu-id="17f98-129">Specifies the timeout interval on attempts to retrieve the certificate revocation list for the remote URL (in milliseconds).</span></span>

</dd> <dt>

<span data-ttu-id="17f98-130"><span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>**\[SslCtlIdentifier = cadeia de caracteres\]**</span><span class="sxs-lookup"><span data-stu-id="17f98-130"><span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>**\[sslctlidentifier=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="17f98-131">Lista os emissores de certificado que podem ser confiáveis.</span><span class="sxs-lookup"><span data-stu-id="17f98-131">Lists the certificate issuers that can be trusted.</span></span> <span data-ttu-id="17f98-132">Essa lista pode ser um subconjunto dos emissores de certificado que são confiáveis para o computador.</span><span class="sxs-lookup"><span data-stu-id="17f98-132">This list can be a subset of the certificate issuers that are trusted by the computer.</span></span>

</dd> <dt>

<span data-ttu-id="17f98-133"><span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>**\[sslctlstorename = cadeia de caracteres\]**</span><span class="sxs-lookup"><span data-stu-id="17f98-133"><span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>**\[sslctlstorename=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="17f98-134">Especifica o nome do repositório no \_ computador local em que SslCtlIdentifier está armazenado.</span><span class="sxs-lookup"><span data-stu-id="17f98-134">Specifies the store name under LOCAL\_MACHINE where SslCtlIdentifier is stored.</span></span>

</dd> <dt>

<span data-ttu-id="17f98-135"><span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage = {habilitar \| desabilitar}\]**</span><span class="sxs-lookup"><span data-stu-id="17f98-135"><span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="17f98-136">Ativa ou desativa os Mapeadores do DS.</span><span class="sxs-lookup"><span data-stu-id="17f98-136">Turns on or turns off DS mappers.</span></span> <span data-ttu-id="17f98-137">O padrão é desabilitado.</span><span class="sxs-lookup"><span data-stu-id="17f98-137">Default is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="17f98-138"><span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertnegotiation = {habilitar \| desabilitar}\]**</span><span class="sxs-lookup"><span data-stu-id="17f98-138"><span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertnegotiation={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="17f98-139">Ativa ou desativa a negociação do certificado.</span><span class="sxs-lookup"><span data-stu-id="17f98-139">Turns on or turns off negotiation of certificate.</span></span> <span data-ttu-id="17f98-140">O padrão é desabilitado.</span><span class="sxs-lookup"><span data-stu-id="17f98-140">Default is disabled.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="17f98-141">Exemplos</span><span class="sxs-lookup"><span data-stu-id="17f98-141">Examples</span></span>

<span data-ttu-id="17f98-142">**Adicionar SSLCERT IPPORT = 1.1.1.1:443**</span><span class="sxs-lookup"><span data-stu-id="17f98-142">**add sslcert ipport=1.1.1.1:443**</span></span>

<span data-ttu-id="17f98-143">**certhash = 0102030405060708090A0B0C0D0E0F1011121314**</span><span class="sxs-lookup"><span data-stu-id="17f98-143">**certhash=0102030405060708090A0B0C0D0E0F1011121314**</span></span>

<span data-ttu-id="17f98-144">**AppID = {00112233-4455-6677-8899-AABBCCDDEEFF}**</span><span class="sxs-lookup"><span data-stu-id="17f98-144">**appid={00112233-4455-6677-8899-AABBCCDDEEFF}**</span></span>

 

 




