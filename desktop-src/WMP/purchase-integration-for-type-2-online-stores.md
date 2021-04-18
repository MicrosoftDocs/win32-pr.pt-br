---
title: Integração de compras para lojas online do tipo 2
description: Integração de compras para lojas online do tipo 2
ms.assetid: aedaa6a0-d559-44b7-9c14-2abf44478b1c
keywords:
- Lojas online do Windows Media Player, integração de compra
- lojas online, integração de compra
- tipo 2 lojas online, integração de compra
- Lojas online do Windows Media Player, integrando compras
- lojas online, integrando compras
- Digite 2 lojas online, integrando compras
- Windows Media Player, integração de compra
- Windows Media Player, integrando compras
- integração de compra
- integrando compras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d8fb56b286b66de12bb59412e7f9077eb398f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105796253"
---
# <a name="purchase-integration-for-type-2-online-stores"></a><span data-ttu-id="77858-113">Integração de compras para lojas online do tipo 2</span><span class="sxs-lookup"><span data-stu-id="77858-113">Purchase Integration for Type 2 Online Stores</span></span>

<span data-ttu-id="77858-114">Quando o Windows Media Player reproduz conteúdo de mídia digital ou o usuário escolhe **localizar informações do álbum**, o Player oferece ao usuário um link para comprar o CD ou DVD do qual o conteúdo se originou, se esse link estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="77858-114">When Windows Media Player plays digital media content or the user chooses **Find Album Info**, the Player offers the user a link to buy the CD or DVD from which the content originated if such a link is available.</span></span> <span data-ttu-id="77858-115">Quando o usuário clica no link, o Windows Media Player 10 ou posterior chama o repositório de música atual para lidar com a solicitação de compra.</span><span class="sxs-lookup"><span data-stu-id="77858-115">When the user clicks the link, Windows Media Player 10 or later calls on the current music store to handle the purchase request.</span></span> <span data-ttu-id="77858-116">Quando isso acontece, o Player navega até o primeiro painel de tarefas de serviço (no Windows Media Player 10) ou a guia lojas online (no Windows Media Player 11) e exibe a página da Web especificada pelo atributo **MediaPlayerURL** do elemento **BuyCD** do documento serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="77858-116">When this happens, the Player navigates to the first service task pane (in Windows Media Player 10) or the Online Stores tab (in Windows Media Player 11) and displays the webpage specified by the **MediaPlayerURL** attribute of the **BuyCD** element of the ServiceInfo document.</span></span> <span data-ttu-id="77858-117">(Os atributos **MediaCenterURL** e **BrowserURL** são usados de maneira semelhante para lidar com chamadas do Windows xp Media Center Edition 2004 e do Windows XP Service Pack 2).</span><span class="sxs-lookup"><span data-stu-id="77858-117">(The **MediaCenterURL** and **BrowserURL** attributes are used in a similar manner to handle calls from Windows XP Media Center Edition 2004 and Windows XP Service Pack 2).</span></span>

<span data-ttu-id="77858-118">O Windows Media Player acrescenta uma cadeia de caracteres de consulta à URL para fornecer informações à loja online sobre o conteúdo que o usuário optou por comprar.</span><span class="sxs-lookup"><span data-stu-id="77858-118">Windows Media Player appends a query string to the URL to provide information to the online store about the content the user chose to purchase.</span></span> <span data-ttu-id="77858-119">A cadeia de caracteres de consulta inclui atributos como **título**, **álbum** e **artista**, que o repositório online pode usar para determinar o álbum correto a ser vendido.</span><span class="sxs-lookup"><span data-stu-id="77858-119">The query string includes attributes like **Title**, **Album**, and **Artist**, which the online store can use to determine the correct album to sell.</span></span> <span data-ttu-id="77858-120">A documentação de referência para o elemento **BuyCD** fornece a lista completa de atributos de cadeia de caracteres de consulta e suas descrições.</span><span class="sxs-lookup"><span data-stu-id="77858-120">The reference documentation for the **BuyCD** element provides the complete list of query string attributes and their descriptions.</span></span>

## <a name="guidelines-for-the-buycd-page"></a><span data-ttu-id="77858-121">Diretrizes para a página BuyCD</span><span class="sxs-lookup"><span data-stu-id="77858-121">Guidelines for the BuyCD Page</span></span>

<span data-ttu-id="77858-122">Ao criar sua página da Web do BuyCD, use as seguintes diretrizes:</span><span class="sxs-lookup"><span data-stu-id="77858-122">When creating your BuyCD webpage, use the following guidelines:</span></span>

-   <span data-ttu-id="77858-123">A página deve identificar claramente a loja online que fornece as informações.</span><span class="sxs-lookup"><span data-stu-id="77858-123">The page must clearly identify the online store providing the information.</span></span> <span data-ttu-id="77858-124">Você pode fazer isso exibindo de forma proeminente seu logotipo, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="77858-124">You can do this by prominently displaying your logo, for example.</span></span>
-   <span data-ttu-id="77858-125">A página deve incluir um link para a política de privacidade da sua empresa.</span><span class="sxs-lookup"><span data-stu-id="77858-125">The page must include a link to your company's privacy statement.</span></span>
-   <span data-ttu-id="77858-126">É melhor fornecer informações de compra inicial sem exigir que o usuário instale programas ou faça logon na sua loja online.</span><span class="sxs-lookup"><span data-stu-id="77858-126">It is best to provide initial purchasing information without requiring the user to install programs or log in to your online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77858-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="77858-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77858-128">**Sobre as lojas online do tipo 2**</span><span class="sxs-lookup"><span data-stu-id="77858-128">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="77858-129">**Elemento BuyCD**</span><span class="sxs-lookup"><span data-stu-id="77858-129">**BuyCD Element**</span></span>](buycd-element.md)
</dt> </dl>

 

 




