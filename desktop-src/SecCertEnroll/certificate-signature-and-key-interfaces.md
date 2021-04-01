---
description: As interfaces a seguir podem ser usadas para gerenciar assinaturas de certificado e chaves públicas e privadas.
ms.assetid: 628d6629-3ec3-447e-8b60-a2db5b23e780
title: Assinatura de certificado e interfaces de chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35d2f3b1404397b1e6f2e436ef27fb740bbb594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829165"
---
# <a name="certificate-signature-and-key-interfaces"></a><span data-ttu-id="6efda-103">Assinatura de certificado e interfaces de chave</span><span class="sxs-lookup"><span data-stu-id="6efda-103">Certificate Signature and Key Interfaces</span></span>

<span data-ttu-id="6efda-104">As interfaces a seguir podem ser usadas para gerenciar assinaturas de certificado e chaves públicas e privadas.</span><span class="sxs-lookup"><span data-stu-id="6efda-104">The following interfaces can be used to manage certificate signatures, and public and private keys.</span></span>



| <span data-ttu-id="6efda-105">Interface</span><span class="sxs-lookup"><span data-stu-id="6efda-105">Interface</span></span>                                                      | <span data-ttu-id="6efda-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="6efda-106">Description</span></span>                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6efda-107">**ISignerCertificate**</span><span class="sxs-lookup"><span data-stu-id="6efda-107">**ISignerCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)               | <span data-ttu-id="6efda-108">Representa um certificado de assinatura que permite assinar uma solicitação de certificado.</span><span class="sxs-lookup"><span data-stu-id="6efda-108">Represents a signing certificate that enables you to sign a certificate request.</span></span>                  |
| [<span data-ttu-id="6efda-109">**ISignerCertificates**</span><span class="sxs-lookup"><span data-stu-id="6efda-109">**ISignerCertificates**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates)             | <span data-ttu-id="6efda-110">Gerencia uma coleção de objetos [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) .</span><span class="sxs-lookup"><span data-stu-id="6efda-110">Manages a collection of [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) objects.</span></span>                 |
| [<span data-ttu-id="6efda-111">**IX509PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="6efda-111">**IX509PrivateKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)                     | <span data-ttu-id="6efda-112">Representa uma chave privada assimétrica que pode ser usada para criptografia, assinatura e contrato de chave.</span><span class="sxs-lookup"><span data-stu-id="6efda-112">Represents an asymmetric private key that can be used for encryption, signing, and key agreement.</span></span> |
| [<span data-ttu-id="6efda-113">**IX509PublicKey**</span><span class="sxs-lookup"><span data-stu-id="6efda-113">**IX509PublicKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey)                       | <span data-ttu-id="6efda-114">Representa uma chave pública em um par de chaves pública/privada.</span><span class="sxs-lookup"><span data-stu-id="6efda-114">Represents a public key in a public/private key pair.</span></span>                                             |
| [<span data-ttu-id="6efda-115">**IX509SignatureInformation**</span><span class="sxs-lookup"><span data-stu-id="6efda-115">**IX509SignatureInformation**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) | <span data-ttu-id="6efda-116">Representa informações usadas para assinar uma solicitação de certificado.</span><span class="sxs-lookup"><span data-stu-id="6efda-116">Represents information used to sign a certificate request.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="6efda-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6efda-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6efda-118">Interfaces CertEnroll</span><span class="sxs-lookup"><span data-stu-id="6efda-118">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



