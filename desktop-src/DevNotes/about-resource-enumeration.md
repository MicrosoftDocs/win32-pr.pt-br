---
description: A enumeração de recursos fornece uma exibição mais próxima e precisa da atividade de instrumentação que ocorre quando um aplicativo está em execução.
ms.assetid: 4a421006-32ff-4555-a3c8-69fffdb46845
title: Sobre a enumeração de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 601e65550dacbd07d493f35a6c35fece98657b6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811133"
---
# <a name="about-resource-enumeration"></a><span data-ttu-id="4d9c8-103">Sobre a enumeração de recursos</span><span class="sxs-lookup"><span data-stu-id="4d9c8-103">About Resource Enumeration</span></span>

<span data-ttu-id="4d9c8-104">A enumeração de recursos fornece uma exibição mais próxima e precisa da atividade de instrumentação que ocorre quando um aplicativo está em execução.</span><span class="sxs-lookup"><span data-stu-id="4d9c8-104">Resource enumeration provides a close and precise view of instrumentation activity that takes place when an application is running.</span></span> <span data-ttu-id="4d9c8-105">As informações de instrumentação podem ser abstratas e categorizadas como um conjunto de itens específicos do processo como parte do processo de depuração.</span><span class="sxs-lookup"><span data-stu-id="4d9c8-105">The instrumentation information can be abstracted and categorized as a set of process-specific items as part of the debugging process.</span></span>

<span data-ttu-id="4d9c8-106">As ferramentas, como os depuradores, geralmente exigem acesso às informações de instrumentação, mas podem achar que não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4d9c8-106">Tools, such as debuggers, often require access to instrumentation information but may find it is unavailable.</span></span> <span data-ttu-id="4d9c8-107">Para resolver esse problema, a função [**VerifierEnumerateResource**](/windows/desktop/api/Avrfsdk/nf-avrfsdk-verifierenumerateresource) extrai esse tipo de informação de aplicativos para fornecer melhores informações de contexto para o problema que está sendo depurado.</span><span class="sxs-lookup"><span data-stu-id="4d9c8-107">To solve this problem, the [**VerifierEnumerateResource**](/windows/desktop/api/Avrfsdk/nf-avrfsdk-verifierenumerateresource) function extracts this type of information from applications to provide better context information for the problem being debugged.</span></span>

 

 



