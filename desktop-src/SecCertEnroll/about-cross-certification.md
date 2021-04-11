---
description: A certificação cruzada habilita entidades em uma PKI (infraestrutura de chave pública) para confiar em entidades em outra PKI.
ms.assetid: 93cdb10d-4b77-4511-8c5b-c27b290f9154
title: Certificação cruzada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18fcb8317145b7239464893391c5d2231ab1cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170648"
---
# <a name="cross-certification"></a><span data-ttu-id="6cc4e-103">Certificação cruzada</span><span class="sxs-lookup"><span data-stu-id="6cc4e-103">Cross Certification</span></span>

<span data-ttu-id="6cc4e-104">A certificação cruzada habilita entidades em uma PKI (infraestrutura de chave pública) para confiar em entidades em outra PKI.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-104">Cross certification enables entities in one public key infrastructure (PKI) to trust entities in another PKI.</span></span> <span data-ttu-id="6cc4e-105">Essa relação de confiança mútua normalmente é suportada por um contrato de certificação cruzada entre as CAs (autoridades de certificação) em cada PKI.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-105">This mutual trust relationship is typically supported by a cross-certification agreement between the certification authorities (CAs) in each PKI.</span></span> <span data-ttu-id="6cc4e-106">O contrato estabelece as responsabilidades e a responsabilidade de cada parte.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-106">The agreement establishes the responsibilities and liability of each party.</span></span>

<span data-ttu-id="6cc4e-107">Uma relação de confiança mútua entre duas CAs requer que cada CA emita um certificado para o outro para estabelecer a relação em ambas as direções.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-107">A mutual trust relationship between two CAs requires that each CA issue a certificate to the other to establish the relationship in both directions.</span></span> <span data-ttu-id="6cc4e-108">O caminho de confiança não é hierárquico (nenhuma das CAs reguladoras é subordinada ao outro), embora as PKIs separadas possam ser hierarquias de certificado.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-108">The path of trust is not hierarchal (neither of the governing CAs is subordinate to the other) although the separate PKIs may be certificate hierarchies.</span></span> <span data-ttu-id="6cc4e-109">Depois que duas CAs tiverem estabelecido e especificado os termos de confiança e os certificados emitidos entre si, as entidades dentro da PKIs separada poderão interagir com as políticas especificadas nos certificados.</span><span class="sxs-lookup"><span data-stu-id="6cc4e-109">After two CAs have established and specified the terms of trust and issued certificates to each other, entities within the separate PKIs can interact subject to the policies specified in the certificates.</span></span>

![diagrama de certificação cruzada](images/cross-certification.png)

## <a name="related-topics"></a><span data-ttu-id="6cc4e-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6cc4e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cc4e-112">Modelos de confiança</span><span class="sxs-lookup"><span data-stu-id="6cc4e-112">Trust Models</span></span>](about-trust-models.md)
</dt> </dl>

 

 



