---
description: Os atributos podem ser adicionados a uma solicitação de certificado para fornecer uma autoridade de certificação (CA) com informações adicionais que podem ser usadas ao criar e emitir um certificado.
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Atributos (API de registro de certificado)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e7a00c30be8bacf5593d78e21fb420c8a899dc7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647645"
---
# <a name="attributes-certificate-enrollment-api"></a><span data-ttu-id="ac838-103">Atributos (API de registro de certificado)</span><span class="sxs-lookup"><span data-stu-id="ac838-103">Attributes (Certificate Enrollment API)</span></span>

<span data-ttu-id="ac838-104">Os atributos podem ser adicionados a uma solicitação de certificado para fornecer uma autoridade de certificação (CA) com informações adicionais que podem ser usadas ao criar e emitir um certificado.</span><span class="sxs-lookup"><span data-stu-id="ac838-104">Attributes can be added to a certificate request to provide a certification authority (CA) with additional information that it can use when creating and issuing a certificate.</span></span> <span data-ttu-id="ac838-105">Cada atributo é uma estrutura ASN (Authorized. 1 [*) codificada*](/windows/desktop/SecGloss/a-gly) de [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der) que contém um OID (identificador de objeto) e zero ou mais valores.</span><span class="sxs-lookup"><span data-stu-id="ac838-105">Each attribute is a [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) encoded [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) structure that contains an object identifier (OID) and zero or more values.</span></span> <span data-ttu-id="ac838-106">Os atributos são definidos usando interfaces incluídas com a API de registro de certificado.</span><span class="sxs-lookup"><span data-stu-id="ac838-106">Attributes are defined by using interfaces included with the Certificate Enrollment API.</span></span> <span data-ttu-id="ac838-107">Os tópicos a seguir abordam os atributos mais detalhadamente:</span><span class="sxs-lookup"><span data-stu-id="ac838-107">The following topics discuss attributes in more detail:</span></span>

-   [<span data-ttu-id="ac838-108">Atributos com suporte</span><span class="sxs-lookup"><span data-stu-id="ac838-108">Supported Attributes</span></span>](supported-attributes.md)
-   [<span data-ttu-id="ac838-109">Arquitetura de atributo</span><span class="sxs-lookup"><span data-stu-id="ac838-109">Attribute Architecture</span></span>](attribute-architecture.md)
-   [<span data-ttu-id="ac838-110">\#Atributos PKCS 7</span><span class="sxs-lookup"><span data-stu-id="ac838-110">PKCS \#7 Attributes</span></span>](pkcs--7-attributes.md)
-   [<span data-ttu-id="ac838-111">\#Atributos PKCS 10</span><span class="sxs-lookup"><span data-stu-id="ac838-111">PKCS \#10 Attributes</span></span>](pkcs--10-attributes.md)
-   [<span data-ttu-id="ac838-112">Atributos CMC</span><span class="sxs-lookup"><span data-stu-id="ac838-112">CMC Attributes</span></span>](cmc-attributes.md)

 

 
