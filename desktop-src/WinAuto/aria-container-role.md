---
title: Erro de função de contêiner do ARIA
description: Erro de função de contêiner do ARIA
ms.assetid: AF207293-1172-43D0-B92C-C3070876DF54
keywords:
- AriaContainerRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02554c868816c05981fa9f008c8f79f0a3eb0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916580"
---
# <a name="aria-container-role-error"></a><span data-ttu-id="cf25f-104">Erro de função de contêiner do ARIA</span><span class="sxs-lookup"><span data-stu-id="cf25f-104">ARIA Container Role Error</span></span>

## <a name="text"></a><span data-ttu-id="cf25f-105">Texto</span><span class="sxs-lookup"><span data-stu-id="cf25f-105">Text</span></span>

<span data-ttu-id="cf25f-106">O elemento com o **descendente** definido como ativo não tem uma função de contêiner (**ComboBox**, **Grid**, **ListBox**, **menu**, **MenuBar** **, Radiogroup,** **Tree**, **árvore**, **tablist**, **Row**).</span><span class="sxs-lookup"><span data-stu-id="cf25f-106">Element with **active-descendant** defined does not have a container role (**combobox**, **grid**, **listbox**, **menu**, **menubar**, **radiogroup**, **tree**, **treegrid**, **tablist**, **row**).</span></span>

## <a name="type"></a><span data-ttu-id="cf25f-107">Type</span><span class="sxs-lookup"><span data-stu-id="cf25f-107">Type</span></span>

<span data-ttu-id="cf25f-108">Erro</span><span class="sxs-lookup"><span data-stu-id="cf25f-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="cf25f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf25f-109">Description</span></span>

<span data-ttu-id="cf25f-110">Esse erro se aplica a elementos que têm o atributo **Aria-activedescendant** .</span><span class="sxs-lookup"><span data-stu-id="cf25f-110">This error applies to elements that have the **aria-activedescendant** attribute.</span></span>

<span data-ttu-id="cf25f-111">Um elemento parece ser um contêiner que tem o atributo **Aria-activedescendant** definido, mas o atributo de função do elemento não tem um valor válido para um contêiner.</span><span class="sxs-lookup"><span data-stu-id="cf25f-111">An element appears to be a container that has the **aria-activedescendant** attribute set, but the element's role attribute doesn’t have a value that is valid for a container.</span></span>

<span data-ttu-id="cf25f-112">Para corrigir esse erro, defina o atributo **role** como um valor de função Rich Internet Applications (WAI-ARIA) acessível para iniciativa de acessibilidade da Web que seja válido para um elemento de contêiner: **ComboBox**, **Grid**, **ListBox**, **menu**, **BarraDeMenu**, **radioobject**, **tablist**, **Tree** ou **árvore**.</span><span class="sxs-lookup"><span data-stu-id="cf25f-112">To fix this error, set the **role** attribute to a Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) role value that is valid for a container element: **combobox**, **grid**, **listbox**, **menu**, **menubar**, **radiogroup**, **tablist**, **tree**, or **treegrid**.</span></span>

## <a name="example"></a><span data-ttu-id="cf25f-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="cf25f-113">Example</span></span>


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1">
  <div role="option" id="listbox1-1" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
  ...
<div>
```



## <a name="related-topics"></a><span data-ttu-id="cf25f-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cf25f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf25f-115">Erro de função do ARIA</span><span class="sxs-lookup"><span data-stu-id="cf25f-115">ARIA Role Error</span></span>](aria-role-invalid.md)
</dt> </dl>

 

 




