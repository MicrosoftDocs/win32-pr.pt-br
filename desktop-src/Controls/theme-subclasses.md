---
title: Usando subclasses de tema
description: As classes de tema que representam controles como ComboBox, Edit, ExplorerBar, Rebar, Tab e Toolbar podem ser subclasses para fornecer variações de tema para esse controle específico.
ms.assetid: 4f5e26c1-72ae-48de-a407-9ac3c0d5f502
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c5448bb5fea90193beed854e833cd34e7691b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635751"
---
# <a name="using-theme-subclasses"></a><span data-ttu-id="0cce3-103">Usando subclasses de tema</span><span class="sxs-lookup"><span data-stu-id="0cce3-103">Using Theme Subclasses</span></span>

<span data-ttu-id="0cce3-104">As classes de tema que representam controles como ComboBox, Edit, ExplorerBar, Rebar, Tab e Toolbar podem ser subclasses para fornecer variações de tema para esse controle específico.</span><span class="sxs-lookup"><span data-stu-id="0cce3-104">Theme classes that represent controls such as ComboBox, Edit, ExplorerBar, Rebar, Tab, and Toolbar can be subclassed in order to provide theme variations for that particular control.</span></span> <span data-ttu-id="0cce3-105">Por exemplo, a classe **Button** é uma subclasse como `Start::Button` para fornecer controle sobre o tema aplicado ao botão **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="0cce3-105">For example, the **Button** class is subclassed as `Start::Button` in order to provide control over the theme applied to the **Start** button.</span></span>

> [!Note]  
> <span data-ttu-id="0cce3-106">Tenha cuidado ao criar subclasses como as que são discutidas neste tópico.</span><span class="sxs-lookup"><span data-stu-id="0cce3-106">Use caution when you create subclasses like those that are discussed in this topic.</span></span> <span data-ttu-id="0cce3-107">Como as subclasses podem ser alteradas ou não estar disponíveis nas versões subsequentes do Windows, você não é incentivado de usá-las.</span><span class="sxs-lookup"><span data-stu-id="0cce3-107">Because subclasses might be altered or unavailable in subsequent versions of Windows, you are discouraged from using them.</span></span>

 

## <a name="two-ways-to-use-a-theme-subclass"></a><span data-ttu-id="0cce3-108">Duas maneiras de usar uma subclasse de Theme</span><span class="sxs-lookup"><span data-stu-id="0cce3-108">Two Ways to Use a Theme Subclass</span></span>

<span data-ttu-id="0cce3-109">Um aplicativo pode usar um tema de subclasse de uma destas duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="0cce3-109">An application can use a subclassed theme in one of these two ways:</span></span>

-   <span data-ttu-id="0cce3-110">Ele pode usar a função [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) com uma cadeia de caracteres do formulário `subclass::class` no parâmetro *pszClassList* .</span><span class="sxs-lookup"><span data-stu-id="0cce3-110">It can use the [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) function with a string of the form `subclass::class` in the *pszClassList* parameter.</span></span>
-   <span data-ttu-id="0cce3-111">Ele pode chamar [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) com o nome da subclasse do tema no parâmetro *pszSubAppName* .</span><span class="sxs-lookup"><span data-stu-id="0cce3-111">It can call [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) with the theme subclass name in the *pszSubAppName* parameter.</span></span>

## <a name="using-theme-messages-that-set-visual-style"></a><span data-ttu-id="0cce3-112">Usando mensagens de tema que definem o estilo visual</span><span class="sxs-lookup"><span data-stu-id="0cce3-112">Using Theme Messages That Set Visual Style</span></span>

<span data-ttu-id="0cce3-113">Determinados controles, como Rebar e Toolbar, fornecem mensagens específicas que você pode enviar para instruir o controle a usar uma subclasse de tema.</span><span class="sxs-lookup"><span data-stu-id="0cce3-113">Certain controls, such as Rebar and Toolbar, provide specific messages that you can send to instruct the control to use a theme subclass.</span></span> <span data-ttu-id="0cce3-114">Para esses controles, forneça um ponteiro para um buffer que contém o nome da subclasse do tema no parâmetro *lParam* da mensagem.</span><span class="sxs-lookup"><span data-stu-id="0cce3-114">For those controls, provide a pointer to a buffer that contains the theme subclass name in the *lParam* parameter of the message.</span></span> <span data-ttu-id="0cce3-115">Use a mensagem de [**CCM \_ SETWINDOWTHEME**](ccm-setwindowtheme.md) genérica ou use uma variante específica como as mostradas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0cce3-115">Use the generic [**CCM\_SETWINDOWTHEME**](ccm-setwindowtheme.md) message, or use a specific variant like those shown in the following table.</span></span>



| <span data-ttu-id="0cce3-116">Control</span><span class="sxs-lookup"><span data-stu-id="0cce3-116">Control</span></span>    | <span data-ttu-id="0cce3-117">Mensagem</span><span class="sxs-lookup"><span data-stu-id="0cce3-117">Message</span></span>                                             |
|------------|-----------------------------------------------------|
| <span data-ttu-id="0cce3-118">Dica de ferramenta</span><span class="sxs-lookup"><span data-stu-id="0cce3-118">Tooltip</span></span>    | [<span data-ttu-id="0cce3-119">**TTM \_ SETWINDOWTHEME**</span><span class="sxs-lookup"><span data-stu-id="0cce3-119">**TTM\_SETWINDOWTHEME**</span></span>](ttm-setwindowtheme.md)   |
| <span data-ttu-id="0cce3-120">Barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="0cce3-120">Toolbar</span></span>    | [<span data-ttu-id="0cce3-121">**TB de \_ SETWINDOWTHEME**</span><span class="sxs-lookup"><span data-stu-id="0cce3-121">**TB\_SETWINDOWTHEME**</span></span>](tb-setwindowtheme.md)     |
| <span data-ttu-id="0cce3-122">Rebar</span><span class="sxs-lookup"><span data-stu-id="0cce3-122">Rebar</span></span>      | [<span data-ttu-id="0cce3-123">**\_SETWINDOWTHEME RB**</span><span class="sxs-lookup"><span data-stu-id="0cce3-123">**RB\_SETWINDOWTHEME**</span></span>](rb-setwindowtheme.md)     |
| <span data-ttu-id="0cce3-124">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="0cce3-124">ComboBoxEx</span></span> | [<span data-ttu-id="0cce3-125">**CBEM \_ SETWINDOWTHEME**</span><span class="sxs-lookup"><span data-stu-id="0cce3-125">**CBEM\_SETWINDOWTHEME**</span></span>](cbem-setwindowtheme.md) |



 

<span data-ttu-id="0cce3-126">A tabela a seguir lista algumas das subclasses que o Windows Vista define.</span><span class="sxs-lookup"><span data-stu-id="0cce3-126">The following table lists some of the subclasses that Windows Vista defines.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0cce3-127">Classe</span><span class="sxs-lookup"><span data-stu-id="0cce3-127">Class</span></span></th>
<th><span data-ttu-id="0cce3-128">Subclasses</span><span class="sxs-lookup"><span data-stu-id="0cce3-128">Subclasses</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0cce3-129">ComboBox</span><span class="sxs-lookup"><span data-stu-id="0cce3-129">ComboBox</span></span></td>
<td><ul>
<li><span data-ttu-id="0cce3-130">Endereço</span><span class="sxs-lookup"><span data-stu-id="0cce3-130">Address</span></span></li>
<li><span data-ttu-id="0cce3-131">AddressComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-131">AddressComposited</span></span></li>
<li><span data-ttu-id="0cce3-132">InactiveAddress</span><span class="sxs-lookup"><span data-stu-id="0cce3-132">InactiveAddress</span></span></li>
<li><span data-ttu-id="0cce3-133">InactiveAddressComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-133">InactiveAddressComposited</span></span></li>
<li><span data-ttu-id="0cce3-134">MaxAddress</span><span class="sxs-lookup"><span data-stu-id="0cce3-134">MaxAddress</span></span></li>
<li><span data-ttu-id="0cce3-135">MaxAddressComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-135">MaxAddressComposited</span></span></li>
<li><span data-ttu-id="0cce3-136">MaxInactiveAddress</span><span class="sxs-lookup"><span data-stu-id="0cce3-136">MaxInactiveAddress</span></span></li>
<li><span data-ttu-id="0cce3-137">MaxInactiveAddressComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-137">MaxInactiveAddressComposited</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0cce3-138">Editar</span><span class="sxs-lookup"><span data-stu-id="0cce3-138">Edit</span></span></td>
<td><ul>
<li><span data-ttu-id="0cce3-139">Endereço</span><span class="sxs-lookup"><span data-stu-id="0cce3-139">Address</span></span></li>
<li><span data-ttu-id="0cce3-140">AddressComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-140">AddressComposited</span></span></li>
<li><span data-ttu-id="0cce3-141">InactiveAddress</span><span class="sxs-lookup"><span data-stu-id="0cce3-141">InactiveAddress</span></span></li>
<li><span data-ttu-id="0cce3-142">InactiveAddressComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-142">InactiveAddressComposited</span></span></li>
<li><span data-ttu-id="0cce3-143">InactiveSearchBoxEdit</span><span class="sxs-lookup"><span data-stu-id="0cce3-143">InactiveSearchBoxEdit</span></span></li>
<li><span data-ttu-id="0cce3-144">InactiveSearchBoxEditComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-144">InactiveSearchBoxEditComposited</span></span></li>
<li><span data-ttu-id="0cce3-145">MaxAddress</span><span class="sxs-lookup"><span data-stu-id="0cce3-145">MaxAddress</span></span></li>
<li><span data-ttu-id="0cce3-146">MaxAddressComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-146">MaxAddressComposited</span></span></li>
<li><span data-ttu-id="0cce3-147">MaxInactiveAddress</span><span class="sxs-lookup"><span data-stu-id="0cce3-147">MaxInactiveAddress</span></span></li>
<li><span data-ttu-id="0cce3-148">MaxInactiveAddressComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-148">MaxInactiveAddressComposited</span></span></li>
<li><span data-ttu-id="0cce3-149">MaxInactiveSearchBoxEdit</span><span class="sxs-lookup"><span data-stu-id="0cce3-149">MaxInactiveSearchBoxEdit</span></span></li>
<li><span data-ttu-id="0cce3-150">MaxInactiveSearchBoxEditComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-150">MaxInactiveSearchBoxEditComposited</span></span></li>
<li><span data-ttu-id="0cce3-151">MaxSearchBoxEdit</span><span class="sxs-lookup"><span data-stu-id="0cce3-151">MaxSearchBoxEdit</span></span></li>
<li><span data-ttu-id="0cce3-152">MaxSearchBoxEditComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-152">MaxSearchBoxEditComposited</span></span></li>
<li><span data-ttu-id="0cce3-153">SearchBoxEdit</span><span class="sxs-lookup"><span data-stu-id="0cce3-153">SearchBoxEdit</span></span></li>
<li><span data-ttu-id="0cce3-154">SearchBoxEditComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-154">SearchBoxEditComposited</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0cce3-155">Rebar</span><span class="sxs-lookup"><span data-stu-id="0cce3-155">Rebar</span></span></td>
<td><ul>
<li><span data-ttu-id="0cce3-156">BrowserTabBar</span><span class="sxs-lookup"><span data-stu-id="0cce3-156">BrowserTabBar</span></span></li>
<li><span data-ttu-id="0cce3-157">InactiveNavbar</span><span class="sxs-lookup"><span data-stu-id="0cce3-157">InactiveNavbar</span></span></li>
<li><span data-ttu-id="0cce3-158">InactiveNavbarComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-158">InactiveNavbarComposited</span></span></li>
<li><span data-ttu-id="0cce3-159">MaxInactiveNavbar</span><span class="sxs-lookup"><span data-stu-id="0cce3-159">MaxInactiveNavbar</span></span></li>
<li><span data-ttu-id="0cce3-160">MaxInactiveNavbarComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-160">MaxInactiveNavbarComposited</span></span></li>
<li><span data-ttu-id="0cce3-161">MaxNavbar</span><span class="sxs-lookup"><span data-stu-id="0cce3-161">MaxNavbar</span></span></li>
<li><span data-ttu-id="0cce3-162">MaxNavbarComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-162">MaxNavbarComposited</span></span></li>
<li><span data-ttu-id="0cce3-163">Barra de navegação</span><span class="sxs-lookup"><span data-stu-id="0cce3-163">Navbar</span></span></li>
<li><span data-ttu-id="0cce3-164">NavbarComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-164">NavbarComposited</span></span></li>
<li><span data-ttu-id="0cce3-165">NavbarNonTopmost</span><span class="sxs-lookup"><span data-stu-id="0cce3-165">NavbarNonTopmost</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0cce3-166">Tab</span><span class="sxs-lookup"><span data-stu-id="0cce3-166">Tab</span></span></td>
<td><ul>
<li><span data-ttu-id="0cce3-167">BrowserTab</span><span class="sxs-lookup"><span data-stu-id="0cce3-167">BrowserTab</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0cce3-168">Barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="0cce3-168">Toolbar</span></span></td>
<td><ul>
<li><span data-ttu-id="0cce3-169">Go</span><span class="sxs-lookup"><span data-stu-id="0cce3-169">Go</span></span></li>
<li><span data-ttu-id="0cce3-170">GoComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-170">GoComposited</span></span></li>
<li><span data-ttu-id="0cce3-171">InactiveGo</span><span class="sxs-lookup"><span data-stu-id="0cce3-171">InactiveGo</span></span></li>
<li><span data-ttu-id="0cce3-172">InactiveGoComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-172">InactiveGoComposited</span></span></li>
<li><span data-ttu-id="0cce3-173">MaxGo</span><span class="sxs-lookup"><span data-stu-id="0cce3-173">MaxGo</span></span></li>
<li><span data-ttu-id="0cce3-174">MaxGoComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-174">MaxGoComposited</span></span></li>
<li><span data-ttu-id="0cce3-175">MaxInactiveGo</span><span class="sxs-lookup"><span data-stu-id="0cce3-175">MaxInactiveGo</span></span></li>
<li><span data-ttu-id="0cce3-176">MaxInactiveGoComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-176">MaxInactiveGoComposited</span></span></li>
<li><span data-ttu-id="0cce3-177">SearchButton</span><span class="sxs-lookup"><span data-stu-id="0cce3-177">SearchButton</span></span></li>
<li><span data-ttu-id="0cce3-178">SearchButtonComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-178">SearchButtonComposited</span></span></li>
<li><span data-ttu-id="0cce3-179">Viagem</span><span class="sxs-lookup"><span data-stu-id="0cce3-179">Travel</span></span></li>
<li><span data-ttu-id="0cce3-180">TravelComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-180">TravelComposited</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="internet-explorer-subclasses"></a><span data-ttu-id="0cce3-181">Subclasses do Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="0cce3-181">Internet Explorer Subclasses</span></span>

<span data-ttu-id="0cce3-182">No Windows Vista, as subclasses de determinadas classes internas ao Windows Internet Explorer e ao Windows Explorer estão disponíveis, embora as próprias classes não sejam.</span><span class="sxs-lookup"><span data-stu-id="0cce3-182">In Windows Vista, the subclasses of certain classes internal to Windows Internet Explorer and Windows Explorer are available even though the classes themselves are not.</span></span> <span data-ttu-id="0cce3-183">A tabela a seguir lista as subclasses disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0cce3-183">The following table lists the available subclasses.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0cce3-184">AddressBand</span><span class="sxs-lookup"><span data-stu-id="0cce3-184">AddressBand</span></span></td>
<td><ul>
<li><span data-ttu-id="0cce3-185">AB</span><span class="sxs-lookup"><span data-stu-id="0cce3-185">AB</span></span></li>
<li><span data-ttu-id="0cce3-186">ABGreen</span><span class="sxs-lookup"><span data-stu-id="0cce3-186">ABGreen</span></span></li>
<li><span data-ttu-id="0cce3-187">ABGreenComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-187">ABGreenComposited</span></span></li>
<li><span data-ttu-id="0cce3-188">ABRed</span><span class="sxs-lookup"><span data-stu-id="0cce3-188">ABRed</span></span></li>
<li><span data-ttu-id="0cce3-189">ABRedComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-189">ABRedComposited</span></span></li>
<li><span data-ttu-id="0cce3-190">ABYellow</span><span class="sxs-lookup"><span data-stu-id="0cce3-190">ABYellow</span></span></li>
<li><span data-ttu-id="0cce3-191">ABYellowComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-191">ABYellowComposited</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0cce3-192">Caixa de pesquisa</span><span class="sxs-lookup"><span data-stu-id="0cce3-192">SearchBox</span></span></td>
<td><ul>
<li><span data-ttu-id="0cce3-193">InactiveSearchBox</span><span class="sxs-lookup"><span data-stu-id="0cce3-193">InactiveSearchBox</span></span></li>
<li><span data-ttu-id="0cce3-194">InactiveSearchBoxComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-194">InactiveSearchBoxComposited</span></span></li>
<li><span data-ttu-id="0cce3-195">MaxInactiveSearchBox</span><span class="sxs-lookup"><span data-stu-id="0cce3-195">MaxInactiveSearchBox</span></span></li>
<li><span data-ttu-id="0cce3-196">MaxInactiveSearchBoxComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-196">MaxInactiveSearchBoxComposited</span></span></li>
<li><span data-ttu-id="0cce3-197">MaxSearchBox</span><span class="sxs-lookup"><span data-stu-id="0cce3-197">MaxSearchBox</span></span></li>
<li><span data-ttu-id="0cce3-198">MaxSearchBoxComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-198">MaxSearchBoxComposited</span></span></li>
<li><span data-ttu-id="0cce3-199">SearchBoxComposited</span><span class="sxs-lookup"><span data-stu-id="0cce3-199">SearchBoxComposited</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0cce3-200">A tabela a seguir mostra as especificidades dessas classes.</span><span class="sxs-lookup"><span data-stu-id="0cce3-200">The following table shows the specifics of these classes.</span></span>



| <span data-ttu-id="0cce3-201">Control</span><span class="sxs-lookup"><span data-stu-id="0cce3-201">Control</span></span>     | <span data-ttu-id="0cce3-202">Parte</span><span class="sxs-lookup"><span data-stu-id="0cce3-202">Part</span></span>         | <span data-ttu-id="0cce3-203">Estados</span><span class="sxs-lookup"><span data-stu-id="0cce3-203">States</span></span>                                                 |
|-------------|--------------|--------------------------------------------------------|
| <span data-ttu-id="0cce3-204">ADDRESSBAND</span><span class="sxs-lookup"><span data-stu-id="0cce3-204">ADDRESSBAND</span></span> | <span data-ttu-id="0cce3-205">ABBACKGROUND</span><span class="sxs-lookup"><span data-stu-id="0cce3-205">ABBACKGROUND</span></span> | <span data-ttu-id="0cce3-206">NORMAL (0x1), quente (0x2), DESABILITAdo (0x3), com foco (0x4)</span><span class="sxs-lookup"><span data-stu-id="0cce3-206">NORMAL (0x1), HOT (0x2), DISABLED (0x3), FOCUSED (0x4)</span></span> |
| <span data-ttu-id="0cce3-207">SEARCHBOX</span><span class="sxs-lookup"><span data-stu-id="0cce3-207">SEARCHBOX</span></span>   | <span data-ttu-id="0cce3-208">SBBACKGROUND</span><span class="sxs-lookup"><span data-stu-id="0cce3-208">SBBACKGROUND</span></span> | <span data-ttu-id="0cce3-209">NORMAL (0x1), quente (0x2), DESABILITAdo (0x3), com foco (0x4)</span><span class="sxs-lookup"><span data-stu-id="0cce3-209">NORMAL (0x1), HOT (0x2), DISABLED (0x3), FOCUSED (0x4)</span></span> |



 

 

 




