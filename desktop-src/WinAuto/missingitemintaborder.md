---
title: MissingItemInTabOrder
description: MissingItemInTabOrder
ms.assetid: 49DE892E-1B15-4F46-B316-217CC76AA1A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9841ab71e9f5d40cf25454e737b9790ce27a04de
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641154"
---
# <a name="missingitemintaborder"></a><span data-ttu-id="2bfc7-103">MissingItemInTabOrder</span><span class="sxs-lookup"><span data-stu-id="2bfc7-103">MissingItemInTabOrder</span></span>

## <a name="text"></a><span data-ttu-id="2bfc7-104">Texto</span><span class="sxs-lookup"><span data-stu-id="2bfc7-104">Text</span></span>

<span data-ttu-id="2bfc7-105">Esse elemento parece ser tabulado, mas não está na ordem de tabulação.</span><span class="sxs-lookup"><span data-stu-id="2bfc7-105">This element appears to be tabbable but is not in the tab order.</span></span>

## <a name="type"></a><span data-ttu-id="2bfc7-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="2bfc7-106">Type</span></span>

<span data-ttu-id="2bfc7-107">Erro</span><span class="sxs-lookup"><span data-stu-id="2bfc7-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="2bfc7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2bfc7-108">Description</span></span>

<span data-ttu-id="2bfc7-109">Um elemento que pode ser focalizado não é acessível usando a navegação de teclado padrão (TAB ou Shift + Tab).</span><span class="sxs-lookup"><span data-stu-id="2bfc7-109">A focusable element is not accessible using standard keyboard navigation (Tab or Shift+Tab).</span></span> <span data-ttu-id="2bfc7-110">Por exemplo, o elemento não foi marcado como uma parada de tabulação ou um índice de tabulação foi atribuído.</span><span class="sxs-lookup"><span data-stu-id="2bfc7-110">For example, the element has not been marked as a tab stop or assigned a tab index.</span></span> <span data-ttu-id="2bfc7-111">Esse problema causa problemas para as pessoas que contam com um leitor de tela e um teclado para navegação porque:</span><span class="sxs-lookup"><span data-stu-id="2bfc7-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because:</span></span>

-   <span data-ttu-id="2bfc7-112">O elemento não é detectável.</span><span class="sxs-lookup"><span data-stu-id="2bfc7-112">The element is not discoverable.</span></span>
-   <span data-ttu-id="2bfc7-113">Se o elemento for um filho de um controle de lista personalizado, as indicações indicando que o elemento filho pode ser navegado usando as teclas de seta ou de página podem estar ausentes.</span><span class="sxs-lookup"><span data-stu-id="2bfc7-113">If the element is a child of a custom list control, cues indicating the child element can be navigated using the Arrow or Page keys may be missing.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="2bfc7-114">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="2bfc7-114">Possible causes</span></span>

-   <span data-ttu-id="2bfc7-115">A função MSAA do elemento ou seu pai não está definido corretamente.</span><span class="sxs-lookup"><span data-stu-id="2bfc7-115">The MSAA role of the element or its parent is not set correctly.</span></span> <span data-ttu-id="2bfc7-116">Por exemplo, se todos os itens de lista em um controle de exibição de lista não forem expostos por meio de MSAA como uma ListItem de sistema de função \_ \_ , a verificação falhará porque os itens de lista não estão acessíveis usando a tecla Tab.</span><span class="sxs-lookup"><span data-stu-id="2bfc7-116">For example, if all list items in a list view control are not exposed through MSAA as a ROLE\_SYSTEM\_LISTITEM, the verification fails because the list items are not accessible using the Tab key.</span></span>
-   <span data-ttu-id="2bfc7-117">O elemento ou seu pai é um controle personalizado que não implementa a Tabulação corretamente.</span><span class="sxs-lookup"><span data-stu-id="2bfc7-117">The element or its parent is a custom control that doesn't implement tabbing correctly.</span></span> <span data-ttu-id="2bfc7-118">Por exemplo, a propriedade de estado MSAA nunca é configurada para o estado do \_ sistema em \_ foco.</span><span class="sxs-lookup"><span data-stu-id="2bfc7-118">For example, the MSAA State property is never set to STATE\_SYSTEM\_FOCUSABLE.</span></span>
-   <span data-ttu-id="2bfc7-119">Um elemento que atua como um contêiner para outros elementos foi selecionado para verificação, mas não dá suporte à navegação de teclado em si.</span><span class="sxs-lookup"><span data-stu-id="2bfc7-119">An element that acts as a container for other elements was selected for verification but does not support keyboard navigation itself.</span></span> <span data-ttu-id="2bfc7-120">Por exemplo, uma barra de ferramentas e seus elementos filho não podem ser acessados usando a tecla TAB.</span><span class="sxs-lookup"><span data-stu-id="2bfc7-120">For example, a toolbar and its child elements are not accessible using the TAB key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2bfc7-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2bfc7-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bfc7-122">Diretrizes para design de interface de usuário de teclado</span><span class="sxs-lookup"><span data-stu-id="2bfc7-122">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 