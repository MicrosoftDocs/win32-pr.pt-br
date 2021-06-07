---
title: Outras funções de objeto e métodos com suporte (referência de elemento de interface do usuário do MSAA)
description: Este tópico fornece informações sobre funções de objeto que não estão incluídas nos tópicos anteriores para elementos de interface do usuário.
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17e8573142a57e0acf08980895fdae3ea6d1841
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443997"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a><span data-ttu-id="faa1b-103">Outras funções de objeto e métodos com suporte (referência de elemento de interface do usuário do MSAA)</span><span class="sxs-lookup"><span data-stu-id="faa1b-103">Other Object Roles and Supported Methods (MSAA UI Element Reference)</span></span>

<span data-ttu-id="faa1b-104">Este tópico fornece informações sobre funções de objeto que não estão incluídas nos tópicos anteriores para elementos de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="faa1b-104">This topic provides information about object roles that are not included in the previous topics for UI elements.</span></span> <span data-ttu-id="faa1b-105">Cada função de objeto inclui uma lista de métodos e propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) com suporte para a função de objeto.</span><span class="sxs-lookup"><span data-stu-id="faa1b-105">Each object role includes a list of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties that are supported for the object role.</span></span> <span data-ttu-id="faa1b-106">Enquanto outros tópicos documentam métodos e propriedades de **IAccessible** com suporte para elementos de interface do usuário, este tópico lista os métodos e propriedades que você pode esperar que tenham suporte para uma função de objeto específica.</span><span class="sxs-lookup"><span data-stu-id="faa1b-106">While other topics document supported **IAccessible** methods and properties for UI elements, this topic lists the methods and properties you can expect to be supported for a particular object role.</span></span> <span data-ttu-id="faa1b-107">Muitos dos elementos da interface do usuário que podem ter uma das funções listadas aqui normalmente são vistos em navegadores.</span><span class="sxs-lookup"><span data-stu-id="faa1b-107">Many of the UI elements which might have one of the roles listed here are typically seen in browsers.</span></span>

> [!Note]  
> <span data-ttu-id="faa1b-108">Use este tópico como uma diretriz.</span><span class="sxs-lookup"><span data-stu-id="faa1b-108">Use this topic as a guideline.</span></span> <span data-ttu-id="faa1b-109">É altamente recomendável que você use as ferramentas de Acessibilidade Ativa da Microsoft para verificar o comportamento esperado de uma função de objeto individual.</span><span class="sxs-lookup"><span data-stu-id="faa1b-109">We strongly suggest that you use Microsoft Active Accessibility tools to verify expected behavior for an individual object role.</span></span>

 

<span data-ttu-id="faa1b-110">A tabela a seguir lista as funções de objeto adicionais às quais Oleacc.dll dá suporte.</span><span class="sxs-lookup"><span data-stu-id="faa1b-110">The following table lists additional object roles which Oleacc.dll supports.</span></span>



| &nbsp; |  &nbsp; |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="faa1b-111">**\_alerta do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-111">**ROLE\_SYSTEM\_ALERT**</span></span>](/windows)                           | [<span data-ttu-id="faa1b-112">**\_lista suspensa do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-112">**ROLE\_SYSTEM\_DROPLIST**</span></span>](/windows)       |
| [<span data-ttu-id="faa1b-113">**\_aplicativo do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-113">**ROLE\_SYSTEM\_APPLICATION**</span></span>](/windows)               | [<span data-ttu-id="faa1b-114">**\_equação do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-114">**ROLE\_SYSTEM\_EQUATION**</span></span>](/windows)       |
| [<span data-ttu-id="faa1b-115">**\_borda do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-115">**ROLE\_SYSTEM\_BORDER**</span></span>](/windows)                         | [<span data-ttu-id="faa1b-116">**\_elemento gráfico do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-116">**ROLE\_SYSTEM\_GRAPHIC**</span></span>](/windows)         |
| [<span data-ttu-id="faa1b-117">**\_BUTTONDROPDOWN do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-117">**ROLE\_SYSTEM\_BUTTONDROPDOWN**</span></span>](/windows)         | [<span data-ttu-id="faa1b-118">**\_HELPBALLOON do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-118">**ROLE\_SYSTEM\_HELPBALLOON**</span></span>](/windows) |
| [<span data-ttu-id="faa1b-119">**\_BUTTONDROPDOWNGRID do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-119">**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**</span></span>](/windows) | [<span data-ttu-id="faa1b-120">**\_IPAddress do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-120">**ROLE\_SYSTEM\_IPADDRESS**</span></span>](/windows)     |
| [<span data-ttu-id="faa1b-121">**\_BUTTONMENU do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-121">**ROLE\_SYSTEM\_BUTTONMENU**</span></span>](/windows)                 | [<span data-ttu-id="faa1b-122">**\_link do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-122">**ROLE\_SYSTEM\_LINK**</span></span>](/windows)               |
| [<span data-ttu-id="faa1b-123">**\_célula do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-123">**ROLE\_SYSTEM\_CELL**</span></span>](/windows)                             | [<span data-ttu-id="faa1b-124">**\_painel do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-124">**ROLE\_SYSTEM\_PANE**</span></span>](/windows)               |
| [<span data-ttu-id="faa1b-125">**\_caractere do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-125">**ROLE\_SYSTEM\_CHARACTER**</span></span>](/windows)                   | [<span data-ttu-id="faa1b-126">**\_linha do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-126">**ROLE\_SYSTEM\_ROW**</span></span>](/windows)                 |
| [<span data-ttu-id="faa1b-127">**\_gráfico do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-127">**ROLE\_SYSTEM\_CHART**</span></span>](/windows)                           | [<span data-ttu-id="faa1b-128">**subcabeçalho de sistema de função \_ \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-128">**ROLE\_SYSTEM\_ROWHEADER**</span></span>](/windows)     |
| [<span data-ttu-id="faa1b-129">**\_relógio do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-129">**ROLE\_SYSTEM\_CLOCK**</span></span>](/windows)                           | [<span data-ttu-id="faa1b-130">**separador de sistema de função \_ \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-130">**ROLE\_SYSTEM\_SEPARATOR**</span></span>](/windows)     |
| [<span data-ttu-id="faa1b-131">**\_coluna do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-131">**ROLE\_SYSTEM\_COLUMN**</span></span>](/windows)                         | [<span data-ttu-id="faa1b-132">**\_som do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-132">**ROLE\_SYSTEM\_SOUND**</span></span>](/windows)             |
| [<span data-ttu-id="faa1b-133">**\_diagrama do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-133">**ROLE\_SYSTEM\_DIAGRAM**</span></span>](/windows)                       | [<span data-ttu-id="faa1b-134">**sistema de função \_ \_ SPLITBUTTON**</span><span class="sxs-lookup"><span data-stu-id="faa1b-134">**ROLE\_SYSTEM\_SPLITBUTTON**</span></span>](/windows) |
| [<span data-ttu-id="faa1b-135">**\_discagem do sistema de função \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-135">**ROLE\_SYSTEM\_DIAL**</span></span>](/windows)                             | [<span data-ttu-id="faa1b-136">**\_tabela do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-136">**ROLE\_SYSTEM\_TABLE**</span></span>](/windows)             |
| [<span data-ttu-id="faa1b-137">**\_documento do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-137">**ROLE\_SYSTEM\_DOCUMENT**</span></span>](/windows)                     | [<span data-ttu-id="faa1b-138">**espaço em branco do \_ sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="faa1b-138">**ROLE\_SYSTEM\_WHITESPACE**</span></span>](/windows)   |



 

## <a name="role_system_alert"></a><span data-ttu-id="faa1b-139">\_alerta do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="faa1b-139">ROLE\_SYSTEM\_ALERT</span></span>

<span data-ttu-id="faa1b-140">Para obter mais informações sobre essa função, [**consulte \_ \_ alerta do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-140">For more information on this role, see [**ROLE\_SYSTEM\_ALERT**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-141">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-141">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-142">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-142">get\_accName</span></span>
-   <span data-ttu-id="faa1b-143">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-143">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-144">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-144">get\_accState</span></span>

## <a name="role_system_application"></a><span data-ttu-id="faa1b-145">\_aplicativo do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="faa1b-145">ROLE\_SYSTEM\_APPLICATION</span></span>

<span data-ttu-id="faa1b-146">Para obter mais informações sobre essa função, [**consulte \_ \_ aplicativo do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-146">For more information on this role, see [**ROLE\_SYSTEM\_APPLICATION**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-147">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-147">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-148">accHitTest</span><span class="sxs-lookup"><span data-stu-id="faa1b-148">accHitTest</span></span>
-   <span data-ttu-id="faa1b-149">accLocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-149">accLocation</span></span>
-   <span data-ttu-id="faa1b-150">accNavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-150">accNavigate</span></span>
-   <span data-ttu-id="faa1b-151">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="faa1b-151">get\_accChild</span></span>
-   <span data-ttu-id="faa1b-152">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="faa1b-152">get\_accChildCount</span></span>
-   <span data-ttu-id="faa1b-153">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="faa1b-153">get\_accFocus</span></span>
-   <span data-ttu-id="faa1b-154">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="faa1b-154">get\_accHelp</span></span>
-   <span data-ttu-id="faa1b-155">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="faa1b-155">get\_accHelpTopic</span></span>
-   <span data-ttu-id="faa1b-156">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="faa1b-156">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="faa1b-157">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-157">get\_accName</span></span>
-   <span data-ttu-id="faa1b-158">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-158">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-159">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-159">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-160">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-160">get\_accState</span></span>

## <a name="role_system_border"></a><span data-ttu-id="faa1b-161">\_borda do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="faa1b-161">ROLE\_SYSTEM\_BORDER</span></span>

<span data-ttu-id="faa1b-162">Para obter mais informações sobre essa função, [**consulte \_ \_ borda do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-162">For more information on this role, see [**ROLE\_SYSTEM\_BORDER**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-163">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-163">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-164">accHitTest</span><span class="sxs-lookup"><span data-stu-id="faa1b-164">accHitTest</span></span>
-   <span data-ttu-id="faa1b-165">accLocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-165">accLocation</span></span>
-   <span data-ttu-id="faa1b-166">accNavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-166">accNavigate</span></span>
-   <span data-ttu-id="faa1b-167">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-167">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-168">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-168">get\_accState</span></span>

## <a name="role_system_buttondropdown"></a><span data-ttu-id="faa1b-169">\_BUTTONDROPDOWN do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="faa1b-169">ROLE\_SYSTEM\_BUTTONDROPDOWN</span></span>

<span data-ttu-id="faa1b-170">Para obter mais informações sobre essa função, [**consulte \_ sistema \_ de funções BUTTONDROPDOWN**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-170">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWN**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-171">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-171">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-172">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="faa1b-172">accDoDefaultAction</span></span>
-   <span data-ttu-id="faa1b-173">accHitTest</span><span class="sxs-lookup"><span data-stu-id="faa1b-173">accHitTest</span></span>
-   <span data-ttu-id="faa1b-174">accLocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-174">accLocation</span></span>
-   <span data-ttu-id="faa1b-175">accNavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-175">accNavigate</span></span>
-   <span data-ttu-id="faa1b-176">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="faa1b-176">get\_accChild</span></span>
-   <span data-ttu-id="faa1b-177">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="faa1b-177">get\_accChildCount</span></span>
-   <span data-ttu-id="faa1b-178">obter \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="faa1b-178">get\_accDefaultAction</span></span>
-   <span data-ttu-id="faa1b-179">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="faa1b-179">get\_accFocus</span></span>
-   <span data-ttu-id="faa1b-180">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="faa1b-180">get\_accHelp</span></span>
-   <span data-ttu-id="faa1b-181">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="faa1b-181">get\_accHelpTopic</span></span>
-   <span data-ttu-id="faa1b-182">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="faa1b-182">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="faa1b-183">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-183">get\_accName</span></span>
-   <span data-ttu-id="faa1b-184">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-184">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-185">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-185">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-186">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-186">get\_accState</span></span>

## <a name="role_system_buttondropdowngrid"></a><span data-ttu-id="faa1b-187">\_BUTTONDROPDOWNGRID do sistema de função \_</span><span class="sxs-lookup"><span data-stu-id="faa1b-187">ROLE\_SYSTEM\_BUTTONDROPDOWNGRID</span></span>

<span data-ttu-id="faa1b-188">Para obter mais informações sobre essa função, [**consulte \_ sistema \_ de funções BUTTONDROPDOWNGRID**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-188">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-189">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-189">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-190">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="faa1b-190">accDoDefaultAction</span></span>
-   <span data-ttu-id="faa1b-191">accHitTest</span><span class="sxs-lookup"><span data-stu-id="faa1b-191">accHitTest</span></span>
-   <span data-ttu-id="faa1b-192">accLocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-192">accLocation</span></span>
-   <span data-ttu-id="faa1b-193">accNavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-193">accNavigate</span></span>
-   <span data-ttu-id="faa1b-194">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="faa1b-194">get\_accChild</span></span>
-   <span data-ttu-id="faa1b-195">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="faa1b-195">get\_accChildCount</span></span>
-   <span data-ttu-id="faa1b-196">obter \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="faa1b-196">get\_accDefaultAction</span></span>
-   <span data-ttu-id="faa1b-197">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="faa1b-197">get\_accFocus</span></span>
-   <span data-ttu-id="faa1b-198">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="faa1b-198">get\_accHelp</span></span>
-   <span data-ttu-id="faa1b-199">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="faa1b-199">get\_accHelpTopic</span></span>
-   <span data-ttu-id="faa1b-200">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="faa1b-200">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="faa1b-201">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-201">get\_accName</span></span>
-   <span data-ttu-id="faa1b-202">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-202">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-203">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-203">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-204">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-204">get\_accState</span></span>

## <a name="role_system_buttonmenu"></a><span data-ttu-id="faa1b-205">BOTÃO \_ DO SISTEMA DE \_ FUNÇÃOMENU</span><span class="sxs-lookup"><span data-stu-id="faa1b-205">ROLE\_SYSTEM\_BUTTONMENU</span></span>

<span data-ttu-id="faa1b-206">Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ BUTTONMENU**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-206">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONMENU**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-207">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-207">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-208">Accdodefaultaction</span><span class="sxs-lookup"><span data-stu-id="faa1b-208">accDoDefaultAction</span></span>
-   <span data-ttu-id="faa1b-209">Acchittest</span><span class="sxs-lookup"><span data-stu-id="faa1b-209">accHitTest</span></span>
-   <span data-ttu-id="faa1b-210">Acclocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-210">accLocation</span></span>
-   <span data-ttu-id="faa1b-211">Accnavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-211">accNavigate</span></span>
-   <span data-ttu-id="faa1b-212">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="faa1b-212">get\_accDefaultAction</span></span>
-   <span data-ttu-id="faa1b-213">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="faa1b-213">get\_accFocus</span></span>
-   <span data-ttu-id="faa1b-214">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="faa1b-214">get\_accHelp</span></span>
-   <span data-ttu-id="faa1b-215">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="faa1b-215">get\_accHelpTopic</span></span>
-   <span data-ttu-id="faa1b-216">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="faa1b-216">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="faa1b-217">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-217">get\_accName</span></span>
-   <span data-ttu-id="faa1b-218">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-218">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-219">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-219">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-220">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-220">get\_accState</span></span>

## <a name="role_system_cell"></a><span data-ttu-id="faa1b-221">CÉLULA \_ DO SISTEMA DE \_ FUNÇÃO</span><span class="sxs-lookup"><span data-stu-id="faa1b-221">ROLE\_SYSTEM\_CELL</span></span>

<span data-ttu-id="faa1b-222">Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ CELL**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-222">For more information on this role, see [**ROLE\_SYSTEM\_CELL**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-223">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-223">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-224">Acchittest</span><span class="sxs-lookup"><span data-stu-id="faa1b-224">accHitTest</span></span>
-   <span data-ttu-id="faa1b-225">Acclocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-225">accLocation</span></span>
-   <span data-ttu-id="faa1b-226">Accnavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-226">accNavigate</span></span>
-   <span data-ttu-id="faa1b-227">Accselect</span><span class="sxs-lookup"><span data-stu-id="faa1b-227">accSelect</span></span>
-   <span data-ttu-id="faa1b-228">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="faa1b-228">get\_accChild</span></span>
-   <span data-ttu-id="faa1b-229">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="faa1b-229">get\_accChildCount</span></span>
-   <span data-ttu-id="faa1b-230">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="faa1b-230">get\_accFocus</span></span>
-   <span data-ttu-id="faa1b-231">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="faa1b-231">get\_accHelp</span></span>
-   <span data-ttu-id="faa1b-232">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="faa1b-232">get\_accHelpTopic</span></span>
-   <span data-ttu-id="faa1b-233">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="faa1b-233">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="faa1b-234">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-234">get\_accName</span></span>
-   <span data-ttu-id="faa1b-235">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-235">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-236">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-236">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-237">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-237">get\_accState</span></span>
-   <span data-ttu-id="faa1b-238">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="faa1b-238">get\_accValue</span></span>

## <a name="role_system_character"></a><span data-ttu-id="faa1b-239">CARACTERE \_ DO SISTEMA DE \_ FUNÇÃO</span><span class="sxs-lookup"><span data-stu-id="faa1b-239">ROLE\_SYSTEM\_CHARACTER</span></span>

<span data-ttu-id="faa1b-240">Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ CHARACTER**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-240">For more information on this role, see [**ROLE\_SYSTEM\_CHARACTER**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-241">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-241">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-242">Acchittest</span><span class="sxs-lookup"><span data-stu-id="faa1b-242">accHitTest</span></span>
-   <span data-ttu-id="faa1b-243">Acclocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-243">accLocation</span></span>
-   <span data-ttu-id="faa1b-244">Accnavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-244">accNavigate</span></span>
-   <span data-ttu-id="faa1b-245">get \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="faa1b-245">get\_accDescription</span></span>
-   <span data-ttu-id="faa1b-246">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="faa1b-246">get\_accFocus</span></span>
-   <span data-ttu-id="faa1b-247">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="faa1b-247">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="faa1b-248">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-248">get\_accName</span></span>
-   <span data-ttu-id="faa1b-249">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-249">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-250">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-250">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-251">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-251">get\_accState</span></span>
-   <span data-ttu-id="faa1b-252">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="faa1b-252">get\_accValue</span></span>

## <a name="role_system_chart"></a><span data-ttu-id="faa1b-253">GRÁFICO \_ DO SISTEMA DE \_ FUNÇÕES</span><span class="sxs-lookup"><span data-stu-id="faa1b-253">ROLE\_SYSTEM\_CHART</span></span>

<span data-ttu-id="faa1b-254">Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ CHART**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-254">For more information on this role, see [**ROLE\_SYSTEM\_CHART**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-255">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-255">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-256">Acchittest</span><span class="sxs-lookup"><span data-stu-id="faa1b-256">accHitTest</span></span>
-   <span data-ttu-id="faa1b-257">Acclocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-257">accLocation</span></span>
-   <span data-ttu-id="faa1b-258">Accnavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-258">accNavigate</span></span>
-   <span data-ttu-id="faa1b-259">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="faa1b-259">get\_accChild</span></span>
-   <span data-ttu-id="faa1b-260">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="faa1b-260">get\_accChildCount</span></span>
-   <span data-ttu-id="faa1b-261">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="faa1b-261">get\_accFocus</span></span>
-   <span data-ttu-id="faa1b-262">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="faa1b-262">get\_accHelp</span></span>
-   <span data-ttu-id="faa1b-263">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="faa1b-263">get\_accHelpTopic</span></span>
-   <span data-ttu-id="faa1b-264">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="faa1b-264">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="faa1b-265">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-265">get\_accName</span></span>
-   <span data-ttu-id="faa1b-266">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-266">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-267">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-267">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-268">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-268">get\_accState</span></span>

## <a name="role_system_clock"></a><span data-ttu-id="faa1b-269">RELÓGIO \_ DO SISTEMA DE \_ FUNÇÃO</span><span class="sxs-lookup"><span data-stu-id="faa1b-269">ROLE\_SYSTEM\_CLOCK</span></span>

<span data-ttu-id="faa1b-270">Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ CLOCK**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-270">For more information on this role, see [**ROLE\_SYSTEM\_CLOCK**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-271">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-271">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-272">Acchittest</span><span class="sxs-lookup"><span data-stu-id="faa1b-272">accHitTest</span></span>
-   <span data-ttu-id="faa1b-273">Acclocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-273">accLocation</span></span>
-   <span data-ttu-id="faa1b-274">Accnavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-274">accNavigate</span></span>
-   <span data-ttu-id="faa1b-275">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="faa1b-275">get\_accFocus</span></span>
-   <span data-ttu-id="faa1b-276">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="faa1b-276">get\_accHelp</span></span>
-   <span data-ttu-id="faa1b-277">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="faa1b-277">get\_accHelpTopic</span></span>
-   <span data-ttu-id="faa1b-278">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="faa1b-278">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="faa1b-279">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-279">get\_accName</span></span>
-   <span data-ttu-id="faa1b-280">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-280">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-281">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-281">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-282">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-282">get\_accState</span></span>
-   <span data-ttu-id="faa1b-283">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="faa1b-283">get\_accValue</span></span>

## <a name="role_system_column"></a><span data-ttu-id="faa1b-284">COLUNA \_ DO SISTEMA DE \_ FUNÇÃO</span><span class="sxs-lookup"><span data-stu-id="faa1b-284">ROLE\_SYSTEM\_COLUMN</span></span>

<span data-ttu-id="faa1b-285">Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ COLUMN**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-285">For more information on this role, see [**ROLE\_SYSTEM\_COLUMN**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-286">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-286">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-287">Acchittest</span><span class="sxs-lookup"><span data-stu-id="faa1b-287">accHitTest</span></span>
-   <span data-ttu-id="faa1b-288">Acclocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-288">accLocation</span></span>
-   <span data-ttu-id="faa1b-289">Accnavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-289">accNavigate</span></span>
-   <span data-ttu-id="faa1b-290">Accselect</span><span class="sxs-lookup"><span data-stu-id="faa1b-290">accSelect</span></span>
-   <span data-ttu-id="faa1b-291">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="faa1b-291">get\_accChild</span></span>
-   <span data-ttu-id="faa1b-292">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="faa1b-292">get\_accChildCount</span></span>
-   <span data-ttu-id="faa1b-293">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="faa1b-293">get\_accFocus</span></span>
-   <span data-ttu-id="faa1b-294">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-294">get\_accName</span></span>
-   <span data-ttu-id="faa1b-295">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-295">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-296">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-296">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-297">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-297">get\_accState</span></span>
-   <span data-ttu-id="faa1b-298">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="faa1b-298">get\_accValue</span></span>

## <a name="role_system_diagram"></a><span data-ttu-id="faa1b-299">DIAGRAMA \_ DO SISTEMA DE \_ FUNÇÃO</span><span class="sxs-lookup"><span data-stu-id="faa1b-299">ROLE\_SYSTEM\_DIAGRAM</span></span>

<span data-ttu-id="faa1b-300">Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ DIAGRAM**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-300">For more information on this role, see [**ROLE\_SYSTEM\_DIAGRAM**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-301">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-301">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-302">Acchittest</span><span class="sxs-lookup"><span data-stu-id="faa1b-302">accHitTest</span></span>
-   <span data-ttu-id="faa1b-303">Acclocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-303">accLocation</span></span>
-   <span data-ttu-id="faa1b-304">Accnavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-304">accNavigate</span></span>
-   <span data-ttu-id="faa1b-305">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="faa1b-305">get\_accChild</span></span>
-   <span data-ttu-id="faa1b-306">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="faa1b-306">get\_accChildCount</span></span>
-   <span data-ttu-id="faa1b-307">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="faa1b-307">get\_accFocus</span></span>
-   <span data-ttu-id="faa1b-308">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="faa1b-308">get\_accHelp</span></span>
-   <span data-ttu-id="faa1b-309">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="faa1b-309">get\_accHelpTopic</span></span>
-   <span data-ttu-id="faa1b-310">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="faa1b-310">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="faa1b-311">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-311">get\_accName</span></span>
-   <span data-ttu-id="faa1b-312">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-312">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-313">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-313">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-314">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-314">get\_accState</span></span>

## <a name="role_system_dial"></a><span data-ttu-id="faa1b-315">ROLE \_ SYSTEM \_ DIAL</span><span class="sxs-lookup"><span data-stu-id="faa1b-315">ROLE\_SYSTEM\_DIAL</span></span>

<span data-ttu-id="faa1b-316">Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ DIAL**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-316">For more information on this role, see [**ROLE\_SYSTEM\_DIAL**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-317">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-317">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-318">Accdodefaultaction</span><span class="sxs-lookup"><span data-stu-id="faa1b-318">accDoDefaultAction</span></span>
-   <span data-ttu-id="faa1b-319">Acchittest</span><span class="sxs-lookup"><span data-stu-id="faa1b-319">accHitTest</span></span>
-   <span data-ttu-id="faa1b-320">Acclocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-320">accLocation</span></span>
-   <span data-ttu-id="faa1b-321">Accnavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-321">accNavigate</span></span>
-   <span data-ttu-id="faa1b-322">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="faa1b-322">get\_accDefaultAction</span></span>
-   <span data-ttu-id="faa1b-323">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="faa1b-323">get\_accFocus</span></span>
-   <span data-ttu-id="faa1b-324">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="faa1b-324">get\_accHelp</span></span>
-   <span data-ttu-id="faa1b-325">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="faa1b-325">get\_accHelpTopic</span></span>
-   <span data-ttu-id="faa1b-326">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="faa1b-326">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="faa1b-327">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-327">get\_accName</span></span>
-   <span data-ttu-id="faa1b-328">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-328">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-329">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-329">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-330">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-330">get\_accState</span></span>
-   <span data-ttu-id="faa1b-331">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="faa1b-331">get\_accValue</span></span>

## <a name="role_system_document"></a><span data-ttu-id="faa1b-332">DOCUMENTO DO \_ SISTEMA \_ DE FUNÇÃO</span><span class="sxs-lookup"><span data-stu-id="faa1b-332">ROLE\_SYSTEM\_DOCUMENT</span></span>

<span data-ttu-id="faa1b-333">Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ DOCUMENT**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-333">For more information on this role, see [**ROLE\_SYSTEM\_DOCUMENT**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-334">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-334">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-335">Acchittest</span><span class="sxs-lookup"><span data-stu-id="faa1b-335">accHitTest</span></span>
-   <span data-ttu-id="faa1b-336">Acclocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-336">accLocation</span></span>
-   <span data-ttu-id="faa1b-337">Accnavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-337">accNavigate</span></span>
-   <span data-ttu-id="faa1b-338">Accselect</span><span class="sxs-lookup"><span data-stu-id="faa1b-338">accSelect</span></span>
-   <span data-ttu-id="faa1b-339">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="faa1b-339">get\_accChild</span></span>
-   <span data-ttu-id="faa1b-340">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="faa1b-340">get\_accChildCount</span></span>
-   <span data-ttu-id="faa1b-341">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="faa1b-341">get\_accFocus</span></span>
-   <span data-ttu-id="faa1b-342">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-342">get\_accName</span></span>
-   <span data-ttu-id="faa1b-343">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-343">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-344">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-344">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-345">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-345">get\_accState</span></span>

## <a name="role_system_droplist"></a><span data-ttu-id="faa1b-346">LISTA \_ DE DROPLIST DO \_ SISTEMA DE FUNÇÕES</span><span class="sxs-lookup"><span data-stu-id="faa1b-346">ROLE\_SYSTEM\_DROPLIST</span></span>

<span data-ttu-id="faa1b-347">Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ DROPLIST**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-347">For more information on this role, see [**ROLE\_SYSTEM\_DROPLIST**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-348">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-348">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-349">Accdodefaultaction</span><span class="sxs-lookup"><span data-stu-id="faa1b-349">accDoDefaultAction</span></span>
-   <span data-ttu-id="faa1b-350">Acchittest</span><span class="sxs-lookup"><span data-stu-id="faa1b-350">accHitTest</span></span>
-   <span data-ttu-id="faa1b-351">Acclocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-351">accLocation</span></span>
-   <span data-ttu-id="faa1b-352">Accnavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-352">accNavigate</span></span>
-   <span data-ttu-id="faa1b-353">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="faa1b-353">get\_accChild</span></span>
-   <span data-ttu-id="faa1b-354">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="faa1b-354">get\_accChildCount</span></span>
-   <span data-ttu-id="faa1b-355">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="faa1b-355">get\_accDefaultAction</span></span>
-   <span data-ttu-id="faa1b-356">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="faa1b-356">get\_accFocus</span></span>
-   <span data-ttu-id="faa1b-357">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="faa1b-357">get\_accHelp</span></span>
-   <span data-ttu-id="faa1b-358">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="faa1b-358">get\_accHelpTopic</span></span>
-   <span data-ttu-id="faa1b-359">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="faa1b-359">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="faa1b-360">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-360">get\_accName</span></span>
-   <span data-ttu-id="faa1b-361">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-361">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-362">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-362">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-363">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-363">get\_accState</span></span>

## <a name="role_system_equation"></a><span data-ttu-id="faa1b-364">EQUAÇÃO \_ DO SISTEMA DE \_ FUNÇÃO</span><span class="sxs-lookup"><span data-stu-id="faa1b-364">ROLE\_SYSTEM\_EQUATION</span></span>

<span data-ttu-id="faa1b-365">Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ EQUATION**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-365">For more information on this role, see [**ROLE\_SYSTEM\_EQUATION**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-366">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-366">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-367">Acchittest</span><span class="sxs-lookup"><span data-stu-id="faa1b-367">accHitTest</span></span>
-   <span data-ttu-id="faa1b-368">Acclocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-368">accLocation</span></span>
-   <span data-ttu-id="faa1b-369">Accnavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-369">accNavigate</span></span>
-   <span data-ttu-id="faa1b-370">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="faa1b-370">get\_accFocus</span></span>
-   <span data-ttu-id="faa1b-371">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-371">get\_accName</span></span>
-   <span data-ttu-id="faa1b-372">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-372">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-373">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-373">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-374">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-374">get\_accState</span></span>
-   <span data-ttu-id="faa1b-375">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="faa1b-375">get\_accValue</span></span>

## <a name="role_system_graphic"></a><span data-ttu-id="faa1b-376">GRÁFICO \_ DO SISTEMA DE \_ FUNÇÃO</span><span class="sxs-lookup"><span data-stu-id="faa1b-376">ROLE\_SYSTEM\_GRAPHIC</span></span>

<span data-ttu-id="faa1b-377">Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ GRAPHIC**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-377">For more information on this role, see [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-378">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-378">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-379">Acchittest</span><span class="sxs-lookup"><span data-stu-id="faa1b-379">accHitTest</span></span>
-   <span data-ttu-id="faa1b-380">Acclocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-380">accLocation</span></span>
-   <span data-ttu-id="faa1b-381">Accnavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-381">accNavigate</span></span>
-   <span data-ttu-id="faa1b-382">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="faa1b-382">get\_accFocus</span></span>
-   <span data-ttu-id="faa1b-383">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="faa1b-383">get\_accHelp</span></span>
-   <span data-ttu-id="faa1b-384">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="faa1b-384">get\_accHelpTopic</span></span>
-   <span data-ttu-id="faa1b-385">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="faa1b-385">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="faa1b-386">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-386">get\_accName</span></span>
-   <span data-ttu-id="faa1b-387">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-387">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-388">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-388">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-389">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-389">get\_accState</span></span>

## <a name="role_system_helpballoon"></a><span data-ttu-id="faa1b-390">ROLE \_ SYSTEM \_ HELPBALLBALLBALLBALL</span><span class="sxs-lookup"><span data-stu-id="faa1b-390">ROLE\_SYSTEM\_HELPBALLOON</span></span>

<span data-ttu-id="faa1b-391">Para obter mais informações sobre essa função, [**consulte ROLE \_ SYSTEM \_ HELPBALLBALLBALL .**](object-roles.md)</span><span class="sxs-lookup"><span data-stu-id="faa1b-391">For more information on this role, see [**ROLE\_SYSTEM\_HELPBALLOON**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-392">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-392">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-393">Acchittest</span><span class="sxs-lookup"><span data-stu-id="faa1b-393">accHitTest</span></span>
-   <span data-ttu-id="faa1b-394">Acclocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-394">accLocation</span></span>
-   <span data-ttu-id="faa1b-395">Accnavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-395">accNavigate</span></span>
-   <span data-ttu-id="faa1b-396">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="faa1b-396">get\_accChild</span></span>
-   <span data-ttu-id="faa1b-397">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="faa1b-397">get\_accChildCount</span></span>
-   <span data-ttu-id="faa1b-398">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="faa1b-398">get\_accDefaultAction</span></span>
-   <span data-ttu-id="faa1b-399">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-399">get\_accName</span></span>
-   <span data-ttu-id="faa1b-400">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-400">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-401">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-401">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-402">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-402">get\_accState</span></span>
-   <span data-ttu-id="faa1b-403">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="faa1b-403">get\_accValue</span></span>

## <a name="role_system_ipaddress"></a><span data-ttu-id="faa1b-404">ROLE \_ SYSTEM \_ IPADDRESS</span><span class="sxs-lookup"><span data-stu-id="faa1b-404">ROLE\_SYSTEM\_IPADDRESS</span></span>

<span data-ttu-id="faa1b-405">Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ IPADDRESS**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-405">For more information on this role, see [**ROLE\_SYSTEM\_IPADDRESS**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-406">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-406">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-407">Acchittest</span><span class="sxs-lookup"><span data-stu-id="faa1b-407">accHitTest</span></span>
-   <span data-ttu-id="faa1b-408">Acclocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-408">accLocation</span></span>
-   <span data-ttu-id="faa1b-409">Accnavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-409">accNavigate</span></span>
-   <span data-ttu-id="faa1b-410">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="faa1b-410">get\_accChild</span></span>
-   <span data-ttu-id="faa1b-411">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="faa1b-411">get\_accChildCount</span></span>
-   <span data-ttu-id="faa1b-412">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="faa1b-412">get\_accFocus</span></span>
-   <span data-ttu-id="faa1b-413">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="faa1b-413">get\_accHelp</span></span>
-   <span data-ttu-id="faa1b-414">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="faa1b-414">get\_accHelpTopic</span></span>
-   <span data-ttu-id="faa1b-415">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="faa1b-415">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="faa1b-416">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-416">get\_accName</span></span>
-   <span data-ttu-id="faa1b-417">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-417">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-418">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-418">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-419">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-419">get\_accState</span></span>
-   <span data-ttu-id="faa1b-420">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="faa1b-420">get\_accValue</span></span>

## <a name="role_system_link"></a><span data-ttu-id="faa1b-421">\_LINK DO SISTEMA DE \_ FUNÇÃO</span><span class="sxs-lookup"><span data-stu-id="faa1b-421">ROLE\_SYSTEM\_LINK</span></span>

<span data-ttu-id="faa1b-422">Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ LINK**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-422">For more information on this role, see [**ROLE\_SYSTEM\_LINK**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-423">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-423">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-424">Accdodefaultaction</span><span class="sxs-lookup"><span data-stu-id="faa1b-424">accDoDefaultAction</span></span>
-   <span data-ttu-id="faa1b-425">Acchittest</span><span class="sxs-lookup"><span data-stu-id="faa1b-425">accHitTest</span></span>
-   <span data-ttu-id="faa1b-426">Acclocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-426">accLocation</span></span>
-   <span data-ttu-id="faa1b-427">Accnavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-427">accNavigate</span></span>
-   <span data-ttu-id="faa1b-428">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="faa1b-428">get\_accChild</span></span>
-   <span data-ttu-id="faa1b-429">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="faa1b-429">get\_accChildCount</span></span>
-   <span data-ttu-id="faa1b-430">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="faa1b-430">get\_accDefaultAction</span></span>
-   <span data-ttu-id="faa1b-431">get \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="faa1b-431">get\_accDescription</span></span>
-   <span data-ttu-id="faa1b-432">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="faa1b-432">get\_accFocus</span></span>
-   <span data-ttu-id="faa1b-433">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="faa1b-433">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="faa1b-434">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-434">get\_accName</span></span>
-   <span data-ttu-id="faa1b-435">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-435">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-436">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-436">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-437">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-437">get\_accState</span></span>
-   <span data-ttu-id="faa1b-438">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="faa1b-438">get\_accValue</span></span>

## <a name="role_system_pane"></a><span data-ttu-id="faa1b-439">PAINEL \_ SISTEMA \_ DE FUNÇÃO</span><span class="sxs-lookup"><span data-stu-id="faa1b-439">ROLE\_SYSTEM\_PANE</span></span>

<span data-ttu-id="faa1b-440">Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ PANE**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-440">For more information on this role, see [**ROLE\_SYSTEM\_PANE**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-441">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-441">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-442">Acchittest</span><span class="sxs-lookup"><span data-stu-id="faa1b-442">accHitTest</span></span>
-   <span data-ttu-id="faa1b-443">Acclocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-443">accLocation</span></span>
-   <span data-ttu-id="faa1b-444">Accnavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-444">accNavigate</span></span>
-   <span data-ttu-id="faa1b-445">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="faa1b-445">get\_accChild</span></span>
-   <span data-ttu-id="faa1b-446">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="faa1b-446">get\_accChildCount</span></span>
-   <span data-ttu-id="faa1b-447">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="faa1b-447">get\_accFocus</span></span>
-   <span data-ttu-id="faa1b-448">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="faa1b-448">get\_accHelp</span></span>
-   <span data-ttu-id="faa1b-449">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="faa1b-449">get\_accHelpTopic</span></span>
-   <span data-ttu-id="faa1b-450">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="faa1b-450">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="faa1b-451">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-451">get\_accName</span></span>
-   <span data-ttu-id="faa1b-452">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-452">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-453">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-453">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-454">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-454">get\_accState</span></span>

## <a name="role_system_row"></a><span data-ttu-id="faa1b-455">LINHA \_ DO SISTEMA DE \_ FUNÇÃO</span><span class="sxs-lookup"><span data-stu-id="faa1b-455">ROLE\_SYSTEM\_ROW</span></span>

<span data-ttu-id="faa1b-456">Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ ROW**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-456">For more information on this role, see [**ROLE\_SYSTEM\_ROW**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-457">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-457">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-458">Acchittest</span><span class="sxs-lookup"><span data-stu-id="faa1b-458">accHitTest</span></span>
-   <span data-ttu-id="faa1b-459">Acclocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-459">accLocation</span></span>
-   <span data-ttu-id="faa1b-460">Accnavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-460">accNavigate</span></span>
-   <span data-ttu-id="faa1b-461">Accselect</span><span class="sxs-lookup"><span data-stu-id="faa1b-461">accSelect</span></span>
-   <span data-ttu-id="faa1b-462">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="faa1b-462">get\_accChild</span></span>
-   <span data-ttu-id="faa1b-463">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="faa1b-463">get\_accChildCount</span></span>
-   <span data-ttu-id="faa1b-464">get \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="faa1b-464">get\_accDescription</span></span>
-   <span data-ttu-id="faa1b-465">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="faa1b-465">get\_accFocus</span></span>
-   <span data-ttu-id="faa1b-466">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-466">get\_accName</span></span>
-   <span data-ttu-id="faa1b-467">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-467">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-468">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-468">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-469">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-469">get\_accState</span></span>
-   <span data-ttu-id="faa1b-470">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="faa1b-470">get\_accValue</span></span>

## <a name="role_system_rowheader"></a><span data-ttu-id="faa1b-471">\_ROWHEADER DO SISTEMA DE \_ FUNÇÃO</span><span class="sxs-lookup"><span data-stu-id="faa1b-471">ROLE\_SYSTEM\_ROWHEADER</span></span>

<span data-ttu-id="faa1b-472">Para obter mais informações sobre essa função, [**consulte ROLE \_ SYSTEM \_ ROWHEADER**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-472">For more information on this role, see [**ROLE\_SYSTEM\_ROWHEADER**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-473">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-473">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-474">Acchittest</span><span class="sxs-lookup"><span data-stu-id="faa1b-474">accHitTest</span></span>
-   <span data-ttu-id="faa1b-475">Acclocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-475">accLocation</span></span>
-   <span data-ttu-id="faa1b-476">Accnavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-476">accNavigate</span></span>
-   <span data-ttu-id="faa1b-477">Accselect</span><span class="sxs-lookup"><span data-stu-id="faa1b-477">accSelect</span></span>
-   <span data-ttu-id="faa1b-478">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="faa1b-478">get\_accChild</span></span>
-   <span data-ttu-id="faa1b-479">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="faa1b-479">get\_accChildCount</span></span>
-   <span data-ttu-id="faa1b-480">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="faa1b-480">get\_accDefaultAction</span></span>
-   <span data-ttu-id="faa1b-481">get \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="faa1b-481">get\_accDescription</span></span>
-   <span data-ttu-id="faa1b-482">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="faa1b-482">get\_accFocus</span></span>
-   <span data-ttu-id="faa1b-483">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-483">get\_accName</span></span>
-   <span data-ttu-id="faa1b-484">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-484">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-485">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-485">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-486">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-486">get\_accState</span></span>
-   <span data-ttu-id="faa1b-487">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="faa1b-487">get\_accValue</span></span>

## <a name="role_system_separator"></a><span data-ttu-id="faa1b-488">SEPARADOR \_ DO \_ SISTEMA DE FUNÇÃO</span><span class="sxs-lookup"><span data-stu-id="faa1b-488">ROLE\_SYSTEM\_SEPARATOR</span></span>

<span data-ttu-id="faa1b-489">Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ SEPARATOR**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-489">For more information on this role, see [**ROLE\_SYSTEM\_SEPARATOR**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-490">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-490">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-491">Acchittest</span><span class="sxs-lookup"><span data-stu-id="faa1b-491">accHitTest</span></span>
-   <span data-ttu-id="faa1b-492">Acclocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-492">accLocation</span></span>
-   <span data-ttu-id="faa1b-493">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="faa1b-493">get\_accChild</span></span>
-   <span data-ttu-id="faa1b-494">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="faa1b-494">get\_accChildCount</span></span>
-   <span data-ttu-id="faa1b-495">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-495">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-496">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-496">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-497">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-497">get\_accState</span></span>

## <a name="role_system_sound"></a><span data-ttu-id="faa1b-498">SOM \_ DO SISTEMA DE \_ FUNÇÃO</span><span class="sxs-lookup"><span data-stu-id="faa1b-498">ROLE\_SYSTEM\_SOUND</span></span>

<span data-ttu-id="faa1b-499">Para obter mais informações sobre essa função, consulte [**ROLE \_ SYSTEM \_ SOUND**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-499">For more information on this role, see [**ROLE\_SYSTEM\_SOUND**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-500">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-500">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-501">obter \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="faa1b-501">get\_accDescription</span></span>
-   <span data-ttu-id="faa1b-502">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-502">get\_accName</span></span>
-   <span data-ttu-id="faa1b-503">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-503">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-504">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-504">get\_accState</span></span>

## <a name="role_system_splitbutton"></a><span data-ttu-id="faa1b-505">sistema de função \_ \_ SPLITBUTTON</span><span class="sxs-lookup"><span data-stu-id="faa1b-505">ROLE\_SYSTEM\_SPLITBUTTON</span></span>

<span data-ttu-id="faa1b-506">Para obter mais informações sobre essa função, [**consulte \_ sistema \_ de função SPLITBUTTON**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-506">For more information on this role, see [**ROLE\_SYSTEM\_SPLITBUTTON**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-507">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-507">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-508">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="faa1b-508">accDoDefaultAction</span></span>
-   <span data-ttu-id="faa1b-509">accHitTest</span><span class="sxs-lookup"><span data-stu-id="faa1b-509">accHitTest</span></span>
-   <span data-ttu-id="faa1b-510">accLocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-510">accLocation</span></span>
-   <span data-ttu-id="faa1b-511">accNavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-511">accNavigate</span></span>
-   <span data-ttu-id="faa1b-512">obter \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="faa1b-512">get\_accDefaultAction</span></span>
-   <span data-ttu-id="faa1b-513">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="faa1b-513">get\_accHelp</span></span>
-   <span data-ttu-id="faa1b-514">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="faa1b-514">get\_accHelpTopic</span></span>
-   <span data-ttu-id="faa1b-515">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="faa1b-515">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="faa1b-516">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-516">get\_accName</span></span>
-   <span data-ttu-id="faa1b-517">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-517">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-518">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-518">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-519">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-519">get\_accState</span></span>

## <a name="role_system_table"></a><span data-ttu-id="faa1b-520">\_tabela do sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="faa1b-520">ROLE\_SYSTEM\_TABLE</span></span>

<span data-ttu-id="faa1b-521">Para obter mais informações sobre essa função, [**consulte \_ \_ tabela do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-521">For more information on this role, see [**ROLE\_SYSTEM\_TABLE**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-522">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-522">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-523">accHitTest</span><span class="sxs-lookup"><span data-stu-id="faa1b-523">accHitTest</span></span>
-   <span data-ttu-id="faa1b-524">accLocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-524">accLocation</span></span>
-   <span data-ttu-id="faa1b-525">accNavigate</span><span class="sxs-lookup"><span data-stu-id="faa1b-525">accNavigate</span></span>
-   <span data-ttu-id="faa1b-526">accSelect</span><span class="sxs-lookup"><span data-stu-id="faa1b-526">accSelect</span></span>
-   <span data-ttu-id="faa1b-527">obter \_ accChild</span><span class="sxs-lookup"><span data-stu-id="faa1b-527">get\_accChild</span></span>
-   <span data-ttu-id="faa1b-528">obter \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="faa1b-528">get\_accChildCount</span></span>
-   <span data-ttu-id="faa1b-529">obter \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="faa1b-529">get\_accDescription</span></span>
-   <span data-ttu-id="faa1b-530">obter \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="faa1b-530">get\_accFocus</span></span>
-   <span data-ttu-id="faa1b-531">obter \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="faa1b-531">get\_accHelp</span></span>
-   <span data-ttu-id="faa1b-532">obter \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="faa1b-532">get\_accHelpTopic</span></span>
-   <span data-ttu-id="faa1b-533">obter \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="faa1b-533">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="faa1b-534">obter \_ accName</span><span class="sxs-lookup"><span data-stu-id="faa1b-534">get\_accName</span></span>
-   <span data-ttu-id="faa1b-535">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-535">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-536">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-536">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-537">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-537">get\_accState</span></span>

## <a name="role_system_whitespace"></a><span data-ttu-id="faa1b-538">espaço em branco do \_ sistema de funções \_</span><span class="sxs-lookup"><span data-stu-id="faa1b-538">ROLE\_SYSTEM\_WHITESPACE</span></span>

<span data-ttu-id="faa1b-539">Para obter mais informações sobre essa função, [**consulte \_ espaço em \_ branco do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="faa1b-539">For more information on this role, see [**ROLE\_SYSTEM\_WHITESPACE**](object-roles.md).</span></span>

<span data-ttu-id="faa1b-540">**Propriedades e métodos com suporte**</span><span class="sxs-lookup"><span data-stu-id="faa1b-540">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="faa1b-541">accLocation</span><span class="sxs-lookup"><span data-stu-id="faa1b-541">accLocation</span></span>
-   <span data-ttu-id="faa1b-542">accSelect</span><span class="sxs-lookup"><span data-stu-id="faa1b-542">accSelect</span></span>
-   <span data-ttu-id="faa1b-543">obter \_ accParent</span><span class="sxs-lookup"><span data-stu-id="faa1b-543">get\_accParent</span></span>
-   <span data-ttu-id="faa1b-544">obter \_ accRole</span><span class="sxs-lookup"><span data-stu-id="faa1b-544">get\_accRole</span></span>
-   <span data-ttu-id="faa1b-545">obter \_ accState</span><span class="sxs-lookup"><span data-stu-id="faa1b-545">get\_accState</span></span>

 

 