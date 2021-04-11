---
title: ElementHasNoName
description: ElementHasNoName
ms.assetid: 893A758F-BD34-4ABE-A99E-8CABE33966E0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc9af7e1ad0a62f35edb88102b68bfa6de3d5c28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292854"
---
# <a name="elementhasnoname"></a><span data-ttu-id="75df6-103">ElementHasNoName</span><span class="sxs-lookup"><span data-stu-id="75df6-103">ElementHasNoName</span></span>

## <a name="text"></a><span data-ttu-id="75df6-104">Texto</span><span class="sxs-lookup"><span data-stu-id="75df6-104">Text</span></span>

<span data-ttu-id="75df6-105">O elemento não tem nome</span><span class="sxs-lookup"><span data-stu-id="75df6-105">Element has no name</span></span>

## <a name="type"></a><span data-ttu-id="75df6-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="75df6-106">Type</span></span>

<span data-ttu-id="75df6-107">Erro</span><span class="sxs-lookup"><span data-stu-id="75df6-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="75df6-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="75df6-108">Description</span></span>

<span data-ttu-id="75df6-109">Um elemento não tem um nome.</span><span class="sxs-lookup"><span data-stu-id="75df6-109">An element does not have a name.</span></span> <span data-ttu-id="75df6-110">Por exemplo, o elemento não tem accName implementado e uma cadeia de caracteres vazia é retornada quando o método [**Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) é usado para recuperar o nome de MSAA do elemento.</span><span class="sxs-lookup"><span data-stu-id="75df6-110">For example, the element does not have accName implemented and an empty string is returned when the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method is used to retrieve the MSAA name of the element.</span></span>

<span data-ttu-id="75df6-111">Esse problema causa problemas para as pessoas que dependem de um leitor de tela e teclado para navegação porque um elemento pode ser identificado incorretamente para o usuário.</span><span class="sxs-lookup"><span data-stu-id="75df6-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might be incorrectly identified to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="75df6-112">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="75df6-112">Possible causes</span></span>

-   <span data-ttu-id="75df6-113">O elemento ou seu pai não tem nome ou rótulo.</span><span class="sxs-lookup"><span data-stu-id="75df6-113">The element or its parent has no name or label.</span></span>
-   <span data-ttu-id="75df6-114">O elemento é atribuído a um [**accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) que sugere que o elemento tenha um nome.</span><span class="sxs-lookup"><span data-stu-id="75df6-114">The element is assigned an [**accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) that suggests the element have a name.</span></span>
-   <span data-ttu-id="75df6-115">O elemento que tem o foco não deve receber o foco.</span><span class="sxs-lookup"><span data-stu-id="75df6-115">The element that has focus should not receive focus.</span></span> <span data-ttu-id="75df6-116">Por exemplo, um rótulo ou um controle desabilitado.</span><span class="sxs-lookup"><span data-stu-id="75df6-116">For example, a label or a disabled control.</span></span>
-   <span data-ttu-id="75df6-117">Um controle invisível recebeu o foco.</span><span class="sxs-lookup"><span data-stu-id="75df6-117">An invisible control has received focus.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75df6-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="75df6-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75df6-119">**IAccessible:: obter \_ accName**</span><span class="sxs-lookup"><span data-stu-id="75df6-119">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="75df6-120">Propriedade Name</span><span class="sxs-lookup"><span data-stu-id="75df6-120">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




