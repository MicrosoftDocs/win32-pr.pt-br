---
description: Os certificados têm propriedades associadas, como um nome de exibição, uma descrição e usos permitidos, que podem ser exibidos e editados.
ms.assetid: 23faaa03-af3e-4497-8607-4e34f8889368
title: Criando, exibindo e gerenciando certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2136f8cd3ea3af1aab95b3c9c89ddd5787b4cefc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748394"
---
# <a name="creating-viewing-and-managing-certificates"></a><span data-ttu-id="2ee10-103">Criando, exibindo e gerenciando certificados</span><span class="sxs-lookup"><span data-stu-id="2ee10-103">Creating, Viewing, and Managing Certificates</span></span>

<span data-ttu-id="2ee10-104">Os [*certificados*](../secgloss/c-gly.md) são estruturas somente leitura.</span><span class="sxs-lookup"><span data-stu-id="2ee10-104">[*Certificates*](../secgloss/c-gly.md) are read-only structures.</span></span> <span data-ttu-id="2ee10-105">O conteúdo de um certificado pode ser exibido, mas não pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="2ee10-105">The contents of a certificate can be viewed but cannot be modified.</span></span> <span data-ttu-id="2ee10-106">As informações contidas no certificado incluem as datas de validade, o emissor, o assunto e a chave pública do certificado.</span><span class="sxs-lookup"><span data-stu-id="2ee10-106">Information in the certificate itself includes the certificate's validity dates, issuer, subject, and the public key.</span></span> <span data-ttu-id="2ee10-107">No entanto, os certificados têm propriedades associadas, como um nome de exibição, uma descrição e usos permitidos, que podem ser exibidos e editados.</span><span class="sxs-lookup"><span data-stu-id="2ee10-107">However, certificates have associated properties, such as a display name, description, and allowed uses, that can be viewed and edited.</span></span>

<span data-ttu-id="2ee10-108">Esta seção demonstra a criação de certificados de teste, a exibição de certificados e o gerenciamento de certificados e outros objetos de segurança.</span><span class="sxs-lookup"><span data-stu-id="2ee10-108">This section demonstrates creating test certificates, viewing certificates, and managing certificates and other security objects.</span></span> <span data-ttu-id="2ee10-109">Os certificados e os [*certificados de fornecedor de software*](../secgloss/s-gly.md) (SPCS) que podem ser criados com MakeCert são estritamente para fins de teste.</span><span class="sxs-lookup"><span data-stu-id="2ee10-109">The certificates and [*Software Publisher Certificates*](../secgloss/s-gly.md) (SPCs) that can be created with MakeCert are strictly for test purposes.</span></span> <span data-ttu-id="2ee10-110">Um [*certificado raiz*](../secgloss/r-gly.md) de teste e uma [*chave privada*](../secgloss/p-gly.md) raiz de teste são fornecidos apenas para fins de teste.</span><span class="sxs-lookup"><span data-stu-id="2ee10-110">A test [*root certificate*](../secgloss/r-gly.md) and a test root [*private key*](../secgloss/p-gly.md) are provided for testing purposes only.</span></span> <span data-ttu-id="2ee10-111">Fornecedores de software independentes devem obter um certificado de GTE, VeriSign, Inc. ou outra [*autoridade de certificação*](../secgloss/c-gly.md) (CA) para assinar o código que será distribuído para o público.</span><span class="sxs-lookup"><span data-stu-id="2ee10-111">Independent software vendors must obtain a certificate from GTE, VeriSign, Inc., or other [*certification authority*](../secgloss/c-gly.md) (CA) to sign code that will be distributed to the public.</span></span>

<span data-ttu-id="2ee10-112">Esta seção inclui os tópicos a seguir:</span><span class="sxs-lookup"><span data-stu-id="2ee10-112">This section includes the following topics:</span></span>

-   [<span data-ttu-id="2ee10-113">Usando MakeCert</span><span class="sxs-lookup"><span data-stu-id="2ee10-113">Using MakeCert</span></span>](using-makecert.md)
-   [<span data-ttu-id="2ee10-114">Usando Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="2ee10-114">Using Cert2SPC</span></span>](using-cert2spc.md)
-   [<span data-ttu-id="2ee10-115">Usando CertMgr</span><span class="sxs-lookup"><span data-stu-id="2ee10-115">Using CertMgr</span></span>](using-certmgr.md)

 

 
