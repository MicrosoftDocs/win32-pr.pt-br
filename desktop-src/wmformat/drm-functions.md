---
title: Funções do Microsoft Windows Media DRM Client
description: Funções do Microsoft Windows Media DRM Client
ms.assetid: 5d726c56-d0f3-4eb8-829f-3a0c1a0e0802
keywords:
- SDK do Windows Media Format, funções
- DRM (gerenciamento de direitos digitais), funções
- DRM (gerenciamento de direitos digitais), funções
- APIs estendidas do cliente DRM, funções
- APIs estendidas do cliente, funções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c1730413a4918b0f748099fbd55714339a7e9b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105782386"
---
# <a name="microsoft-windows-media-drm-client-functions"></a><span data-ttu-id="9c67e-108">Funções do Microsoft Windows Media DRM Client</span><span class="sxs-lookup"><span data-stu-id="9c67e-108">Microsoft Windows Media DRM Client Functions</span></span>

<span data-ttu-id="9c67e-109">As funções a seguir são implementadas como parte das APIs estendidas do Microsoft Windows Media DRM Client.</span><span class="sxs-lookup"><span data-stu-id="9c67e-109">The following functions are implemented as part of the Microsoft Windows Media DRM Client Extended APIs.</span></span>



| <span data-ttu-id="9c67e-110">Função</span><span class="sxs-lookup"><span data-stu-id="9c67e-110">Function</span></span>                                                             | <span data-ttu-id="9c67e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="9c67e-111">Description</span></span>                                                                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c67e-112">**WMDRMCreateProvider**</span><span class="sxs-lookup"><span data-stu-id="9c67e-112">**WMDRMCreateProvider**</span></span>](wmdrmcreateprovider.md)                   | <span data-ttu-id="9c67e-113">Cria uma fábrica de classes que pode criar outros objetos DRM.</span><span class="sxs-lookup"><span data-stu-id="9c67e-113">Creates a class factory that can create the other DRM objects.</span></span> <span data-ttu-id="9c67e-114">Essa função não requer uma biblioteca de stub da Microsoft e cria objetos que não dão suporte aos recursos protegidos do DRM.</span><span class="sxs-lookup"><span data-stu-id="9c67e-114">This function does not require a stub library from Microsoft and creates objects that do not support the protected DRM features.</span></span> |
| [<span data-ttu-id="9c67e-115">**WMDRMCreateProtectedProvider**</span><span class="sxs-lookup"><span data-stu-id="9c67e-115">**WMDRMCreateProtectedProvider**</span></span>](wmdrmcreateprotectedprovider.md) | <span data-ttu-id="9c67e-116">Cria uma fábrica de classes que pode criar outros objetos DRM.</span><span class="sxs-lookup"><span data-stu-id="9c67e-116">Creates a class factory that can create the other DRM objects.</span></span> <span data-ttu-id="9c67e-117">Essa função requer uma biblioteca de stub da Microsoft e cria objetos que dão suporte aos recursos protegidos do DRM.</span><span class="sxs-lookup"><span data-stu-id="9c67e-117">This function requires a stub library from Microsoft and creates objects that support the protected DRM features.</span></span>                |
| [<span data-ttu-id="9c67e-118">**WMDRMShutdown**</span><span class="sxs-lookup"><span data-stu-id="9c67e-118">**WMDRMShutdown**</span></span>](wmdrmshutdown.md)                               | <span data-ttu-id="9c67e-119">Libera recursos usados pelas APIs.</span><span class="sxs-lookup"><span data-stu-id="9c67e-119">Releases resources used by the APIs.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="9c67e-120">**WMDRMStartup**</span><span class="sxs-lookup"><span data-stu-id="9c67e-120">**WMDRMStartup**</span></span>](wmdrmstartup.md)                                 | <span data-ttu-id="9c67e-121">Inicializa os recursos usados pelas APIs.</span><span class="sxs-lookup"><span data-stu-id="9c67e-121">Initializes resources used by the APIs.</span></span>                                                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="9c67e-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9c67e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c67e-123">**Referência de programação**</span><span class="sxs-lookup"><span data-stu-id="9c67e-123">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




