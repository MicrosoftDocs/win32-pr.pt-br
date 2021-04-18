---
description: O CryptXML oferece suporte nativo aos URIs listados abaixo.
ms.assetid: 012bad01-228a-4bb0-b883-0c2c7abd9271
title: Algoritmos criptográficos de assinatura digital XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896348375d1d1a51288980aad3793dfffc69eb18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796364"
---
# <a name="xml-digital-signature-cryptographic-algorithms"></a><span data-ttu-id="32e0d-103">Algoritmos criptográficos de assinatura digital XML</span><span class="sxs-lookup"><span data-stu-id="32e0d-103">XML Digital Signature Cryptographic Algorithms</span></span>

<span data-ttu-id="32e0d-104">O CryptXML oferece suporte nativo aos URIs listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="32e0d-104">CryptXML natively supports the URIs listed below.</span></span> <span data-ttu-id="32e0d-105">Se o suporte for necessário para algoritmos criptográficos e transformações que não fazem parte do suporte nativo, você poderá usar a [API de criptografia: próxima geração](../seccng/cng-portal.md) e [extensões criptográficas de assinatura digital XML](xml-digital-signature-cryptographic-extensions.md) para dar suporte a novos algoritmos.</span><span class="sxs-lookup"><span data-stu-id="32e0d-105">If support is required for cryptographic algorithms and transforms that are not part of the native support, you can use [Cryptography API: Next Generation](../seccng/cng-portal.md) and [XML Digital Signature Cryptographic Extensions](xml-digital-signature-cryptographic-extensions.md) to support new algorithms.</span></span>

## <a name="supported-uris"></a><span data-ttu-id="32e0d-106">URIs com suporte</span><span class="sxs-lookup"><span data-stu-id="32e0d-106">Supported URIs</span></span>

<span data-ttu-id="32e0d-107">Métodos de resumo</span><span class="sxs-lookup"><span data-stu-id="32e0d-107">Digest Methods</span></span>



| <span data-ttu-id="32e0d-108">Constante</span><span class="sxs-lookup"><span data-stu-id="32e0d-108">Constant</span></span>                                 | <span data-ttu-id="32e0d-109">Valor do URI</span><span class="sxs-lookup"><span data-stu-id="32e0d-109">URI value</span></span>                                                   |
|------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="32e0d-110">wszURI \_ xmlns \_ DIGSIG \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="32e0d-110">wszURI\_XMLNS\_DIGSIG\_SHA1</span></span><br/>   | <span data-ttu-id="32e0d-111">"https://www.w3.org/2000/09/xmldsig\#sha1"</span><span class="sxs-lookup"><span data-stu-id="32e0d-111">"https://www.w3.org/2000/09/xmldsig\#sha1"</span></span><br/>        |
| <span data-ttu-id="32e0d-112">wszURI \_ xmlns \_ DIGSIG \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="32e0d-112">wszURI\_XMLNS\_DIGSIG\_SHA256</span></span><br/> | <span data-ttu-id="32e0d-113">"https://www.w3.org/2001/04/xmlenc\#sha256"</span><span class="sxs-lookup"><span data-stu-id="32e0d-113">"https://www.w3.org/2001/04/xmlenc\#sha256"</span></span><br/>       |
| <span data-ttu-id="32e0d-114">wszURI \_ xmlns \_ DIGSIG \_ Sha384</span><span class="sxs-lookup"><span data-stu-id="32e0d-114">wszURI\_XMLNS\_DIGSIG\_SHA384</span></span><br/> | <span data-ttu-id="32e0d-115">"https://www.w3.org/2001/04/xmldsig-more\#sha384"</span><span class="sxs-lookup"><span data-stu-id="32e0d-115">"https://www.w3.org/2001/04/xmldsig-more\#sha384"</span></span><br/> |
| <span data-ttu-id="32e0d-116">wszURI \_ xmlns \_ DIGSIG \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="32e0d-116">wszURI\_XMLNS\_DIGSIG\_SHA512</span></span><br/> | <span data-ttu-id="32e0d-117">"https://www.w3.org/2001/04/xmlenc\#sha512"</span><span class="sxs-lookup"><span data-stu-id="32e0d-117">"https://www.w3.org/2001/04/xmlenc\#sha512"</span></span><br/>       |



 

<span data-ttu-id="32e0d-118">Métodos de assinatura</span><span class="sxs-lookup"><span data-stu-id="32e0d-118">Signature Methods</span></span>



| <span data-ttu-id="32e0d-119">Constante</span><span class="sxs-lookup"><span data-stu-id="32e0d-119">Constant</span></span>                                        | <span data-ttu-id="32e0d-120">Valor do URI</span><span class="sxs-lookup"><span data-stu-id="32e0d-120">URI value</span></span>                                                         |
|-------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="32e0d-121">wszURI \_ xmlns \_ DIGSIG \_ RSA \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="32e0d-121">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA1</span></span><br/>     | <span data-ttu-id="32e0d-122">"https://www.w3.org/2000/09/xmldsig\#rsa-sha1"</span><span class="sxs-lookup"><span data-stu-id="32e0d-122">"https://www.w3.org/2000/09/xmldsig\#rsa-sha1"</span></span><br/>          |
| <span data-ttu-id="32e0d-123">wszURI \_ xmlns \_ DIGSIG \_ DSA \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="32e0d-123">wszURI\_XMLNS\_DIGSIG\_DSA\_SHA1</span></span><br/>     | <span data-ttu-id="32e0d-124">"https://www.w3.org/2000/09/xmldsig\#dsa-sha1"</span><span class="sxs-lookup"><span data-stu-id="32e0d-124">"https://www.w3.org/2000/09/xmldsig\#dsa-sha1"</span></span><br/>          |
| <span data-ttu-id="32e0d-125">wszURI \_ xmlns \_ DIGSIG \_ RSA \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="32e0d-125">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA256</span></span><br/>   | <span data-ttu-id="32e0d-126">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha256"</span><span class="sxs-lookup"><span data-stu-id="32e0d-126">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha256"</span></span><br/>   |
| <span data-ttu-id="32e0d-127">wszURI \_ xmlns \_ DIGSIG \_ RSA \_ Sha384</span><span class="sxs-lookup"><span data-stu-id="32e0d-127">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA384</span></span><br/>   | <span data-ttu-id="32e0d-128">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha384"</span><span class="sxs-lookup"><span data-stu-id="32e0d-128">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha384"</span></span><br/>   |
| <span data-ttu-id="32e0d-129">wszURI \_ xmlns \_ DIGSIG \_ RSA \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="32e0d-129">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA512</span></span><br/>   | <span data-ttu-id="32e0d-130">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha512"</span><span class="sxs-lookup"><span data-stu-id="32e0d-130">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha512"</span></span><br/>   |
| <span data-ttu-id="32e0d-131">wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="32e0d-131">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA1</span></span><br/>   | <span data-ttu-id="32e0d-132">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha1"</span><span class="sxs-lookup"><span data-stu-id="32e0d-132">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha1"</span></span><br/>   |
| <span data-ttu-id="32e0d-133">wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="32e0d-133">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA256</span></span><br/> | <span data-ttu-id="32e0d-134">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha256"</span><span class="sxs-lookup"><span data-stu-id="32e0d-134">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha256"</span></span><br/> |
| <span data-ttu-id="32e0d-135">wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ Sha384</span><span class="sxs-lookup"><span data-stu-id="32e0d-135">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA384</span></span><br/> | <span data-ttu-id="32e0d-136">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha384"</span><span class="sxs-lookup"><span data-stu-id="32e0d-136">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha384"</span></span><br/> |
| <span data-ttu-id="32e0d-137">wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="32e0d-137">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA512</span></span><br/> | <span data-ttu-id="32e0d-138">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha512"</span><span class="sxs-lookup"><span data-stu-id="32e0d-138">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha512"</span></span><br/> |
| <span data-ttu-id="32e0d-139">wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="32e0d-139">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA1</span></span><br/>    | <span data-ttu-id="32e0d-140">"https://www.w3.org/2000/09/xmldsig\#hmac-sha1"</span><span class="sxs-lookup"><span data-stu-id="32e0d-140">"https://www.w3.org/2000/09/xmldsig\#hmac-sha1"</span></span><br/>         |
| <span data-ttu-id="32e0d-141">wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="32e0d-141">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA256</span></span><br/>  | <span data-ttu-id="32e0d-142">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha256"</span><span class="sxs-lookup"><span data-stu-id="32e0d-142">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha256"</span></span><br/>  |
| <span data-ttu-id="32e0d-143">wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ Sha384</span><span class="sxs-lookup"><span data-stu-id="32e0d-143">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA384</span></span><br/>  | <span data-ttu-id="32e0d-144">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha384"</span><span class="sxs-lookup"><span data-stu-id="32e0d-144">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha384"</span></span><br/>  |
| <span data-ttu-id="32e0d-145">wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="32e0d-145">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA512</span></span><br/>  | <span data-ttu-id="32e0d-146">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha512"</span><span class="sxs-lookup"><span data-stu-id="32e0d-146">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha512"</span></span><br/>  |



 

 

 
