---
title: Práticas recomendadas para usar matrizes seguras
description: Muitos métodos de interface da automação da interface do usuário da Microsoft \ 32; API usam argumentos chamados matrizes seguras, do tipo de dados SAFEARRAY. Este tópico descreve as práticas recomendadas para usar matrizes seguras em aplicativos de automação de interface do usuário.
ms.assetid: 07e87cfd-d565-41b5-a68d-b99dd191fa95
keywords:
- Automação da interface do usuário, matrizes seguras
- Automação da interface do usuário, provedores
- Automação da interface do usuário, clientes
- Automação da interface do usuário, convertendo entre tipos de dados
- clientes, matrizes seguras
- provedores, automação da interface do usuário
- matrizes seguras
- tipos de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ade30398f8fbeb43336707f66a0709dfab83d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105812146"
---
# <a name="best-practices-for-using-safe-arrays"></a><span data-ttu-id="075ce-112">Práticas recomendadas para usar matrizes seguras</span><span class="sxs-lookup"><span data-stu-id="075ce-112">Best Practices for Using Safe Arrays</span></span>

<span data-ttu-id="075ce-113">Muitos métodos de interface da API de automação da interface do usuário da Microsoft levam argumentos chamados matrizes seguras, do tipo de dados [**SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray) .</span><span class="sxs-lookup"><span data-stu-id="075ce-113">Many interface methods of the Microsoft UI Automation API take arguments called safe arrays, of the [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) data type.</span></span> <span data-ttu-id="075ce-114">Este tópico descreve as práticas recomendadas para usar matrizes seguras em aplicativos de automação de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="075ce-114">This topic describes the best practices for using safe arrays in a UI Automation applications.</span></span>

## <a name="clients"></a><span data-ttu-id="075ce-115">Clientes</span><span class="sxs-lookup"><span data-stu-id="075ce-115">Clients</span></span>

<span data-ttu-id="075ce-116">Todas as matrizes seguras que são usadas com os métodos de API do cliente de automação da interface do usuário são matrizes unidimensionais baseadas em zero.</span><span class="sxs-lookup"><span data-stu-id="075ce-116">All safe arrays that are used with the UI Automation client API methods are zero-based, one-dimensional arrays.</span></span> <span data-ttu-id="075ce-117">Para criar uma matriz segura para um método de cliente de automação da interface do usuário, use a função [**SafeArrayCreateVector**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) e para ler e gravar em uma matriz segura, use as funções [**SafeArrayGetElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) e [**SafeArrayPutElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) .</span><span class="sxs-lookup"><span data-stu-id="075ce-117">To create a safe array for a UI Automation client method, use the [**SafeArrayCreateVector**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) function, and to read from and write to a safe array, use the [**SafeArrayGetElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) and [**SafeArrayPutElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) functions.</span></span> <span data-ttu-id="075ce-118">Quando você terminar de usar uma matriz segura, sempre a destruirá usando a função [**SafeArrayDestroy**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) , se você criou a matriz segura ou a recebeu de um método de cliente de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="075ce-118">When you finish using a safe array, always destroy it by using the [**SafeArrayDestroy**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) function, whether you created the safe array or received it from a UI Automation client method.</span></span>

<span data-ttu-id="075ce-119">Vários métodos de automação da interface do usuário, incluindo métodos de recuperação de propriedade, como [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue), recuperam [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant)s que podem conter estruturas [**Point**](/previous-versions//dd162805(v=vs.85)) ou [**UiaRect**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect) .</span><span class="sxs-lookup"><span data-stu-id="075ce-119">Several UI Automation methods, including property-retrieval methods such as [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue), retrieve [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)s that can contain [**POINT**](/previous-versions//dd162805(v=vs.85)) or [**UiaRect**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect) structures.</span></span> <span data-ttu-id="075ce-120">Um **ponto** é empacotado em uma **variante** como uma matriz segura de duplicatas (VT \_ R8) com o membro **x** no índice 0 e o membro **y** no índice 1.</span><span class="sxs-lookup"><span data-stu-id="075ce-120">A **POINT** is packed into a **VARIANT** as a safe array of doubles (VT\_R8) with the **x** member at index 0, and the **y** member at index 1.</span></span> <span data-ttu-id="075ce-121">Da mesma forma, um **UiaRect** é empacotado em uma **variante** como uma matriz segura de duplicatas com os membros **esquerdo**, **superior**, **largura** e **altura** nos índices de 0 a 3, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="075ce-121">Similarly, a **UiaRect** is packed into a **VARIANT** as a safe array of doubles with the **left**, **top**, **width**, and **height** members at indexes 0 through 3, respectively.</span></span> <span data-ttu-id="075ce-122">Para uma matriz de estruturas **UiaRect** , a matriz segura contém uma matriz sequencial de quatro duplos para cada **UiaRect**.</span><span class="sxs-lookup"><span data-stu-id="075ce-122">For an array of **UiaRect** structures, the safe array contains a sequential array of four doubles for each **UiaRect**.</span></span> <span data-ttu-id="075ce-123">Os membros **esquerdo**, **superior**, **largura** e **altura** do primeiro **UiaRect** ocupam o índice 0 até 3, os membros do segundo retângulo ocupam o índice 4 até 7 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="075ce-123">The **left**, **top**, **width**, and **height** members of the first **UiaRect** occupy index 0 through 3, the members of the second rectangle occupy index 4 through 7, and so on.</span></span>

<span data-ttu-id="075ce-124">A interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) inclui os seguintes métodos para converter entre [**SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray) e vários outros tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="075ce-124">The [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface includes the following methods for converting between [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) and various other data types.</span></span>



| <span data-ttu-id="075ce-125">Método</span><span class="sxs-lookup"><span data-stu-id="075ce-125">Method</span></span>                                                                                               | <span data-ttu-id="075ce-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="075ce-126">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="075ce-127">**IUIAutomation::IntNativeArrayToSafeArray**</span><span class="sxs-lookup"><span data-stu-id="075ce-127">**IUIAutomation::IntNativeArrayToSafeArray**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intnativearraytosafearray)   | <span data-ttu-id="075ce-128">Converte uma matriz de inteiros em um [**SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span><span class="sxs-lookup"><span data-stu-id="075ce-128">Converts an array of integers to a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span>                                          |
| [<span data-ttu-id="075ce-129">**IUIAutomation::IntSafeArrayToNativeArray**</span><span class="sxs-lookup"><span data-stu-id="075ce-129">**IUIAutomation::IntSafeArrayToNativeArray**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intsafearraytonativearray)   | <span data-ttu-id="075ce-130">Converte um [**SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray) de inteiros em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="075ce-130">Converts a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of integers to an array.</span></span>                                          |
| [<span data-ttu-id="075ce-131">**IUIAutomation::SafeArrayToRectNativeArray**</span><span class="sxs-lookup"><span data-stu-id="075ce-131">**IUIAutomation::SafeArrayToRectNativeArray**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-safearraytorectnativearray) | <span data-ttu-id="075ce-132">Converte um [**SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray) que contém coordenadas de retângulo em uma matriz do tipo **Rect**.</span><span class="sxs-lookup"><span data-stu-id="075ce-132">Converts a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) that contains rectangle coordinates to an array of type **RECT**.</span></span> |



 

## <a name="providers"></a><span data-ttu-id="075ce-133">Provedores</span><span class="sxs-lookup"><span data-stu-id="075ce-133">Providers</span></span>

<span data-ttu-id="075ce-134">Um provedor deve implementar vários métodos de interface que a automação da interface do usuário chama para recuperar informações do provedor.</span><span class="sxs-lookup"><span data-stu-id="075ce-134">A provider must implement a number of interface methods that UI Automation calls to retrieve information from the provider.</span></span> <span data-ttu-id="075ce-135">Muitas vezes, essas informações consistem em uma matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="075ce-135">Many times, this information consists of an array of values.</span></span> <span data-ttu-id="075ce-136">Para retornar uma matriz à automação da interface do usuário, o provedor deve empacotar a matriz em uma estrutura [**SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray) .</span><span class="sxs-lookup"><span data-stu-id="075ce-136">To return an array to UI Automation, the provider must pack the array into a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) structure.</span></span> <span data-ttu-id="075ce-137">Os elementos da matriz devem ser do tipo de dados esperado e devem aparecer na ordem esperada.</span><span class="sxs-lookup"><span data-stu-id="075ce-137">The array elements must be of the expected data type, and must appear in the expected order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="075ce-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="075ce-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="075ce-139">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="075ce-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="075ce-140">Visão geral das propriedades de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="075ce-140">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="075ce-141">Conceitos básicos de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="075ce-141">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 