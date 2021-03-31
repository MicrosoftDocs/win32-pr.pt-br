---
title: Outras funções de objeto e métodos com suporte (referência de elemento de interface do usuário do MSAA)
description: Este tópico fornece informações sobre funções de objeto que não estão incluídas nos tópicos anteriores para elementos de interface do usuário.
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3d7fbdbb6dfbf83729f3e1c1d4caa3027f8d51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641531"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a><span data-ttu-id="1ae77-103">Outras funções de objeto e métodos com suporte (referência de elemento de interface do usuário do MSAA)</span><span class="sxs-lookup"><span data-stu-id="1ae77-103">Other Object Roles and Supported Methods (MSAA UI Element Reference)</span></span>

<span data-ttu-id="1ae77-104">Este tópico fornece informações sobre funções de objeto que não estão incluídas nos tópicos anteriores para elementos de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1ae77-104">This topic provides information about object roles that are not included in the previous topics for UI elements.</span></span> <span data-ttu-id="1ae77-105">Cada função de objeto inclui uma lista de métodos e propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) com suporte para a função de objeto.</span><span class="sxs-lookup"><span data-stu-id="1ae77-105">Each object role includes a list of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties that are supported for the object role.</span></span> <span data-ttu-id="1ae77-106">Enquanto outros tópicos documentam métodos e propriedades de **IAccessible** com suporte para elementos de interface do usuário, este tópico lista os métodos e propriedades que você pode esperar que tenham suporte para uma função de objeto específica.</span><span class="sxs-lookup"><span data-stu-id="1ae77-106">While other topics document supported **IAccessible** methods and properties for UI elements, this topic lists the methods and properties you can expect to be supported for a particular object role.</span></span> <span data-ttu-id="1ae77-107">Muitos dos elementos da interface do usuário que podem ter uma das funções listadas aqui normalmente são vistos em navegadores.</span><span class="sxs-lookup"><span data-stu-id="1ae77-107">Many of the UI elements which might have one of the roles listed here are typically seen in browsers.</span></span>

> [!Note]  
> <span data-ttu-id="1ae77-108">Use este tópico como uma diretriz.</span><span class="sxs-lookup"><span data-stu-id="1ae77-108">Use this topic as a guideline.</span></span> <span data-ttu-id="1ae77-109">É altamente recomendável que você use as ferramentas de Acessibilidade Ativa da Microsoft para verificar o comportamento esperado de uma função de objeto individual.</span><span class="sxs-lookup"><span data-stu-id="1ae77-109">We strongly suggest that you use Microsoft Active Accessibility tools to verify expected behavior for an individual object role.</span></span>

 

<span data-ttu-id="1ae77-110">A tabela a seguir lista as funções de objeto adicionais às quais Oleacc.dll dá suporte.</span><span class="sxs-lookup"><span data-stu-id="1ae77-110">The following table lists additional object roles which Oleacc.dll supports.</span></span>



|                                                                         |                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="1ae77-111">**\_alerta do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-111">**ROLE\_SYSTEM\_ALERT**</span></span>](/windows)                           | [<span data-ttu-id="1ae77-112">**\_lista suspensa do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-112">**ROLE\_SYSTEM\_DROPLIST**</span></span>](/windows)       |
| [<span data-ttu-id="1ae77-113">**\_aplicativo do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-113">**ROLE\_SYSTEM\_APPLICATION**</span></span>](/windows)               | [<span data-ttu-id="1ae77-114">**\_equação do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-114">**ROLE\_SYSTEM\_EQUATION**</span></span>](/windows)       |
| [<span data-ttu-id="1ae77-115">**\_borda do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-115">**ROLE\_SYSTEM\_BORDER**</span></span>](/windows)                         | [<span data-ttu-id="1ae77-116">**\_elemento gráfico do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-116">**ROLE\_SYSTEM\_GRAPHIC**</span></span>](/windows)         |
| [<span data-ttu-id="1ae77-117">**\_BUTTONDROPDOWN do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-117">**ROLE\_SYSTEM\_BUTTONDROPDOWN**</span></span>](/windows)         | [<span data-ttu-id="1ae77-118">**\_HELPBALLOON do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-118">**ROLE\_SYSTEM\_HELPBALLOON**</span></span>](/windows) |
| [<span data-ttu-id="1ae77-119">**\_BUTTONDROPDOWNGRID do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-119">**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**</span></span>](/windows) | [<span data-ttu-id="1ae77-120">**\_IPAddress do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-120">**ROLE\_SYSTEM\_IPADDRESS**</span></span>](/windows)     |
| [<span data-ttu-id="1ae77-121">**\_BUTTONMENU do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-121">**ROLE\_SYSTEM\_BUTTONMENU**</span></span>](/windows)                 | [<span data-ttu-id="1ae77-122">**\_link do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-122">**ROLE\_SYSTEM\_LINK**</span></span>](/windows)               |
| [<span data-ttu-id="1ae77-123">**\_célula do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-123">**ROLE\_SYSTEM\_CELL**</span></span>](/windows)                             | [<span data-ttu-id="1ae77-124">**\_painel do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-124">**ROLE\_SYSTEM\_PANE**</span></span>](/windows)               |
| [<span data-ttu-id="1ae77-125">**\_caractere do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-125">**ROLE\_SYSTEM\_CHARACTER**</span></span>](/windows)                   | [<span data-ttu-id="1ae77-126">**\_linha do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-126">**ROLE\_SYSTEM\_ROW**</span></span>](/windows)                 |
| [<span data-ttu-id="1ae77-127">**\_gráfico do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-127">**ROLE\_SYSTEM\_CHART**</span></span>](/windows)                           | [<span data-ttu-id="1ae77-128">**subcabeçalho de sistema de função \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-128">**ROLE\_SYSTEM\_ROWHEADER**</span></span>](/windows)     |
| [<span data-ttu-id="1ae77-129">**\_relógio do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-129">**ROLE\_SYSTEM\_CLOCK**</span></span>](/windows)                           | [<span data-ttu-id="1ae77-130">**separador de sistema de função \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-130">**ROLE\_SYSTEM\_SEPARATOR**</span></span>](/windows)     |
| [<span data-ttu-id="1ae77-131">**\_coluna do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-131">**ROLE\_SYSTEM\_COLUMN**</span></span>](/windows)                         | [<span data-ttu-id="1ae77-132">**\_som do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-132">**ROLE\_SYSTEM\_SOUND**</span></span>](/windows)             |
| [<span data-ttu-id="1ae77-133">**\_diagrama do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-133">**ROLE\_SYSTEM\_DIAGRAM**</span></span>](/windows)                       | [<span data-ttu-id="1ae77-134">**sistema de função \_ \_ SPLITBUTTON**</span><span class="sxs-lookup"><span data-stu-id="1ae77-134">**ROLE\_SYSTEM\_SPLITBUTTON**</span></span>](/windows) |
| [<span data-ttu-id="1ae77-135">**\_discagem do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-135">**ROLE\_SYSTEM\_DIAL**</span></span>](/windows)                             | [<span data-ttu-id="1ae77-136">**\_tabela do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-136">**ROLE\_SYSTEM\_TABLE**</span></span>](/windows)             |
| [<span data-ttu-id="1ae77-137">**\_documento do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-137">**ROLE\_SYSTEM\_DOCUMENT**</span></span>](/windows)                     | [<span data-ttu-id="1ae77-138">**espaço em branco do \_ sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="1ae77-138">**ROLE\_SYSTEM\_WHITESPACE**</span></span>](/windows)   |



 

## <a name="role_system_alert"></a><span data-ttu-id="1ae77-139">\_alerta do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-139">ROLE\_SYSTEM\_ALERT</span></span>

<span data-ttu-id="1ae77-140">Para obter mais informações sobre essa função, [**consulte \_ \_ alerta do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-140">For more information on this role, see [**ROLE\_SYSTEM\_ALERT**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-141">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-141">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-142">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-142">get\_accName</span></span>
-   <span data-ttu-id="1ae77-143">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-143">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-144">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-144">get\_accState</span></span>

## <a name="role_system_application"></a><span data-ttu-id="1ae77-145">\_aplicativo do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-145">ROLE\_SYSTEM\_APPLICATION</span></span>

<span data-ttu-id="1ae77-146">Para obter mais informações sobre essa função, [**consulte \_ \_ aplicativo do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-146">For more information on this role, see [**ROLE\_SYSTEM\_APPLICATION**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-147">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-147">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-148">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-148">accHitTest</span></span>
-   <span data-ttu-id="1ae77-149">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-149">accLocation</span></span>
-   <span data-ttu-id="1ae77-150">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-150">accNavigate</span></span>
-   <span data-ttu-id="1ae77-151">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="1ae77-151">get\_accChild</span></span>
-   <span data-ttu-id="1ae77-152">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="1ae77-152">get\_accChildCount</span></span>
-   <span data-ttu-id="1ae77-153">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="1ae77-153">get\_accFocus</span></span>
-   <span data-ttu-id="1ae77-154">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="1ae77-154">get\_accHelp</span></span>
-   <span data-ttu-id="1ae77-155">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="1ae77-155">get\_accHelpTopic</span></span>
-   <span data-ttu-id="1ae77-156">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="1ae77-156">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="1ae77-157">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-157">get\_accName</span></span>
-   <span data-ttu-id="1ae77-158">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-158">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-159">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-159">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-160">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-160">get\_accState</span></span>

## <a name="role_system_border"></a><span data-ttu-id="1ae77-161">\_borda do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-161">ROLE\_SYSTEM\_BORDER</span></span>

<span data-ttu-id="1ae77-162">Para obter mais informações sobre essa função, [**consulte \_ \_ borda do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-162">For more information on this role, see [**ROLE\_SYSTEM\_BORDER**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-163">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-163">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-164">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-164">accHitTest</span></span>
-   <span data-ttu-id="1ae77-165">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-165">accLocation</span></span>
-   <span data-ttu-id="1ae77-166">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-166">accNavigate</span></span>
-   <span data-ttu-id="1ae77-167">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-167">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-168">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-168">get\_accState</span></span>

## <a name="role_system_buttondropdown"></a><span data-ttu-id="1ae77-169">\_BUTTONDROPDOWN do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-169">ROLE\_SYSTEM\_BUTTONDROPDOWN</span></span>

<span data-ttu-id="1ae77-170">Para obter mais informações sobre essa função, [**consulte \_ sistema \_ de funções BUTTONDROPDOWN**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-170">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWN**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-171">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-171">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-172">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="1ae77-172">accDoDefaultAction</span></span>
-   <span data-ttu-id="1ae77-173">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-173">accHitTest</span></span>
-   <span data-ttu-id="1ae77-174">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-174">accLocation</span></span>
-   <span data-ttu-id="1ae77-175">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-175">accNavigate</span></span>
-   <span data-ttu-id="1ae77-176">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="1ae77-176">get\_accChild</span></span>
-   <span data-ttu-id="1ae77-177">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="1ae77-177">get\_accChildCount</span></span>
-   <span data-ttu-id="1ae77-178">obter \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="1ae77-178">get\_accDefaultAction</span></span>
-   <span data-ttu-id="1ae77-179">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="1ae77-179">get\_accFocus</span></span>
-   <span data-ttu-id="1ae77-180">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="1ae77-180">get\_accHelp</span></span>
-   <span data-ttu-id="1ae77-181">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="1ae77-181">get\_accHelpTopic</span></span>
-   <span data-ttu-id="1ae77-182">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="1ae77-182">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="1ae77-183">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-183">get\_accName</span></span>
-   <span data-ttu-id="1ae77-184">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-184">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-185">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-185">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-186">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-186">get\_accState</span></span>

## <a name="role_system_buttondropdowngrid"></a><span data-ttu-id="1ae77-187">\_BUTTONDROPDOWNGRID do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-187">ROLE\_SYSTEM\_BUTTONDROPDOWNGRID</span></span>

<span data-ttu-id="1ae77-188">Para obter mais informações sobre essa função, [**consulte \_ sistema \_ de funções BUTTONDROPDOWNGRID**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-188">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-189">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-189">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-190">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="1ae77-190">accDoDefaultAction</span></span>
-   <span data-ttu-id="1ae77-191">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-191">accHitTest</span></span>
-   <span data-ttu-id="1ae77-192">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-192">accLocation</span></span>
-   <span data-ttu-id="1ae77-193">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-193">accNavigate</span></span>
-   <span data-ttu-id="1ae77-194">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="1ae77-194">get\_accChild</span></span>
-   <span data-ttu-id="1ae77-195">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="1ae77-195">get\_accChildCount</span></span>
-   <span data-ttu-id="1ae77-196">obter \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="1ae77-196">get\_accDefaultAction</span></span>
-   <span data-ttu-id="1ae77-197">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="1ae77-197">get\_accFocus</span></span>
-   <span data-ttu-id="1ae77-198">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="1ae77-198">get\_accHelp</span></span>
-   <span data-ttu-id="1ae77-199">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="1ae77-199">get\_accHelpTopic</span></span>
-   <span data-ttu-id="1ae77-200">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="1ae77-200">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="1ae77-201">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-201">get\_accName</span></span>
-   <span data-ttu-id="1ae77-202">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-202">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-203">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-203">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-204">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-204">get\_accState</span></span>

## <a name="role_system_buttonmenu"></a><span data-ttu-id="1ae77-205">\_BUTTONMENU do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-205">ROLE\_SYSTEM\_BUTTONMENU</span></span>

<span data-ttu-id="1ae77-206">Para obter mais informações sobre essa função, [**consulte \_ sistema \_ de funções BUTTONMENU**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-206">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONMENU**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-207">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-207">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-208">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="1ae77-208">accDoDefaultAction</span></span>
-   <span data-ttu-id="1ae77-209">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-209">accHitTest</span></span>
-   <span data-ttu-id="1ae77-210">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-210">accLocation</span></span>
-   <span data-ttu-id="1ae77-211">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-211">accNavigate</span></span>
-   <span data-ttu-id="1ae77-212">obter \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="1ae77-212">get\_accDefaultAction</span></span>
-   <span data-ttu-id="1ae77-213">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="1ae77-213">get\_accFocus</span></span>
-   <span data-ttu-id="1ae77-214">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="1ae77-214">get\_accHelp</span></span>
-   <span data-ttu-id="1ae77-215">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="1ae77-215">get\_accHelpTopic</span></span>
-   <span data-ttu-id="1ae77-216">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="1ae77-216">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="1ae77-217">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-217">get\_accName</span></span>
-   <span data-ttu-id="1ae77-218">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-218">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-219">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-219">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-220">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-220">get\_accState</span></span>

## <a name="role_system_cell"></a><span data-ttu-id="1ae77-221">\_célula do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-221">ROLE\_SYSTEM\_CELL</span></span>

<span data-ttu-id="1ae77-222">Para obter mais informações sobre essa função, [**consulte \_ \_ célula do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-222">For more information on this role, see [**ROLE\_SYSTEM\_CELL**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-223">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-223">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-224">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-224">accHitTest</span></span>
-   <span data-ttu-id="1ae77-225">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-225">accLocation</span></span>
-   <span data-ttu-id="1ae77-226">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-226">accNavigate</span></span>
-   <span data-ttu-id="1ae77-227">accSelect</span><span class="sxs-lookup"><span data-stu-id="1ae77-227">accSelect</span></span>
-   <span data-ttu-id="1ae77-228">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="1ae77-228">get\_accChild</span></span>
-   <span data-ttu-id="1ae77-229">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="1ae77-229">get\_accChildCount</span></span>
-   <span data-ttu-id="1ae77-230">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="1ae77-230">get\_accFocus</span></span>
-   <span data-ttu-id="1ae77-231">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="1ae77-231">get\_accHelp</span></span>
-   <span data-ttu-id="1ae77-232">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="1ae77-232">get\_accHelpTopic</span></span>
-   <span data-ttu-id="1ae77-233">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="1ae77-233">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="1ae77-234">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-234">get\_accName</span></span>
-   <span data-ttu-id="1ae77-235">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-235">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-236">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-236">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-237">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-237">get\_accState</span></span>
-   <span data-ttu-id="1ae77-238">obter \_ accValue</span><span class="sxs-lookup"><span data-stu-id="1ae77-238">get\_accValue</span></span>

## <a name="role_system_character"></a><span data-ttu-id="1ae77-239">\_caractere do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-239">ROLE\_SYSTEM\_CHARACTER</span></span>

<span data-ttu-id="1ae77-240">Para obter mais informações sobre essa função, consulte [**função do \_ \_ caractere do sistema**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-240">For more information on this role, see [**ROLE\_SYSTEM\_CHARACTER**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-241">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-241">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-242">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-242">accHitTest</span></span>
-   <span data-ttu-id="1ae77-243">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-243">accLocation</span></span>
-   <span data-ttu-id="1ae77-244">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-244">accNavigate</span></span>
-   <span data-ttu-id="1ae77-245">obter \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="1ae77-245">get\_accDescription</span></span>
-   <span data-ttu-id="1ae77-246">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="1ae77-246">get\_accFocus</span></span>
-   <span data-ttu-id="1ae77-247">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="1ae77-247">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="1ae77-248">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-248">get\_accName</span></span>
-   <span data-ttu-id="1ae77-249">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-249">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-250">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-250">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-251">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-251">get\_accState</span></span>
-   <span data-ttu-id="1ae77-252">obter \_ accValue</span><span class="sxs-lookup"><span data-stu-id="1ae77-252">get\_accValue</span></span>

## <a name="role_system_chart"></a><span data-ttu-id="1ae77-253">\_gráfico do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-253">ROLE\_SYSTEM\_CHART</span></span>

<span data-ttu-id="1ae77-254">Para obter mais informações sobre essa função, [**consulte \_ \_ gráfico do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-254">For more information on this role, see [**ROLE\_SYSTEM\_CHART**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-255">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-255">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-256">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-256">accHitTest</span></span>
-   <span data-ttu-id="1ae77-257">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-257">accLocation</span></span>
-   <span data-ttu-id="1ae77-258">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-258">accNavigate</span></span>
-   <span data-ttu-id="1ae77-259">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="1ae77-259">get\_accChild</span></span>
-   <span data-ttu-id="1ae77-260">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="1ae77-260">get\_accChildCount</span></span>
-   <span data-ttu-id="1ae77-261">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="1ae77-261">get\_accFocus</span></span>
-   <span data-ttu-id="1ae77-262">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="1ae77-262">get\_accHelp</span></span>
-   <span data-ttu-id="1ae77-263">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="1ae77-263">get\_accHelpTopic</span></span>
-   <span data-ttu-id="1ae77-264">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="1ae77-264">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="1ae77-265">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-265">get\_accName</span></span>
-   <span data-ttu-id="1ae77-266">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-266">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-267">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-267">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-268">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-268">get\_accState</span></span>

## <a name="role_system_clock"></a><span data-ttu-id="1ae77-269">\_relógio do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-269">ROLE\_SYSTEM\_CLOCK</span></span>

<span data-ttu-id="1ae77-270">Para obter mais informações sobre essa função, [**consulte \_ \_ relógio do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-270">For more information on this role, see [**ROLE\_SYSTEM\_CLOCK**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-271">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-271">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-272">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-272">accHitTest</span></span>
-   <span data-ttu-id="1ae77-273">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-273">accLocation</span></span>
-   <span data-ttu-id="1ae77-274">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-274">accNavigate</span></span>
-   <span data-ttu-id="1ae77-275">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="1ae77-275">get\_accFocus</span></span>
-   <span data-ttu-id="1ae77-276">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="1ae77-276">get\_accHelp</span></span>
-   <span data-ttu-id="1ae77-277">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="1ae77-277">get\_accHelpTopic</span></span>
-   <span data-ttu-id="1ae77-278">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="1ae77-278">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="1ae77-279">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-279">get\_accName</span></span>
-   <span data-ttu-id="1ae77-280">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-280">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-281">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-281">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-282">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-282">get\_accState</span></span>
-   <span data-ttu-id="1ae77-283">obter \_ accValue</span><span class="sxs-lookup"><span data-stu-id="1ae77-283">get\_accValue</span></span>

## <a name="role_system_column"></a><span data-ttu-id="1ae77-284">\_coluna do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-284">ROLE\_SYSTEM\_COLUMN</span></span>

<span data-ttu-id="1ae77-285">Para obter mais informações sobre essa função, [**consulte \_ \_ coluna do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-285">For more information on this role, see [**ROLE\_SYSTEM\_COLUMN**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-286">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-286">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-287">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-287">accHitTest</span></span>
-   <span data-ttu-id="1ae77-288">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-288">accLocation</span></span>
-   <span data-ttu-id="1ae77-289">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-289">accNavigate</span></span>
-   <span data-ttu-id="1ae77-290">accSelect</span><span class="sxs-lookup"><span data-stu-id="1ae77-290">accSelect</span></span>
-   <span data-ttu-id="1ae77-291">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="1ae77-291">get\_accChild</span></span>
-   <span data-ttu-id="1ae77-292">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="1ae77-292">get\_accChildCount</span></span>
-   <span data-ttu-id="1ae77-293">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="1ae77-293">get\_accFocus</span></span>
-   <span data-ttu-id="1ae77-294">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-294">get\_accName</span></span>
-   <span data-ttu-id="1ae77-295">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-295">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-296">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-296">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-297">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-297">get\_accState</span></span>
-   <span data-ttu-id="1ae77-298">obter \_ accValue</span><span class="sxs-lookup"><span data-stu-id="1ae77-298">get\_accValue</span></span>

## <a name="role_system_diagram"></a><span data-ttu-id="1ae77-299">\_diagrama do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-299">ROLE\_SYSTEM\_DIAGRAM</span></span>

<span data-ttu-id="1ae77-300">Para obter mais informações sobre essa função, [**consulte \_ \_ diagrama do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-300">For more information on this role, see [**ROLE\_SYSTEM\_DIAGRAM**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-301">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-301">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-302">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-302">accHitTest</span></span>
-   <span data-ttu-id="1ae77-303">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-303">accLocation</span></span>
-   <span data-ttu-id="1ae77-304">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-304">accNavigate</span></span>
-   <span data-ttu-id="1ae77-305">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="1ae77-305">get\_accChild</span></span>
-   <span data-ttu-id="1ae77-306">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="1ae77-306">get\_accChildCount</span></span>
-   <span data-ttu-id="1ae77-307">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="1ae77-307">get\_accFocus</span></span>
-   <span data-ttu-id="1ae77-308">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="1ae77-308">get\_accHelp</span></span>
-   <span data-ttu-id="1ae77-309">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="1ae77-309">get\_accHelpTopic</span></span>
-   <span data-ttu-id="1ae77-310">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="1ae77-310">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="1ae77-311">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-311">get\_accName</span></span>
-   <span data-ttu-id="1ae77-312">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-312">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-313">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-313">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-314">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-314">get\_accState</span></span>

## <a name="role_system_dial"></a><span data-ttu-id="1ae77-315">\_discagem do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-315">ROLE\_SYSTEM\_DIAL</span></span>

<span data-ttu-id="1ae77-316">Para obter mais informações sobre essa função, consulte [**role \_ System \_ Dial**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-316">For more information on this role, see [**ROLE\_SYSTEM\_DIAL**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-317">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-317">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-318">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="1ae77-318">accDoDefaultAction</span></span>
-   <span data-ttu-id="1ae77-319">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-319">accHitTest</span></span>
-   <span data-ttu-id="1ae77-320">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-320">accLocation</span></span>
-   <span data-ttu-id="1ae77-321">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-321">accNavigate</span></span>
-   <span data-ttu-id="1ae77-322">obter \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="1ae77-322">get\_accDefaultAction</span></span>
-   <span data-ttu-id="1ae77-323">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="1ae77-323">get\_accFocus</span></span>
-   <span data-ttu-id="1ae77-324">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="1ae77-324">get\_accHelp</span></span>
-   <span data-ttu-id="1ae77-325">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="1ae77-325">get\_accHelpTopic</span></span>
-   <span data-ttu-id="1ae77-326">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="1ae77-326">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="1ae77-327">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-327">get\_accName</span></span>
-   <span data-ttu-id="1ae77-328">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-328">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-329">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-329">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-330">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-330">get\_accState</span></span>
-   <span data-ttu-id="1ae77-331">obter \_ accValue</span><span class="sxs-lookup"><span data-stu-id="1ae77-331">get\_accValue</span></span>

## <a name="role_system_document"></a><span data-ttu-id="1ae77-332">\_documento do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-332">ROLE\_SYSTEM\_DOCUMENT</span></span>

<span data-ttu-id="1ae77-333">Para obter mais informações sobre essa função, [**consulte \_ \_ documento do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-333">For more information on this role, see [**ROLE\_SYSTEM\_DOCUMENT**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-334">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-334">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-335">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-335">accHitTest</span></span>
-   <span data-ttu-id="1ae77-336">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-336">accLocation</span></span>
-   <span data-ttu-id="1ae77-337">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-337">accNavigate</span></span>
-   <span data-ttu-id="1ae77-338">accSelect</span><span class="sxs-lookup"><span data-stu-id="1ae77-338">accSelect</span></span>
-   <span data-ttu-id="1ae77-339">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="1ae77-339">get\_accChild</span></span>
-   <span data-ttu-id="1ae77-340">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="1ae77-340">get\_accChildCount</span></span>
-   <span data-ttu-id="1ae77-341">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="1ae77-341">get\_accFocus</span></span>
-   <span data-ttu-id="1ae77-342">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-342">get\_accName</span></span>
-   <span data-ttu-id="1ae77-343">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-343">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-344">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-344">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-345">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-345">get\_accState</span></span>

## <a name="role_system_droplist"></a><span data-ttu-id="1ae77-346">\_lista suspensa do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-346">ROLE\_SYSTEM\_DROPLIST</span></span>

<span data-ttu-id="1ae77-347">Para obter mais informações sobre essa função, [**consulte \_ \_ lista suspensa do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-347">For more information on this role, see [**ROLE\_SYSTEM\_DROPLIST**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-348">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-348">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-349">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="1ae77-349">accDoDefaultAction</span></span>
-   <span data-ttu-id="1ae77-350">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-350">accHitTest</span></span>
-   <span data-ttu-id="1ae77-351">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-351">accLocation</span></span>
-   <span data-ttu-id="1ae77-352">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-352">accNavigate</span></span>
-   <span data-ttu-id="1ae77-353">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="1ae77-353">get\_accChild</span></span>
-   <span data-ttu-id="1ae77-354">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="1ae77-354">get\_accChildCount</span></span>
-   <span data-ttu-id="1ae77-355">obter \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="1ae77-355">get\_accDefaultAction</span></span>
-   <span data-ttu-id="1ae77-356">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="1ae77-356">get\_accFocus</span></span>
-   <span data-ttu-id="1ae77-357">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="1ae77-357">get\_accHelp</span></span>
-   <span data-ttu-id="1ae77-358">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="1ae77-358">get\_accHelpTopic</span></span>
-   <span data-ttu-id="1ae77-359">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="1ae77-359">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="1ae77-360">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-360">get\_accName</span></span>
-   <span data-ttu-id="1ae77-361">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-361">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-362">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-362">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-363">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-363">get\_accState</span></span>

## <a name="role_system_equation"></a><span data-ttu-id="1ae77-364">\_equação do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-364">ROLE\_SYSTEM\_EQUATION</span></span>

<span data-ttu-id="1ae77-365">Para obter mais informações sobre essa função, [**consulte \_ \_ equação do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-365">For more information on this role, see [**ROLE\_SYSTEM\_EQUATION**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-366">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-366">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-367">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-367">accHitTest</span></span>
-   <span data-ttu-id="1ae77-368">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-368">accLocation</span></span>
-   <span data-ttu-id="1ae77-369">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-369">accNavigate</span></span>
-   <span data-ttu-id="1ae77-370">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="1ae77-370">get\_accFocus</span></span>
-   <span data-ttu-id="1ae77-371">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-371">get\_accName</span></span>
-   <span data-ttu-id="1ae77-372">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-372">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-373">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-373">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-374">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-374">get\_accState</span></span>
-   <span data-ttu-id="1ae77-375">obter \_ accValue</span><span class="sxs-lookup"><span data-stu-id="1ae77-375">get\_accValue</span></span>

## <a name="role_system_graphic"></a><span data-ttu-id="1ae77-376">\_elemento gráfico do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-376">ROLE\_SYSTEM\_GRAPHIC</span></span>

<span data-ttu-id="1ae77-377">Para obter mais informações sobre essa função, [**consulte \_ \_ elemento gráfico do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-377">For more information on this role, see [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-378">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-378">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-379">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-379">accHitTest</span></span>
-   <span data-ttu-id="1ae77-380">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-380">accLocation</span></span>
-   <span data-ttu-id="1ae77-381">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-381">accNavigate</span></span>
-   <span data-ttu-id="1ae77-382">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="1ae77-382">get\_accFocus</span></span>
-   <span data-ttu-id="1ae77-383">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="1ae77-383">get\_accHelp</span></span>
-   <span data-ttu-id="1ae77-384">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="1ae77-384">get\_accHelpTopic</span></span>
-   <span data-ttu-id="1ae77-385">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="1ae77-385">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="1ae77-386">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-386">get\_accName</span></span>
-   <span data-ttu-id="1ae77-387">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-387">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-388">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-388">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-389">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-389">get\_accState</span></span>

## <a name="role_system_helpballoon"></a><span data-ttu-id="1ae77-390">\_HELPBALLOON do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-390">ROLE\_SYSTEM\_HELPBALLOON</span></span>

<span data-ttu-id="1ae77-391">Para obter mais informações sobre essa função, [**consulte \_ sistema \_ de funções HELPBALLOON**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-391">For more information on this role, see [**ROLE\_SYSTEM\_HELPBALLOON**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-392">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-392">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-393">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-393">accHitTest</span></span>
-   <span data-ttu-id="1ae77-394">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-394">accLocation</span></span>
-   <span data-ttu-id="1ae77-395">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-395">accNavigate</span></span>
-   <span data-ttu-id="1ae77-396">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="1ae77-396">get\_accChild</span></span>
-   <span data-ttu-id="1ae77-397">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="1ae77-397">get\_accChildCount</span></span>
-   <span data-ttu-id="1ae77-398">obter \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="1ae77-398">get\_accDefaultAction</span></span>
-   <span data-ttu-id="1ae77-399">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-399">get\_accName</span></span>
-   <span data-ttu-id="1ae77-400">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-400">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-401">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-401">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-402">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-402">get\_accState</span></span>
-   <span data-ttu-id="1ae77-403">obter \_ accValue</span><span class="sxs-lookup"><span data-stu-id="1ae77-403">get\_accValue</span></span>

## <a name="role_system_ipaddress"></a><span data-ttu-id="1ae77-404">\_IPAddress do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-404">ROLE\_SYSTEM\_IPADDRESS</span></span>

<span data-ttu-id="1ae77-405">Para obter mais informações sobre essa função, [**consulte \_ \_ IPAddress do sistema de função**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-405">For more information on this role, see [**ROLE\_SYSTEM\_IPADDRESS**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-406">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-406">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-407">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-407">accHitTest</span></span>
-   <span data-ttu-id="1ae77-408">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-408">accLocation</span></span>
-   <span data-ttu-id="1ae77-409">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-409">accNavigate</span></span>
-   <span data-ttu-id="1ae77-410">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="1ae77-410">get\_accChild</span></span>
-   <span data-ttu-id="1ae77-411">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="1ae77-411">get\_accChildCount</span></span>
-   <span data-ttu-id="1ae77-412">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="1ae77-412">get\_accFocus</span></span>
-   <span data-ttu-id="1ae77-413">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="1ae77-413">get\_accHelp</span></span>
-   <span data-ttu-id="1ae77-414">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="1ae77-414">get\_accHelpTopic</span></span>
-   <span data-ttu-id="1ae77-415">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="1ae77-415">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="1ae77-416">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-416">get\_accName</span></span>
-   <span data-ttu-id="1ae77-417">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-417">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-418">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-418">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-419">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-419">get\_accState</span></span>
-   <span data-ttu-id="1ae77-420">obter \_ accValue</span><span class="sxs-lookup"><span data-stu-id="1ae77-420">get\_accValue</span></span>

## <a name="role_system_link"></a><span data-ttu-id="1ae77-421">\_link do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-421">ROLE\_SYSTEM\_LINK</span></span>

<span data-ttu-id="1ae77-422">Para obter mais informações sobre essa função, [**consulte \_ \_ link do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-422">For more information on this role, see [**ROLE\_SYSTEM\_LINK**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-423">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-423">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-424">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="1ae77-424">accDoDefaultAction</span></span>
-   <span data-ttu-id="1ae77-425">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-425">accHitTest</span></span>
-   <span data-ttu-id="1ae77-426">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-426">accLocation</span></span>
-   <span data-ttu-id="1ae77-427">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-427">accNavigate</span></span>
-   <span data-ttu-id="1ae77-428">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="1ae77-428">get\_accChild</span></span>
-   <span data-ttu-id="1ae77-429">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="1ae77-429">get\_accChildCount</span></span>
-   <span data-ttu-id="1ae77-430">obter \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="1ae77-430">get\_accDefaultAction</span></span>
-   <span data-ttu-id="1ae77-431">obter \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="1ae77-431">get\_accDescription</span></span>
-   <span data-ttu-id="1ae77-432">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="1ae77-432">get\_accFocus</span></span>
-   <span data-ttu-id="1ae77-433">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="1ae77-433">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="1ae77-434">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-434">get\_accName</span></span>
-   <span data-ttu-id="1ae77-435">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-435">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-436">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-436">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-437">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-437">get\_accState</span></span>
-   <span data-ttu-id="1ae77-438">obter \_ accValue</span><span class="sxs-lookup"><span data-stu-id="1ae77-438">get\_accValue</span></span>

## <a name="role_system_pane"></a><span data-ttu-id="1ae77-439">\_painel do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-439">ROLE\_SYSTEM\_PANE</span></span>

<span data-ttu-id="1ae77-440">Para obter mais informações sobre essa função, [**consulte \_ \_ painel do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-440">For more information on this role, see [**ROLE\_SYSTEM\_PANE**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-441">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-441">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-442">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-442">accHitTest</span></span>
-   <span data-ttu-id="1ae77-443">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-443">accLocation</span></span>
-   <span data-ttu-id="1ae77-444">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-444">accNavigate</span></span>
-   <span data-ttu-id="1ae77-445">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="1ae77-445">get\_accChild</span></span>
-   <span data-ttu-id="1ae77-446">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="1ae77-446">get\_accChildCount</span></span>
-   <span data-ttu-id="1ae77-447">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="1ae77-447">get\_accFocus</span></span>
-   <span data-ttu-id="1ae77-448">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="1ae77-448">get\_accHelp</span></span>
-   <span data-ttu-id="1ae77-449">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="1ae77-449">get\_accHelpTopic</span></span>
-   <span data-ttu-id="1ae77-450">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="1ae77-450">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="1ae77-451">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-451">get\_accName</span></span>
-   <span data-ttu-id="1ae77-452">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-452">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-453">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-453">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-454">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-454">get\_accState</span></span>

## <a name="role_system_row"></a><span data-ttu-id="1ae77-455">\_linha do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-455">ROLE\_SYSTEM\_ROW</span></span>

<span data-ttu-id="1ae77-456">Para obter mais informações sobre essa função, [**consulte \_ \_ linha do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-456">For more information on this role, see [**ROLE\_SYSTEM\_ROW**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-457">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-457">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-458">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-458">accHitTest</span></span>
-   <span data-ttu-id="1ae77-459">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-459">accLocation</span></span>
-   <span data-ttu-id="1ae77-460">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-460">accNavigate</span></span>
-   <span data-ttu-id="1ae77-461">accSelect</span><span class="sxs-lookup"><span data-stu-id="1ae77-461">accSelect</span></span>
-   <span data-ttu-id="1ae77-462">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="1ae77-462">get\_accChild</span></span>
-   <span data-ttu-id="1ae77-463">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="1ae77-463">get\_accChildCount</span></span>
-   <span data-ttu-id="1ae77-464">obter \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="1ae77-464">get\_accDescription</span></span>
-   <span data-ttu-id="1ae77-465">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="1ae77-465">get\_accFocus</span></span>
-   <span data-ttu-id="1ae77-466">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-466">get\_accName</span></span>
-   <span data-ttu-id="1ae77-467">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-467">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-468">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-468">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-469">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-469">get\_accState</span></span>
-   <span data-ttu-id="1ae77-470">obter \_ accValue</span><span class="sxs-lookup"><span data-stu-id="1ae77-470">get\_accValue</span></span>

## <a name="role_system_rowheader"></a><span data-ttu-id="1ae77-471">subcabeçalho de sistema de função \_ \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-471">ROLE\_SYSTEM\_ROWHEADER</span></span>

<span data-ttu-id="1ae77-472">Para obter mais informações sobre essa função, consulte [**função do sistema de funções \_ \_**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-472">For more information on this role, see [**ROLE\_SYSTEM\_ROWHEADER**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-473">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-473">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-474">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-474">accHitTest</span></span>
-   <span data-ttu-id="1ae77-475">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-475">accLocation</span></span>
-   <span data-ttu-id="1ae77-476">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-476">accNavigate</span></span>
-   <span data-ttu-id="1ae77-477">accSelect</span><span class="sxs-lookup"><span data-stu-id="1ae77-477">accSelect</span></span>
-   <span data-ttu-id="1ae77-478">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="1ae77-478">get\_accChild</span></span>
-   <span data-ttu-id="1ae77-479">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="1ae77-479">get\_accChildCount</span></span>
-   <span data-ttu-id="1ae77-480">obter \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="1ae77-480">get\_accDefaultAction</span></span>
-   <span data-ttu-id="1ae77-481">obter \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="1ae77-481">get\_accDescription</span></span>
-   <span data-ttu-id="1ae77-482">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="1ae77-482">get\_accFocus</span></span>
-   <span data-ttu-id="1ae77-483">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-483">get\_accName</span></span>
-   <span data-ttu-id="1ae77-484">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-484">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-485">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-485">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-486">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-486">get\_accState</span></span>
-   <span data-ttu-id="1ae77-487">obter \_ accValue</span><span class="sxs-lookup"><span data-stu-id="1ae77-487">get\_accValue</span></span>

## <a name="role_system_separator"></a><span data-ttu-id="1ae77-488">separador de sistema de função \_ \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-488">ROLE\_SYSTEM\_SEPARATOR</span></span>

<span data-ttu-id="1ae77-489">Para obter mais informações sobre essa função, [**consulte \_ \_ separador de sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-489">For more information on this role, see [**ROLE\_SYSTEM\_SEPARATOR**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-490">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-490">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-491">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-491">accHitTest</span></span>
-   <span data-ttu-id="1ae77-492">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-492">accLocation</span></span>
-   <span data-ttu-id="1ae77-493">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="1ae77-493">get\_accChild</span></span>
-   <span data-ttu-id="1ae77-494">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="1ae77-494">get\_accChildCount</span></span>
-   <span data-ttu-id="1ae77-495">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-495">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-496">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-496">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-497">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-497">get\_accState</span></span>

## <a name="role_system_sound"></a><span data-ttu-id="1ae77-498">\_som do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-498">ROLE\_SYSTEM\_SOUND</span></span>

<span data-ttu-id="1ae77-499">Para obter mais informações sobre essa função, [**consulte \_ \_ som do sistema de função**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-499">For more information on this role, see [**ROLE\_SYSTEM\_SOUND**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-500">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-500">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-501">obter \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="1ae77-501">get\_accDescription</span></span>
-   <span data-ttu-id="1ae77-502">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-502">get\_accName</span></span>
-   <span data-ttu-id="1ae77-503">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-503">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-504">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-504">get\_accState</span></span>

## <a name="role_system_splitbutton"></a><span data-ttu-id="1ae77-505">sistema de função \_ \_ SPLITBUTTON</span><span class="sxs-lookup"><span data-stu-id="1ae77-505">ROLE\_SYSTEM\_SPLITBUTTON</span></span>

<span data-ttu-id="1ae77-506">Para obter mais informações sobre essa função, [**consulte \_ sistema \_ de função SPLITBUTTON**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-506">For more information on this role, see [**ROLE\_SYSTEM\_SPLITBUTTON**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-507">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-507">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-508">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="1ae77-508">accDoDefaultAction</span></span>
-   <span data-ttu-id="1ae77-509">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-509">accHitTest</span></span>
-   <span data-ttu-id="1ae77-510">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-510">accLocation</span></span>
-   <span data-ttu-id="1ae77-511">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-511">accNavigate</span></span>
-   <span data-ttu-id="1ae77-512">obter \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="1ae77-512">get\_accDefaultAction</span></span>
-   <span data-ttu-id="1ae77-513">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="1ae77-513">get\_accHelp</span></span>
-   <span data-ttu-id="1ae77-514">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="1ae77-514">get\_accHelpTopic</span></span>
-   <span data-ttu-id="1ae77-515">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="1ae77-515">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="1ae77-516">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-516">get\_accName</span></span>
-   <span data-ttu-id="1ae77-517">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-517">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-518">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-518">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-519">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-519">get\_accState</span></span>

## <a name="role_system_table"></a><span data-ttu-id="1ae77-520">\_tabela do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-520">ROLE\_SYSTEM\_TABLE</span></span>

<span data-ttu-id="1ae77-521">Para obter mais informações sobre essa função, [**consulte \_ \_ tabela do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-521">For more information on this role, see [**ROLE\_SYSTEM\_TABLE**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-522">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-522">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-523">accHitTest</span><span class="sxs-lookup"><span data-stu-id="1ae77-523">accHitTest</span></span>
-   <span data-ttu-id="1ae77-524">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-524">accLocation</span></span>
-   <span data-ttu-id="1ae77-525">accNavigate</span><span class="sxs-lookup"><span data-stu-id="1ae77-525">accNavigate</span></span>
-   <span data-ttu-id="1ae77-526">accSelect</span><span class="sxs-lookup"><span data-stu-id="1ae77-526">accSelect</span></span>
-   <span data-ttu-id="1ae77-527">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="1ae77-527">get\_accChild</span></span>
-   <span data-ttu-id="1ae77-528">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="1ae77-528">get\_accChildCount</span></span>
-   <span data-ttu-id="1ae77-529">obter \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="1ae77-529">get\_accDescription</span></span>
-   <span data-ttu-id="1ae77-530">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="1ae77-530">get\_accFocus</span></span>
-   <span data-ttu-id="1ae77-531">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="1ae77-531">get\_accHelp</span></span>
-   <span data-ttu-id="1ae77-532">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="1ae77-532">get\_accHelpTopic</span></span>
-   <span data-ttu-id="1ae77-533">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="1ae77-533">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="1ae77-534">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="1ae77-534">get\_accName</span></span>
-   <span data-ttu-id="1ae77-535">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-535">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-536">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-536">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-537">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-537">get\_accState</span></span>

## <a name="role_system_whitespace"></a><span data-ttu-id="1ae77-538">espaço em branco do \_ sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="1ae77-538">ROLE\_SYSTEM\_WHITESPACE</span></span>

<span data-ttu-id="1ae77-539">Para obter mais informações sobre essa função, [**consulte \_ espaço em \_ branco do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1ae77-539">For more information on this role, see [**ROLE\_SYSTEM\_WHITESPACE**](object-roles.md).</span></span>

<span data-ttu-id="1ae77-540">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="1ae77-540">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="1ae77-541">accLocation</span><span class="sxs-lookup"><span data-stu-id="1ae77-541">accLocation</span></span>
-   <span data-ttu-id="1ae77-542">accSelect</span><span class="sxs-lookup"><span data-stu-id="1ae77-542">accSelect</span></span>
-   <span data-ttu-id="1ae77-543">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="1ae77-543">get\_accParent</span></span>
-   <span data-ttu-id="1ae77-544">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="1ae77-544">get\_accRole</span></span>
-   <span data-ttu-id="1ae77-545">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="1ae77-545">get\_accState</span></span>

 

 