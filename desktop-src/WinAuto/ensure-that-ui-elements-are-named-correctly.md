---
title: Garantindo que os elementos da interface do usuário sejam nomeados corretamente
description: Este tópico descreve a maneira correta de especificar os nomes dos elementos da interface do usuário em seus aplicativos Microsoft Win32 para que o Microsoft Acessibilidade Ativa possa expor com precisão os nomes para aplicativos cliente por meio do IAccessible \ 32; Propriedade Name.
ms.assetid: 5b8f23cb-9906-4cc4-83d4-73fdf96ed681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db3c4f1fc129aea9b793bac1935d678645b28fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917364"
---
# <a name="ensuring-that-ui-elements-are-correctly-named"></a><span data-ttu-id="b1c99-103">Garantindo que os elementos da interface do usuário sejam nomeados corretamente</span><span class="sxs-lookup"><span data-stu-id="b1c99-103">Ensuring that UI Elements are Correctly Named</span></span>

<span data-ttu-id="b1c99-104">Este tópico descreve a maneira correta de especificar os nomes dos elementos da interface do usuário em seus aplicativos do Microsoft Win32 para que o Microsoft Acessibilidade Ativa possa expor com precisão os nomes aos aplicativos cliente por meio da [propriedade nome](name-property.md)do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="b1c99-104">This topic describes the correct way to specify the names of the UI elements in your Microsoft Win32 applications so that Microsoft Active Accessibility can accurately expose the names to client applications through the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) [Name property](name-property.md).</span></span>

<span data-ttu-id="b1c99-105">As informações nesta seção aplicam-se somente ao Microsoft Acessibilidade Ativa.</span><span class="sxs-lookup"><span data-stu-id="b1c99-105">The information in this section applies to Microsoft Active Accessibility only.</span></span> <span data-ttu-id="b1c99-106">Ele não se aplica a aplicativos que usam a automação da interface do usuário da Microsoft ou aqueles baseados em linguagens de marcação, como HTML, HTML dinâmico (DHTML) ou XML.</span><span class="sxs-lookup"><span data-stu-id="b1c99-106">It does not apply to applications that use Microsoft UI Automation or those based on markup languages such as HTML, Dynamic HTML (DHTML), or XML.</span></span>

-   [<span data-ttu-id="b1c99-107">Visão geral</span><span class="sxs-lookup"><span data-stu-id="b1c99-107">Overview</span></span>](#overview)
-   [<span data-ttu-id="b1c99-108">Como a nomenclatura incorreta causa problemas</span><span class="sxs-lookup"><span data-stu-id="b1c99-108">How Incorrect Naming Causes Problems</span></span>](#how-incorrect-naming-causes-problems)
-   [<span data-ttu-id="b1c99-109">Como a MSAA Obtém a propriedade Name</span><span class="sxs-lookup"><span data-stu-id="b1c99-109">How MSAA Gets the Name Property</span></span>](#how-msaa-gets-the-name-property)
-   [<span data-ttu-id="b1c99-110">Como localizar e corrigir problemas de nomenclatura</span><span class="sxs-lookup"><span data-stu-id="b1c99-110">How to Find and Correct Naming Problems</span></span>](#how-to-find-and-correct-naming-problems)
-   [<span data-ttu-id="b1c99-111">Como nomear corretamente um TrackBar</span><span class="sxs-lookup"><span data-stu-id="b1c99-111">How to Correctly Name a Trackbar</span></span>](#how-to-correctly-name-a-trackbar)
-   [<span data-ttu-id="b1c99-112">Como usar rótulos invisíveis em controles de nome</span><span class="sxs-lookup"><span data-stu-id="b1c99-112">How to Use Invisible Labels to Name Controls</span></span>](#how-to-use-invisible-labels-to-name-controls)
-   [<span data-ttu-id="b1c99-113">Como usar a anotação direta para especificar a propriedade Name</span><span class="sxs-lookup"><span data-stu-id="b1c99-113">How to Use Direct Annotation to Specify the Name Property</span></span>](#how-to-use-direct-annotation-to-specify-the-name-property)
    -   [<span data-ttu-id="b1c99-114">Etapas para anotar a propriedade Name</span><span class="sxs-lookup"><span data-stu-id="b1c99-114">Steps for Annotating the Name Property</span></span>](#steps-for-annotating-the-name-property)
    -   [<span data-ttu-id="b1c99-115">Exemplo de anotação da propriedade Name</span><span class="sxs-lookup"><span data-stu-id="b1c99-115">Example of Annotating the Name Property</span></span>](#example-of-annotating-the-name-property)
-   [<span data-ttu-id="b1c99-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b1c99-116">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="b1c99-117">Visão geral</span><span class="sxs-lookup"><span data-stu-id="b1c99-117">Overview</span></span>

<span data-ttu-id="b1c99-118">No Microsoft Acessibilidade Ativa, cada elemento da interface do usuário em um aplicativo é representado por um objeto que expõe a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="b1c99-118">In Microsoft Active Accessibility, each UI element in an application is represented by an object that exposes the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="b1c99-119">Os aplicativos cliente usam as propriedades e os métodos da interface **IAccessible** para interagir com o elemento de interface do usuário e para recuperar informações sobre ele.</span><span class="sxs-lookup"><span data-stu-id="b1c99-119">Client applications use the properties and methods of the **IAccessible** interface to interact with the UI element and to retrieve information about it.</span></span> <span data-ttu-id="b1c99-120">Uma das propriedades mais importantes expostas pela interface **IAccessible** é a [Propriedade Name](name-property.md).</span><span class="sxs-lookup"><span data-stu-id="b1c99-120">One of the most important properties exposed by the **IAccessible** interface is the [Name property](name-property.md).</span></span> <span data-ttu-id="b1c99-121">Os aplicativos cliente contam com a propriedade Name para localizar, identificar ou anunciar um elemento de interface do usuário para ele.</span><span class="sxs-lookup"><span data-stu-id="b1c99-121">Client applications rely on the Name property to find, identify, or announce a UI element to the user.</span></span> <span data-ttu-id="b1c99-122">Se o Microsoft Acessibilidade Ativa não puder expor corretamente a propriedade Name de um determinado elemento de interface do usuário, os aplicativos cliente não poderão apresentar esse elemento de interface do usuário e o elemento de interface do usuário ficará inacessível aos usuários com deficiências.</span><span class="sxs-lookup"><span data-stu-id="b1c99-122">If Microsoft Active Accessibility cannot properly expose the Name property of a particular UI element, client applications will be unable to present that UI element to the user, and the UI element will be inaccessible to users with disabilities.</span></span>

## <a name="how-incorrect-naming-causes-problems"></a><span data-ttu-id="b1c99-123">Como a nomenclatura incorreta causa problemas</span><span class="sxs-lookup"><span data-stu-id="b1c99-123">How Incorrect Naming Causes Problems</span></span>

<span data-ttu-id="b1c99-124">Para ilustrar os problemas causados pela nomenclatura incorreta de elementos da interface do usuário, considere o formulário de entrada de nome mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1c99-124">To illustrate the problems caused by incorrect naming of UI elements, consider the name entry form shown in the following illustration.</span></span>

![ilustração de um formulário simples para inserir o nome e o sobrenome](images/incorrect-form.png)

<span data-ttu-id="b1c99-126">Embora os elementos da interface do usuário no formulário pareçam Ok, a implementação programática está incorreta.</span><span class="sxs-lookup"><span data-stu-id="b1c99-126">Although the UI elements in the form look okay, the programmatic implementation is incorrect.</span></span> <span data-ttu-id="b1c99-127">Para um cliente Microsoft Acessibilidade Ativa, como um leitor de tela, a [Propriedade Name](name-property.md) do controle de edição superior é "Last Name:", e a propriedade Name do controle de edição inferior é uma cadeia de caracteres vazia ("").</span><span class="sxs-lookup"><span data-stu-id="b1c99-127">To a Microsoft Active Accessibility client such as a screen reader, the [Name property](name-property.md) of the top edit control is "Last Name:", and the Name property of the bottom edit control is an empty string ("").</span></span> <span data-ttu-id="b1c99-128">O leitor de tela lerá o controle de edição superior como "Last Name", embora o usuário deva digitar o nome.</span><span class="sxs-lookup"><span data-stu-id="b1c99-128">The screen reader will read the top edit control as "Last Name", although the user is expected to type in the first name.</span></span> <span data-ttu-id="b1c99-129">O leitor de tela lerá o segundo controle de edição como "sem nome", de modo que o usuário não terá idéia do que digitar no segundo controle de edição.</span><span class="sxs-lookup"><span data-stu-id="b1c99-129">The screen reader will read the second edit control as "no name", so the user will have no idea what to type into the second edit control.</span></span> <span data-ttu-id="b1c99-130">O leitor de tela não pode ajudar o usuário a inserir dados nesse formulário simples.</span><span class="sxs-lookup"><span data-stu-id="b1c99-130">The screen reader is unable to assist the user in entering data into this simple form.</span></span>

<span data-ttu-id="b1c99-131">Outro problema com o formulário é que nenhuma tecla de atalho é atribuída a nenhum dos controles de edição.</span><span class="sxs-lookup"><span data-stu-id="b1c99-131">Another problem with the form is that no shortcut keys are assigned to either of the edit controls.</span></span> <span data-ttu-id="b1c99-132">O usuário é forçado a fazer uma tabulação para os controles ou usar o mouse.</span><span class="sxs-lookup"><span data-stu-id="b1c99-132">The user is forced to either tab to the controls or use the mouse.</span></span>

<span data-ttu-id="b1c99-133">As seções a seguir explicam a origem desses problemas e fornecem diretrizes para corrigi-los.</span><span class="sxs-lookup"><span data-stu-id="b1c99-133">The following sections explain the source of these problems and provide guidelines for correcting them.</span></span>

## <a name="how-msaa-gets-the-name-property"></a><span data-ttu-id="b1c99-134">Como a MSAA Obtém a propriedade Name</span><span class="sxs-lookup"><span data-stu-id="b1c99-134">How MSAA Gets the Name Property</span></span>

<span data-ttu-id="b1c99-135">O Microsoft Acessibilidade Ativa Obtém a cadeia de caracteres de [propriedade de nome](name-property.md) de diferentes locais, dependendo do tipo do elemento de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="b1c99-135">Microsoft Active Accessibility gets the [Name property](name-property.md) string from different locations depending on the type of the UI element.</span></span> <span data-ttu-id="b1c99-136">Para a maioria dos elementos da interface do usuário que têm texto de janela associado, o Microsoft Acessibilidade Ativa usa o texto da janela como a cadeia de caracteres de propriedade de nome.</span><span class="sxs-lookup"><span data-stu-id="b1c99-136">For most UI elements that have associated window text, Microsoft Active Accessibility uses the window text as the Name property string.</span></span> <span data-ttu-id="b1c99-137">Exemplos desse tipo de elemento de interface do usuário incluem controles como botões, itens de menu e dicas de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="b1c99-137">Examples of this type of UI element include controls such as buttons, menu items, and tooltips.</span></span>

<span data-ttu-id="b1c99-138">Para os seguintes controles, o Microsoft Acessibilidade Ativa ignora o texto da janela e, em vez disso, procura um rótulo de texto estático (ou rótulo da caixa de grupo) imediatamente antes do controle na ordem de tabulação.</span><span class="sxs-lookup"><span data-stu-id="b1c99-138">For the following controls, Microsoft Active Accessibility ignores the window text and instead looks for a static text label (or group box label) immediately preceding the control in the tab order.</span></span>

-   <span data-ttu-id="b1c99-139">Caixas de combinação</span><span class="sxs-lookup"><span data-stu-id="b1c99-139">Combo Boxes</span></span>
-   <span data-ttu-id="b1c99-140">Seletores de data e hora</span><span class="sxs-lookup"><span data-stu-id="b1c99-140">Date and Time Pickers</span></span>
-   <span data-ttu-id="b1c99-141">Editar e elaborar controles de edição</span><span class="sxs-lookup"><span data-stu-id="b1c99-141">Edit and Rich Edit controls</span></span>
-   <span data-ttu-id="b1c99-142">Controles de endereço IP</span><span class="sxs-lookup"><span data-stu-id="b1c99-142">IP Address controls</span></span>
-   <span data-ttu-id="b1c99-143">Caixas de listagem</span><span class="sxs-lookup"><span data-stu-id="b1c99-143">List Boxes</span></span>
-   <span data-ttu-id="b1c99-144">Listar exibições</span><span class="sxs-lookup"><span data-stu-id="b1c99-144">List Views</span></span>
-   <span data-ttu-id="b1c99-145">Barras de progresso</span><span class="sxs-lookup"><span data-stu-id="b1c99-145">Progress Bars</span></span>
-   <span data-ttu-id="b1c99-146">Rolagem</span><span class="sxs-lookup"><span data-stu-id="b1c99-146">Scrollbars</span></span>
-   <span data-ttu-id="b1c99-147">Controles estáticos que têm o \_ ícone SS ou o \_ estilo de bitmap SS</span><span class="sxs-lookup"><span data-stu-id="b1c99-147">Static controls that have the SS\_ICON or SS\_BITMAP style</span></span>
-   <span data-ttu-id="b1c99-148">Trackbars</span><span class="sxs-lookup"><span data-stu-id="b1c99-148">Trackbars</span></span>
-   <span data-ttu-id="b1c99-149">Exibições de árvore</span><span class="sxs-lookup"><span data-stu-id="b1c99-149">Tree Views</span></span>

<span data-ttu-id="b1c99-150">Se os controles anteriores não forem acompanhados por rótulos de texto estáticos ou se os rótulos não forem implementados corretamente, o Microsoft Acessibilidade Ativa não poderá fornecer a [propriedade de nome](name-property.md) correta para aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="b1c99-150">If the preceding controls are not accompanied by static text labels, or if the labels are not implemented correctly, Microsoft Active Accessibility cannot provide the correct [Name property](name-property.md) to client applications.</span></span>

<span data-ttu-id="b1c99-151">A maioria dos controles anteriores realmente tem texto de janela associado.</span><span class="sxs-lookup"><span data-stu-id="b1c99-151">Most of the preceding controls actually do have associated window text.</span></span> <span data-ttu-id="b1c99-152">O editor de recursos gera automaticamente o texto da janela, que consiste em uma cadeia de caracteres genérica, como "Edit1" ou "listbox3".</span><span class="sxs-lookup"><span data-stu-id="b1c99-152">The resource editor automatically generates the window text, which consists of a generic string such as "edit1" or "listbox3".</span></span> <span data-ttu-id="b1c99-153">Embora os desenvolvedores possam substituir o texto da janela gerada por texto mais significativo, a maioria nunca faz.</span><span class="sxs-lookup"><span data-stu-id="b1c99-153">Although developers can replace the generated window text with more meaningful text, most never do.</span></span> <span data-ttu-id="b1c99-154">Como o texto da janela gerado não tem significado para o usuário, o Microsoft Acessibilidade Ativa o ignora e usa o rótulo de texto estático que o acompanha.</span><span class="sxs-lookup"><span data-stu-id="b1c99-154">Because the generated window text has no meaning to the user, Microsoft Active Accessibility ignores it and uses the accompanying static text label instead.</span></span>

## <a name="how-to-find-and-correct-naming-problems"></a><span data-ttu-id="b1c99-155">Como localizar e corrigir problemas de nomenclatura</span><span class="sxs-lookup"><span data-stu-id="b1c99-155">How to Find and Correct Naming Problems</span></span>

<span data-ttu-id="b1c99-156">No formulário de entrada de nome mostrado em como a nomenclatura incorreta causa problemas, a causa dos problemas é que a ordem de tabulação dos controles está incorreta.</span><span class="sxs-lookup"><span data-stu-id="b1c99-156">In the name entry form shown in How Incorrect Naming Causes Problems, the cause of the problems is that the tab order of the controls is incorrect.</span></span> <span data-ttu-id="b1c99-157">Examinar a interface do usuário com uma ferramenta de teste como [inspecionar](inspect-objects.md) revelaria os problemas com a hierarquia de objetos.</span><span class="sxs-lookup"><span data-stu-id="b1c99-157">Examining the UI with a testing tool such as [Inspect](inspect-objects.md) would reveal the problems with the object hierarchy.</span></span> <span data-ttu-id="b1c99-158">A captura de tela a seguir mostra a hierarquia de objetos desfeitos do formulário de entrada de nome como ele aparece na inspeção.</span><span class="sxs-lookup"><span data-stu-id="b1c99-158">The following screen shot shows the broken object hierarchy of the name entry form as it appears in Inspect.</span></span>

![captura de tela da ferramenta inspecionar mostrando uma hierarquia de objeto incorreta do formulário de entrada de nome](images/incorrect-object-hierarchy.png)

<span data-ttu-id="b1c99-160">Na captura de tela anterior, observe que a hierarquia de objetos não corresponde à estrutura dos controles conforme eles aparecem na interface do usuário do formulário de entrada de nome.</span><span class="sxs-lookup"><span data-stu-id="b1c99-160">In the previous screen shot, notice that the object hierarchy does not match the structure of the controls as they appear in the user interface of the name entry form.</span></span> <span data-ttu-id="b1c99-161">Observe também que a [inspeção](inspect-objects.md) atribuiu o nome incorreto ao próximo item (é o controle de edição para inserir o nome e deve ser um "nome:".</span><span class="sxs-lookup"><span data-stu-id="b1c99-161">Also notice that [Inspect](inspect-objects.md) has assigned the incorrect name to the next-to-last item (it is the edit control for entering the first name and should be a named "First Name:".</span></span> <span data-ttu-id="b1c99-162">Por fim, observe que inspecionar não pôde localizar um nome para o último item (é o controle de edição para inserir o sobrenome e deve ter o nome "Last Name:".</span><span class="sxs-lookup"><span data-stu-id="b1c99-162">Finally, notice that Inspect could not find a name for the last item (it is the edit control for entering the last name and should have a name of "Last Name:".</span></span>

<span data-ttu-id="b1c99-163">O exemplo a seguir mostra o conteúdo do arquivo de recurso para o formulário de entrada de nome.</span><span class="sxs-lookup"><span data-stu-id="b1c99-163">The following example shows the contents of the resource file for the name entry form.</span></span> <span data-ttu-id="b1c99-164">Observe que a ordem de tabulação não é consistente com a estrutura lógica dos controles conforme eles aparecem na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="b1c99-164">Notice that the tab order is not consistent with the logical structure of the controls as they appear in the user interface.</span></span> <span data-ttu-id="b1c99-165">Observe também que nenhuma tecla de atalho foi especificada para os dois controles de edição.</span><span class="sxs-lookup"><span data-stu-id="b1c99-165">Also notice that no shortcut keys are specified for the two edit controls.</span></span>

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
END
```

<span data-ttu-id="b1c99-166">Para corrigir os problemas com o formulário de entrada de nome, o arquivo de recurso (. rc) deve ser editado para especificar atalhos de teclado e os controles devem ser colocados na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="b1c99-166">To correct the problems with the name entry form, the resource (.rc) file should be edited to specify keyboard shortcuts, and the controls should be placed in the following order:</span></span>

1.  <span data-ttu-id="b1c99-167">O rótulo de texto estático "&primeiro nome:".</span><span class="sxs-lookup"><span data-stu-id="b1c99-167">The "&First Name:" static text label.</span></span>
2.  <span data-ttu-id="b1c99-168">O controle de edição para inserir o primeiro nome (IDC \_ EDIT1).</span><span class="sxs-lookup"><span data-stu-id="b1c99-168">The edit control for entering the first name (IDC\_EDIT1).</span></span>
3.  <span data-ttu-id="b1c99-169">O rótulo de texto estático "&sobrenome:".</span><span class="sxs-lookup"><span data-stu-id="b1c99-169">The "&Last Name:" static text label.</span></span>
4.  <span data-ttu-id="b1c99-170">O controle de edição para inserir o sobrenome (IDC \_ Edit2).</span><span class="sxs-lookup"><span data-stu-id="b1c99-170">The edit control for entering the last name (IDC\_EDIT2).</span></span>
5.  <span data-ttu-id="b1c99-171">O botão de ação padrão "OK".</span><span class="sxs-lookup"><span data-stu-id="b1c99-171">The "OK" default push button.</span></span>

<span data-ttu-id="b1c99-172">O exemplo a seguir mostra o arquivo de recurso corrigido para o formulário de entrada de nome:</span><span class="sxs-lookup"><span data-stu-id="b1c99-172">The following example shows the corrected resource file for the name entry form:</span></span>

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```

<span data-ttu-id="b1c99-173">Para fazer correções em um arquivo de recurso, você pode editar o arquivo diretamente ou pode usar a ferramenta de ordem de tabulação no Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b1c99-173">To make corrections to a resource file, you can either edit the file directly, or you can use the Tab Order tool in Microsoft Visual Studio.</span></span> <span data-ttu-id="b1c99-174">Você pode acessar a ferramenta de ordem de tabulação no Visual Studio pressionando CTRL + D ou selecionando **ordem de tabulação** no menu **Formatar** .</span><span class="sxs-lookup"><span data-stu-id="b1c99-174">You can access the Tab Order tool in Visual Studio either by pressing CTRL+D, or by selecting **Tab Order** from the **Format** menu.</span></span>

<span data-ttu-id="b1c99-175">Depois de corrigir e recompilar o aplicativo, a interface do usuário do formulário de entrada de nomes terá a mesma aparência anterior.</span><span class="sxs-lookup"><span data-stu-id="b1c99-175">After correcting and rebuilding the application, the UI of the names entry form will look the same as it did before.</span></span> <span data-ttu-id="b1c99-176">No entanto, o Microsoft Acessibilidade Ativa agora fornecerá as propriedades de nome corretas para aplicativos cliente e definirá o foco corretamente quando o usuário pressionar os atalhos de teclado ALT + F ou ALT + L.</span><span class="sxs-lookup"><span data-stu-id="b1c99-176">However, Microsoft Active Accessibility will now provide the correct Name properties to client applications, and will set the focus correctly when the user presses the ALT+F or ALT+L keyboard shortcuts.</span></span> <span data-ttu-id="b1c99-177">Além disso, [Inspecione](inspect-objects.md) mostrará a hierarquia de objetos correta, como mostra a captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1c99-177">Also, [Inspect](inspect-objects.md) will show the correct object hierarchy, as the following screen shot shows.</span></span>

![captura de tela da ferramenta Gerenciador acessível mostrando uma hierarquia de objeto correta do formulário de entrada de nome](images/correct-object-hierarchy.png)

## <a name="how-to-correctly-name-a-trackbar"></a><span data-ttu-id="b1c99-179">Como nomear corretamente um TrackBar</span><span class="sxs-lookup"><span data-stu-id="b1c99-179">How to Correctly Name a Trackbar</span></span>

<span data-ttu-id="b1c99-180">Ao definir um TrackBar (ou controle deslizante), verifique se o rótulo de texto estático principal para o TrackBar aparece antes do TrackBar e se os rótulos de texto estáticos para os intervalos mínimo e máximo aparecem após o TrackBar.</span><span class="sxs-lookup"><span data-stu-id="b1c99-180">When defining a trackbar (or slider), ensure that the main static text label for the trackbar appears before the trackbar, and that the static text labels for the minimum and maximum ranges appear after the trackbar.</span></span> <span data-ttu-id="b1c99-181">Lembre-se de que o Microsoft Acessibilidade Ativa usa o rótulo de texto estático que precede imediatamente um controle como a [Propriedade Name](name-property.md) para o controle.</span><span class="sxs-lookup"><span data-stu-id="b1c99-181">Remember that Microsoft Active Accessibility uses the static text label that immediately precedes a control as the [Name property](name-property.md) for the control.</span></span> <span data-ttu-id="b1c99-182">Colocar o rótulo de texto estático principal imediatamente antes do TrackBar e os outros rótulos depois dele garante que o Microsoft Acessibilidade Ativa forneça a propriedade Name correta para um cliente.</span><span class="sxs-lookup"><span data-stu-id="b1c99-182">Placing the main static text label immediately before the trackbar, and the other labels after it, ensures that Microsoft Active Accessibility provides the correct Name property to a client.</span></span>

<span data-ttu-id="b1c99-183">A ilustração a seguir mostra um TrackBar típico com um rótulo de texto estático principal chamado "velocidade" e rótulos de texto estáticos para os intervalos mínimo ("min") e máximo ("Max").</span><span class="sxs-lookup"><span data-stu-id="b1c99-183">The following illustration shows a typical trackbar with a main static text label called "Speed", and static text labels for the minimum ("min") and maximum ("max") ranges.</span></span>

![ilustração de um controle TrackBar que tem um rótulo principal e rótulos para os intervalos mínimo e máximo](images/speed-trackbar.png)

<span data-ttu-id="b1c99-185">O exemplo a seguir mostra a maneira correta de definir um TrackBar e seus rótulos de texto estáticos no arquivo de recurso:</span><span class="sxs-lookup"><span data-stu-id="b1c99-185">The following example shows the correct way to define a trackbar and its static text labels in the resource file:</span></span>

``` syntax
BEGIN
    ...

    LTEXT           "&Speed",IDC_STATIC,47,20,43,8
    CONTROL         "",IDC_SLIDER1,"msctls_trackbar32",
                    TBS_AUTOTICKS | TBS_BOTH | WS_TABSTOP,
                    32,32,62,23
    LTEXT           "min",IDC_STATIC,16,37,15,8
    LTEXT           "max",IDC_STATIC,94,38,43,8

    ...
END
```

## <a name="how-to-use-invisible-labels-to-name-controls"></a><span data-ttu-id="b1c99-186">Como usar rótulos invisíveis em controles de nome</span><span class="sxs-lookup"><span data-stu-id="b1c99-186">How to Use Invisible Labels to Name Controls</span></span>

<span data-ttu-id="b1c99-187">Nem sempre é possível ou desejável ter um rótulo visível para cada controle.</span><span class="sxs-lookup"><span data-stu-id="b1c99-187">It is not always possible or desirable to have a visible label for every control.</span></span> <span data-ttu-id="b1c99-188">Por exemplo, às vezes, a adição de rótulos pode causar alterações indesejáveis na aparência da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="b1c99-188">For example, sometimes adding labels can cause undesirable changes in the appearance of the UI.</span></span> <span data-ttu-id="b1c99-189">Nesse caso, você pode usar rótulos invisíveis.</span><span class="sxs-lookup"><span data-stu-id="b1c99-189">In this case, you can use invisible labels.</span></span> <span data-ttu-id="b1c99-190">O Microsoft Acessibilidade Ativa ainda coletará o texto associado a um rótulo invisível, mas o rótulo não aparecerá ou interferirá com a interface do usuário visual.</span><span class="sxs-lookup"><span data-stu-id="b1c99-190">Microsoft Active Accessibility will still pick up the text associated with an invisible label, but the label will not appear in, or interfere with, the visual UI.</span></span>

<span data-ttu-id="b1c99-191">Assim como acontece com rótulos visíveis, um rótulo invisível deve preceder imediatamente o controle na ordem de tabulação.</span><span class="sxs-lookup"><span data-stu-id="b1c99-191">As with visible labels, an invisible label must immediately precede the control in the tab order.</span></span> <span data-ttu-id="b1c99-192">Para tornar um rótulo invisível em um arquivo de recurso (. rc), adicione `NOT WS_VISIBLE` ou `|~WS_VISIBLE` à parte do estilo do controle de texto estático.</span><span class="sxs-lookup"><span data-stu-id="b1c99-192">To make a label invisible in a resource file (.rc), add `NOT WS_VISIBLE` or `|~WS_VISIBLE` to the style part of the static text control.</span></span> <span data-ttu-id="b1c99-193">Se você estiver usando o editor de recursos no Visual Studio, poderá definir a propriedade Visible como false.</span><span class="sxs-lookup"><span data-stu-id="b1c99-193">If you are using the Resource Editor in Visual Studio, you can set the Visible property to False.</span></span>

## <a name="how-to-use-direct-annotation-to-specify-the-name-property"></a><span data-ttu-id="b1c99-194">Como usar a anotação direta para especificar a propriedade Name</span><span class="sxs-lookup"><span data-stu-id="b1c99-194">How to Use Direct Annotation to Specify the Name Property</span></span>

<span data-ttu-id="b1c99-195">Os proxies padrão incluídos no componente Microsoft Acessibilidade Ativa Runtime, Oleacc.dll, fornecem automaticamente um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para todos os controles padrão do Windows.</span><span class="sxs-lookup"><span data-stu-id="b1c99-195">The default proxies included in the Microsoft Active Accessibility runtime component, Oleacc.dll, automatically provide an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for all of the standard Windows controls.</span></span> <span data-ttu-id="b1c99-196">Se você personalizar um controle padrão do Windows, os proxies padrão farão seu melhor para fornecer com precisão todas as propriedades de **IAccessible** para seu controle personalizado.</span><span class="sxs-lookup"><span data-stu-id="b1c99-196">If you customize a standard Windows control, the default proxies do their best to accurately provide all of the **IAccessible** properties for your customized control.</span></span> <span data-ttu-id="b1c99-197">Você deve testar exaustivamente um controle personalizado para garantir que os proxies padrão estejam fornecendo valores de propriedade precisos e completos.</span><span class="sxs-lookup"><span data-stu-id="b1c99-197">You should thoroughly test a customized control to ensure that the default proxies are providing accurate and complete property values.</span></span> <span data-ttu-id="b1c99-198">Se o teste revelar valores de propriedade imprecisos ou incompletos, você poderá usar a técnica de anotação dinâmica chamada anotação direta para fornecer valores de propriedade corretos e adicionar os que estão ausentes.</span><span class="sxs-lookup"><span data-stu-id="b1c99-198">If testing reveals inaccurate or incomplete property values, you may be able to use the Dynamic Annotation technique called direct annotation to provide correct property values and add those that are missing.</span></span>

<span data-ttu-id="b1c99-199">Observe que a anotação dinâmica não é apenas para controles suportados pelos proxies do Microsoft Acessibilidade Ativa.</span><span class="sxs-lookup"><span data-stu-id="b1c99-199">Note that Dynamic Annotation is not just for controls supported by the Microsoft Active Accessibility proxies.</span></span> <span data-ttu-id="b1c99-200">Você também pode usá-lo para modificar ou fornecer propriedades para qualquer controle que forneça sua própria implementação de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="b1c99-200">You can also use it to modify or provide properties for any control that provides its own [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation.</span></span>

<span data-ttu-id="b1c99-201">Esta seção se concentra em usar a anotação direta para fornecer um valor correto para a [Propriedade Name](name-property.md) do objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para um controle.</span><span class="sxs-lookup"><span data-stu-id="b1c99-201">This section focuses on using direct annotation to provide a correct value for the [Name property](name-property.md) of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for a control.</span></span> <span data-ttu-id="b1c99-202">Você também pode usar a anotação direta para fornecer outros valores de propriedades.</span><span class="sxs-lookup"><span data-stu-id="b1c99-202">You can use direct annotation to provide other properties values as well.</span></span> <span data-ttu-id="b1c99-203">Além disso, outras técnicas de anotação dinâmica ao lado da anotação direta estão disponíveis, e os recursos e funcionalidades da API de anotação dinâmica se estendem muito além do que é descrito nesta seção.</span><span class="sxs-lookup"><span data-stu-id="b1c99-203">Also, other Dynamic Annotation techniques beside direct annotation are available, and the features and capabilities of the Dynamic Annotation API extend far beyond what is described in this section.</span></span> <span data-ttu-id="b1c99-204">Para obter mais informações sobre a anotação dinâmica, consulte [API de anotação dinâmica](dynamic-annotation-api.md).</span><span class="sxs-lookup"><span data-stu-id="b1c99-204">For more information about Dynamic Annotation, see [Dynamic Annotation API](dynamic-annotation-api.md).</span></span>

### <a name="steps-for-annotating-the-name-property"></a><span data-ttu-id="b1c99-205">Etapas para anotar a propriedade Name</span><span class="sxs-lookup"><span data-stu-id="b1c99-205">Steps for Annotating the Name Property</span></span>

<span data-ttu-id="b1c99-206">Usar a anotação direta para alterar a [Propriedade Name](name-property.md) de um controle envolve as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1c99-206">Using direct annotation to change the [Name Property](name-property.md) of a control involves the following steps.</span></span>

1.  <span data-ttu-id="b1c99-207">Inclua os seguintes arquivos de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b1c99-207">Include the following header files:</span></span>
    -   <span data-ttu-id="b1c99-208">Initguid. h</span><span class="sxs-lookup"><span data-stu-id="b1c99-208">Initguid.h</span></span>
    -   <span data-ttu-id="b1c99-209">OleAcc. h</span><span class="sxs-lookup"><span data-stu-id="b1c99-209">Oleacc.h</span></span>

    > [!Note]  
    > <span data-ttu-id="b1c99-210">Para definir GUIDs, você deve incluir Initguid. h antes de OleAcc. h no mesmo arquivo.</span><span class="sxs-lookup"><span data-stu-id="b1c99-210">To define GUIDs, you must include Initguid.h before Oleacc.h in the same file.</span></span>

     

2.  <span data-ttu-id="b1c99-211">Inicialize a biblioteca de Component Object Model (COM) chamando a função [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) , normalmente durante o processo de inicialização do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b1c99-211">Initialize the Component Object Model (COM) library by calling the [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function, typically during the application initialization process.</span></span>
3.  <span data-ttu-id="b1c99-212">Logo após a criação do controle de destino (normalmente durante a mensagem [ \_ INITDIALOG do WM](../dlgbox/wm-initdialog.md) ), crie uma instância do Gerenciador de anotações e obtenha um ponteiro para o ponteiro [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="b1c99-212">Soon after the target control is created (typically during the [WM\_INITDIALOG](../dlgbox/wm-initdialog.md) message), create an instance of the annotation manager and obtain a pointer to its [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) pointer.</span></span>
4.  <span data-ttu-id="b1c99-213">Anote a [Propriedade Name](name-property.md) do controle de destino usando o método [**IAccPropServices:: SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) .</span><span class="sxs-lookup"><span data-stu-id="b1c99-213">Annotate the [Name Property](name-property.md) of the target control by using the [**IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) method.</span></span>

5.  <span data-ttu-id="b1c99-214">Libere o ponteiro [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="b1c99-214">Release the [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) pointer.</span></span>
6.  <span data-ttu-id="b1c99-215">Antes de o controle de destino ser destruído (normalmente ao manipular a mensagem de [ \_ destruição do WM](../winmsg/wm-destroy.md) ), crie uma instância do Gerenciador de anotações e obtenha um ponteiro para sua interface [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="b1c99-215">Before the target control is destroyed (typically when handling the [WM\_DESTROY](../winmsg/wm-destroy.md) message), create an instance of the annotation manager and obtain a pointer to its [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) interface.</span></span>
7.  <span data-ttu-id="b1c99-216">Use o método [**IAccPropServices:: ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) para limpar as anotações de [propriedade de nome](name-property.md) do controle de destino.</span><span class="sxs-lookup"><span data-stu-id="b1c99-216">Use the [**IAccPropServices::ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) method to clear the [Name property](name-property.md) annotations from the target control.</span></span>
8.  <span data-ttu-id="b1c99-217">Libere o ponteiro [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="b1c99-217">Release the [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) pointer.</span></span>
9.  <span data-ttu-id="b1c99-218">Antes de o aplicativo sair (normalmente durante o processamento da mensagem do [WM \_ Destroy](../winmsg/wm-destroy.md) ), libere a biblioteca com chamando a função [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .</span><span class="sxs-lookup"><span data-stu-id="b1c99-218">Before your application exits (typically while processing the [WM\_DESTROY](../winmsg/wm-destroy.md) message), release the COM library by calling the [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function.</span></span>

<span data-ttu-id="b1c99-219">A função [**IAccPropServices:: SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) usa cinco parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b1c99-219">The [**IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) function takes five parameters.</span></span> <span data-ttu-id="b1c99-220">Os três primeiros —*HWND*, *idObject* e *idChild*— combinam para identificar o controle.</span><span class="sxs-lookup"><span data-stu-id="b1c99-220">The first three—*hwnd*, *idObject*, and *idChild*—combine to identify the control.</span></span> <span data-ttu-id="b1c99-221">O quarto parâmetro, *idProp*, especifica o identificador da propriedade a ser alterada.</span><span class="sxs-lookup"><span data-stu-id="b1c99-221">The fourth parameter, *idProp*, specifies the identifier of the property to be changed.</span></span> <span data-ttu-id="b1c99-222">Para alterar a [Propriedade Name](name-property.md), defina *idProp* como **Propid \_ ACC \_ Name**.</span><span class="sxs-lookup"><span data-stu-id="b1c99-222">To change the [Name property](name-property.md), set *idProp* to **PROPID\_ACC\_NAME**.</span></span> <span data-ttu-id="b1c99-223">(Para obter uma lista de outras propriedades que podem ser definidas por meio da anotação direta, consulte [usando anotação direta](using-direct-annotation.md).) O último parâmetro de **SetHwndPropStr**, *Str*, é a nova cadeia de caracteres a ser usada como a propriedade Name.</span><span class="sxs-lookup"><span data-stu-id="b1c99-223">(For a list of other properties that you can set through direct annotation, see [Using Direct Annotation](using-direct-annotation.md).) The last parameter of **SetHwndPropStr**, *str*, is the new string to use as the Name property.</span></span>

### <a name="example-of-annotating-the-name-property"></a><span data-ttu-id="b1c99-224">Exemplo de anotação da propriedade Name</span><span class="sxs-lookup"><span data-stu-id="b1c99-224">Example of Annotating the Name Property</span></span>

<span data-ttu-id="b1c99-225">O código de exemplo a seguir mostra como usar a anotação direta para alterar a [Propriedade Name](name-property.md) do objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para um controle.</span><span class="sxs-lookup"><span data-stu-id="b1c99-225">The following example code shows how to use direct annotation to change the [Name property](name-property.md) of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for a control.</span></span> <span data-ttu-id="b1c99-226">Para simplificar as coisas, o exemplo usa uma cadeia de caracteres embutida em código ("novo nome do controle") para definir a propriedade Name.</span><span class="sxs-lookup"><span data-stu-id="b1c99-226">To keep things simple, the example uses a hard-coded string ("New Control Name") to set the Name property.</span></span> <span data-ttu-id="b1c99-227">As cadeias de caracteres embutidas em código não devem ser usadas na versão final do seu aplicativo porque não podem ser localizadas.</span><span class="sxs-lookup"><span data-stu-id="b1c99-227">Hard-coded strings should not be used in the final version of your application because they cannot be localized.</span></span> <span data-ttu-id="b1c99-228">Em vez disso, sempre carregue as cadeias de caracteres do arquivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b1c99-228">Instead, always load strings from your resource file.</span></span> <span data-ttu-id="b1c99-229">Além disso, o exemplo não mostra as chamadas para as funções [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .</span><span class="sxs-lookup"><span data-stu-id="b1c99-229">Also, the example does not show the calls to the [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) functions.</span></span>


```C++
#include <initguid.h>
#include <oleacc.h>

// AnnotateControlName - Uses direct annotation to change the Name property 
// of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose Name property is to be changed.
HRESULT AnnotateControlName(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;        

    IAccPropServices *pAccPropSvc = NULL;  

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Set the Name property for the control.
    // Note: A hard-coded string is used here to keep the example simple.
    // Always use localizable string resources in your applications. 
    hr = pAccPropSvc->SetHwndPropStr(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        PROPID_ACC_NAME, L"New Control Name");

    pAccPropSvc->Release();
    
    return hr;
}

// RemoveAnnotatedNameFromControl - Removes the annotated name from the 
// Name property of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose annotated name is to be removed.
HRESULT RemoveAnnotatedNameFromControl(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;

    IAccPropServices *pAccPropSvc = NULL;

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Remove the annotated name from the Name property for the control.
    MSAAPROPID propid = PROPID_ACC_NAME;
    hr = pAccPropSvc->ClearHwndProps(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        &propid, 1);

    // Release the annotation manager.
    pAccPropSvc->Release();

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="b1c99-230">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b1c99-230">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b1c99-231">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="b1c99-231">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b1c99-232">API de anotação dinâmica</span><span class="sxs-lookup"><span data-stu-id="b1c99-232">Dynamic Annotation API</span></span>](dynamic-annotation-api.md)
</dt> <dt>

[<span data-ttu-id="b1c99-233">Fornecendo a propriedade Name</span><span class="sxs-lookup"><span data-stu-id="b1c99-233">Providing the Name Property</span></span>](providing-the-name-property.md)
</dt> <dt>

[<span data-ttu-id="b1c99-234">Ferramentas de teste</span><span class="sxs-lookup"><span data-stu-id="b1c99-234">Testing Tools</span></span>](testing-tools.md)
</dt> </dl>

 

 