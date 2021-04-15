---
description: Como o número de certificados emitidos em uma infraestrutura de chave pública (PKI) aumenta, pode se tornar difícil para uma única autoridade de certificação (CA) controlar efetivamente os certificados emitidos.
ms.assetid: f1642c1c-d2cd-4fa4-8a26-cebf3d6dcf23
title: Hierarquia de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05c4ed9a69ff96ec0904e658444d6a32b65ed82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554430"
---
# <a name="certificate-hierarchy"></a><span data-ttu-id="4c5e2-103">Hierarquia de certificados</span><span class="sxs-lookup"><span data-stu-id="4c5e2-103">Certificate Hierarchy</span></span>

<span data-ttu-id="4c5e2-104">Como o número de certificados emitidos em uma infraestrutura de chave pública (PKI) aumenta, pode se tornar difícil para uma única autoridade de certificação (CA) controlar efetivamente os certificados emitidos.</span><span class="sxs-lookup"><span data-stu-id="4c5e2-104">As the number of issued certificates in a public key infrastructure (PKI) increases, it can become difficult for a single certification authority (CA) to effectively track the certificates it has issued.</span></span> <span data-ttu-id="4c5e2-105">Uma maneira de resolver isso é criar uma hierarquia de certificados na qual a autoridade de certificação delega a autoridade para emitir certificados para autoridades subordinadas que podem, por sua vez, delegar autoridade a suas subordinadas.</span><span class="sxs-lookup"><span data-stu-id="4c5e2-105">One way to address this is to create a certificate hierarchy in which the CA delegates the authority to issue certificates to subordinate authorities which can, in turn, delegate authority to their subordinates.</span></span> <span data-ttu-id="4c5e2-106">Cada autoridade de certificação Delega autoridade emitindo um certificado de autoridade de certificação para um subordinado.</span><span class="sxs-lookup"><span data-stu-id="4c5e2-106">Each CA delegates authority by issuing a CA certificate to a subordinate.</span></span> <span data-ttu-id="4c5e2-107">A autoridade de certificação inicial na cadeia é chamada de raiz, e não é necessário que uma entidade estabeleça confiança com qualquer AC que resida em uma [cadeia de certificados](about-certificate-chain.md) diferente da qual a entidade reside.</span><span class="sxs-lookup"><span data-stu-id="4c5e2-107">The initial CA in the chain is called the root, and it is not necessary for an entity to establish trust with any CA that resides on a different [Certificate Chain](about-certificate-chain.md) from that on which the entity resides.</span></span>

<span data-ttu-id="4c5e2-108">A ilustração a seguir mostra uma hierarquia de certificado composta de uma CA raiz, duas CAs subordinadas à raiz (uma para o departamento de marketing e outra para o departamento de produção) e CAs subordinadas a elas.</span><span class="sxs-lookup"><span data-stu-id="4c5e2-108">The following illustration shows a certificate hierarchy made up of one root CA, two CAs subordinate to the root (one for the marketing department and one for the manufacturing department), and CAs that are subordinate to these.</span></span>

![diagrama de hierarquia de certificado](images/certificate-hierarchy.png)

## <a name="related-topics"></a><span data-ttu-id="4c5e2-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4c5e2-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c5e2-111">Modelos de confiança</span><span class="sxs-lookup"><span data-stu-id="4c5e2-111">Trust Models</span></span>](about-trust-models.md)
</dt> </dl>

 

 



