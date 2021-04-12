---
description: Várias funções adicionam um contexto de certificado ou um link a um contexto para um \[ SDK (Software Development Kit) da plataforma de armazenamento \] .
ms.assetid: 0355b254-be52-4af4-9567-ee2df092075f
title: Trabalhando com certificados em repositórios de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba1ce89c9b9352ef787ed65230b709967125532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297181"
---
# <a name="working-with-certificates-in-certificate-stores"></a><span data-ttu-id="6da89-103">Trabalhando com certificados em repositórios de certificados</span><span class="sxs-lookup"><span data-stu-id="6da89-103">Working with Certificates in Certificate Stores</span></span>

<span data-ttu-id="6da89-104">Várias funções adicionam um contexto de certificado ou um link a um contexto para um repositório.</span><span class="sxs-lookup"><span data-stu-id="6da89-104">Several functions add a certificate context or a link to a context to a store.</span></span>

<span data-ttu-id="6da89-105">Para certificados que já estão no formulário de contexto de certificado:</span><span class="sxs-lookup"><span data-stu-id="6da89-105">For certificates already in certificate context form:</span></span>

-   [<span data-ttu-id="6da89-106">**CertAddCertificateContextToStore**</span><span class="sxs-lookup"><span data-stu-id="6da89-106">**CertAddCertificateContextToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore)
-   [<span data-ttu-id="6da89-107">**CertAddCRLContextToStore**</span><span class="sxs-lookup"><span data-stu-id="6da89-107">**CertAddCRLContextToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrlcontexttostore)
-   [<span data-ttu-id="6da89-108">**CertAddCTLContextToStore**</span><span class="sxs-lookup"><span data-stu-id="6da89-108">**CertAddCTLContextToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctlcontexttostore)
-   [<span data-ttu-id="6da89-109">**CertAddCertificateLinkToStore**</span><span class="sxs-lookup"><span data-stu-id="6da89-109">**CertAddCertificateLinkToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)
-   [<span data-ttu-id="6da89-110">**CertAddCRLLinkToStore**</span><span class="sxs-lookup"><span data-stu-id="6da89-110">**CertAddCRLLinkToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)
-   [<span data-ttu-id="6da89-111">**CertAddCTLLinkToStore**</span><span class="sxs-lookup"><span data-stu-id="6da89-111">**CertAddCTLLinkToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore)

<span data-ttu-id="6da89-112">Para certificados que estão em formato codificado, mas não em contextos de certificado completos:</span><span class="sxs-lookup"><span data-stu-id="6da89-112">For certificates that are in encoded form but not full certificate contexts:</span></span>

-   [<span data-ttu-id="6da89-113">**CertAddEncodedCertificateToStore**</span><span class="sxs-lookup"><span data-stu-id="6da89-113">**CertAddEncodedCertificateToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore)
-   [<span data-ttu-id="6da89-114">**CertAddEncodedCRLToStore**</span><span class="sxs-lookup"><span data-stu-id="6da89-114">**CertAddEncodedCRLToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcrltostore)
-   [<span data-ttu-id="6da89-115">**CertAddEncodedCTLToStore**</span><span class="sxs-lookup"><span data-stu-id="6da89-115">**CertAddEncodedCTLToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)

<span data-ttu-id="6da89-116">As funções a seguir excluem um certificado, CRL ou CTL de um repositório decrementando sua contagem de referência em um.</span><span class="sxs-lookup"><span data-stu-id="6da89-116">The following functions delete a certificate, CRL, or CTL from a store by decrementing its reference count by one.</span></span> <span data-ttu-id="6da89-117">Se isso fizer com que a contagem de referência se torne zero, a memória usada para armazenar o certificado, CRL ou CTL será liberada.</span><span class="sxs-lookup"><span data-stu-id="6da89-117">If this causes the reference count to become zero, the memory used to store the certificate, CRL, or CTL is freed.</span></span>

-   [<span data-ttu-id="6da89-118">**CertDeleteCertificateFromStore**</span><span class="sxs-lookup"><span data-stu-id="6da89-118">**CertDeleteCertificateFromStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore)
-   [<span data-ttu-id="6da89-119">**CertDeleteCRLFromStore**</span><span class="sxs-lookup"><span data-stu-id="6da89-119">**CertDeleteCRLFromStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecrlfromstore)
-   [<span data-ttu-id="6da89-120">**CertDeleteCTLFromStore**</span><span class="sxs-lookup"><span data-stu-id="6da89-120">**CertDeleteCTLFromStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore)

 

 



