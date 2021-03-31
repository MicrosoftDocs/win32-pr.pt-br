---
title: Adicionando drivers dentro de um aplicativo
description: Adicionando drivers dentro de um aplicativo
ms.assetid: cd9bd0a8-652b-440b-a197-81e20a9d71f1
keywords:
- Gerenciador de compactação de áudio (ACM), adicionando drivers
- ACM (Gerenciador de compactação de áudio), adicionando drivers
- Exemplos do ACM, adicionando drivers
- adicionando drivers
- função acmDriverAdd
- drivers globais
- drivers locais
- Gerenciador de compactação de áudio (ACM), drivers globais
- ACM (Gerenciador de compactação de áudio), drivers globais
- Gerenciador de compactação de áudio (ACM), drivers locais
- ACM (Gerenciador de compactação de áudio), drivers locais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000bf7bded89b778f271599d5ce0f8d7f7bd5f72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005534"
---
# <a name="adding-drivers-within-an-application"></a><span data-ttu-id="4ee1d-114">Adicionando drivers dentro de um aplicativo</span><span class="sxs-lookup"><span data-stu-id="4ee1d-114">Adding Drivers Within an Application</span></span>

<span data-ttu-id="4ee1d-115">Se você precisar que seu aplicativo implemente suas próprias rotinas de compactação internamente, o aplicativo poderá adicionar drivers ao ACM chamando a função [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) .</span><span class="sxs-lookup"><span data-stu-id="4ee1d-115">If you need your application to implement its own compression routines internally, the application can add drivers to the ACM by calling the [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) function.</span></span> <span data-ttu-id="4ee1d-116">O aplicativo implementa o driver fornecendo uma função que está de acordo com o protótipo do [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc) .</span><span class="sxs-lookup"><span data-stu-id="4ee1d-116">The application implements the driver by providing a function that conforms to the [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc) prototype.</span></span> <span data-ttu-id="4ee1d-117">Depois que o aplicativo tiver adicionado o driver, o aplicativo poderá usar o driver por meio do ACM, pois ele usaria qualquer outro driver.</span><span class="sxs-lookup"><span data-stu-id="4ee1d-117">After the application has added the driver, the application can use the driver through the ACM as it would use any other driver.</span></span>

<span data-ttu-id="4ee1d-118">O ACM trata os drivers como global ou local.</span><span class="sxs-lookup"><span data-stu-id="4ee1d-118">The ACM treats drivers as either global or local.</span></span> <span data-ttu-id="4ee1d-119">Um aplicativo especifica se um driver deve ser adicionado como global ou local quando chama **acmDriverAdd**.</span><span class="sxs-lookup"><span data-stu-id="4ee1d-119">An application specifies whether a driver should be added as global or local when it calls **acmDriverAdd**.</span></span> <span data-ttu-id="4ee1d-120">Há duas diferenças entre os drivers globais e locais:</span><span class="sxs-lookup"><span data-stu-id="4ee1d-120">There are two differences between global and local drivers:</span></span>

-   <span data-ttu-id="4ee1d-121">Drivers adicionados como drivers globais não são compartilhados com outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="4ee1d-121">Drivers added as global drivers are not shared with other applications.</span></span>
-   <span data-ttu-id="4ee1d-122">Um aplicativo pode alterar diretamente a prioridade de um driver global (mas não de um driver local) chamando a função [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority) .</span><span class="sxs-lookup"><span data-stu-id="4ee1d-122">An application can directly alter the priority of a global driver (but not a local driver) by calling the [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority) function.</span></span> <span data-ttu-id="4ee1d-123">O ACM realiza uma pesquisa priorizada ao procurar um driver apropriado para fornecer uma implementação de uma chamada de função.</span><span class="sxs-lookup"><span data-stu-id="4ee1d-123">The ACM conducts a prioritized search when seeking an appropriate driver to provide an implementation of a function call.</span></span> <span data-ttu-id="4ee1d-124">O ACM sempre fornece aos drivers locais prioridade mais alta do que os drivers globais.</span><span class="sxs-lookup"><span data-stu-id="4ee1d-124">The ACM always gives local drivers higher priority than global drivers.</span></span> <span data-ttu-id="4ee1d-125">O driver local adicionado mais recentemente tem a prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="4ee1d-125">The most recently added local driver has highest priority.</span></span>

 

 




