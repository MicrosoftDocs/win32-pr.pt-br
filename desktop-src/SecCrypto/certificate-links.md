---
description: As funções CertAddCertificateLinkToStore, CertAddCRLLinkToStore e CertAddCTLLinkToStore adicionam links a contextos existentes em repositórios de certificados em vez de adicionar cópias desses contextos.
ms.assetid: 482fb11e-eb59-4de2-a2ad-c1960617e64b
title: Links de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2954c52bcc7b2d98ab5ebb8d732abcbc8f0dea81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091519"
---
# <a name="certificate-links"></a><span data-ttu-id="8ce40-103">Links de certificado</span><span class="sxs-lookup"><span data-stu-id="8ce40-103">Certificate Links</span></span>

<span data-ttu-id="8ce40-104">As funções [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), [**CertAddCRLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)e [**CertAddCTLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore) adicionam links a contextos existentes em [*repositórios de certificados*](../secgloss/c-gly.md) em vez de adicionar cópias desses contextos.</span><span class="sxs-lookup"><span data-stu-id="8ce40-104">The functions [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), [**CertAddCRLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore), and [**CertAddCTLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore) add links to existing contexts into [*certificate stores*](../secgloss/c-gly.md) rather than adding copies of those contexts.</span></span> <span data-ttu-id="8ce40-105">A adição de links a lojas torna o mesmo [*certificado*](../secgloss/c-gly.md)físico, [*CRL*](../secgloss/c-gly.md)ou [*CTL*](../secgloss/c-gly.md) disponível por meio de vários repositórios diferentes.</span><span class="sxs-lookup"><span data-stu-id="8ce40-105">Adding links to stores makes the same physical [*certificate*](../secgloss/c-gly.md), [*CRL*](../secgloss/c-gly.md), or [*CTL*](../secgloss/c-gly.md) available through several different stores.</span></span> <span data-ttu-id="8ce40-106">As alterações feitas nas propriedades estendidas de um [*contexto*](../secgloss/c-gly.md) do repositório do contexto original ou de uma loja em que um link para esse contexto são armazenadas, estão disponíveis na loja que contém o contexto original e em todos os outros repositórios que têm links para esse contexto.</span><span class="sxs-lookup"><span data-stu-id="8ce40-106">Changes made to the extended properties of a [*context*](../secgloss/c-gly.md) from the store of the original context, or from a store where a link to that context is stored, are available in the store that holds the original context and in all other stores that have links to that context.</span></span>

<span data-ttu-id="8ce40-107">Para obter um exemplo que usa [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), consulte [exemplo C programa: operações de repositório de certificados](example-c-program-certificate-store-operations.md).</span><span class="sxs-lookup"><span data-stu-id="8ce40-107">For an example that uses [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), see [Example C Program: Certificate Store Operations](example-c-program-certificate-store-operations.md).</span></span>

![links de certificado](images/mancert1.png)

<span data-ttu-id="8ce40-109">Suponha que os certificados A. 1, A. 2, A. 3 e A. 4 estejam originalmente no armazenamento A e os certificados B. 1, B. 2, B. 3 e B. 4 estão originalmente no repositório B.</span><span class="sxs-lookup"><span data-stu-id="8ce40-109">Assume that certificates A.1, A.2, A.3, and A.4 are originally in store A, and certificates B.1, B.2, B.3, and B.4 are originally in store B.</span></span>

-   <span data-ttu-id="8ce40-110">O diagrama mostra um link adicionado no repositório B para o certificado A. 2 e um link adicionado no repositório A para o certificado B. 2.</span><span class="sxs-lookup"><span data-stu-id="8ce40-110">The diagram shows a link added in store B to certificate A.2 and a link added in store A to certificate B.2.</span></span>
-   <span data-ttu-id="8ce40-111">O original do certificado A. 2 ainda está no armazenamento A. O original de B. 2 ainda está no armazenamento B.</span><span class="sxs-lookup"><span data-stu-id="8ce40-111">The original of certificate A.2 is still in store A. The original of B.2 is still in store B.</span></span>
-   <span data-ttu-id="8ce40-112">Todas as alterações feitas nas propriedades estendidas do certificado A. 2 ou do certificado B. 2 do armazenamento A ou da loja B estarão disponíveis para ambos os repositórios.</span><span class="sxs-lookup"><span data-stu-id="8ce40-112">Any changes made to the extended properties of certificate A.2 or certificate B.2 from either store A or store B will be available to both stores.</span></span>
-   <span data-ttu-id="8ce40-113">Se uma cópia do certificado A. 3 tiver sido feita e armazenada no repositório B, quaisquer alterações nas propriedades estendidas do certificado original A. 3 feito do repositório A não ficarão visíveis na nova cópia no repositório B. Se foram feitas alterações nas propriedades estendidas da cópia do certificado A. 3 no repositório B, essas alterações não afetariam o conteúdo do certificado original A. 3 e não seriam visíveis no armazenamento A.</span><span class="sxs-lookup"><span data-stu-id="8ce40-113">If a copy of certificate A.3 were made and stored in store B, any changes to the extended properties of the original A.3 certificate made from store A would not be visible in the new copy in store B. If changes were made to the extended properties of the copy of certificate A.3 in store B, those changes would not affect the contents of the original A.3 certificate and would not be visible from store A.</span></span>

 

 
