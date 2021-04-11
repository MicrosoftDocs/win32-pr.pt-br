---
description: As interfaces a seguir podem ser usadas para recuperar informações sobre provedores criptográficos.
ms.assetid: f4f6a763-707d-48a2-acb9-2a0c3530cf6b
title: Interfaces de provedor criptográfico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1fa42a9a2704849552fadeb79933d85df9e9f78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090740"
---
# <a name="cryptographic-provider-interfaces"></a><span data-ttu-id="2daa4-103">Interfaces de provedor criptográfico</span><span class="sxs-lookup"><span data-stu-id="2daa4-103">Cryptographic Provider Interfaces</span></span>

<span data-ttu-id="2daa4-104">As interfaces a seguir podem ser usadas para recuperar informações sobre provedores criptográficos.</span><span class="sxs-lookup"><span data-stu-id="2daa4-104">The following interfaces can be used to retrieve information about cryptographic providers.</span></span>



| <span data-ttu-id="2daa4-105">Interface</span><span class="sxs-lookup"><span data-stu-id="2daa4-105">Interface</span></span>                                    | <span data-ttu-id="2daa4-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="2daa4-106">Description</span></span>                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="2daa4-107">**ICspAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="2daa4-107">**ICspAlgorithm**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm)       | <span data-ttu-id="2daa4-108">Representa um algoritmo implementado por um provedor criptográfico.</span><span class="sxs-lookup"><span data-stu-id="2daa4-108">Represents an algorithm implemented by a cryptographic provider.</span></span>             |
| [<span data-ttu-id="2daa4-109">**ICspAlgorithms**</span><span class="sxs-lookup"><span data-stu-id="2daa4-109">**ICspAlgorithms**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithms)     | <span data-ttu-id="2daa4-110">Gerencia uma coleção de objetos [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) .</span><span class="sxs-lookup"><span data-stu-id="2daa4-110">Manages a collection of [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) objects.</span></span> |
| [<span data-ttu-id="2daa4-111">**ICspInformation**</span><span class="sxs-lookup"><span data-stu-id="2daa4-111">**ICspInformation**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)   | <span data-ttu-id="2daa4-112">Fornece acesso a informações gerais sobre um provedor criptográfico.</span><span class="sxs-lookup"><span data-stu-id="2daa4-112">Provides access to general information about a cryptographic provider.</span></span>       |
| [<span data-ttu-id="2daa4-113">**ICspInformations**</span><span class="sxs-lookup"><span data-stu-id="2daa4-113">**ICspInformations**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) | <span data-ttu-id="2daa4-114">Gerencia uma coleção de objetos [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) .</span><span class="sxs-lookup"><span data-stu-id="2daa4-114">Manages a collection of [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) objects.</span></span>  |
| [<span data-ttu-id="2daa4-115">**ICspStatus**</span><span class="sxs-lookup"><span data-stu-id="2daa4-115">**ICspStatus**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus)             | <span data-ttu-id="2daa4-116">Contém informações sobre um par provedor/algoritmo criptográfico.</span><span class="sxs-lookup"><span data-stu-id="2daa4-116">Contains information about a cryptographic provider/algorithm pair.</span></span>          |
| [<span data-ttu-id="2daa4-117">**ICspStatuses**</span><span class="sxs-lookup"><span data-stu-id="2daa4-117">**ICspStatuses**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatuses)         | <span data-ttu-id="2daa4-118">Gerencia uma coleção de objetos [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) .</span><span class="sxs-lookup"><span data-stu-id="2daa4-118">Manages a collection of [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) objects.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="2daa4-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2daa4-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2daa4-120">Interfaces CertEnroll</span><span class="sxs-lookup"><span data-stu-id="2daa4-120">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



