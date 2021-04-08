---
title: Circunflexo (referência de elemento de interface do usuário MSAA)
description: O cursor é uma linha, bloco ou bitmap piscando na área do cliente de uma janela ou em um controle que aceita entrada de teclado.
ms.assetid: f2c48c36-1859-4e0a-8833-3ca90b4da323
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3855e4825c6c8b8498f0b4b278a099452baa9d
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "103823533"
---
# <a name="caret-msaa-ui-element-reference"></a><span data-ttu-id="57418-103">Circunflexo (referência de elemento de interface do usuário MSAA)</span><span class="sxs-lookup"><span data-stu-id="57418-103">Caret (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="57418-104">Este tópico descreve os Cursors para fins de referência de elemento da interface do usuário do MSAA.</span><span class="sxs-lookup"><span data-stu-id="57418-104">This topic describes carets for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="57418-105">Como usar os Cursors em várias estruturas de interface do usuário não é descrito aqui.</span><span class="sxs-lookup"><span data-stu-id="57418-105">How to use carets in various UI frameworks is not described here.</span></span> <span data-ttu-id="57418-106">Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.</span><span class="sxs-lookup"><span data-stu-id="57418-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="57418-107">O cursor é uma linha, bloco ou bitmap piscando na área do cliente de uma janela ou em um controle que aceita entrada de teclado.</span><span class="sxs-lookup"><span data-stu-id="57418-107">The caret is a flashing line, block, or bitmap in the client area of a window or in a control that accepts keyboard input.</span></span> <span data-ttu-id="57418-108">Indica o local no qual o texto ou os gráficos são inseridos.</span><span class="sxs-lookup"><span data-stu-id="57418-108">It indicates the place at which text or graphics are inserted.</span></span> <span data-ttu-id="57418-109">Como apenas uma janela de cada vez tem o foco do teclado, há apenas um cursor no sistema.</span><span class="sxs-lookup"><span data-stu-id="57418-109">Because only one window at a time has the keyboard focus, there is only one caret in the system.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="57418-110">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="57418-110">IAccessible Methods</span></span>

<span data-ttu-id="57418-111">O cursor dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="57418-111">The caret supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="57418-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="57418-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="57418-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="57418-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a><span data-ttu-id="57418-114">Propriedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="57418-114">IAccessible Properties</span></span>

<span data-ttu-id="57418-115">O cursor dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="57418-115">The caret supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="57418-116">Propriedade</span><span class="sxs-lookup"><span data-stu-id="57418-116">Property</span></span></th>
<th><span data-ttu-id="57418-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="57418-117">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="57418-118"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span><span class="sxs-lookup"><span data-stu-id="57418-118"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span></span></td>
<td><span data-ttu-id="57418-119">A propriedade <strong>ChildCount</strong> é zero.</span><span class="sxs-lookup"><span data-stu-id="57418-119">The <strong>ChildCount</strong> property is zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57418-120"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a></span><span class="sxs-lookup"><span data-stu-id="57418-120"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a></span></span></td>
<td><span data-ttu-id="57418-121">A propriedade <strong>Name</strong> é &quot; Edit &quot; .</span><span class="sxs-lookup"><span data-stu-id="57418-121">The <strong>Name</strong> property is &quot;Edit&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57418-122"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a></span><span class="sxs-lookup"><span data-stu-id="57418-122"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a></span></span></td>
<td><span data-ttu-id="57418-123">A propriedade de <strong>função</strong> é <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>.</span><span class="sxs-lookup"><span data-stu-id="57418-123">The <strong>Role</strong> property is <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57418-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a></span><span class="sxs-lookup"><span data-stu-id="57418-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a></span></span></td>
<td><span data-ttu-id="57418-125">Os valores possíveis para a propriedade <strong>State</strong> incluem:</span><span class="sxs-lookup"><span data-stu-id="57418-125">Possible values for the <strong>State</strong> property include:</span></span>
<ul>
<li><span data-ttu-id="57418-126">Zero, o que significa que o cursor está visível</span><span class="sxs-lookup"><span data-stu-id="57418-126">Zero, which means the caret is visible</span></span></li>
<li><span data-ttu-id="57418-127"><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></span><span class="sxs-lookup"><span data-stu-id="57418-127"><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a><span data-ttu-id="57418-128">Observações</span><span class="sxs-lookup"><span data-stu-id="57418-128">Notes</span></span>

-   <span data-ttu-id="57418-129">Ao contrário de outros elementos da interface do usuário, o objeto de cursor não tem um identificador de janela associado.</span><span class="sxs-lookup"><span data-stu-id="57418-129">Unlike other UI elements, the caret object does not have an associated window handle.</span></span> <span data-ttu-id="57418-130">Para obter acesso ao objeto de cursor, os clientes devem definir um [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) e aguardar o objeto de cursor gerar eventos.</span><span class="sxs-lookup"><span data-stu-id="57418-130">To obtain access to the caret object, clients must set a [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) and wait for the caret object to generate events.</span></span>
-   <span data-ttu-id="57418-131">O objeto de cursor no controle rich edit fornecido pelo Riched20.dll (que é usado em editores de texto como o Microsoft WordPad no Windows 98) não envia nenhum [WinEvents](winevents-infrastructure.md) quando sua posição é alterada durante a seleção de texto.</span><span class="sxs-lookup"><span data-stu-id="57418-131">The caret object in the rich edit control provided by Riched20.dll (which is used in text editors such as Microsoft WordPad in Windows 98) does not send any [WinEvents](winevents-infrastructure.md) when its position is changed during text selection.</span></span> <span data-ttu-id="57418-132">Quando os usuários pressionam SHIFT e teclas de seta para selecionar texto, o objeto de cursor não dispara o [**objeto de evento \_ \_ LOCATIONCHANGE**](event-constants.md) WinEvent.</span><span class="sxs-lookup"><span data-stu-id="57418-132">When users press SHIFT and arrow keys to select text, the caret object does not trigger the [**EVENT\_OBJECT\_LOCATIONCHANGE**](event-constants.md) WinEvent.</span></span> <span data-ttu-id="57418-133">Da mesma forma, quando a seleção é definida programaticamente por meio de mensagens de edição avançadas, o objeto de cursor não envia nenhum evento para indicar sua nova posição.</span><span class="sxs-lookup"><span data-stu-id="57418-133">Similarly, when the selection is set programmatically through rich edit messages, the caret object does not send any events to indicate its new position.</span></span>

    <span data-ttu-id="57418-134">Todos os aplicativos que usam Riched20.dll apresentam esse problema.</span><span class="sxs-lookup"><span data-stu-id="57418-134">All applications that use Riched20.dll exhibit this problem.</span></span> <span data-ttu-id="57418-135">Os aplicativos que usam versões anteriores do controle de edição rico enviam eventos corretamente com base na seleção.</span><span class="sxs-lookup"><span data-stu-id="57418-135">Applications using earlier versions of the rich edit control correctly send events based on the selection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57418-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="57418-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57418-137">Interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="57418-137">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




