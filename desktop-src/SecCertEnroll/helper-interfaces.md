---
description: As interfaces de uso gerais a seguir têm suporte da API de registro de certificado.
ms.assetid: 6b9d9761-6131-4408-8177-5418abd5e406
title: Interfaces auxiliares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a0c6948e9b0fe09aee0b983d230f53bc8e76b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796386"
---
# <a name="helper-interfaces"></a><span data-ttu-id="13049-103">Interfaces auxiliares</span><span class="sxs-lookup"><span data-stu-id="13049-103">Helper Interfaces</span></span>

<span data-ttu-id="13049-104">As interfaces de uso gerais a seguir têm suporte da API de registro de certificado.</span><span class="sxs-lookup"><span data-stu-id="13049-104">The following general use interfaces are supported by the Certificate Enrollment API.</span></span>



| <span data-ttu-id="13049-105">Interface</span><span class="sxs-lookup"><span data-stu-id="13049-105">Interface</span></span>                                                                    | <span data-ttu-id="13049-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="13049-106">Description</span></span>                                                                                                                                                            |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13049-107">**IBinaryConverter**</span><span class="sxs-lookup"><span data-stu-id="13049-107">**IBinaryConverter**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)                                 | <span data-ttu-id="13049-108">Cria uma cadeia de caracteres codificada em Unicode de uma matriz de bytes, cria uma matriz de bytes a partir de uma cadeia de caracteres codificada em Unicode e modifica o tipo de codificação Unicode aplicado a uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="13049-108">Creates a Unicode-encoded string from a byte array, creates a byte array from a Unicode-encoded string, and modifies the type of Unicode encoding applied to a string.</span></span> |
| [<span data-ttu-id="13049-109">**ICertificateAttestationChallenge**</span><span class="sxs-lookup"><span data-stu-id="13049-109">**ICertificateAttestationChallenge**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-icertificateattestationchallenge) | <span data-ttu-id="13049-110">Dá suporte a desafios de atestado de certificado.</span><span class="sxs-lookup"><span data-stu-id="13049-110">Supports certificate attestation challenges.</span></span>                                                                                                                           |
| [<span data-ttu-id="13049-111">**IObjectId**</span><span class="sxs-lookup"><span data-stu-id="13049-111">**IObjectId**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid)                                               | <span data-ttu-id="13049-112">Representa um identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="13049-112">Represents an object identifier.</span></span>                                                                                                                                       |
| [<span data-ttu-id="13049-113">**IObjectIds**</span><span class="sxs-lookup"><span data-stu-id="13049-113">**IObjectIds**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectids)                                             | <span data-ttu-id="13049-114">Gerencia uma coleção de objetos [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) .</span><span class="sxs-lookup"><span data-stu-id="13049-114">Manages a collection of [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) objects.</span></span>                                                                                                        |
| [<span data-ttu-id="13049-115">**IX500DistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="13049-115">**IX500DistinguishedName**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname)                     | <span data-ttu-id="13049-116">Representa um nome diferenciado X. 500.</span><span class="sxs-lookup"><span data-stu-id="13049-116">Represents an X.500 distinguished name.</span></span>                                                                                                                                |
| [<span data-ttu-id="13049-117">**IX509EndorsementKey**</span><span class="sxs-lookup"><span data-stu-id="13049-117">**IX509EndorsementKey**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey)                           | <span data-ttu-id="13049-118">Interface de chave de endosso X. 509</span><span class="sxs-lookup"><span data-stu-id="13049-118">X.509 Endorsement Key Interface</span></span>                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="13049-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="13049-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13049-120">Interfaces CertEnroll</span><span class="sxs-lookup"><span data-stu-id="13049-120">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



