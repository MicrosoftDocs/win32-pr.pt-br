---
title: Atributos de EAP
description: É uma \_ estrutura de atributo EAP que contém um tipo predeterminado de dados relacionados a uma sessão de autenticação.
ms.assetid: 3c54cca2-cd3b-4149-bb0e-036d490cdd3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5348ee300c0e4d07d6aaf110ba9074b1ac32c02a
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "105811994"
---
# <a name="eap-attributes"></a><span data-ttu-id="3ab6e-103">Atributos de EAP</span><span class="sxs-lookup"><span data-stu-id="3ab6e-103">EAP Attributes</span></span>

<span data-ttu-id="3ab6e-104">Um atributo EAP é uma estrutura de [**\_ atributo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) que contém um tipo predeterminado de dados relacionados a uma sessão de autenticação.</span><span class="sxs-lookup"><span data-stu-id="3ab6e-104">An EAP attribute is an [**EAP\_ATTRIBUTE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) structure that contains a predetermined type of data relating to an authentication session.</span></span> <span data-ttu-id="3ab6e-105">Os atributos são usados para comunicar informações entre os métodos EAP e suplicantes ou entre métodos EAP e autenticadores.</span><span class="sxs-lookup"><span data-stu-id="3ab6e-105">Attributes are used to communicate information between EAP methods and supplicants or between EAP methods and authenticators.</span></span> <span data-ttu-id="3ab6e-106">As implementações de ponto e autenticador de um método EAP podem trocar esses atributos por uma rede.</span><span class="sxs-lookup"><span data-stu-id="3ab6e-106">Peer and authenticator implementations of an EAP method may exchange these attributes over a network.</span></span>

<span data-ttu-id="3ab6e-107">Uma lista completa dos tipos de atributo com suporte aparece no [**tópico \_ \_ tipo de atributo EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span><span class="sxs-lookup"><span data-stu-id="3ab6e-107">A complete list of supported attribute types appears in the topic [**EAP\_ATTRIBUTE\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span></span>

## <a name="attributes-consumed-by-supplicants"></a><span data-ttu-id="3ab6e-108">Atributos consumidos por suplicantes</span><span class="sxs-lookup"><span data-stu-id="3ab6e-108">Attributes Consumed by Supplicants</span></span>

<span data-ttu-id="3ab6e-109">Os seguintes tipos de atributo são consumidos por suplicantes 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="3ab6e-109">The following attribute types are consumed by 802.1X supplicants.</span></span>

-   <span data-ttu-id="3ab6e-110">**eatVendorSpecific**</span><span class="sxs-lookup"><span data-stu-id="3ab6e-110">**eatVendorSpecific**</span></span>

<span data-ttu-id="3ab6e-111">Os seguintes tipos de atributo são consumidos por suplicantes de cliente PPP.</span><span class="sxs-lookup"><span data-stu-id="3ab6e-111">The following attribute types are consumed by PPP client supplicants.</span></span>

-   <span data-ttu-id="3ab6e-112">**eatMinimum**</span><span class="sxs-lookup"><span data-stu-id="3ab6e-112">**eatMinimum**</span></span>
-   <span data-ttu-id="3ab6e-113">**eatEAPTLV**</span><span class="sxs-lookup"><span data-stu-id="3ab6e-113">**eatEAPTLV**</span></span>

<span data-ttu-id="3ab6e-114">Os seguintes tipos de atributo são consumidos por suplicantes de servidor PPP.</span><span class="sxs-lookup"><span data-stu-id="3ab6e-114">The following attribute types are consumed by PPP server supplicants.</span></span>

-   <span data-ttu-id="3ab6e-115">**eatUserName**</span><span class="sxs-lookup"><span data-stu-id="3ab6e-115">**eatUserName**</span></span>
-   <span data-ttu-id="3ab6e-116">**eatReplyMessage**</span><span class="sxs-lookup"><span data-stu-id="3ab6e-116">**eatReplyMessage**</span></span>
-   <span data-ttu-id="3ab6e-117">**eatState**</span><span class="sxs-lookup"><span data-stu-id="3ab6e-117">**eatState**</span></span>
-   <span data-ttu-id="3ab6e-118">**eatSessionTimeout**</span><span class="sxs-lookup"><span data-stu-id="3ab6e-118">**eatSessionTimeout**</span></span>
-   <span data-ttu-id="3ab6e-119">**eatEAPMessage**</span><span class="sxs-lookup"><span data-stu-id="3ab6e-119">**eatEAPMessage**</span></span>

## <a name="attributes-exported-by-methods"></a><span data-ttu-id="3ab6e-120">Atributos exportados por métodos</span><span class="sxs-lookup"><span data-stu-id="3ab6e-120">Attributes Exported by Methods</span></span>

<span data-ttu-id="3ab6e-121">Os seguintes tipos de atributo podem ser exportados por métodos EAP.</span><span class="sxs-lookup"><span data-stu-id="3ab6e-121">The following attribute types could be exported by EAP methods.</span></span>

-   <span data-ttu-id="3ab6e-122">**eatClearTextPassword**</span><span class="sxs-lookup"><span data-stu-id="3ab6e-122">**eatClearTextPassword**</span></span>
-   <span data-ttu-id="3ab6e-123">**eatQuarantineSoH**</span><span class="sxs-lookup"><span data-stu-id="3ab6e-123">**eatQuarantineSoH**</span></span>
-   <span data-ttu-id="3ab6e-124">**eatMethodId**</span><span class="sxs-lookup"><span data-stu-id="3ab6e-124">**eatMethodId**</span></span>

<span data-ttu-id="3ab6e-125">O tipo de atributo a seguir é exportado por métodos de TLS (EAP-TLS) de [nível de transporte](/previous-versions/windows/embedded/ms885336(v=msdn.10)) EAP.</span><span class="sxs-lookup"><span data-stu-id="3ab6e-125">The following attribute type is exported by EAP [Transport Level Security (TLS)](/previous-versions/windows/embedded/ms885336(v=msdn.10)) (EAP-TLS) methods.</span></span>

-   <span data-ttu-id="3ab6e-126">**eatCertificateOID**</span><span class="sxs-lookup"><span data-stu-id="3ab6e-126">**eatCertificateOID**</span></span>

<span data-ttu-id="3ab6e-127">Os seguintes tipos de atributo são exportados pelos métodos [Microsoft Challenge Handshake Authentication Protocol versão 2,0](/previous-versions/windows/embedded/ms899190(v=msdn.10)) (MS-CHAPv2).</span><span class="sxs-lookup"><span data-stu-id="3ab6e-127">The following attribute types are exported by [Microsoft Challenge Handshake Authentication Protocol version 2.0](/previous-versions/windows/embedded/ms899190(v=msdn.10)) (MS-CHAPv2) methods.</span></span>

-   <span data-ttu-id="3ab6e-128">**eatUserName**</span><span class="sxs-lookup"><span data-stu-id="3ab6e-128">**eatUserName**</span></span>
-   <span data-ttu-id="3ab6e-129">**eatCredentialsChanged**</span><span class="sxs-lookup"><span data-stu-id="3ab6e-129">**eatCredentialsChanged**</span></span>

<span data-ttu-id="3ab6e-130">O tipo de atributo a seguir é consumido pelo NPS (servidor de diretivas de rede).</span><span class="sxs-lookup"><span data-stu-id="3ab6e-130">The following attribute type is consumed by Network Policy Server (NPS).</span></span>

-   <span data-ttu-id="3ab6e-131">**eatCertificateOID**</span><span class="sxs-lookup"><span data-stu-id="3ab6e-131">**eatCertificateOID**</span></span>

<span data-ttu-id="3ab6e-132">Os tipos de atributo a seguir são exportados por métodos [PEAP (Protected Extensible Authentication Protocol)](/previous-versions/windows/embedded/ms899190(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="3ab6e-132">The following attribute types are exported by [Protected Extensible Authentication Protocol (PEAP)](/previous-versions/windows/embedded/ms899190(v=msdn.10)) methods.</span></span>

-   <span data-ttu-id="3ab6e-133">**eatUserName**</span><span class="sxs-lookup"><span data-stu-id="3ab6e-133">**eatUserName**</span></span>
-   <span data-ttu-id="3ab6e-134">**eatPEAPEmbeddedEAPTypeId**</span><span class="sxs-lookup"><span data-stu-id="3ab6e-134">**eatPEAPEmbeddedEAPTypeId**</span></span>
-   <span data-ttu-id="3ab6e-135">**eatPEAPFastRoamedSession**</span><span class="sxs-lookup"><span data-stu-id="3ab6e-135">**eatPEAPFastRoamedSession**</span></span>
-   <span data-ttu-id="3ab6e-136">**eatQuarantineSoH**</span><span class="sxs-lookup"><span data-stu-id="3ab6e-136">**eatQuarantineSoH**</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ab6e-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3ab6e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ab6e-138">**\_atributo EAP**</span><span class="sxs-lookup"><span data-stu-id="3ab6e-138">**EAP\_ATTRIBUTE**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)
</dt> <dt>

[<span data-ttu-id="3ab6e-139">**\_tipo de atributo EAP \_**</span><span class="sxs-lookup"><span data-stu-id="3ab6e-139">**EAP\_ATTRIBUTE\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
</dt> </dl>

 

 