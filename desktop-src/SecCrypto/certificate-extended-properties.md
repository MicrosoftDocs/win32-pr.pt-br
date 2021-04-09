---
description: Os dados em um certificado, CRL (lista de certificados revogados) ou contexto de lista de certificados confiáveis (CTL), incluindo todas as extensões, são somente leitura e não podem ser alterados.
ms.assetid: a9958c59-dc89-4d59-8ad3-6651ea4a1e56
title: Propriedades estendidas do certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29853736433cb143a201ca352fceff0141cc96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091322"
---
# <a name="certificate-extended-properties"></a><span data-ttu-id="9fbbe-103">Propriedades estendidas do certificado</span><span class="sxs-lookup"><span data-stu-id="9fbbe-103">Certificate Extended Properties</span></span>

<span data-ttu-id="9fbbe-104">Os dados em um [*certificado*](../secgloss/c-gly.md), CRL ( [*lista de certificados revogados*](../secgloss/c-gly.md) ) ou [*contexto*](../secgloss/c-gly.md)de [*lista de certificados confiáveis*](../secgloss/c-gly.md) (CTL), incluindo todas as extensões, são somente leitura e não podem ser alterados.</span><span class="sxs-lookup"><span data-stu-id="9fbbe-104">The data in a [*certificate*](../secgloss/c-gly.md), [*certificate revocation list*](../secgloss/c-gly.md) (CRL), or [*certificate trust list*](../secgloss/c-gly.md) (CTL) [*context*](../secgloss/c-gly.md), including any extensions, is read-only and cannot be changed.</span></span> <span data-ttu-id="9fbbe-105">No entanto, em plataformas Microsoft, os certificados CryptoAPI também têm propriedades estendidas dinâmicas que podem ser adicionadas e alteradas.</span><span class="sxs-lookup"><span data-stu-id="9fbbe-105">However, on Microsoft platforms, CryptoAPI certificates also have dynamic extended properties that can be added and changed.</span></span>

> [!Note]  
> <span data-ttu-id="9fbbe-106">As propriedades estendidas são associadas a um certificado e não fazem parte de um certificado, conforme emitido por uma [*autoridade de certificação*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="9fbbe-106">Extended properties are associated with a certificate and are not part of a certificate as issued by a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span> <span data-ttu-id="9fbbe-107">As propriedades estendidas não estão disponíveis em um certificado quando ele é usado em uma plataforma que não seja da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9fbbe-107">Extended properties are not available on a certificate when it is used on a non-Microsoft platform.</span></span>

 

<span data-ttu-id="9fbbe-108">Essas propriedades incluem dados que:</span><span class="sxs-lookup"><span data-stu-id="9fbbe-108">These properties include data that:</span></span>

-   <span data-ttu-id="9fbbe-109">Pertence à chave privada a ser usada com o certificado.</span><span class="sxs-lookup"><span data-stu-id="9fbbe-109">Pertains to the private key to be used with the certificate.</span></span>
-   <span data-ttu-id="9fbbe-110">Indica o tipo de hashes a ser executado no certificado.</span><span class="sxs-lookup"><span data-stu-id="9fbbe-110">Indicates the type of hashes to be performed on the certificate.</span></span>
-   <span data-ttu-id="9fbbe-111">Fornece informações definidas pelo usuário associadas ao certificado.</span><span class="sxs-lookup"><span data-stu-id="9fbbe-111">Provides user-defined information associated with the certificate.</span></span>

<span data-ttu-id="9fbbe-112">Em plataformas Microsoft, os valores para essas propriedades são anexados e movidos com o certificado.</span><span class="sxs-lookup"><span data-stu-id="9fbbe-112">On Microsoft platforms, values for these properties are attached to and move with the certificate.</span></span> <span data-ttu-id="9fbbe-113">As propriedades predefinidas atualmente identificadas com as IDs de propriedade incluem as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="9fbbe-113">Currently predefined properties identified with property IDs include the following properties:</span></span>

-   <span data-ttu-id="9fbbe-114">Essas propriedades vinculam um certificado a um CSP específico e, dentro desse CSP, a uma chave privada específica:</span><span class="sxs-lookup"><span data-stu-id="9fbbe-114">These properties tie a certificate to a particular CSP and, within that CSP, to a particular private key:</span></span>
    -   <span data-ttu-id="9fbbe-115">\_ID de \_ \_ prop do \_ identificador \_ da chave de certificado Prov</span><span class="sxs-lookup"><span data-stu-id="9fbbe-115">CERT\_KEY\_PROV\_HANDLE\_PROP\_ID</span></span>
    -   <span data-ttu-id="9fbbe-116">\_ID de \_ \_ prop. \_ informações \_ da chave de certificado Prov</span><span class="sxs-lookup"><span data-stu-id="9fbbe-116">CERT\_KEY\_PROV\_INFO\_PROP\_ID</span></span>
    -   <span data-ttu-id="9fbbe-117">\_ID de \_ prop de contexto de chave de certificado \_ \_</span><span class="sxs-lookup"><span data-stu-id="9fbbe-117">CERT\_KEY\_CONTEXT\_PROP\_ID</span></span>
-   <span data-ttu-id="9fbbe-118">Essas propriedades indicam o algoritmo de hash a ser usado quando uma operação de hash é executada:</span><span class="sxs-lookup"><span data-stu-id="9fbbe-118">These properties indicate the hashing algorithm to be used when a hashing operation is performed:</span></span>
    -   <span data-ttu-id="9fbbe-119">\_ID de \_ \_ prop hash SHA1 de \_ certificado</span><span class="sxs-lookup"><span data-stu-id="9fbbe-119">CERT\_SHA1\_HASH\_PROP\_ID</span></span>
    -   <span data-ttu-id="9fbbe-120">\_ID de \_ \_ prop hash MD5 de \_ certificado</span><span class="sxs-lookup"><span data-stu-id="9fbbe-120">CERT\_MD5\_HASH\_PROP\_ID</span></span>

<span data-ttu-id="9fbbe-121">Para obter listas completas das propriedades de certificado estendido definidas no momento e descrições do significado e uso de cada propriedade, consulte [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty).</span><span class="sxs-lookup"><span data-stu-id="9fbbe-121">For complete lists of currently defined extended certificate properties and descriptions of the meaning and use of each property, see [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fbbe-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9fbbe-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fbbe-123">**CertGetCRLContextProperty**</span><span class="sxs-lookup"><span data-stu-id="9fbbe-123">**CertGetCRLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)
</dt> <dt>

[<span data-ttu-id="9fbbe-124">**CertGetCTLContextProperty**</span><span class="sxs-lookup"><span data-stu-id="9fbbe-124">**CertGetCTLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetctlcontextproperty)
</dt> <dt>

[<span data-ttu-id="9fbbe-125">**CertSetCRLContextProperty**</span><span class="sxs-lookup"><span data-stu-id="9fbbe-125">**CertSetCRLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty)
</dt> <dt>

[<span data-ttu-id="9fbbe-126">**CertSetCTLContextProperty**</span><span class="sxs-lookup"><span data-stu-id="9fbbe-126">**CertSetCTLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetctlcontextproperty)
</dt> </dl>

 

 
