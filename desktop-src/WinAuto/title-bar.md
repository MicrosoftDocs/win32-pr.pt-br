---
title: Barra de título (referência de elemento da interface do usuário do MSAA)
description: A barra de título na parte superior de uma janela exibe um ícone e uma linha de texto definidos pelo aplicativo.
ms.assetid: f41ab777-6c94-4d8e-b743-c635e93df396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fee3642a67be85b27eac6a73ac7c452f2349d1
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104365481"
---
# <a name="title-bar-msaa-ui-element-reference"></a><span data-ttu-id="571e0-103">Barra de título (referência de elemento da interface do usuário do MSAA)</span><span class="sxs-lookup"><span data-stu-id="571e0-103">Title Bar (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="571e0-104">Este tópico descreve objetos da **barra de título** para fins de referência de elemento da interface do usuário do MSAA.</span><span class="sxs-lookup"><span data-stu-id="571e0-104">This topic describes **Title Bar** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="571e0-105">Como criar objetos de **barra de título** em várias estruturas de interface do usuário não é descrito aqui.</span><span class="sxs-lookup"><span data-stu-id="571e0-105">How to create **Title Bar** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="571e0-106">Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.</span><span class="sxs-lookup"><span data-stu-id="571e0-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="571e0-107">A barra de título na parte superior de uma janela exibe um ícone e uma linha de texto definidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="571e0-107">The title bar at the top of a window displays an application-defined icon and line of text.</span></span> <span data-ttu-id="571e0-108">O texto especifica o nome do aplicativo e indica a finalidade da janela.</span><span class="sxs-lookup"><span data-stu-id="571e0-108">The text specifies the name of the application and indicates the purpose of the window.</span></span> <span data-ttu-id="571e0-109">A barra de título também torna possível que o usuário mova a janela usando um mouse ou outro dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="571e0-109">The title bar also makes it possible for the user to move the window using a mouse or other pointing device.</span></span>

<span data-ttu-id="571e0-110">As barras de título contêm pelo menos três botões pequenos que minimizam, maximizam ou restauram e fecham a janela associada à barra de título.</span><span class="sxs-lookup"><span data-stu-id="571e0-110">Title bars contain at least three small buttons that minimize, maximize or restore, and close the window associated with the title bar.</span></span> <span data-ttu-id="571e0-111">As barras de título também contêm um botão de ajuda contextual.</span><span class="sxs-lookup"><span data-stu-id="571e0-111">Title bars also contain a context-sensitive Help button.</span></span> <span data-ttu-id="571e0-112">Os aplicativos executados na versão Far-East do sistema operacional Windows também podem conter botões do IME (editor de método de entrada).</span><span class="sxs-lookup"><span data-stu-id="571e0-112">Applications running in the Far-East version of the Windows operating system may also contain Input Method Editor (IME) buttons.</span></span> <span data-ttu-id="571e0-113">O Microsoft Acessibilidade Ativa expõe esses botões como elementos filho da barra de título.</span><span class="sxs-lookup"><span data-stu-id="571e0-113">Microsoft Active Accessibility exposes these buttons as child elements of the title bar.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="571e0-114">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="571e0-114">IAccessible Methods</span></span>

<span data-ttu-id="571e0-115">As barras de título dão suporte aos seguintes métodos de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="571e0-115">Title bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="571e0-116">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="571e0-116">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="571e0-117">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="571e0-117">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="571e0-118">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="571e0-118">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="571e0-119">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="571e0-119">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="571e0-120">Propriedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="571e0-120">IAccessible Properties</span></span>

<span data-ttu-id="571e0-121">As barras de título dão suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="571e0-121">Title bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="571e0-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="571e0-122">Property</span></span></th>
<th><span data-ttu-id="571e0-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="571e0-123">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="571e0-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span><span class="sxs-lookup"><span data-stu-id="571e0-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span></span></td>
<td><span data-ttu-id="571e0-125">A propriedade <strong>ChildCount</strong> é cinco.</span><span class="sxs-lookup"><span data-stu-id="571e0-125">The <strong>ChildCount</strong> property is five.</span></span> <span data-ttu-id="571e0-126">A propriedade <strong>ChildCount</strong> inclui o IME e botões de ajuda sensíveis ao contexto, mesmo quando eles não são exibidos.</span><span class="sxs-lookup"><span data-stu-id="571e0-126">The <strong>ChildCount</strong> property includes the IME and context-sensitive Help buttons even when they are not displayed.</span></span> <span data-ttu-id="571e0-127">Os botões que não são exibidos têm a propriedade <strong>State</strong> <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="571e0-127">Buttons that are not displayed have the <strong>State</strong> property <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="571e0-128"><strong>get_accDescription</strong></span><span class="sxs-lookup"><span data-stu-id="571e0-128"><strong>get_accDescription</strong></span></span></td>
<td><span data-ttu-id="571e0-129">A propriedade <strong>Description</strong> da própria barra de título é: &quot; exibe o nome da janela e contém controles para manipulá-la. &quot; Os botões filho na barra de título têm as seguintes descrições:</span><span class="sxs-lookup"><span data-stu-id="571e0-129">The <strong>Description</strong> property of the title bar itself is: &quot;Displays the name of the window and contains controls to manipulate it.&quot; The child buttons in the title bar have the following descriptions:</span></span><br/>
<ul>
<li><span data-ttu-id="571e0-130">&quot;Move a janela para fora de</span><span class="sxs-lookup"><span data-stu-id="571e0-130">&quot;Moves the window out of</span></span></li>
<li><span data-ttu-id="571e0-131">&quot;Torna a janela completa</span><span class="sxs-lookup"><span data-stu-id="571e0-131">&quot;Makes the window full</span></span></li>
<li><span data-ttu-id="571e0-132">&quot;Coloca um minimizado ou um</span><span class="sxs-lookup"><span data-stu-id="571e0-132">&quot;Puts a minimized or</span></span></li>
<li><span data-ttu-id="571e0-133">&quot;Fecha a janela&quot;</span><span class="sxs-lookup"><span data-stu-id="571e0-133">&quot;Closes the window&quot;</span></span></li>
<li><span data-ttu-id="571e0-134">&quot;Entra ou sai do contexto-</span><span class="sxs-lookup"><span data-stu-id="571e0-134">&quot;Enters or leaves context-</span></span></li>
<li><span data-ttu-id="571e0-135">&quot;Abre o teclado quando pressionado&quot;</span><span class="sxs-lookup"><span data-stu-id="571e0-135">&quot;Brings up the keyboard when pressed&quot;</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="571e0-136"><strong>get_accName</strong></span><span class="sxs-lookup"><span data-stu-id="571e0-136"><strong>get_accName</strong></span></span></td>
<td><span data-ttu-id="571e0-137">A barra de título em si não oferece suporte à propriedade <strong>Name</strong> .</span><span class="sxs-lookup"><span data-stu-id="571e0-137">The title bar itself does not support the <strong>Name</strong> property.</span></span> <span data-ttu-id="571e0-138">Os botões filho na barra de título têm os seguintes nomes:</span><span class="sxs-lookup"><span data-stu-id="571e0-138">The child buttons in the title bar have the following names:</span></span>
<ul>
<li><span data-ttu-id="571e0-139">&quot;Minimizar&quot;</span><span class="sxs-lookup"><span data-stu-id="571e0-139">&quot;Minimize&quot;</span></span></li>
<li><span data-ttu-id="571e0-140">&quot;Maximizar &quot; ou &quot; restaurar &quot; ,</span><span class="sxs-lookup"><span data-stu-id="571e0-140">&quot;Maximize&quot; or &quot;Restore&quot;,</span></span></li>
<li><span data-ttu-id="571e0-141">&quot;Fechar&quot;</span><span class="sxs-lookup"><span data-stu-id="571e0-141">&quot;Close&quot;</span></span></li>
<li><span data-ttu-id="571e0-142">&quot;Ajuda de contexto&quot;</span><span class="sxs-lookup"><span data-stu-id="571e0-142">&quot;Context help&quot;</span></span></li>
<li><span data-ttu-id="571e0-143">&quot;IME&quot;</span><span class="sxs-lookup"><span data-stu-id="571e0-143">&quot;IME&quot;</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="571e0-144"><strong>get_accParent</strong></span><span class="sxs-lookup"><span data-stu-id="571e0-144"><strong>get_accParent</strong></span></span></td>
<td><span data-ttu-id="571e0-145">A propriedade <strong>Parent</strong> da barra de título é a janela principal do aplicativo ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ) que tem o mesmo nome de classe da janela definida pelo aplicativo que a barra de título.</span><span class="sxs-lookup"><span data-stu-id="571e0-145">The <strong>Parent</strong> property of the title bar is the main application window ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ) that has the same application-defined window class name as the title bar.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="571e0-146"><strong>get_accRole</strong></span><span class="sxs-lookup"><span data-stu-id="571e0-146"><strong>get_accRole</strong></span></span></td>
<td><span data-ttu-id="571e0-147">A propriedade de <strong>função</strong> é <a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="571e0-147">The <strong>Role</strong> property is <a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>.</span></span> <span data-ttu-id="571e0-148">Os botões filho na barra de título têm a <strong></strong> propriedade Role <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="571e0-148">The child buttons in the title bar have the <strong>Role</strong> property <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="571e0-149"><strong>get_accState</strong></span><span class="sxs-lookup"><span data-stu-id="571e0-149"><strong>get_accState</strong></span></span></td>
<td><span data-ttu-id="571e0-150">A propriedade <strong>State</strong> para a barra de título e os botões filho pode ser uma combinação de um ou mais dos seguintes <a href="object-state-constants.md">valores</a>: <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="571e0-150">The <strong>State</strong> property for the title bar and the child buttons can be a combination of one or more of the following <a href="object-state-constants.md">values</a>: <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="571e0-151"><strong>get_accValue</strong></span><span class="sxs-lookup"><span data-stu-id="571e0-151"><strong>get_accValue</strong></span></span></td>
<td><span data-ttu-id="571e0-152">A propriedade <strong>Value</strong> é uma cadeia de caracteres que é igual ao texto exibido na barra de título.</span><span class="sxs-lookup"><span data-stu-id="571e0-152">The <strong>Value</strong> property is a string that is the same as the text displayed in the title bar.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a><span data-ttu-id="571e0-153">Observações</span><span class="sxs-lookup"><span data-stu-id="571e0-153">Notes</span></span>

-   <span data-ttu-id="571e0-154">Embora a barra de título de um aplicativo tenha o estado de sinalizador de propriedade de **estado** , o sistema de estado do **sinalizador de** estado não [**tem foco. \_ \_**](object-state-constants.md) [**\_ \_**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="571e0-154">Although an application's title bar has the **State** property flag [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md), it never has the **State** flag [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md).</span></span> <span data-ttu-id="571e0-155">Definir o foco para um objeto de barra de título enfoca a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="571e0-155">Setting focus to a title bar object focuses the application window.</span></span>
-   <span data-ttu-id="571e0-156">Como o objeto da barra de título não dá suporte a [**Get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild), os botões na barra de título são elementos simples.</span><span class="sxs-lookup"><span data-stu-id="571e0-156">Because the title bar object does not support [**get\_accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild), the buttons on the title bar are simple elements.</span></span> <span data-ttu-id="571e0-157">Eles não oferecem suporte à própria interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="571e0-157">They do not support the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface themselves.</span></span> <span data-ttu-id="571e0-158">O objeto da barra de título fornece informações sobre esses botões filho.</span><span class="sxs-lookup"><span data-stu-id="571e0-158">The title bar object provides information about these child buttons.</span></span>
-   <span data-ttu-id="571e0-159">Como as barras de título não têm foco e não têm nenhuma ação padrão, os métodos [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) e [**Get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) não têm suporte para esse controle.</span><span class="sxs-lookup"><span data-stu-id="571e0-159">Because title bars do not get focus and have no default action, the [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) and [**get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) methods are not supported for this control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="571e0-160">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="571e0-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="571e0-161">Interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="571e0-161">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





