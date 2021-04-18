---
title: Erro de função do ARIA
description: Erro de função do ARIA
ms.assetid: FEEB4F28-4A71-4417-A2F9-ABCB86B44F0F
keywords:
- AriaRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df04ad94d68ae1e8e2e8d3352aa349834a2389fa
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "105760430"
---
# <a name="aria-role-error"></a><span data-ttu-id="3bc2a-104">Erro de função do ARIA</span><span class="sxs-lookup"><span data-stu-id="3bc2a-104">ARIA Role Error</span></span>

## <a name="text"></a><span data-ttu-id="3bc2a-105">Texto</span><span class="sxs-lookup"><span data-stu-id="3bc2a-105">Text</span></span>

<span data-ttu-id="3bc2a-106">O elemento tem uma função WAI-ARIA inválida.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-106">Element has invalid WAI-ARIA role.</span></span>

## <a name="type"></a><span data-ttu-id="3bc2a-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="3bc2a-107">Type</span></span>

<span data-ttu-id="3bc2a-108">Erro</span><span class="sxs-lookup"><span data-stu-id="3bc2a-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="3bc2a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="3bc2a-109">Description</span></span>

<span data-ttu-id="3bc2a-110">Esse erro se aplica a todos os elementos que têm o atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) .</span><span class="sxs-lookup"><span data-stu-id="3bc2a-110">This error applies to all elements that have the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute.</span></span> <span data-ttu-id="3bc2a-111">Ele indica que o atributo de **função** não é um valor de função de Wai (aplicativos de Internet avançado) acessível para iniciativa de acessibilidade da Web, conforme definido pela especificação WAI-ARIA.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-111">It indicates that the **role** attribute is not a valid Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) role value as defined by the WAI-ARIA specification.</span></span> <span data-ttu-id="3bc2a-112">Definir uma função válida ajuda a garantir que o elemento seja interpretado corretamente por leitores de tela e por outras ferramentas de tecnologia assistencial.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-112">Setting a valid role helps ensure that the element is correctly interpreted by screen readers and other assistive technology tools.</span></span>

<span data-ttu-id="3bc2a-113">Para corrigir esse erro, defina o atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) como um valor de função WAI-ARIA válido.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-113">To fix this error, set the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute to a valid WAI-ARIA role value.</span></span> <span data-ttu-id="3bc2a-114">Observe que as funções abstratas WAI-ARIA não são válidas.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-114">Note that abstract WAI-ARIA roles are not valid.</span></span>

## <a name="example"></a><span data-ttu-id="3bc2a-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3bc2a-115">Example</span></span>


```HTML
<!—The invalid role will not expose this element as a button. -->
<div role="backbutton" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >

<!—Setting the correct role will expose this as a button that can be clicked. -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



## <a name="related-topics"></a><span data-ttu-id="3bc2a-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3bc2a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bc2a-117">Erro de função de contêiner do ARIA</span><span class="sxs-lookup"><span data-stu-id="3bc2a-117">ARIA Container Role Error</span></span>](aria-container-role.md)
</dt> </dl>

 

 




