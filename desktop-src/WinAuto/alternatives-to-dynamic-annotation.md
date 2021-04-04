---
title: Alternativas para anotação dinâmica
description: Alternativas para anotação dinâmica
ms.assetid: d8019c65-620b-4aa2-a631-cc32f34e5510
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0027cf9a9913efdff379d2f0c01e7bf22bc94f44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084665"
---
# <a name="alternatives-to-dynamic-annotation"></a><span data-ttu-id="3c2b3-103">Alternativas para anotação dinâmica</span><span class="sxs-lookup"><span data-stu-id="3c2b3-103">Alternatives to Dynamic Annotation</span></span>

<span data-ttu-id="3c2b3-104">Há outras maneiras de fornecer suporte personalizado para o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para elementos de interface do usuário e, em alguns casos, eles são a solução correta.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-104">There are other ways to provide customized [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) support for UI elements, and in some cases, they are the correct solution.</span></span> <span data-ttu-id="3c2b3-105">Antes da anotação dinâmica, essas técnicas alternativas eram as únicas opções disponíveis para os desenvolvedores.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-105">Prior to Dynamic Annotation, these alternative techniques were the only options available to developers.</span></span> <span data-ttu-id="3c2b3-106">Eles incluem a implementação de toda a interface **IAccessible** e técnicas programáticas.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-106">They include implementing all of the **IAccessible** interface and programmatic techniques.</span></span>

## <a name="implementing-all-of-the-iaccessible-interface"></a><span data-ttu-id="3c2b3-107">Implementando toda a interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="3c2b3-107">Implementing All of the IAccessible Interface</span></span>

<span data-ttu-id="3c2b3-108">Uma técnica alternativa é implementar toda a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="3c2b3-108">One alternative technique is to implement all of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="3c2b3-109">Essa abordagem é geralmente necessária para controles personalizados ou elementos de interface de usuário diferentes. no entanto, os custos de desenvolvimento e teste são significativos o suficiente para que sejam evitados, a menos que sejam verdadeiramente necessários.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-109">This approach is often necessary for custom controls or radically different UI elements; however, the development and test costs are significant enough that it should be avoided unless truly necessary.</span></span> <span data-ttu-id="3c2b3-110">Se a meta for modificar uma única propriedade, o custo será difícil de justificar.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-110">If the goal is to modify a single property, the cost is difficult to justify.</span></span>

## <a name="programmatic-techniques"></a><span data-ttu-id="3c2b3-111">Técnicas programáticas</span><span class="sxs-lookup"><span data-stu-id="3c2b3-111">Programmatic Techniques</span></span>

<span data-ttu-id="3c2b3-112">Outra opção é usar as técnicas de subclasse e encapsulamento para modificar as informações que estão sendo expostas para uma propriedade específica.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-112">Another option is to use subclassing and wrapping techniques to modify the information being exposed for a specific property.</span></span> <span data-ttu-id="3c2b3-113">Essa é a técnica que a anotação dinâmica pretende substituir.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-113">This is the technique that Dynamic Annotation is intended to replace.</span></span> <span data-ttu-id="3c2b3-114">Para substituir uma única propriedade usando a subclasse e o encapsulamento, o desenvolvedor deve executar as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="3c2b3-114">To override a single property by using subclassing and wrapping, the developer must perform the following steps:</span></span>

1.  <span data-ttu-id="3c2b3-115">Subclasse a HWND do objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="3c2b3-115">Subclass the HWND of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object.</span></span>
2.  <span data-ttu-id="3c2b3-116">Interceptar a mensagem do [**WM \_ GetObject**](wm-getobject.md) para o valor correto de IParam/OBJID.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-116">Intercept the [**WM\_GETOBJECT**](wm-getobject.md) message for the correct IParam/OBJID value.</span></span>
3.  <span data-ttu-id="3c2b3-117">Encaminhe a mensagem do [**WM \_ GetObject**](wm-getobject.md) para a classe base usando a função [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3c2b3-117">Forward the [**WM\_GETOBJECT**](wm-getobject.md) message to the base class using the [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) function.</span></span> <span data-ttu-id="3c2b3-118">Se zero for retornado, chame [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject); caso contrário, chame [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) no valor retornado para obter o ponteiro de interface de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativo do controle.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-118">If zero is returned, call [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject); otherwise, call [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) on the returned value to obtain the control's native [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>
4.  <span data-ttu-id="3c2b3-119">Crie uma classe wrapper, que implementa o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e encapsula o ponteiro da interface **IAccessible** retornado da etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-119">Create a wrapper class, which implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) and wraps the **IAccessible** interface pointer returned from the previous step.</span></span> <span data-ttu-id="3c2b3-120">Essa classe wrapper envia todos os métodos e propriedades para o ponteiro da interface **IAccessible** original, exceto aqueles que devem ser substituídos.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-120">This wrapper class sends all methods and properties to the original **IAccessible** interface pointer, except those that are to be overridden.</span></span> <span data-ttu-id="3c2b3-121">Isso envolve escrever código de encaminhamento para todas as propriedades e métodos de 21 da interface do **IAccessible** , independentemente de quantos são realmente substituídos.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-121">This involves writing forwarding code for all of the **IAccessible** interface's 21 properties and methods, regardless of how many are actually overridden.</span></span>

<span data-ttu-id="3c2b3-122">Além disso, os desenvolvedores devem verificar as seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="3c2b3-122">Also, developers must verify the following conditions:</span></span>

-   <span data-ttu-id="3c2b3-123">O método ou a propriedade substituído só deve manipular as IDs filho necessárias e encaminhar todas as outras para o ponteiro da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) original.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-123">The overridden method or property must only handle the required child IDs, and forward all others to the original [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>
-   <span data-ttu-id="3c2b3-124">O encapsulamento também deve encaminhar as interfaces [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) e [**IOleWindow**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) somente se o objeto original oferecer suporte a elas.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-124">Wrapping must also forward [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) and [**IOleWindow**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) interfaces only if the original object supports them.</span></span>
-   <span data-ttu-id="3c2b3-125">A contagem de referência deve ser tratada corretamente, especialmente se houver suporte para outras interfaces.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-125">Reference counting must be handled correctly, especially if other interfaces are supported.</span></span>
-   <span data-ttu-id="3c2b3-126">Os valores de retorno de [**IDispatch**](idispatch-interface.md) devem ser tratados corretamente, especialmente com o método [**ITypeInfo:: Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) , que deve ser chamado com um ponteiro de interface para a interface do wrapper, não um ponteiro para a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) original.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-126">[**IDispatch**](idispatch-interface.md) return values must be handled correctly, especially with the [**ITypeInfo::Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) method, which must be called with an interface pointer to the wrapper interface, not a pointer to the original [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span>

<span data-ttu-id="3c2b3-127">Essas técnicas exigem uma quantidade considerável de trabalho, mesmo se apenas uma ou duas propriedades precisarem ser substituídas.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-127">These techniques require a considerable amount of work, even if only one or two properties need to be overridden.</span></span> <span data-ttu-id="3c2b3-128">A maior parte do código resultante se preocupa com a subclasse e o encapsulamento, e apenas uma pequena fração está, na verdade, fornecendo as informações substituídas.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-128">The majority of the resulting code is concerned with subclassing and wrapping, and only a small fraction is actually providing the overridden information.</span></span>

<span data-ttu-id="3c2b3-129">No entanto, há cenários em que essas técnicas são necessárias.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-129">However, there are scenarios in which these techniques are needed.</span></span> <span data-ttu-id="3c2b3-130">Por exemplo, se você estiver fazendo alterações estruturais para criar um elemento de interface do usuário de espaço reservado, deverá usar essas técnicas em vez da anotação dinâmica.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-130">For example, if you are making structural changes to create a placeholder UI element, then you should use these techniques rather than Dynamic Annotation.</span></span>

## <a name="fixing-names-derived-from-labels"></a><span data-ttu-id="3c2b3-131">Corrigindo nomes derivados de rótulos</span><span class="sxs-lookup"><span data-stu-id="3c2b3-131">Fixing Names Derived from Labels</span></span>

<span data-ttu-id="3c2b3-132">Alguns controles comuns do Microsoft Win32, como o controle caixa de edição, são quase sempre usados com um rótulo (uma entrada LTEXT no arquivo de recurso) ou uma caixa de grupo (GROUPBOX no arquivo de recurso).</span><span class="sxs-lookup"><span data-stu-id="3c2b3-132">Some Microsoft Win32 common controls, such as the edit box control, are nearly always used with a label (an LTEXT entry in the resource file) or a group box (GROUPBOX in the resource file).</span></span> <span data-ttu-id="3c2b3-133">O Microsoft Acessibilidade Ativa deriva automaticamente a propriedade Name do controle a partir de seu rótulo.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-133">Microsoft Active Accessibility automatically derives the name property of the control from its label.</span></span> <span data-ttu-id="3c2b3-134">Para esses controles, o texto da janela (mostrado em Microsoft Visual Studio como a propriedade Name ou ID) é ignorado, pois geralmente é gerado automaticamente e raramente é muito descritivo; por exemplo, "IDC \_ EDIT1".</span><span class="sxs-lookup"><span data-stu-id="3c2b3-134">For such controls, the window text (shown in Microsoft Visual Studio as the Name or ID property) is ignored, because it is usually autogenerated and seldom very descriptive; for example, "IDC\_EDIT1".</span></span>

<span data-ttu-id="3c2b3-135">Se a interface do usuário do aplicativo não for projetada corretamente, o Microsoft Acessibilidade Ativa poderá não conseguir definir o nome corretamente.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-135">If the user interface of the application is not designed correctly, Microsoft Active Accessibility might not be able to set the name correctly.</span></span> <span data-ttu-id="3c2b3-136">Para ser associado a um controle, a caixa rótulo ou grupo deve ser colocada imediatamente antes do controle dinâmico na ordem de tabulação.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-136">To be associated with a control, the label or group box must be placed immediately before the dynamic control in the tab order.</span></span>

<span data-ttu-id="3c2b3-137">A ordem de Tabulação pode ser alterada usando a ferramenta no Visual Studio (no menu **Formatar** quando o editor de recursos está aberto) ou editando diretamente o arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-137">Tab order can be changed by using the tool in Visual Studio (on the **Format** menu when the resource editor is open) or by directly editing the resource file.</span></span>

<span data-ttu-id="3c2b3-138">O exemplo a seguir mostra a descrição de um arquivo de recurso de uma caixa de diálogo que contém duas caixas de edição rotuladas.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-138">The following example shows a resource file's description of a dialog box that contains two labeled edit boxes.</span></span>


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
END
```



<span data-ttu-id="3c2b3-139">Neste exemplo, os rótulos e controles não estão listados na ordem de tabulação correta.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-139">In this example, the labels and controls are not listed in the correct tab order.</span></span> <span data-ttu-id="3c2b3-140">Como resultado, o Microsoft Acessibilidade Ativa atribui o nome "Last Name" à caixa de edição First-Name e não há nenhum nome à caixa de edição Last-Name.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-140">As a result, Microsoft Active Accessibility assigns the name "Last Name" to the first-name edit box, and no name at all to the last-name edit box.</span></span>

<span data-ttu-id="3c2b3-141">O exemplo a seguir mostra a listagem de recursos correta.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-141">The following example shows the correct resource listing.</span></span> <span data-ttu-id="3c2b3-142">Observe também que as teclas de atalho foram designadas nos rótulos.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-142">Note also that shortcut keys have been designated in the labels.</span></span>


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```



<span data-ttu-id="3c2b3-143">Quando os controles têm rótulos suplementares, como para valores mínimo e máximo em um TrackBar, esses rótulos devem ser colocados após o controle na ordem de tabulação.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-143">When controls have supplementary labels, such as for minimum and maximum values on a trackbar, these labels should be placed after the control in the tab order.</span></span> <span data-ttu-id="3c2b3-144">O rótulo principal do controle deve aparecer imediatamente antes do próprio controle.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-144">The main label of the control must appear immediately before the control itself.</span></span>

## <a name="naming-controls-without-labels"></a><span data-ttu-id="3c2b3-145">Controles de nomenclatura sem rótulos</span><span class="sxs-lookup"><span data-stu-id="3c2b3-145">Naming Controls Without Labels</span></span>

<span data-ttu-id="3c2b3-146">Nem sempre é possível ou desejável ter um rótulo visível para cada controle.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-146">It is not always possible or desirable to have a visible label for every control.</span></span> <span data-ttu-id="3c2b3-147">No entanto, você ainda pode fornecer um nome para o controle adicionando um rótulo invisível.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-147">However, you can still provide a name for the control by adding an invisible label.</span></span> <span data-ttu-id="3c2b3-148">Como sempre, o rótulo invisível deve preceder imediatamente o controle na ordem de tabulação.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-148">As always, the invisible label must immediately precede the control in the tab order.</span></span>

<span data-ttu-id="3c2b3-149">Se você estiver usando o editor de recursos no Microsoft Visual Studio .NET, poderá definir a propriedade Visible como false.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-149">If you are using the Resource Editor in Microsoft Visual Studio .NET, you can set the Visible property to False.</span></span> <span data-ttu-id="3c2b3-150">Para tornar o rótulo invisível ao editar o arquivo de recurso (. rc), adicione NOT WS \_ visível ou à parte de estilo do controle rótulo, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-150">To make the label invisible when editing the resource file (.rc), add NOT WS\_VISIBLE or to the style part of the label control, as shown in the following example.</span></span>


```C++
    LTEXT           "&FullName:",IDC_STATIC,111,23,44,8,NOT WS_VISIBLE
```



<span data-ttu-id="3c2b3-151">Observe que qualquer tecla de atalho designada funciona mesmo que o rótulo esteja invisível.</span><span class="sxs-lookup"><span data-stu-id="3c2b3-151">Note that any designated shortcut key works even though the label is invisible.</span></span>

 

 