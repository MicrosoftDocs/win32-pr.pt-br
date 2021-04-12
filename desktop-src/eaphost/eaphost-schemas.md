---
title: EAPHost e esquema herdado
description: Descreve o esquema EAPHost e o esquema herdado para criar o XML de configuração e a credencial XML.
ms.assetid: d4572866-7e2b-4e7c-afe1-66394b549bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dbe40f447618a9ca0da89875521349101c1191f
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104365333"
---
# <a name="eaphost-and-legacy-schema"></a><span data-ttu-id="f094f-103">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="f094f-103">EAPHost and Legacy Schema</span></span>

<span data-ttu-id="f094f-104">Este tópico descreve o esquema EAPHost e o esquema herdado para criar o XML de configuração e a credencial XML.</span><span class="sxs-lookup"><span data-stu-id="f094f-104">This topic describes the EAPHost schema and legacy schema for creating configuration XML and credential XML.</span></span>

## <a name="about-eaphost-and-legacy-schema"></a><span data-ttu-id="f094f-105">Sobre o EAPHost e o esquema herdado</span><span class="sxs-lookup"><span data-stu-id="f094f-105">About EAPHost and Legacy Schema</span></span>

<span data-ttu-id="f094f-106">A criação do XML de configuração começa com o esquema [eaphostconfig](eaphostconfigschema-schema.md) ; a criação de credencial XML começa com o esquema [eaphostusercredentials](eaphostusercredentialsschema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="f094f-106">Creating configuration XML commences with the [eaphostconfig](eaphostconfigschema-schema.md) schema; creating credential XML commences with the [eaphostusercredentials](eaphostusercredentialsschema-schema.md) schema.</span></span>

<span data-ttu-id="f094f-107">Vários dos esquemas nativos e herdados contêm elementos de esquema comuns.</span><span class="sxs-lookup"><span data-stu-id="f094f-107">Several of the native and legacy schema contain common schema elements.</span></span> <span data-ttu-id="f094f-108">Os elementos comuns usados na configuração do método e as credenciais do método são dissociados em um único arquivo de esquema, conhecido como "esquema comum".</span><span class="sxs-lookup"><span data-stu-id="f094f-108">Common elements used in method configuration and method credentials are abstracted into a single schema file, referred to as the "common schema".</span></span>

<span data-ttu-id="f094f-109">Os termos "configuração do método" e "Propriedades da conexão" são usados de maneira intercambiável.</span><span class="sxs-lookup"><span data-stu-id="f094f-109">The terms "method configuration" and "connection properties" are used interchangeably.</span></span> <span data-ttu-id="f094f-110">Da mesma forma, os termos "credenciais do método" e "Propriedades do usuário" também são usados de maneira intercambiável.</span><span class="sxs-lookup"><span data-stu-id="f094f-110">Likewise, the terms "method credentials" and "user properties" are also used interchangeably.</span></span>

## <a name="eaphost-schema"></a><span data-ttu-id="f094f-111">Esquema EAPHost</span><span class="sxs-lookup"><span data-stu-id="f094f-111">EAPHost Schema</span></span>



| <span data-ttu-id="f094f-112">Esquema</span><span class="sxs-lookup"><span data-stu-id="f094f-112">Schema</span></span>                                                                        | <span data-ttu-id="f094f-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="f094f-113">Description</span></span>                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="f094f-114">baseeapmethodconfig</span><span class="sxs-lookup"><span data-stu-id="f094f-114">baseeapmethodconfig</span></span>](baseeapmethodconfigschema-schema.md)                   | <span data-ttu-id="f094f-115">Contém elementos de esquema de configuração comuns.</span><span class="sxs-lookup"><span data-stu-id="f094f-115">Contains common configuration schema elements.</span></span>     |
| [<span data-ttu-id="f094f-116">baseeapmethodusercredentials</span><span class="sxs-lookup"><span data-stu-id="f094f-116">baseeapmethodusercredentials</span></span>](baseeapmethodusercredentialsschema-schema.md) | <span data-ttu-id="f094f-117">Contém elementos de esquema de credencial comuns.</span><span class="sxs-lookup"><span data-stu-id="f094f-117">Contains common credential schema elements.</span></span>        |
| [<span data-ttu-id="f094f-118">eapcommon</span><span class="sxs-lookup"><span data-stu-id="f094f-118">eapcommon</span></span>](eapcommonschema-schema.md)                                       | <span data-ttu-id="f094f-119">Contém a definição do elemento **EapMethodType** .</span><span class="sxs-lookup"><span data-stu-id="f094f-119">Contains the **EapMethodType** element definition.</span></span> |
| [<span data-ttu-id="f094f-120">eaphostconfig</span><span class="sxs-lookup"><span data-stu-id="f094f-120">eaphostconfig</span></span>](eaphostconfigschema-schema.md)                               | <span data-ttu-id="f094f-121">Contém o esquema de configuração do EAPHost.</span><span class="sxs-lookup"><span data-stu-id="f094f-121">Contains EAPHost configuration schema.</span></span>             |
| [<span data-ttu-id="f094f-122">eaphostusercredentials</span><span class="sxs-lookup"><span data-stu-id="f094f-122">eaphostusercredentials</span></span>](eaphostusercredentialsschema-schema.md)             | <span data-ttu-id="f094f-123">Contém o esquema de credencial EAPHost.</span><span class="sxs-lookup"><span data-stu-id="f094f-123">Contains EAPHost credential schema.</span></span>                |



 

## <a name="legacy-schema"></a><span data-ttu-id="f094f-124">Esquema herdado</span><span class="sxs-lookup"><span data-stu-id="f094f-124">Legacy Schema</span></span>



| <span data-ttu-id="f094f-125">Esquema</span><span class="sxs-lookup"><span data-stu-id="f094f-125">Schema</span></span>                                                                            | <span data-ttu-id="f094f-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="f094f-126">Description</span></span>                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f094f-127">baseeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f094f-127">baseeapconnectionpropertiesv1</span></span>](baseeapconnectionpropertiesv1schema-schema.md)   | <span data-ttu-id="f094f-128">Contém elementos de esquema de configuração comuns.</span><span class="sxs-lookup"><span data-stu-id="f094f-128">Contains common configuration schema elements.</span></span>                                               |
| [<span data-ttu-id="f094f-129">baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f094f-129">baseeapuserpropertiesv1</span></span>](baseeapuserpropertiesv1schema-schema.md)               | <span data-ttu-id="f094f-130">Contém elementos de esquema de credencial comuns.</span><span class="sxs-lookup"><span data-stu-id="f094f-130">Contains common credential schema elements.</span></span>                                                  |
| [<span data-ttu-id="f094f-131">eapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f094f-131">eapconnectionpropertiesv1</span></span>](eapconnectionpropertiesv1schema-schema.md)           | <span data-ttu-id="f094f-132">Contém elementos de esquema de configuração comuns.</span><span class="sxs-lookup"><span data-stu-id="f094f-132">Contains common configuration schema elements.</span></span>                                               |
| [<span data-ttu-id="f094f-133">eapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f094f-133">eapuserpropertiesv1</span></span>](eapuserpropertiesv1schema-schema.md)                       | <span data-ttu-id="f094f-134">Contém elementos de esquema de credencial comuns.</span><span class="sxs-lookup"><span data-stu-id="f094f-134">Contains common credential schema elements.</span></span>                                                  |
| [<span data-ttu-id="f094f-135">eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f094f-135">eaptlsconnectionpropertiesv1</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)     | <span data-ttu-id="f094f-136">É usado com EAP-TLS para descrever os dados de configuração de autenticação.</span><span class="sxs-lookup"><span data-stu-id="f094f-136">Is used with EAP-TLS to describe authentication configuration data.</span></span>                          |
| [<span data-ttu-id="f094f-137">eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="f094f-137">eaptlsconnectionpropertiesv2</span></span>](eaptlsconnectionpropertiesv2schema-schema.md)     | <span data-ttu-id="f094f-138">É usado com EAP-TLS para descrever os dados de configuração de autenticação a partir do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f094f-138">Is used with EAP-TLS to describe authentication configuration data beginning with Windows 7.</span></span> |
| [<span data-ttu-id="f094f-139">eaptlsuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f094f-139">eaptlsuserpropertiesv1</span></span>](eaptlsuserpropertiesv1schema-schema.md)                 | <span data-ttu-id="f094f-140">É usado com EAP-TLS para descrever as credenciais de autenticação e as opções de credenciais.</span><span class="sxs-lookup"><span data-stu-id="f094f-140">Is used with EAP-TLS to describe authentication credentials and credential options.</span></span>          |
| [<span data-ttu-id="f094f-141">mschapv2connectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f094f-141">mschapv2connectionpropertiesv1</span></span>](mschapv2connectionpropertiesv1schema-schema.md) | <span data-ttu-id="f094f-142">É usado com MS-CHAPv2 para descrever os dados de configuração de autenticação.</span><span class="sxs-lookup"><span data-stu-id="f094f-142">Is used with MS-CHAPv2 to describe authentication configuration data.</span></span>                        |
| [<span data-ttu-id="f094f-143">mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f094f-143">mschapv2userpropertiesv1</span></span>](mschapv2userpropertiesv1schema-schema.md)             | <span data-ttu-id="f094f-144">É usado com MS-CHAPv2 para descrever as credenciais de autenticação e as opções de credenciais.</span><span class="sxs-lookup"><span data-stu-id="f094f-144">Is used with MS-CHAPv2 to describe authentication credentials and credential options.</span></span>        |
| [<span data-ttu-id="f094f-145">mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f094f-145">mspeapconnectionpropertiesv1</span></span>](mspeapconnectionpropertiesv1schema-schema.md)     | <span data-ttu-id="f094f-146">É usado com o PEAPv0 para descrever os dados de configuração de autenticação.</span><span class="sxs-lookup"><span data-stu-id="f094f-146">Is used with PEAPv0 to describe authentication configuration data.</span></span>                           |
| [<span data-ttu-id="f094f-147">mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="f094f-147">mspeapconnectionpropertiesv2</span></span>](mspeapconnectionpropertiesv2schema-schema.md)     | <span data-ttu-id="f094f-148">É usado com o PEAPv0 para descrever os dados de configuração de autenticação que começam com o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f094f-148">Is used with PEAPv0 to describe authentication configuration data beginning with Windows 7.</span></span>  |
| [<span data-ttu-id="f094f-149">mspeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f094f-149">mspeapuserpropertiesv1</span></span>](mspeapuserpropertiesv1schema-schema.md)                 | <span data-ttu-id="f094f-150">É usado com o PEAPv0 para descrever as credenciais de autenticação e as opções de credenciais.</span><span class="sxs-lookup"><span data-stu-id="f094f-150">Is used with PEAPv0 to describe authentication credentials and credential options.</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="f094f-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f094f-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f094f-152">Revisão do EAPHost e exemplos de esquema herdados</span><span class="sxs-lookup"><span data-stu-id="f094f-152">Reviewing EAPHost and Legacy Schema Samples</span></span>](eaphost-schemas.md)
</dt> </dl>

 

 




