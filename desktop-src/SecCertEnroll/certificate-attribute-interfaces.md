---
description: As interfaces a seguir podem ser usadas para criar atributos de certificado.
ms.assetid: 3701f9b2-0857-45f0-b3ed-4f1b3db4d6d8
title: Interfaces de atributo de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 930f427ae6333084c8a180e5d227e4c24daa5426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748870"
---
# <a name="certificate-attribute-interfaces"></a><span data-ttu-id="24327-103">Interfaces de atributo de certificado</span><span class="sxs-lookup"><span data-stu-id="24327-103">Certificate Attribute Interfaces</span></span>

<span data-ttu-id="24327-104">As interfaces a seguir podem ser usadas para criar atributos de certificado.</span><span class="sxs-lookup"><span data-stu-id="24327-104">The following interfaces can be used to create certificate attributes.</span></span>



| <span data-ttu-id="24327-105">Interface</span><span class="sxs-lookup"><span data-stu-id="24327-105">Interface</span></span>                                                                    | <span data-ttu-id="24327-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="24327-106">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="24327-107">**ICryptAttribute**</span><span class="sxs-lookup"><span data-stu-id="24327-107">**ICryptAttribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)                                   | <span data-ttu-id="24327-108">Representa um atributo criptográfico em uma solicitação de certificado.</span><span class="sxs-lookup"><span data-stu-id="24327-108">Represents a cryptographic attribute in a certificate request.</span></span>                                                                              |
| [<span data-ttu-id="24327-109">**ICryptAttributes**</span><span class="sxs-lookup"><span data-stu-id="24327-109">**ICryptAttributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)                                 | <span data-ttu-id="24327-110">Gerencia uma coleção de objetos [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) .</span><span class="sxs-lookup"><span data-stu-id="24327-110">Manages a collection of [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) objects.</span></span>                                                                 |
| [<span data-ttu-id="24327-111">**IX509Attribute**</span><span class="sxs-lookup"><span data-stu-id="24327-111">**IX509Attribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)                                     | <span data-ttu-id="24327-112">Representa um atributo em uma \# solicitação de certificado PKCS 7, PKCS \# 10 ou CMC.</span><span class="sxs-lookup"><span data-stu-id="24327-112">Represents an attribute in a PKCS \#7, PKCS \#10, or CMC certificate request.</span></span>                                                               |
| [<span data-ttu-id="24327-113">**IX509AttributeClientId**</span><span class="sxs-lookup"><span data-stu-id="24327-113">**IX509AttributeClientId**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)                     | <span data-ttu-id="24327-114">Representa um atributo que pode ser usado para identificar o cliente que gerou uma solicitação de certificado.</span><span class="sxs-lookup"><span data-stu-id="24327-114">Represents an attribute that can be used to identify the client that generated a certificate request.</span></span>                                       |
| [<span data-ttu-id="24327-115">**IX509AttributeExtensions**</span><span class="sxs-lookup"><span data-stu-id="24327-115">**IX509AttributeExtensions**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)                 | <span data-ttu-id="24327-116">Representa as extensões de certificado em uma solicitação de certificado.</span><span class="sxs-lookup"><span data-stu-id="24327-116">Represents the certificate extensions in a certificate request.</span></span>                                                                             |
| [<span data-ttu-id="24327-117">**IX509AttributeArchiveKey**</span><span class="sxs-lookup"><span data-stu-id="24327-117">**IX509AttributeArchiveKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)                 | <span data-ttu-id="24327-118">Representa um atributo que contém uma chave privada criptografada a ser arquivada por uma autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="24327-118">Represents an attribute that contains an encrypted private key to be archived by a certification authority.</span></span>                                 |
| [<span data-ttu-id="24327-119">**IX509AttributeArchiveKeyHash**</span><span class="sxs-lookup"><span data-stu-id="24327-119">**IX509AttributeArchiveKeyHash**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)         | <span data-ttu-id="24327-120">Representa um atributo que contém um hash SHA-1 da chave privada criptografada a ser arquivada por uma autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="24327-120">Represents an attribute that contains a SHA-1 hash of the encrypted private key to be archived by a certification authority.</span></span>                |
| [<span data-ttu-id="24327-121">**IX509AttributeCspProvider**</span><span class="sxs-lookup"><span data-stu-id="24327-121">**IX509AttributeCspProvider**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)               | <span data-ttu-id="24327-122">Representa um atributo que identifica o provedor criptográfico usado pela entidade que solicita o certificado.</span><span class="sxs-lookup"><span data-stu-id="24327-122">Represents an attribute that identifies the cryptographic provider used by the entity requesting the certificate.</span></span>                           |
| [<span data-ttu-id="24327-123">**IX509AttributeOSVersion**</span><span class="sxs-lookup"><span data-stu-id="24327-123">**IX509AttributeOSVersion**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)                   | <span data-ttu-id="24327-124">Representa um atributo que contém informações de versão sobre o sistema operacional do cliente no qual a solicitação de certificado foi gerada.</span><span class="sxs-lookup"><span data-stu-id="24327-124">Represents an attribute that contains version information about the client operating system on which the certificate request was generated.</span></span> |
| [<span data-ttu-id="24327-125">**IX509AttributeRenewalCertificate**</span><span class="sxs-lookup"><span data-stu-id="24327-125">**IX509AttributeRenewalCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) | <span data-ttu-id="24327-126">Representa um atributo que contém o certificado que está sendo renovado.</span><span class="sxs-lookup"><span data-stu-id="24327-126">Represents an attribute that contains the certificate being renewed.</span></span>                                                                        |
| [<span data-ttu-id="24327-127">**IX509Attributes**</span><span class="sxs-lookup"><span data-stu-id="24327-127">**IX509Attributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)                                   | <span data-ttu-id="24327-128">Gerencia uma coleção de objetos [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) .</span><span class="sxs-lookup"><span data-stu-id="24327-128">Manages a collection of [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) objects.</span></span>                                                                   |
| [<span data-ttu-id="24327-129">**IX509NameValuePair**</span><span class="sxs-lookup"><span data-stu-id="24327-129">**IX509NameValuePair**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)                             | <span data-ttu-id="24327-130">Representa um par de nome-valor genérico.</span><span class="sxs-lookup"><span data-stu-id="24327-130">Represents a generic name-value pair.</span></span>                                                                                                       |
| [<span data-ttu-id="24327-131">**IX509NameValuePairs**</span><span class="sxs-lookup"><span data-stu-id="24327-131">**IX509NameValuePairs**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)                           | <span data-ttu-id="24327-132">Gerencia uma coleção de objetos [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) .</span><span class="sxs-lookup"><span data-stu-id="24327-132">Manages a collection of [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) objects.</span></span>                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="24327-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="24327-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24327-134">Interfaces CertEnroll</span><span class="sxs-lookup"><span data-stu-id="24327-134">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



