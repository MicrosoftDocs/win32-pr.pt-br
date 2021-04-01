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
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a><span data-ttu-id="7b05c-103">Outras funções de objeto e métodos com suporte (referência de elemento de interface do usuário do MSAA)</span><span class="sxs-lookup"><span data-stu-id="7b05c-103">Other Object Roles and Supported Methods (MSAA UI Element Reference)</span></span>

<span data-ttu-id="7b05c-104">Este tópico fornece informações sobre funções de objeto que não estão incluídas nos tópicos anteriores para elementos de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="7b05c-104">This topic provides information about object roles that are not included in the previous topics for UI elements.</span></span> <span data-ttu-id="7b05c-105">Cada função de objeto inclui uma lista de métodos e propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) com suporte para a função de objeto.</span><span class="sxs-lookup"><span data-stu-id="7b05c-105">Each object role includes a list of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties that are supported for the object role.</span></span> <span data-ttu-id="7b05c-106">Enquanto outros tópicos documentam métodos e propriedades de **IAccessible** com suporte para elementos de interface do usuário, este tópico lista os métodos e propriedades que você pode esperar que tenham suporte para uma função de objeto específica.</span><span class="sxs-lookup"><span data-stu-id="7b05c-106">While other topics document supported **IAccessible** methods and properties for UI elements, this topic lists the methods and properties you can expect to be supported for a particular object role.</span></span> <span data-ttu-id="7b05c-107">Muitos dos elementos da interface do usuário que podem ter uma das funções listadas aqui normalmente são vistos em navegadores.</span><span class="sxs-lookup"><span data-stu-id="7b05c-107">Many of the UI elements which might have one of the roles listed here are typically seen in browsers.</span></span>

> [!Note]  
> <span data-ttu-id="7b05c-108">Use este tópico como uma diretriz.</span><span class="sxs-lookup"><span data-stu-id="7b05c-108">Use this topic as a guideline.</span></span> <span data-ttu-id="7b05c-109">É altamente recomendável que você use as ferramentas de Acessibilidade Ativa da Microsoft para verificar o comportamento esperado de uma função de objeto individual.</span><span class="sxs-lookup"><span data-stu-id="7b05c-109">We strongly suggest that you use Microsoft Active Accessibility tools to verify expected behavior for an individual object role.</span></span>

 

<span data-ttu-id="7b05c-110">A tabela a seguir lista as funções de objeto adicionais às quais Oleacc.dll dá suporte.</span><span class="sxs-lookup"><span data-stu-id="7b05c-110">The following table lists additional object roles which Oleacc.dll supports.</span></span>



|                                                                         |                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="7b05c-111">**\_alerta do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-111">**ROLE\_SYSTEM\_ALERT**</span></span>](/windows)                           | [<span data-ttu-id="7b05c-112">**\_lista suspensa do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-112">**ROLE\_SYSTEM\_DROPLIST**</span></span>](/windows)       |
| [<span data-ttu-id="7b05c-113">**\_aplicativo do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-113">**ROLE\_SYSTEM\_APPLICATION**</span></span>](/windows)               | [<span data-ttu-id="7b05c-114">**\_equação do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-114">**ROLE\_SYSTEM\_EQUATION**</span></span>](/windows)       |
| [<span data-ttu-id="7b05c-115">**\_borda do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-115">**ROLE\_SYSTEM\_BORDER**</span></span>](/windows)                         | [<span data-ttu-id="7b05c-116">**\_elemento gráfico do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-116">**ROLE\_SYSTEM\_GRAPHIC**</span></span>](/windows)         |
| [<span data-ttu-id="7b05c-117">**\_BUTTONDROPDOWN do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-117">**ROLE\_SYSTEM\_BUTTONDROPDOWN**</span></span>](/windows)         | [<span data-ttu-id="7b05c-118">**\_HELPBALLOON do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-118">**ROLE\_SYSTEM\_HELPBALLOON**</span></span>](/windows) |
| [<span data-ttu-id="7b05c-119">**\_BUTTONDROPDOWNGRID do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-119">**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**</span></span>](/windows) | [<span data-ttu-id="7b05c-120">**\_IPAddress do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-120">**ROLE\_SYSTEM\_IPADDRESS**</span></span>](/windows)     |
| [<span data-ttu-id="7b05c-121">**\_BUTTONMENU do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-121">**ROLE\_SYSTEM\_BUTTONMENU**</span></span>](/windows)                 | [<span data-ttu-id="7b05c-122">**\_link do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-122">**ROLE\_SYSTEM\_LINK**</span></span>](/windows)               |
| [<span data-ttu-id="7b05c-123">**\_célula do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-123">**ROLE\_SYSTEM\_CELL**</span></span>](/windows)                             | [<span data-ttu-id="7b05c-124">**\_painel do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-124">**ROLE\_SYSTEM\_PANE**</span></span>](/windows)               |
| [<span data-ttu-id="7b05c-125">**\_caractere do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-125">**ROLE\_SYSTEM\_CHARACTER**</span></span>](/windows)                   | [<span data-ttu-id="7b05c-126">**\_linha do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-126">**ROLE\_SYSTEM\_ROW**</span></span>](/windows)                 |
| [<span data-ttu-id="7b05c-127">**\_gráfico do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-127">**ROLE\_SYSTEM\_CHART**</span></span>](/windows)                           | [<span data-ttu-id="7b05c-128">**subcabeçalho de sistema de função \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-128">**ROLE\_SYSTEM\_ROWHEADER**</span></span>](/windows)     |
| [<span data-ttu-id="7b05c-129">**\_relógio do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-129">**ROLE\_SYSTEM\_CLOCK**</span></span>](/windows)                           | [<span data-ttu-id="7b05c-130">**separador de sistema de função \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-130">**ROLE\_SYSTEM\_SEPARATOR**</span></span>](/windows)     |
| [<span data-ttu-id="7b05c-131">**\_coluna do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-131">**ROLE\_SYSTEM\_COLUMN**</span></span>](/windows)                         | [<span data-ttu-id="7b05c-132">**\_som do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-132">**ROLE\_SYSTEM\_SOUND**</span></span>](/windows)             |
| [<span data-ttu-id="7b05c-133">**\_diagrama do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-133">**ROLE\_SYSTEM\_DIAGRAM**</span></span>](/windows)                       | [<span data-ttu-id="7b05c-134">**sistema de função \_ \_ SPLITBUTTON**</span><span class="sxs-lookup"><span data-stu-id="7b05c-134">**ROLE\_SYSTEM\_SPLITBUTTON**</span></span>](/windows) |
| [<span data-ttu-id="7b05c-135">**\_discagem do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-135">**ROLE\_SYSTEM\_DIAL**</span></span>](/windows)                             | [<span data-ttu-id="7b05c-136">**\_tabela do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-136">**ROLE\_SYSTEM\_TABLE**</span></span>](/windows)             |
| [<span data-ttu-id="7b05c-137">**\_documento do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-137">**ROLE\_SYSTEM\_DOCUMENT**</span></span>](/windows)                     | [<span data-ttu-id="7b05c-138">**espaço em branco do \_ sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="7b05c-138">**ROLE\_SYSTEM\_WHITESPACE**</span></span>](/windows)   |



 

## <a name="role_system_alert"></a><span data-ttu-id="7b05c-139">\_alerta do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-139">ROLE\_SYSTEM\_ALERT</span></span>

<span data-ttu-id="7b05c-140">Para obter mais informações sobre essa função, [**consulte \_ \_ alerta do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-140">For more information on this role, see [**ROLE\_SYSTEM\_ALERT**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-141">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-141">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-142">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-142">get\_accName</span></span>
-   <span data-ttu-id="7b05c-143">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-143">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-144">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-144">get\_accState</span></span>

## <a name="role_system_application"></a><span data-ttu-id="7b05c-145">\_aplicativo do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-145">ROLE\_SYSTEM\_APPLICATION</span></span>

<span data-ttu-id="7b05c-146">Para obter mais informações sobre essa função, [**consulte \_ \_ aplicativo do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-146">For more information on this role, see [**ROLE\_SYSTEM\_APPLICATION**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-147">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-147">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-148">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-148">accHitTest</span></span>
-   <span data-ttu-id="7b05c-149">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-149">accLocation</span></span>
-   <span data-ttu-id="7b05c-150">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-150">accNavigate</span></span>
-   <span data-ttu-id="7b05c-151">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="7b05c-151">get\_accChild</span></span>
-   <span data-ttu-id="7b05c-152">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="7b05c-152">get\_accChildCount</span></span>
-   <span data-ttu-id="7b05c-153">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="7b05c-153">get\_accFocus</span></span>
-   <span data-ttu-id="7b05c-154">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="7b05c-154">get\_accHelp</span></span>
-   <span data-ttu-id="7b05c-155">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="7b05c-155">get\_accHelpTopic</span></span>
-   <span data-ttu-id="7b05c-156">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="7b05c-156">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="7b05c-157">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-157">get\_accName</span></span>
-   <span data-ttu-id="7b05c-158">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-158">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-159">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-159">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-160">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-160">get\_accState</span></span>

## <a name="role_system_border"></a><span data-ttu-id="7b05c-161">\_borda do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-161">ROLE\_SYSTEM\_BORDER</span></span>

<span data-ttu-id="7b05c-162">Para obter mais informações sobre essa função, [**consulte \_ \_ borda do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-162">For more information on this role, see [**ROLE\_SYSTEM\_BORDER**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-163">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-163">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-164">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-164">accHitTest</span></span>
-   <span data-ttu-id="7b05c-165">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-165">accLocation</span></span>
-   <span data-ttu-id="7b05c-166">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-166">accNavigate</span></span>
-   <span data-ttu-id="7b05c-167">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-167">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-168">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-168">get\_accState</span></span>

## <a name="role_system_buttondropdown"></a><span data-ttu-id="7b05c-169">\_BUTTONDROPDOWN do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-169">ROLE\_SYSTEM\_BUTTONDROPDOWN</span></span>

<span data-ttu-id="7b05c-170">Para obter mais informações sobre essa função, [**consulte \_ sistema \_ de funções BUTTONDROPDOWN**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-170">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWN**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-171">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-171">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-172">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="7b05c-172">accDoDefaultAction</span></span>
-   <span data-ttu-id="7b05c-173">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-173">accHitTest</span></span>
-   <span data-ttu-id="7b05c-174">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-174">accLocation</span></span>
-   <span data-ttu-id="7b05c-175">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-175">accNavigate</span></span>
-   <span data-ttu-id="7b05c-176">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="7b05c-176">get\_accChild</span></span>
-   <span data-ttu-id="7b05c-177">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="7b05c-177">get\_accChildCount</span></span>
-   <span data-ttu-id="7b05c-178">obter \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="7b05c-178">get\_accDefaultAction</span></span>
-   <span data-ttu-id="7b05c-179">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="7b05c-179">get\_accFocus</span></span>
-   <span data-ttu-id="7b05c-180">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="7b05c-180">get\_accHelp</span></span>
-   <span data-ttu-id="7b05c-181">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="7b05c-181">get\_accHelpTopic</span></span>
-   <span data-ttu-id="7b05c-182">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="7b05c-182">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="7b05c-183">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-183">get\_accName</span></span>
-   <span data-ttu-id="7b05c-184">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-184">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-185">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-185">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-186">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-186">get\_accState</span></span>

## <a name="role_system_buttondropdowngrid"></a><span data-ttu-id="7b05c-187">\_BUTTONDROPDOWNGRID do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-187">ROLE\_SYSTEM\_BUTTONDROPDOWNGRID</span></span>

<span data-ttu-id="7b05c-188">Para obter mais informações sobre essa função, [**consulte \_ sistema \_ de funções BUTTONDROPDOWNGRID**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-188">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-189">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-189">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-190">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="7b05c-190">accDoDefaultAction</span></span>
-   <span data-ttu-id="7b05c-191">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-191">accHitTest</span></span>
-   <span data-ttu-id="7b05c-192">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-192">accLocation</span></span>
-   <span data-ttu-id="7b05c-193">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-193">accNavigate</span></span>
-   <span data-ttu-id="7b05c-194">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="7b05c-194">get\_accChild</span></span>
-   <span data-ttu-id="7b05c-195">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="7b05c-195">get\_accChildCount</span></span>
-   <span data-ttu-id="7b05c-196">obter \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="7b05c-196">get\_accDefaultAction</span></span>
-   <span data-ttu-id="7b05c-197">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="7b05c-197">get\_accFocus</span></span>
-   <span data-ttu-id="7b05c-198">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="7b05c-198">get\_accHelp</span></span>
-   <span data-ttu-id="7b05c-199">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="7b05c-199">get\_accHelpTopic</span></span>
-   <span data-ttu-id="7b05c-200">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="7b05c-200">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="7b05c-201">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-201">get\_accName</span></span>
-   <span data-ttu-id="7b05c-202">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-202">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-203">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-203">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-204">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-204">get\_accState</span></span>

## <a name="role_system_buttonmenu"></a><span data-ttu-id="7b05c-205">\_BUTTONMENU do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-205">ROLE\_SYSTEM\_BUTTONMENU</span></span>

<span data-ttu-id="7b05c-206">Para obter mais informações sobre essa função, [**consulte \_ sistema \_ de funções BUTTONMENU**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-206">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONMENU**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-207">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-207">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-208">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="7b05c-208">accDoDefaultAction</span></span>
-   <span data-ttu-id="7b05c-209">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-209">accHitTest</span></span>
-   <span data-ttu-id="7b05c-210">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-210">accLocation</span></span>
-   <span data-ttu-id="7b05c-211">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-211">accNavigate</span></span>
-   <span data-ttu-id="7b05c-212">obter \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="7b05c-212">get\_accDefaultAction</span></span>
-   <span data-ttu-id="7b05c-213">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="7b05c-213">get\_accFocus</span></span>
-   <span data-ttu-id="7b05c-214">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="7b05c-214">get\_accHelp</span></span>
-   <span data-ttu-id="7b05c-215">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="7b05c-215">get\_accHelpTopic</span></span>
-   <span data-ttu-id="7b05c-216">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="7b05c-216">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="7b05c-217">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-217">get\_accName</span></span>
-   <span data-ttu-id="7b05c-218">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-218">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-219">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-219">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-220">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-220">get\_accState</span></span>

## <a name="role_system_cell"></a><span data-ttu-id="7b05c-221">\_célula do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-221">ROLE\_SYSTEM\_CELL</span></span>

<span data-ttu-id="7b05c-222">Para obter mais informações sobre essa função, [**consulte \_ \_ célula do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-222">For more information on this role, see [**ROLE\_SYSTEM\_CELL**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-223">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-223">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-224">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-224">accHitTest</span></span>
-   <span data-ttu-id="7b05c-225">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-225">accLocation</span></span>
-   <span data-ttu-id="7b05c-226">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-226">accNavigate</span></span>
-   <span data-ttu-id="7b05c-227">accSelect</span><span class="sxs-lookup"><span data-stu-id="7b05c-227">accSelect</span></span>
-   <span data-ttu-id="7b05c-228">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="7b05c-228">get\_accChild</span></span>
-   <span data-ttu-id="7b05c-229">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="7b05c-229">get\_accChildCount</span></span>
-   <span data-ttu-id="7b05c-230">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="7b05c-230">get\_accFocus</span></span>
-   <span data-ttu-id="7b05c-231">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="7b05c-231">get\_accHelp</span></span>
-   <span data-ttu-id="7b05c-232">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="7b05c-232">get\_accHelpTopic</span></span>
-   <span data-ttu-id="7b05c-233">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="7b05c-233">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="7b05c-234">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-234">get\_accName</span></span>
-   <span data-ttu-id="7b05c-235">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-235">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-236">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-236">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-237">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-237">get\_accState</span></span>
-   <span data-ttu-id="7b05c-238">obter \_ accValue</span><span class="sxs-lookup"><span data-stu-id="7b05c-238">get\_accValue</span></span>

## <a name="role_system_character"></a><span data-ttu-id="7b05c-239">\_caractere do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-239">ROLE\_SYSTEM\_CHARACTER</span></span>

<span data-ttu-id="7b05c-240">Para obter mais informações sobre essa função, consulte [**função do \_ \_ caractere do sistema**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-240">For more information on this role, see [**ROLE\_SYSTEM\_CHARACTER**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-241">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-241">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-242">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-242">accHitTest</span></span>
-   <span data-ttu-id="7b05c-243">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-243">accLocation</span></span>
-   <span data-ttu-id="7b05c-244">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-244">accNavigate</span></span>
-   <span data-ttu-id="7b05c-245">obter \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="7b05c-245">get\_accDescription</span></span>
-   <span data-ttu-id="7b05c-246">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="7b05c-246">get\_accFocus</span></span>
-   <span data-ttu-id="7b05c-247">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="7b05c-247">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="7b05c-248">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-248">get\_accName</span></span>
-   <span data-ttu-id="7b05c-249">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-249">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-250">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-250">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-251">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-251">get\_accState</span></span>
-   <span data-ttu-id="7b05c-252">obter \_ accValue</span><span class="sxs-lookup"><span data-stu-id="7b05c-252">get\_accValue</span></span>

## <a name="role_system_chart"></a><span data-ttu-id="7b05c-253">\_gráfico do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-253">ROLE\_SYSTEM\_CHART</span></span>

<span data-ttu-id="7b05c-254">Para obter mais informações sobre essa função, [**consulte \_ \_ gráfico do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-254">For more information on this role, see [**ROLE\_SYSTEM\_CHART**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-255">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-255">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-256">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-256">accHitTest</span></span>
-   <span data-ttu-id="7b05c-257">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-257">accLocation</span></span>
-   <span data-ttu-id="7b05c-258">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-258">accNavigate</span></span>
-   <span data-ttu-id="7b05c-259">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="7b05c-259">get\_accChild</span></span>
-   <span data-ttu-id="7b05c-260">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="7b05c-260">get\_accChildCount</span></span>
-   <span data-ttu-id="7b05c-261">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="7b05c-261">get\_accFocus</span></span>
-   <span data-ttu-id="7b05c-262">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="7b05c-262">get\_accHelp</span></span>
-   <span data-ttu-id="7b05c-263">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="7b05c-263">get\_accHelpTopic</span></span>
-   <span data-ttu-id="7b05c-264">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="7b05c-264">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="7b05c-265">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-265">get\_accName</span></span>
-   <span data-ttu-id="7b05c-266">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-266">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-267">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-267">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-268">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-268">get\_accState</span></span>

## <a name="role_system_clock"></a><span data-ttu-id="7b05c-269">\_relógio do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-269">ROLE\_SYSTEM\_CLOCK</span></span>

<span data-ttu-id="7b05c-270">Para obter mais informações sobre essa função, [**consulte \_ \_ relógio do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-270">For more information on this role, see [**ROLE\_SYSTEM\_CLOCK**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-271">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-271">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-272">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-272">accHitTest</span></span>
-   <span data-ttu-id="7b05c-273">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-273">accLocation</span></span>
-   <span data-ttu-id="7b05c-274">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-274">accNavigate</span></span>
-   <span data-ttu-id="7b05c-275">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="7b05c-275">get\_accFocus</span></span>
-   <span data-ttu-id="7b05c-276">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="7b05c-276">get\_accHelp</span></span>
-   <span data-ttu-id="7b05c-277">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="7b05c-277">get\_accHelpTopic</span></span>
-   <span data-ttu-id="7b05c-278">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="7b05c-278">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="7b05c-279">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-279">get\_accName</span></span>
-   <span data-ttu-id="7b05c-280">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-280">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-281">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-281">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-282">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-282">get\_accState</span></span>
-   <span data-ttu-id="7b05c-283">obter \_ accValue</span><span class="sxs-lookup"><span data-stu-id="7b05c-283">get\_accValue</span></span>

## <a name="role_system_column"></a><span data-ttu-id="7b05c-284">\_coluna do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-284">ROLE\_SYSTEM\_COLUMN</span></span>

<span data-ttu-id="7b05c-285">Para obter mais informações sobre essa função, [**consulte \_ \_ coluna do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-285">For more information on this role, see [**ROLE\_SYSTEM\_COLUMN**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-286">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-286">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-287">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-287">accHitTest</span></span>
-   <span data-ttu-id="7b05c-288">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-288">accLocation</span></span>
-   <span data-ttu-id="7b05c-289">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-289">accNavigate</span></span>
-   <span data-ttu-id="7b05c-290">accSelect</span><span class="sxs-lookup"><span data-stu-id="7b05c-290">accSelect</span></span>
-   <span data-ttu-id="7b05c-291">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="7b05c-291">get\_accChild</span></span>
-   <span data-ttu-id="7b05c-292">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="7b05c-292">get\_accChildCount</span></span>
-   <span data-ttu-id="7b05c-293">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="7b05c-293">get\_accFocus</span></span>
-   <span data-ttu-id="7b05c-294">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-294">get\_accName</span></span>
-   <span data-ttu-id="7b05c-295">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-295">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-296">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-296">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-297">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-297">get\_accState</span></span>
-   <span data-ttu-id="7b05c-298">obter \_ accValue</span><span class="sxs-lookup"><span data-stu-id="7b05c-298">get\_accValue</span></span>

## <a name="role_system_diagram"></a><span data-ttu-id="7b05c-299">\_diagrama do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-299">ROLE\_SYSTEM\_DIAGRAM</span></span>

<span data-ttu-id="7b05c-300">Para obter mais informações sobre essa função, [**consulte \_ \_ diagrama do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-300">For more information on this role, see [**ROLE\_SYSTEM\_DIAGRAM**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-301">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-301">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-302">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-302">accHitTest</span></span>
-   <span data-ttu-id="7b05c-303">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-303">accLocation</span></span>
-   <span data-ttu-id="7b05c-304">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-304">accNavigate</span></span>
-   <span data-ttu-id="7b05c-305">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="7b05c-305">get\_accChild</span></span>
-   <span data-ttu-id="7b05c-306">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="7b05c-306">get\_accChildCount</span></span>
-   <span data-ttu-id="7b05c-307">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="7b05c-307">get\_accFocus</span></span>
-   <span data-ttu-id="7b05c-308">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="7b05c-308">get\_accHelp</span></span>
-   <span data-ttu-id="7b05c-309">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="7b05c-309">get\_accHelpTopic</span></span>
-   <span data-ttu-id="7b05c-310">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="7b05c-310">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="7b05c-311">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-311">get\_accName</span></span>
-   <span data-ttu-id="7b05c-312">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-312">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-313">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-313">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-314">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-314">get\_accState</span></span>

## <a name="role_system_dial"></a><span data-ttu-id="7b05c-315">\_discagem do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-315">ROLE\_SYSTEM\_DIAL</span></span>

<span data-ttu-id="7b05c-316">Para obter mais informações sobre essa função, consulte [**role \_ System \_ Dial**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-316">For more information on this role, see [**ROLE\_SYSTEM\_DIAL**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-317">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-317">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-318">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="7b05c-318">accDoDefaultAction</span></span>
-   <span data-ttu-id="7b05c-319">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-319">accHitTest</span></span>
-   <span data-ttu-id="7b05c-320">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-320">accLocation</span></span>
-   <span data-ttu-id="7b05c-321">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-321">accNavigate</span></span>
-   <span data-ttu-id="7b05c-322">obter \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="7b05c-322">get\_accDefaultAction</span></span>
-   <span data-ttu-id="7b05c-323">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="7b05c-323">get\_accFocus</span></span>
-   <span data-ttu-id="7b05c-324">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="7b05c-324">get\_accHelp</span></span>
-   <span data-ttu-id="7b05c-325">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="7b05c-325">get\_accHelpTopic</span></span>
-   <span data-ttu-id="7b05c-326">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="7b05c-326">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="7b05c-327">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-327">get\_accName</span></span>
-   <span data-ttu-id="7b05c-328">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-328">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-329">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-329">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-330">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-330">get\_accState</span></span>
-   <span data-ttu-id="7b05c-331">obter \_ accValue</span><span class="sxs-lookup"><span data-stu-id="7b05c-331">get\_accValue</span></span>

## <a name="role_system_document"></a><span data-ttu-id="7b05c-332">\_documento do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-332">ROLE\_SYSTEM\_DOCUMENT</span></span>

<span data-ttu-id="7b05c-333">Para obter mais informações sobre essa função, [**consulte \_ \_ documento do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-333">For more information on this role, see [**ROLE\_SYSTEM\_DOCUMENT**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-334">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-334">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-335">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-335">accHitTest</span></span>
-   <span data-ttu-id="7b05c-336">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-336">accLocation</span></span>
-   <span data-ttu-id="7b05c-337">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-337">accNavigate</span></span>
-   <span data-ttu-id="7b05c-338">accSelect</span><span class="sxs-lookup"><span data-stu-id="7b05c-338">accSelect</span></span>
-   <span data-ttu-id="7b05c-339">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="7b05c-339">get\_accChild</span></span>
-   <span data-ttu-id="7b05c-340">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="7b05c-340">get\_accChildCount</span></span>
-   <span data-ttu-id="7b05c-341">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="7b05c-341">get\_accFocus</span></span>
-   <span data-ttu-id="7b05c-342">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-342">get\_accName</span></span>
-   <span data-ttu-id="7b05c-343">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-343">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-344">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-344">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-345">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-345">get\_accState</span></span>

## <a name="role_system_droplist"></a><span data-ttu-id="7b05c-346">\_lista suspensa do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-346">ROLE\_SYSTEM\_DROPLIST</span></span>

<span data-ttu-id="7b05c-347">Para obter mais informações sobre essa função, [**consulte \_ \_ lista suspensa do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-347">For more information on this role, see [**ROLE\_SYSTEM\_DROPLIST**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-348">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-348">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-349">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="7b05c-349">accDoDefaultAction</span></span>
-   <span data-ttu-id="7b05c-350">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-350">accHitTest</span></span>
-   <span data-ttu-id="7b05c-351">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-351">accLocation</span></span>
-   <span data-ttu-id="7b05c-352">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-352">accNavigate</span></span>
-   <span data-ttu-id="7b05c-353">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="7b05c-353">get\_accChild</span></span>
-   <span data-ttu-id="7b05c-354">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="7b05c-354">get\_accChildCount</span></span>
-   <span data-ttu-id="7b05c-355">obter \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="7b05c-355">get\_accDefaultAction</span></span>
-   <span data-ttu-id="7b05c-356">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="7b05c-356">get\_accFocus</span></span>
-   <span data-ttu-id="7b05c-357">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="7b05c-357">get\_accHelp</span></span>
-   <span data-ttu-id="7b05c-358">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="7b05c-358">get\_accHelpTopic</span></span>
-   <span data-ttu-id="7b05c-359">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="7b05c-359">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="7b05c-360">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-360">get\_accName</span></span>
-   <span data-ttu-id="7b05c-361">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-361">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-362">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-362">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-363">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-363">get\_accState</span></span>

## <a name="role_system_equation"></a><span data-ttu-id="7b05c-364">\_equação do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-364">ROLE\_SYSTEM\_EQUATION</span></span>

<span data-ttu-id="7b05c-365">Para obter mais informações sobre essa função, [**consulte \_ \_ equação do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-365">For more information on this role, see [**ROLE\_SYSTEM\_EQUATION**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-366">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-366">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-367">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-367">accHitTest</span></span>
-   <span data-ttu-id="7b05c-368">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-368">accLocation</span></span>
-   <span data-ttu-id="7b05c-369">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-369">accNavigate</span></span>
-   <span data-ttu-id="7b05c-370">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="7b05c-370">get\_accFocus</span></span>
-   <span data-ttu-id="7b05c-371">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-371">get\_accName</span></span>
-   <span data-ttu-id="7b05c-372">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-372">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-373">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-373">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-374">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-374">get\_accState</span></span>
-   <span data-ttu-id="7b05c-375">obter \_ accValue</span><span class="sxs-lookup"><span data-stu-id="7b05c-375">get\_accValue</span></span>

## <a name="role_system_graphic"></a><span data-ttu-id="7b05c-376">\_elemento gráfico do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-376">ROLE\_SYSTEM\_GRAPHIC</span></span>

<span data-ttu-id="7b05c-377">Para obter mais informações sobre essa função, [**consulte \_ \_ elemento gráfico do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-377">For more information on this role, see [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-378">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-378">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-379">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-379">accHitTest</span></span>
-   <span data-ttu-id="7b05c-380">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-380">accLocation</span></span>
-   <span data-ttu-id="7b05c-381">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-381">accNavigate</span></span>
-   <span data-ttu-id="7b05c-382">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="7b05c-382">get\_accFocus</span></span>
-   <span data-ttu-id="7b05c-383">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="7b05c-383">get\_accHelp</span></span>
-   <span data-ttu-id="7b05c-384">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="7b05c-384">get\_accHelpTopic</span></span>
-   <span data-ttu-id="7b05c-385">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="7b05c-385">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="7b05c-386">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-386">get\_accName</span></span>
-   <span data-ttu-id="7b05c-387">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-387">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-388">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-388">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-389">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-389">get\_accState</span></span>

## <a name="role_system_helpballoon"></a><span data-ttu-id="7b05c-390">\_HELPBALLOON do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-390">ROLE\_SYSTEM\_HELPBALLOON</span></span>

<span data-ttu-id="7b05c-391">Para obter mais informações sobre essa função, [**consulte \_ sistema \_ de funções HELPBALLOON**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-391">For more information on this role, see [**ROLE\_SYSTEM\_HELPBALLOON**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-392">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-392">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-393">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-393">accHitTest</span></span>
-   <span data-ttu-id="7b05c-394">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-394">accLocation</span></span>
-   <span data-ttu-id="7b05c-395">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-395">accNavigate</span></span>
-   <span data-ttu-id="7b05c-396">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="7b05c-396">get\_accChild</span></span>
-   <span data-ttu-id="7b05c-397">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="7b05c-397">get\_accChildCount</span></span>
-   <span data-ttu-id="7b05c-398">obter \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="7b05c-398">get\_accDefaultAction</span></span>
-   <span data-ttu-id="7b05c-399">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-399">get\_accName</span></span>
-   <span data-ttu-id="7b05c-400">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-400">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-401">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-401">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-402">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-402">get\_accState</span></span>
-   <span data-ttu-id="7b05c-403">obter \_ accValue</span><span class="sxs-lookup"><span data-stu-id="7b05c-403">get\_accValue</span></span>

## <a name="role_system_ipaddress"></a><span data-ttu-id="7b05c-404">\_IPAddress do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-404">ROLE\_SYSTEM\_IPADDRESS</span></span>

<span data-ttu-id="7b05c-405">Para obter mais informações sobre essa função, [**consulte \_ \_ IPAddress do sistema de função**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-405">For more information on this role, see [**ROLE\_SYSTEM\_IPADDRESS**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-406">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-406">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-407">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-407">accHitTest</span></span>
-   <span data-ttu-id="7b05c-408">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-408">accLocation</span></span>
-   <span data-ttu-id="7b05c-409">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-409">accNavigate</span></span>
-   <span data-ttu-id="7b05c-410">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="7b05c-410">get\_accChild</span></span>
-   <span data-ttu-id="7b05c-411">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="7b05c-411">get\_accChildCount</span></span>
-   <span data-ttu-id="7b05c-412">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="7b05c-412">get\_accFocus</span></span>
-   <span data-ttu-id="7b05c-413">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="7b05c-413">get\_accHelp</span></span>
-   <span data-ttu-id="7b05c-414">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="7b05c-414">get\_accHelpTopic</span></span>
-   <span data-ttu-id="7b05c-415">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="7b05c-415">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="7b05c-416">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-416">get\_accName</span></span>
-   <span data-ttu-id="7b05c-417">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-417">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-418">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-418">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-419">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-419">get\_accState</span></span>
-   <span data-ttu-id="7b05c-420">obter \_ accValue</span><span class="sxs-lookup"><span data-stu-id="7b05c-420">get\_accValue</span></span>

## <a name="role_system_link"></a><span data-ttu-id="7b05c-421">\_link do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-421">ROLE\_SYSTEM\_LINK</span></span>

<span data-ttu-id="7b05c-422">Para obter mais informações sobre essa função, [**consulte \_ \_ link do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-422">For more information on this role, see [**ROLE\_SYSTEM\_LINK**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-423">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-423">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-424">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="7b05c-424">accDoDefaultAction</span></span>
-   <span data-ttu-id="7b05c-425">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-425">accHitTest</span></span>
-   <span data-ttu-id="7b05c-426">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-426">accLocation</span></span>
-   <span data-ttu-id="7b05c-427">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-427">accNavigate</span></span>
-   <span data-ttu-id="7b05c-428">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="7b05c-428">get\_accChild</span></span>
-   <span data-ttu-id="7b05c-429">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="7b05c-429">get\_accChildCount</span></span>
-   <span data-ttu-id="7b05c-430">obter \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="7b05c-430">get\_accDefaultAction</span></span>
-   <span data-ttu-id="7b05c-431">obter \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="7b05c-431">get\_accDescription</span></span>
-   <span data-ttu-id="7b05c-432">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="7b05c-432">get\_accFocus</span></span>
-   <span data-ttu-id="7b05c-433">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="7b05c-433">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="7b05c-434">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-434">get\_accName</span></span>
-   <span data-ttu-id="7b05c-435">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-435">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-436">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-436">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-437">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-437">get\_accState</span></span>
-   <span data-ttu-id="7b05c-438">obter \_ accValue</span><span class="sxs-lookup"><span data-stu-id="7b05c-438">get\_accValue</span></span>

## <a name="role_system_pane"></a><span data-ttu-id="7b05c-439">\_painel do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-439">ROLE\_SYSTEM\_PANE</span></span>

<span data-ttu-id="7b05c-440">Para obter mais informações sobre essa função, [**consulte \_ \_ painel do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-440">For more information on this role, see [**ROLE\_SYSTEM\_PANE**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-441">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-441">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-442">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-442">accHitTest</span></span>
-   <span data-ttu-id="7b05c-443">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-443">accLocation</span></span>
-   <span data-ttu-id="7b05c-444">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-444">accNavigate</span></span>
-   <span data-ttu-id="7b05c-445">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="7b05c-445">get\_accChild</span></span>
-   <span data-ttu-id="7b05c-446">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="7b05c-446">get\_accChildCount</span></span>
-   <span data-ttu-id="7b05c-447">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="7b05c-447">get\_accFocus</span></span>
-   <span data-ttu-id="7b05c-448">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="7b05c-448">get\_accHelp</span></span>
-   <span data-ttu-id="7b05c-449">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="7b05c-449">get\_accHelpTopic</span></span>
-   <span data-ttu-id="7b05c-450">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="7b05c-450">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="7b05c-451">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-451">get\_accName</span></span>
-   <span data-ttu-id="7b05c-452">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-452">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-453">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-453">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-454">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-454">get\_accState</span></span>

## <a name="role_system_row"></a><span data-ttu-id="7b05c-455">\_linha do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-455">ROLE\_SYSTEM\_ROW</span></span>

<span data-ttu-id="7b05c-456">Para obter mais informações sobre essa função, [**consulte \_ \_ linha do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-456">For more information on this role, see [**ROLE\_SYSTEM\_ROW**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-457">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-457">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-458">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-458">accHitTest</span></span>
-   <span data-ttu-id="7b05c-459">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-459">accLocation</span></span>
-   <span data-ttu-id="7b05c-460">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-460">accNavigate</span></span>
-   <span data-ttu-id="7b05c-461">accSelect</span><span class="sxs-lookup"><span data-stu-id="7b05c-461">accSelect</span></span>
-   <span data-ttu-id="7b05c-462">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="7b05c-462">get\_accChild</span></span>
-   <span data-ttu-id="7b05c-463">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="7b05c-463">get\_accChildCount</span></span>
-   <span data-ttu-id="7b05c-464">obter \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="7b05c-464">get\_accDescription</span></span>
-   <span data-ttu-id="7b05c-465">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="7b05c-465">get\_accFocus</span></span>
-   <span data-ttu-id="7b05c-466">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-466">get\_accName</span></span>
-   <span data-ttu-id="7b05c-467">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-467">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-468">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-468">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-469">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-469">get\_accState</span></span>
-   <span data-ttu-id="7b05c-470">obter \_ accValue</span><span class="sxs-lookup"><span data-stu-id="7b05c-470">get\_accValue</span></span>

## <a name="role_system_rowheader"></a><span data-ttu-id="7b05c-471">subcabeçalho de sistema de função \_ \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-471">ROLE\_SYSTEM\_ROWHEADER</span></span>

<span data-ttu-id="7b05c-472">Para obter mais informações sobre essa função, consulte [**função do sistema de funções \_ \_**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-472">For more information on this role, see [**ROLE\_SYSTEM\_ROWHEADER**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-473">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-473">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-474">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-474">accHitTest</span></span>
-   <span data-ttu-id="7b05c-475">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-475">accLocation</span></span>
-   <span data-ttu-id="7b05c-476">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-476">accNavigate</span></span>
-   <span data-ttu-id="7b05c-477">accSelect</span><span class="sxs-lookup"><span data-stu-id="7b05c-477">accSelect</span></span>
-   <span data-ttu-id="7b05c-478">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="7b05c-478">get\_accChild</span></span>
-   <span data-ttu-id="7b05c-479">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="7b05c-479">get\_accChildCount</span></span>
-   <span data-ttu-id="7b05c-480">obter \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="7b05c-480">get\_accDefaultAction</span></span>
-   <span data-ttu-id="7b05c-481">obter \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="7b05c-481">get\_accDescription</span></span>
-   <span data-ttu-id="7b05c-482">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="7b05c-482">get\_accFocus</span></span>
-   <span data-ttu-id="7b05c-483">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-483">get\_accName</span></span>
-   <span data-ttu-id="7b05c-484">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-484">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-485">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-485">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-486">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-486">get\_accState</span></span>
-   <span data-ttu-id="7b05c-487">obter \_ accValue</span><span class="sxs-lookup"><span data-stu-id="7b05c-487">get\_accValue</span></span>

## <a name="role_system_separator"></a><span data-ttu-id="7b05c-488">separador de sistema de função \_ \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-488">ROLE\_SYSTEM\_SEPARATOR</span></span>

<span data-ttu-id="7b05c-489">Para obter mais informações sobre essa função, [**consulte \_ \_ separador de sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-489">For more information on this role, see [**ROLE\_SYSTEM\_SEPARATOR**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-490">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-490">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-491">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-491">accHitTest</span></span>
-   <span data-ttu-id="7b05c-492">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-492">accLocation</span></span>
-   <span data-ttu-id="7b05c-493">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="7b05c-493">get\_accChild</span></span>
-   <span data-ttu-id="7b05c-494">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="7b05c-494">get\_accChildCount</span></span>
-   <span data-ttu-id="7b05c-495">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-495">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-496">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-496">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-497">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-497">get\_accState</span></span>

## <a name="role_system_sound"></a><span data-ttu-id="7b05c-498">\_som do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-498">ROLE\_SYSTEM\_SOUND</span></span>

<span data-ttu-id="7b05c-499">Para obter mais informações sobre essa função, [**consulte \_ \_ som do sistema de função**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-499">For more information on this role, see [**ROLE\_SYSTEM\_SOUND**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-500">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-500">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-501">obter \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="7b05c-501">get\_accDescription</span></span>
-   <span data-ttu-id="7b05c-502">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-502">get\_accName</span></span>
-   <span data-ttu-id="7b05c-503">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-503">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-504">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-504">get\_accState</span></span>

## <a name="role_system_splitbutton"></a><span data-ttu-id="7b05c-505">sistema de função \_ \_ SPLITBUTTON</span><span class="sxs-lookup"><span data-stu-id="7b05c-505">ROLE\_SYSTEM\_SPLITBUTTON</span></span>

<span data-ttu-id="7b05c-506">Para obter mais informações sobre essa função, [**consulte \_ sistema \_ de função SPLITBUTTON**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-506">For more information on this role, see [**ROLE\_SYSTEM\_SPLITBUTTON**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-507">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-507">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-508">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="7b05c-508">accDoDefaultAction</span></span>
-   <span data-ttu-id="7b05c-509">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-509">accHitTest</span></span>
-   <span data-ttu-id="7b05c-510">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-510">accLocation</span></span>
-   <span data-ttu-id="7b05c-511">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-511">accNavigate</span></span>
-   <span data-ttu-id="7b05c-512">obter \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="7b05c-512">get\_accDefaultAction</span></span>
-   <span data-ttu-id="7b05c-513">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="7b05c-513">get\_accHelp</span></span>
-   <span data-ttu-id="7b05c-514">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="7b05c-514">get\_accHelpTopic</span></span>
-   <span data-ttu-id="7b05c-515">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="7b05c-515">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="7b05c-516">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-516">get\_accName</span></span>
-   <span data-ttu-id="7b05c-517">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-517">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-518">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-518">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-519">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-519">get\_accState</span></span>

## <a name="role_system_table"></a><span data-ttu-id="7b05c-520">\_tabela do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-520">ROLE\_SYSTEM\_TABLE</span></span>

<span data-ttu-id="7b05c-521">Para obter mais informações sobre essa função, [**consulte \_ \_ tabela do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-521">For more information on this role, see [**ROLE\_SYSTEM\_TABLE**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-522">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-522">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-523">accHitTest</span><span class="sxs-lookup"><span data-stu-id="7b05c-523">accHitTest</span></span>
-   <span data-ttu-id="7b05c-524">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-524">accLocation</span></span>
-   <span data-ttu-id="7b05c-525">accNavigate</span><span class="sxs-lookup"><span data-stu-id="7b05c-525">accNavigate</span></span>
-   <span data-ttu-id="7b05c-526">accSelect</span><span class="sxs-lookup"><span data-stu-id="7b05c-526">accSelect</span></span>
-   <span data-ttu-id="7b05c-527">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="7b05c-527">get\_accChild</span></span>
-   <span data-ttu-id="7b05c-528">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="7b05c-528">get\_accChildCount</span></span>
-   <span data-ttu-id="7b05c-529">obter \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="7b05c-529">get\_accDescription</span></span>
-   <span data-ttu-id="7b05c-530">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="7b05c-530">get\_accFocus</span></span>
-   <span data-ttu-id="7b05c-531">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="7b05c-531">get\_accHelp</span></span>
-   <span data-ttu-id="7b05c-532">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="7b05c-532">get\_accHelpTopic</span></span>
-   <span data-ttu-id="7b05c-533">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="7b05c-533">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="7b05c-534">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="7b05c-534">get\_accName</span></span>
-   <span data-ttu-id="7b05c-535">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-535">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-536">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-536">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-537">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-537">get\_accState</span></span>

## <a name="role_system_whitespace"></a><span data-ttu-id="7b05c-538">espaço em branco do \_ sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="7b05c-538">ROLE\_SYSTEM\_WHITESPACE</span></span>

<span data-ttu-id="7b05c-539">Para obter mais informações sobre essa função, [**consulte \_ espaço em \_ branco do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7b05c-539">For more information on this role, see [**ROLE\_SYSTEM\_WHITESPACE**](object-roles.md).</span></span>

<span data-ttu-id="7b05c-540">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="7b05c-540">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="7b05c-541">accLocation</span><span class="sxs-lookup"><span data-stu-id="7b05c-541">accLocation</span></span>
-   <span data-ttu-id="7b05c-542">accSelect</span><span class="sxs-lookup"><span data-stu-id="7b05c-542">accSelect</span></span>
-   <span data-ttu-id="7b05c-543">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="7b05c-543">get\_accParent</span></span>
-   <span data-ttu-id="7b05c-544">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="7b05c-544">get\_accRole</span></span>
-   <span data-ttu-id="7b05c-545">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="7b05c-545">get\_accState</span></span>

 

 