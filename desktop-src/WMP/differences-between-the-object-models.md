---
title: Diferenças entre os modelos de objeto
description: Diferenças entre os modelos de objeto
ms.assetid: a6d2a2d5-2892-461a-aa6d-7e11b504b2af
keywords:
- Windows Media Player, modelo de objeto
- Modelo de objeto do Windows Media Player, diferenças de versão
- modelo de objeto, diferenças de versão
- Controle ActiveX do Windows Media Player, diferenças de versão
- Controle ActiveX, diferenças de versão
- Controle ActiveX móvel do Windows Media Player, diferenças de versão
- Windows Media Player Mobile, modelo de objeto
- Guia de migração, diferenças de versão
- versões do Windows Media Player, modelo de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a5341067e2daad0f44fbdd7075f0f543bac2fd4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105759724"
---
# <a name="differences-between-the-object-models"></a><span data-ttu-id="5ef74-112">Diferenças entre os modelos de objeto</span><span class="sxs-lookup"><span data-stu-id="5ef74-112">Differences Between the Object Models</span></span>

<span data-ttu-id="5ef74-113">Há duas diferenças principais entre o modelo de objeto do Windows Media Player 6,4 e o modelo de objeto do Windows Media Player 7 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="5ef74-113">There are two primary differences between the Windows Media Player 6.4 object model and the Windows Media Player 7 or later object model.</span></span>

-   <span data-ttu-id="5ef74-114">**CLSID** do O modelo de objeto do Windows Media Player 7 ou posterior é uma partida completa do modelo de objeto da versão 6,4.</span><span class="sxs-lookup"><span data-stu-id="5ef74-114">**CLSID** The Windows Media Player 7 or later object model is a complete departure from the version 6.4 object model.</span></span> <span data-ttu-id="5ef74-115">A especificação de Component Object Model (COM) requer que todas as interfaces existentes continuem a funcionar em novas versões de um componente COM.</span><span class="sxs-lookup"><span data-stu-id="5ef74-115">The Component Object Model (COM) specification requires that all existing interfaces must continue to function in new versions of a COM component.</span></span> <span data-ttu-id="5ef74-116">Isso significa que novas interfaces podem ser adicionadas a um componente COM, mas as interfaces existentes nunca devem ser alteradas, garantindo que o código do cliente mais antigo sempre funcione com o componente específico que ele foi projetado para usar.</span><span class="sxs-lookup"><span data-stu-id="5ef74-116">This means that new interfaces can be added to a COM component, but existing interfaces must never be altered, ensuring older client code will always work with the particular component it was designed to use.</span></span> <span data-ttu-id="5ef74-117">Portanto, o controle ActiveX do Windows Media Player 7 ou posterior tem uma nova ID de classe: 6BF52A52-394A-11D3-B153-00C04F79FAA6.</span><span class="sxs-lookup"><span data-stu-id="5ef74-117">Therefore, the Windows Media Player 7 or later ActiveX control has a new class ID: 6BF52A52-394A-11D3-B153-00C04F79FAA6.</span></span> <span data-ttu-id="5ef74-118">Se você quiser aproveitar a nova funcionalidade do controle para esta versão, você deve alterar seu CLSID.</span><span class="sxs-lookup"><span data-stu-id="5ef74-118">If you want to take advantage of the new functionality of the control for this version, you must change your CLSID.</span></span>
-   <span data-ttu-id="5ef74-119">**Modelo de objeto hierárquico** Se você estiver usando o controle ActiveX do Windows Media Player 6,4, talvez tenha notado que todas as propriedades, métodos e eventos são acessados por meio do mesmo objeto: o objeto **Player** .</span><span class="sxs-lookup"><span data-stu-id="5ef74-119">**Hierarchical Object Model** If you've been using the Windows Media Player 6.4 ActiveX control, you may have noticed that all the properties, methods, and events are accessed through the same object: the **Player** object.</span></span> <span data-ttu-id="5ef74-120">Por outro lado, o modelo de objeto do Windows Media Player 7 ou posterior é organizado como uma hierarquia de objetos.</span><span class="sxs-lookup"><span data-stu-id="5ef74-120">By contrast, the Windows Media Player 7 or later object model is organized as a hierarchy of objects.</span></span> <span data-ttu-id="5ef74-121">O objeto **Player** ainda é o objeto raiz, mas as funções agora são acessadas por meio de uma variedade de objetos filho.</span><span class="sxs-lookup"><span data-stu-id="5ef74-121">The **Player** object is still the root object, but functions are now accessed through a variety of child objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ef74-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5ef74-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ef74-123">**Guia de migração do modelo de objeto**</span><span class="sxs-lookup"><span data-stu-id="5ef74-123">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




