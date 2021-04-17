---
title: Integrando o recurso de exibição do centro de informações
description: Integrando o recurso de exibição do centro de informações
ms.assetid: ce6692d2-a780-4aab-809f-c63236edd912
keywords:
- Lojas online do Windows Media Player, integrando o modo de exibição do centro de informações
- lojas online, integração da exibição do centro de informações
- Digite 1 lojas online, integração da exibição do centro de informações
- Digite 2 lojas online, integrando a exibição do centro de informações
- Lojas online do Windows Media Player, exibição do centro de informações
- lojas online, exibição do centro de informações
- tipo 1 lojas online, exibição do centro de informações
- tipo 2 lojas online, exibição do centro de informações
- integração da exibição do centro de informações
- Exibição do centro de informações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9564a6210181e0500bd1e447f621568f634817c4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761442"
---
# <a name="integrating-the-info-center-view-feature"></a><span data-ttu-id="afab4-113">Integrando o recurso de exibição do centro de informações</span><span class="sxs-lookup"><span data-stu-id="afab4-113">Integrating the Info Center View Feature</span></span>

<span data-ttu-id="afab4-114">O Windows Media Player permite que os usuários abram e fechem o recurso de exibição do centro de informações.</span><span class="sxs-lookup"><span data-stu-id="afab4-114">Windows Media Player enables users to open and close the Info Center View feature.</span></span> <span data-ttu-id="afab4-115">A exibição do centro de informações é o recurso em que os usuários esperam encontrar informações avançadas e estendidas sobre o conteúdo específico de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="afab4-115">Info Center View is the feature where users expect to find rich, extended information about specific digital media content.</span></span> <span data-ttu-id="afab4-116">Quando o usuário opta por abrir a exibição do centro de informações, o Windows Media Player chama o repositório de músicas atual para exibir a página da Web de exibição do info Center especificada pelo atributo **URL** do elemento **InfoCenter** do documento serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="afab4-116">When the user chooses to open Info Center View, Windows Media Player calls on the current music store to display the Info Center View webpage specified by the **URL** attribute of the **InfoCenter** element of the ServiceInfo document.</span></span>

<span data-ttu-id="afab4-117">Para recuperar informações sobre o conteúdo de mídia digital em execução no momento, você deve inserir uma instância do controle do Windows Media Player em sua página da Web e usar o modelo de objeto do Player.</span><span class="sxs-lookup"><span data-stu-id="afab4-117">To retrieve information about the currently playing digital media content, you must embed an instance of the Windows Media Player control in your webpage and use the Player object model.</span></span> <span data-ttu-id="afab4-118">Por exemplo, para recuperar o título, você pode usar o seguinte código JScript:</span><span class="sxs-lookup"><span data-stu-id="afab4-118">For example, to retrieve the title, you could use the following JScript code:</span></span>


```C++
// The control was created with ID = "Player"
var title = Player.currentMedia.getItemInfoByType("Title", "", 0);
```



## <a name="guidelines-for-info-center-view"></a><span data-ttu-id="afab4-119">Diretrizes para a exibição do centro de informações</span><span class="sxs-lookup"><span data-stu-id="afab4-119">Guidelines for Info Center View</span></span>

<span data-ttu-id="afab4-120">Ao criar sua página da Web de **exibição do info Center** , use as seguintes diretrizes:</span><span class="sxs-lookup"><span data-stu-id="afab4-120">When creating your **Info Center View** webpage, use the following guidelines:</span></span>

-   <span data-ttu-id="afab4-121">A página deve identificar claramente a loja online que fornece as informações.</span><span class="sxs-lookup"><span data-stu-id="afab4-121">The page must clearly identify the online store providing the information.</span></span> <span data-ttu-id="afab4-122">Você pode fazer isso exibindo de forma proeminente seu logotipo, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="afab4-122">You can do this by prominently displaying your logo, for example.</span></span>
-   <span data-ttu-id="afab4-123">A página deve incluir um link para a política de privacidade da sua empresa.</span><span class="sxs-lookup"><span data-stu-id="afab4-123">The page must include a link to your company's privacy statement.</span></span>
-   <span data-ttu-id="afab4-124">Evite navegação de página dentro do recurso de exibição do info Center sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="afab4-124">Avoid page navigation within the Info Center View feature whenever possible.</span></span> <span data-ttu-id="afab4-125">Você deve navegar até sua loja online para a maioria das atividades.</span><span class="sxs-lookup"><span data-stu-id="afab4-125">You should navigate to your online store for most activities.</span></span>
-   <span data-ttu-id="afab4-126">É melhor fornecer informações valiosas sem exigir que o usuário instale programas ou faça logon na sua loja online.</span><span class="sxs-lookup"><span data-stu-id="afab4-126">It is best to provide valuable information without requiring the user to install programs or log in to your online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="afab4-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="afab4-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afab4-128">**External. NavigateTaskPaneURL**</span><span class="sxs-lookup"><span data-stu-id="afab4-128">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> <dt>

[<span data-ttu-id="afab4-129">**Elemento do InfoCenter**</span><span class="sxs-lookup"><span data-stu-id="afab4-129">**InfoCenter Element**</span></span>](infocenter-element.md)
</dt> <dt>

[<span data-ttu-id="afab4-130">**Informações comuns às lojas online tipo 1 e tipo 2**</span><span class="sxs-lookup"><span data-stu-id="afab4-130">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="afab4-131">**Usando o controle do Windows Media Player em uma página da Web**</span><span class="sxs-lookup"><span data-stu-id="afab4-131">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




