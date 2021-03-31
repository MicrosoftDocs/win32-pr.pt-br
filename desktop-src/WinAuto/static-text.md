---
title: Texto estático (referência de elemento de interface do usuário do MSAA)
description: Os controles de texto estáticos fornecem uma maneira conveniente de exibir texto em caixas de diálogo e outras janelas. Controles de texto estáticos geralmente servem como rótulos para outros controles.
ms.assetid: 2c4b29bc-54e6-4c96-93a3-1fcb96d68269
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f35581a9b305f28782d8faeac81105afb0d5147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822989"
---
# <a name="static-text-msaa-ui-element-reference"></a><span data-ttu-id="f0315-104">Texto estático (referência de elemento de interface do usuário do MSAA)</span><span class="sxs-lookup"><span data-stu-id="f0315-104">Static Text (MSAA UI Element Reference)</span></span>

<span data-ttu-id="f0315-105">Os controles de texto estáticos fornecem uma maneira conveniente de exibir texto em caixas de diálogo e outras janelas.</span><span class="sxs-lookup"><span data-stu-id="f0315-105">Static text controls provide a convenient way to display text on dialog boxes and other windows.</span></span> <span data-ttu-id="f0315-106">Controles de texto estáticos geralmente servem como rótulos para outros controles.</span><span class="sxs-lookup"><span data-stu-id="f0315-106">Static text controls often serve as labels for other controls.</span></span>

<span data-ttu-id="f0315-107">O nome de classe da janela para um controle de texto estático é "estático".</span><span class="sxs-lookup"><span data-stu-id="f0315-107">The window class name for a static text control is "STATIC".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="f0315-108">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="f0315-108">IAccessible Methods</span></span>

<span data-ttu-id="f0315-109">Os controles de texto estáticos dão suporte aos seguintes métodos de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="f0315-109">Static text controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="f0315-110">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="f0315-110">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="f0315-111">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="f0315-111">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="f0315-112">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="f0315-112">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="f0315-113">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="f0315-113">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="f0315-114">Propriedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="f0315-114">IAccessible Properties</span></span>

<span data-ttu-id="f0315-115">Os controles de texto estáticos dão suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="f0315-115">Static text controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="f0315-116">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f0315-116">Property</span></span>                                                                             | <span data-ttu-id="f0315-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0315-117">Comments</span></span>                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0315-118">**obter \_ accChild**</span><span class="sxs-lookup"><span data-stu-id="f0315-118">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="f0315-119">**obter \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="f0315-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | <span data-ttu-id="f0315-120">A propriedade **ChildCount** é zero.</span><span class="sxs-lookup"><span data-stu-id="f0315-120">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="f0315-121">**obter \_ accDescription**</span><span class="sxs-lookup"><span data-stu-id="f0315-121">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="f0315-122">**obter \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="f0315-122">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="f0315-123">**obter \_ accHelp**</span><span class="sxs-lookup"><span data-stu-id="f0315-123">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="f0315-124">**obter \_ accHelpTopic**</span><span class="sxs-lookup"><span data-stu-id="f0315-124">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="f0315-125">**obter \_ accKeyboardShortcut**</span><span class="sxs-lookup"><span data-stu-id="f0315-125">**get\_accKeyboardShortcut**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | <span data-ttu-id="f0315-126">A propriedade **KeyboardShortcut** é a chave de acesso, que é o caractere sublinhado no texto que ativa o controle associado ao texto estático.</span><span class="sxs-lookup"><span data-stu-id="f0315-126">The **KeyboardShortcut** property is the access key, which is the underlined character in the text that activates the control associated with the static text.</span></span> <span data-ttu-id="f0315-127">A cadeia de caracteres retornada contém o caractere de chave de acesso anexado à cadeia de caracteres "Alt +".</span><span class="sxs-lookup"><span data-stu-id="f0315-127">The returned string contains the access key character appended to the string "Alt+".</span></span>                                           |
| [<span data-ttu-id="f0315-128">**obter \_ accName**</span><span class="sxs-lookup"><span data-stu-id="f0315-128">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | <span data-ttu-id="f0315-129">A propriedade **Name** é igual ao texto no controle de texto estático.</span><span class="sxs-lookup"><span data-stu-id="f0315-129">The **Name** property is the same as the text in the static text control.</span></span>                                                                                                                                                                                                                     |
| [<span data-ttu-id="f0315-130">**obter \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="f0315-130">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | <span data-ttu-id="f0315-131">A propriedade **Parent** é uma janela ( [**\_ \_ janela do sistema de funções**](object-roles.md) ) que circunda o controle e tem a mesma propriedade **Name** e o nome da classe Window que o controle.</span><span class="sxs-lookup"><span data-stu-id="f0315-131">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                   |
| [<span data-ttu-id="f0315-132">**obter \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="f0315-132">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | <span data-ttu-id="f0315-133">A propriedade **role** é [**\_ System role \_ STATICTEXT**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="f0315-133">The **Role** property is [**ROLE\_SYSTEM\_STATICTEXT**](object-roles.md).</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="f0315-134">**obter \_ accState**</span><span class="sxs-lookup"><span data-stu-id="f0315-134">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | <span data-ttu-id="f0315-135">A propriedade **State** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md): [**estado \_ sistema \_ somente leitura**](object-state-constants.md) sistema de estado \| [**\_ \_ invisível**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="f0315-135">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_READONLY**](object-state-constants.md) \| [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="notes"></a><span data-ttu-id="f0315-136">Observações</span><span class="sxs-lookup"><span data-stu-id="f0315-136">Notes</span></span>

-   <span data-ttu-id="f0315-137">O método [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) retorna DISP \_ E \_ MEMBERNOTFOUND quando ele é chamado com [**SELFLAG \_ TAKEFOCUS**](selflag.md) em um objeto de texto estático.</span><span class="sxs-lookup"><span data-stu-id="f0315-137">The [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) method returns DISP\_E\_MEMBERNOTFOUND when it is called with [**SELFLAG\_TAKEFOCUS**](selflag.md) on a static text object.</span></span>
-   <span data-ttu-id="f0315-138">Os controles estáticos com o \_ estilo de ícone SS retornam dados inválidos na propriedade **Name** .</span><span class="sxs-lookup"><span data-stu-id="f0315-138">Static controls with the SS\_ICON style return invalid data in the **Name** property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0315-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f0315-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0315-140">Interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="f0315-140">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





