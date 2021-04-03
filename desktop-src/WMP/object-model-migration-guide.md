---
title: Guia de migração do modelo de objeto
description: Guia de migração do modelo de objeto
ms.assetid: 2fd4f7ec-36b0-49da-9a11-546dd41c7a98
keywords:
- Windows Media Player, modelo de objeto
- Windows Media Player, guia de migração
- Modelo de objeto do Windows Media Player, guia de migração
- modelo de objeto, guia de migração
- Controle ActiveX do Windows Media Player, guia de migração
- Controle ActiveX, guia de migração
- Controle ActiveX móvel do Windows Media Player, guia de migração
- Windows Media Player Mobile, modelo de objeto
- Windows Media Player Mobile, guia de migração
- Guia de migração, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29c9be40e3cc252ed9461bcb18ea5bfed49bb58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005946"
---
# <a name="object-model-migration-guide"></a><span data-ttu-id="7dc3e-113">Guia de migração do modelo de objeto</span><span class="sxs-lookup"><span data-stu-id="7dc3e-113">Object Model Migration Guide</span></span>

<span data-ttu-id="7dc3e-114">O Windows Media Player 7 introduziu um novo modelo de objeto que oferece um novo conjunto avançado de funcionalidades que você pode usar para aprimorar suas páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="7dc3e-114">Windows Media Player 7 introduced a new object model that offers a rich new set of functionality that you can use to enhance your webpages.</span></span> <span data-ttu-id="7dc3e-115">As versões subsequentes estenderam o modelo de objeto versão 7 com propriedades, métodos e eventos adicionais.</span><span class="sxs-lookup"><span data-stu-id="7dc3e-115">Subsequent versions have extended the version 7 object model with additional properties, methods, and events.</span></span> <span data-ttu-id="7dc3e-116">No entanto, o novo modelo de objeto difere substancialmente do modelo de objeto do Windows Media Player 6,4, portanto, você precisa entender como atualizar seu código existente se desejar oferecer suporte ao Windows Media Player 7 e posterior em seus projetos.</span><span class="sxs-lookup"><span data-stu-id="7dc3e-116">However, the new object model differs substantially from the Windows Media Player 6.4 object model, so you need to understand how to update your existing code if you want to support Windows Media Player 7 and later in your projects.</span></span>

<span data-ttu-id="7dc3e-117">Para obter um exemplo que demonstra como detectar a versão do Windows Media Player e o navegador atual do usuário, consulte o exemplo chamado "detecção" instalado com este SDK.</span><span class="sxs-lookup"><span data-stu-id="7dc3e-117">For a sample that demonstrates how to detect the user's Windows Media Player version and current browser, see the sample named "detection" that is installed with this SDK.</span></span> <span data-ttu-id="7dc3e-118">Para obter mais informações sobre exemplos, consulte [exemplos](samples.md).</span><span class="sxs-lookup"><span data-stu-id="7dc3e-118">For more information about samples, see [Samples](samples.md).</span></span>

<span data-ttu-id="7dc3e-119">Este guia refere-se ao novo modelo de objeto como o modelo de objeto do Windows Media Player 7 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="7dc3e-119">This guide refers to the new object model as the Windows Media Player 7 or later object model.</span></span> <span data-ttu-id="7dc3e-120">Para obter detalhes sobre qual funcionalidade está disponível em cada versão do Windows Media Player, consulte [referência de modelo de objeto para scripts](object-model-reference-for-scripting.md).</span><span class="sxs-lookup"><span data-stu-id="7dc3e-120">For details about which functionality is available in each version of Windows Media Player, see [Object Model Reference for Scripting](object-model-reference-for-scripting.md).</span></span>

<span data-ttu-id="7dc3e-121">Esses problemas de modelo de objeto são cobertos pelos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="7dc3e-121">These object model issues are covered by the following topics:</span></span>

-   [<span data-ttu-id="7dc3e-122">Diferenças entre os modelos de objeto</span><span class="sxs-lookup"><span data-stu-id="7dc3e-122">Differences Between the Object Models</span></span>](differences-between-the-object-models.md)
-   [<span data-ttu-id="7dc3e-123">Usando o modelo de objeto do Windows Media Player 7 ou posterior</span><span class="sxs-lookup"><span data-stu-id="7dc3e-123">Using the Windows Media Player 7 or Later Object Model</span></span>](using-the-windows-media-player-7-or-later-object-model.md)
-   [<span data-ttu-id="7dc3e-124">Tratamento de erro</span><span class="sxs-lookup"><span data-stu-id="7dc3e-124">Error Handling</span></span>](error-handling.md)
-   [<span data-ttu-id="7dc3e-125">Playlists</span><span class="sxs-lookup"><span data-stu-id="7dc3e-125">Playlists</span></span>](playlists.md)
-   [<span data-ttu-id="7dc3e-126">Legendagem oculta</span><span class="sxs-lookup"><span data-stu-id="7dc3e-126">Closed Captioning</span></span>](closed-captioning.md)
-   [<span data-ttu-id="7dc3e-127">DVD</span><span class="sxs-lookup"><span data-stu-id="7dc3e-127">DVD</span></span>](dvd.md)
-   [<span data-ttu-id="7dc3e-128">Comparação de modelo de objeto detalhado</span><span class="sxs-lookup"><span data-stu-id="7dc3e-128">Detailed Object Model Comparison</span></span>](detailed-object-model-comparison.md)

## <a name="related-topics"></a><span data-ttu-id="7dc3e-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7dc3e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dc3e-130">**Guia de controle do Player**</span><span class="sxs-lookup"><span data-stu-id="7dc3e-130">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




