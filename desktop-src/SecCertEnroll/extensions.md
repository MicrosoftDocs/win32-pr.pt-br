---
description: O formato de certificado X. 509 versão 3 identifica várias extensões que podem ser adicionadas a um certificado.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Extensões (API de registro de certificado)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5478b8edeff3524ada760cc5680f5c9dca359e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752536"
---
# <a name="extensions-certificate-enrollment-api"></a><span data-ttu-id="5bc5d-103">Extensões (API de registro de certificado)</span><span class="sxs-lookup"><span data-stu-id="5bc5d-103">Extensions (Certificate Enrollment API)</span></span>

<span data-ttu-id="5bc5d-104">O formato de certificado X. 509 versão 3 identifica várias extensões que podem ser adicionadas a um certificado.</span><span class="sxs-lookup"><span data-stu-id="5bc5d-104">The X.509 version 3 certificate format identifies multiple extensions that can be added to a certificate.</span></span> <span data-ttu-id="5bc5d-105">As extensões fornecem informações aprimoradas sobre o uso da chave, políticas de certificado e restrições, formulários de nome alternativo e muito mais.</span><span class="sxs-lookup"><span data-stu-id="5bc5d-105">The extensions provide enhanced information about key usage, certificate policies and constraints, alternative name forms, and more.</span></span> <span data-ttu-id="5bc5d-106">Você pode usar a interface [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) para definir um valor de extensão.</span><span class="sxs-lookup"><span data-stu-id="5bc5d-106">You can use the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface to define an extension value.</span></span> <span data-ttu-id="5bc5d-107">Muitas das extensões comuns podem ser criadas usando interfaces predefinidas derivadas de **IX509Extension**.</span><span class="sxs-lookup"><span data-stu-id="5bc5d-107">Many of the common extensions can be created by using predefined interfaces derived from **IX509Extension**.</span></span> <span data-ttu-id="5bc5d-108">Uma coleção de extensões é adicionada a uma solicitação de certificado, incluindo a coleção nos atributos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="5bc5d-108">A collection of extensions is added to a certificate request by including the collection in the request attributes.</span></span> <span data-ttu-id="5bc5d-109">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="5bc5d-109">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="5bc5d-110">Extensões com suporte</span><span class="sxs-lookup"><span data-stu-id="5bc5d-110">Supported Extensions</span></span>](supported-extensions.md)
-   [<span data-ttu-id="5bc5d-111">\#Extensões PKCS 10</span><span class="sxs-lookup"><span data-stu-id="5bc5d-111">PKCS \#10 Extensions</span></span>](pkcs--10-extensions.md)
-   [<span data-ttu-id="5bc5d-112">Extensões CMC</span><span class="sxs-lookup"><span data-stu-id="5bc5d-112">CMC Extensions</span></span>](cmc-extensions.md)

 

 



