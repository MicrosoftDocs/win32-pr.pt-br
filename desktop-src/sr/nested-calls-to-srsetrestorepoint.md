---
title: Chamadas aninhadas para SRSetRestorePoint
description: Este tópico descreve o suporte para chamadas aninhadas para SRSetRestorePoint por meio dos \_ tipos de evento iniciar alteração do sistema aninhado \_ \_ e encerrar \_ alteração do sistema aninhado \_ \_ .
ms.assetid: ee2dea47-f95d-4293-ac33-eff622b84db6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5654dc7bb6e42ae55cbad18fc2418df3bdd942d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159916"
---
# <a name="nested-calls-to-srsetrestorepoint"></a><span data-ttu-id="50f22-103">Chamadas aninhadas para SRSetRestorePoint</span><span class="sxs-lookup"><span data-stu-id="50f22-103">Nested Calls to SRSetRestorePoint</span></span>

<span data-ttu-id="50f22-104">Este tópico descreve o suporte para chamadas aninhadas para [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) por meio dos \_ tipos de evento iniciar alteração do sistema aninhado \_ \_ e encerrar \_ alteração do sistema aninhado \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="50f22-104">This topic describes support for nested calls to [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) through the BEGIN\_NESTED\_SYSTEM\_CHANGE and END\_NESTED\_SYSTEM\_CHANGE event types.</span></span>

<span data-ttu-id="50f22-105">Os aplicativos podem chamar [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) com segurança ao usar esses tipos de evento.</span><span class="sxs-lookup"><span data-stu-id="50f22-105">Applications can safely call [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) when using these event types.</span></span> <span data-ttu-id="50f22-106">A primeira chamada para a função cria um ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="50f22-106">The first call to the function creates a restore point.</span></span> <span data-ttu-id="50f22-107">As chamadas aninhadas subsequentes para a função não criam pontos de restauração.</span><span class="sxs-lookup"><span data-stu-id="50f22-107">Subsequent nested calls to the function do not create restore points.</span></span> <span data-ttu-id="50f22-108">Por exemplo, suponha que um aplicativo faça as seguintes chamadas para **SRSetRestorePoint**:</span><span class="sxs-lookup"><span data-stu-id="50f22-108">For example, suppose an application makes the following calls to **SRSetRestorePoint**:</span></span><dl> <span data-ttu-id="50f22-109">Para o ponto de restauração A com dwEventType = iniciar \_ alteração do sistema aninhado \_ \_</span><span class="sxs-lookup"><span data-stu-id="50f22-109">For restore point A with dwEventType = BEGIN\_NESTED\_SYSTEM\_CHANGE</span></span>  
<span data-ttu-id="50f22-110">Para o ponto de restauração B com dwEventType = iniciar \_ alteração do sistema aninhado \_ \_</span><span class="sxs-lookup"><span data-stu-id="50f22-110">For restore point B with dwEventType = BEGIN\_NESTED\_SYSTEM\_CHANGE</span></span>  
<span data-ttu-id="50f22-111">Para o ponto de restauração B com dwEventType = encerrar \_ alteração do sistema aninhado \_ \_</span><span class="sxs-lookup"><span data-stu-id="50f22-111">For restore point B with dwEventType = END\_NESTED\_SYSTEM\_CHANGE</span></span>  
<span data-ttu-id="50f22-112">Para o ponto de restauração A com dwEventType = encerrar \_ alteração do sistema aninhado \_ \_</span><span class="sxs-lookup"><span data-stu-id="50f22-112">For restore point A with dwEventType = END\_NESTED\_SYSTEM\_CHANGE</span></span>  
</dl>

<span data-ttu-id="50f22-113">A segunda chamada não cria um novo ponto de restauração porque a chamada está aninhada.</span><span class="sxs-lookup"><span data-stu-id="50f22-113">The second call does not create a new restore point because the call is nested.</span></span>

 

 




