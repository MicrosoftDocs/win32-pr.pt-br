---
title: ControlShouldHaveValue
description: ControlShouldHaveValue
ms.assetid: 90C37CC5-21D2-4D26-B6D9-2C95C52127BF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b078712319ffcfde386df519837ba467ca2fcf4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159976"
---
# <a name="controlshouldhavevalue"></a><span data-ttu-id="2910f-103">ControlShouldHaveValue</span><span class="sxs-lookup"><span data-stu-id="2910f-103">ControlShouldHaveValue</span></span>

## <a name="text"></a><span data-ttu-id="2910f-104">Texto</span><span class="sxs-lookup"><span data-stu-id="2910f-104">Text</span></span>

<span data-ttu-id="2910f-105">Um controle com a função de {0} deve ter um valor, mas get \_ accValue não está implementado</span><span class="sxs-lookup"><span data-stu-id="2910f-105">A control with role of {0} should have a value but get\_accValue is not implemented</span></span>

## <a name="type"></a><span data-ttu-id="2910f-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="2910f-106">Type</span></span>

<span data-ttu-id="2910f-107">Erro</span><span class="sxs-lookup"><span data-stu-id="2910f-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="2910f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2910f-108">Description</span></span>

<span data-ttu-id="2910f-109">Um elemento não fornece um valor conforme esperado com base na função de MSAA atribuída, implicando que o elemento não tem o método [**Get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) implementado.</span><span class="sxs-lookup"><span data-stu-id="2910f-109">An element does not supply a value as expected based on the assigned MSAA role, implying that the element does not have the [**get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) method implemented.</span></span> <span data-ttu-id="2910f-110">Por exemplo, as seguintes funções de MSAA devem fornecer um valor.</span><span class="sxs-lookup"><span data-stu-id="2910f-110">For example, the following MSAA roles should all supply a value.</span></span>

-   <span data-ttu-id="2910f-111">\_ComboBox do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="2910f-111">ROLE\_SYSTEM\_COMBOBOX</span></span>
-   <span data-ttu-id="2910f-112">\_IPAddress do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="2910f-112">ROLE\_SYSTEM\_IPADDRESS</span></span>
-   <span data-ttu-id="2910f-113">\_link do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="2910f-113">ROLE\_SYSTEM\_LINK</span></span>
-   <span data-ttu-id="2910f-114">\_OUTLINEITEM do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="2910f-114">ROLE\_SYSTEM\_OUTLINEITEM</span></span>
-   <span data-ttu-id="2910f-115">\_PROGRESSBAR do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="2910f-115">ROLE\_SYSTEM\_PROGRESSBAR</span></span>
-   <span data-ttu-id="2910f-116">\_controle deslizante do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="2910f-116">ROLE\_SYSTEM\_SLIDER</span></span>
-   <span data-ttu-id="2910f-117">\_SPINBUTTON do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="2910f-117">ROLE\_SYSTEM\_SPINBUTTON</span></span>
-   <span data-ttu-id="2910f-118">\_barra de rolagem do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="2910f-118">ROLE\_SYSTEM\_SCROLLBAR</span></span>
-   <span data-ttu-id="2910f-119">\_texto do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="2910f-119">ROLE\_SYSTEM\_TEXT</span></span>

<span data-ttu-id="2910f-120">Esse problema é um problema para as pessoas que contam com um leitor de tela e um teclado para navegação porque um elemento que tem um valor intrínseco deve ser capaz de relatar esse valor a um usuário.</span><span class="sxs-lookup"><span data-stu-id="2910f-120">This issue is a problem for people who rely on a screen-reader and keyboard for navigation because an element that has an intrinsic value must be able to report that value to a user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="2910f-121">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="2910f-121">Possible causes</span></span>

<span data-ttu-id="2910f-122">O elemento ou seu pai tem uma função de MSAA definida incorretamente.</span><span class="sxs-lookup"><span data-stu-id="2910f-122">The element or its parent has an MSAA role set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2910f-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2910f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2910f-124">**IAccessible:: obter \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="2910f-124">**IAccessible::get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[<span data-ttu-id="2910f-125">**Funções de objeto**</span><span class="sxs-lookup"><span data-stu-id="2910f-125">**Object Roles**</span></span>](object-roles.md)
</dt> </dl>

 

 




