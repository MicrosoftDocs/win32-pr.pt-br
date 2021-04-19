---
description: Os serviços de certificados oferecem suporte a hierarquias de autoridade de certificação (CA).
ms.assetid: bcae26cd-41bc-4436-8f8b-cd8c20e9fcfc
title: Hierarquias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1fe484d752fc7efc7f098aa1cd1af34d88e799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754600"
---
# <a name="hierarchies"></a><span data-ttu-id="5e8c1-103">Hierarquias</span><span class="sxs-lookup"><span data-stu-id="5e8c1-103">Hierarchies</span></span>

<span data-ttu-id="5e8c1-104">Os serviços de certificados oferecem suporte a hierarquias de [*autoridade de certificação*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="5e8c1-104">Certificate Services supports [*certification authority*](../secgloss/c-gly.md) (CA) hierarchies.</span></span> <span data-ttu-id="5e8c1-105">Uma [*hierarquia de CA*](../secgloss/c-gly.md) consiste em uma autoridade de certificação de nível superior (chamada de CA raiz) com uma ou mais CAS subordinadas que receberam certificados pela autoridade de certificação raiz.</span><span class="sxs-lookup"><span data-stu-id="5e8c1-105">A [*CA hierarchy*](../secgloss/c-gly.md) consists of a top-level CA (called the Root CA) with one or more subordinate CAs which have been issued certificates by the root CA.</span></span> <span data-ttu-id="5e8c1-106">Um cenário de hierarquia de autoridade de certificação pode estar em uma organização com uma AC raiz, que foi usada para emitir certificados para várias CAs subordinadas.</span><span class="sxs-lookup"><span data-stu-id="5e8c1-106">A possible CA hierarchy scenario would be in an organization with one root CA, which was used to issue certificates to several subordinate CAs.</span></span> <span data-ttu-id="5e8c1-107">As CAs subordinadas podem emitir certificados de entidade final, como certificados emitidos para um usuário.</span><span class="sxs-lookup"><span data-stu-id="5e8c1-107">The subordinate CAs can then issue end-entity certificates, such as certificates issued to a user.</span></span> <span data-ttu-id="5e8c1-108">O certificado do usuário conterá um caminho de confiança para a hierarquia da autoridade de certificação, nesse caso, incluindo o certificado para a AC subordinada emissora, bem como a autoridade de certificação raiz.</span><span class="sxs-lookup"><span data-stu-id="5e8c1-108">The user's certificate will contain a trust path for the CA hierarchy, in this case, including the certificate for both the issuing subordinate CA as well as the root CA.</span></span>

 

 
