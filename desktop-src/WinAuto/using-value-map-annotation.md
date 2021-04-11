---
title: Usando anotação de mapa de valor
description: Para o código de exemplo, consulte exemplo de anotação de mapa de valor.
ms.assetid: 29be74c7-a7c2-41f4-8b94-5771988b74ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a3e8d003d863372e21a413fad56bc93b977ee3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366069"
---
# <a name="using-value-map-annotation"></a><span data-ttu-id="5c684-103">Usando anotação de mapa de valor</span><span class="sxs-lookup"><span data-stu-id="5c684-103">Using Value Map Annotation</span></span>

<span data-ttu-id="5c684-104">**Para criar um mapa de valor**</span><span class="sxs-lookup"><span data-stu-id="5c684-104">**To create a value map**</span></span>

1.  <span data-ttu-id="5c684-105">**Crie uma cadeia de caracteres de mapeamento.**</span><span class="sxs-lookup"><span data-stu-id="5c684-105">**Create a mapping string.**</span></span>

    <span data-ttu-id="5c684-106">Uma cadeia de caracteres de mapeamento é uma lista dos valores numéricos de um controle que correspondem a uma cadeia de caracteres legível em Unicode.</span><span class="sxs-lookup"><span data-stu-id="5c684-106">A mapping string is a list of a control's numeric values corresponding to a human-readable string in Unicode.</span></span> <span data-ttu-id="5c684-107">Ele começa com "A:" seguido de um número que indica o tipo de índice usado.</span><span class="sxs-lookup"><span data-stu-id="5c684-107">It starts with "A:" followed by a number that indicates the type of index used.</span></span> <span data-ttu-id="5c684-108">Somente índices de imagem têm suporte; Portanto, o tipo de índice é sempre 0.</span><span class="sxs-lookup"><span data-stu-id="5c684-108">Only image indexes are supported; therefore the index type is always 0.</span></span>

    <span data-ttu-id="5c684-109">A cadeia de caracteres é seguida por: índice: pares de resultados.</span><span class="sxs-lookup"><span data-stu-id="5c684-109">The string is followed by :index:result pairs.</span></span> <span data-ttu-id="5c684-110">O "índice" é um número que representa um índice de imagem para uma exibição de List-View ou de árvore ou o valor de um controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="5c684-110">The "index" is a number representing an image index for a List-View or Tree-View, or the value for a slider control.</span></span>

    <span data-ttu-id="5c684-111">O valor resultante é um número obtido ao mapear a propriedade de função ou estado para um controle de exibição de lista ou de árvore.</span><span class="sxs-lookup"><span data-stu-id="5c684-111">The resulting value is a number obtained when you map the Role or State property for a list view or tree view control.</span></span> <span data-ttu-id="5c684-112">Esses números são expressos em decimal ou hexadecimal com um prefixo "0x".</span><span class="sxs-lookup"><span data-stu-id="5c684-112">Such numbers are expressed in decimal or hexadecimal with an "0x" prefix.</span></span>

    <span data-ttu-id="5c684-113">A cadeia de caracteres de mapeamento sempre termina com um dois pontos finais (":").</span><span class="sxs-lookup"><span data-stu-id="5c684-113">The mapping string is always terminated with a final colon (":").</span></span>

    <span data-ttu-id="5c684-114">Veja a seguir um exemplo de um mapa de anotação para as propriedades State e role de uma caixa de seleção em um controle de exibição de lista ou de árvore.</span><span class="sxs-lookup"><span data-stu-id="5c684-114">The following is an example of an annotation map for the State and Role properties of a check box in a list view or tree view control.</span></span> <span data-ttu-id="5c684-115">Há dois itens na exibição que representam as caixas de seleção e cada uma tem imagens correspondentes ao estado marcado e desmarcado.</span><span class="sxs-lookup"><span data-stu-id="5c684-115">There are two items in the view that represent check boxes, and each has images corresponding to the checked and unchecked state.</span></span>

    ```C++
    LPCWSTR g_ListOrTreeStateMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x00" // Image 0 is normal !
    L":1:0x10" // Image 1 is checked - STATE_SYSTEM_CHECKED (0x10) !
    L":";

    LPCWSTR g_ListOrTreeRoleMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x2C" // Image 0 is a check box - ROLE_SYSTEM_CHECKBUTTON
    (0x2c) !
    L":1:0x2C" // image 1 is also a check box !
    L":";
    ```

    

    <span data-ttu-id="5c684-116">Para valores de função e estado válidos, consulte [funções de objeto](object-roles.md) e constantes de estado do [objeto](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5c684-116">For valid Role and State values, see [Object Roles](object-roles.md) and [Object State Constants](object-state-constants.md).</span></span>

    <span data-ttu-id="5c684-117">O valor do índice pode ser negativo quando você mapeia as propriedades de um controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="5c684-117">The index value may be negative when you map properties for a slider control.</span></span>

    <span data-ttu-id="5c684-118">Quando você mapeia um valor ou uma propriedade de descrição, o resultado é uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5c684-118">When you map a Value or Description property, the result is a string.</span></span> <span data-ttu-id="5c684-119">As cadeias de caracteres não estão entre aspas e os dois-pontos atuam como delimitadores.</span><span class="sxs-lookup"><span data-stu-id="5c684-119">Strings are not quoted and the colons act as delimiters.</span></span>

    <span data-ttu-id="5c684-120">Para obter mais informações, consulte [formato do mapa de anotação](value-map-annotation.md).</span><span class="sxs-lookup"><span data-stu-id="5c684-120">For more information, see [Annotation Map Format](value-map-annotation.md).</span></span>

2.  <span data-ttu-id="5c684-121">**Crie o Gerenciador de anotações e obtenha um ponteiro para sua** interface [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)**.**</span><span class="sxs-lookup"><span data-stu-id="5c684-121">**Create the annotation manager and obtain a pointer to its**[**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)**interface.**</span></span>

    <span data-ttu-id="5c684-122">Veja a seguir um exemplo de como criar o Gerenciador de anotações.</span><span class="sxs-lookup"><span data-stu-id="5c684-122">The following is an example of how to create the annotation manager.</span></span>

    ```C++
    IAccPropServices * pAccPropSvc = NULL;
    HRESULT hr = CoCreateInstance(CLSID_AccPropServices, NULL,
    CLSCTX_SERVER, IID_IAccPropServices, (void**) & pAccPropSvc));
    
    ```

    

3.  <span data-ttu-id="5c684-123">**Anexe a cadeia de caracteres de mapeamento ao controle.**</span><span class="sxs-lookup"><span data-stu-id="5c684-123">**Attach the mapping string to the control.**</span></span>

    <span data-ttu-id="5c684-124">Chame [**IAccPropServices:: SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr), passando o **HWND** do controle e um ponteiro para a cadeia de caracteres de mapeamento.</span><span class="sxs-lookup"><span data-stu-id="5c684-124">Call [**IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr), passing the **HWND** of the control and a pointer to the mapping string.</span></span>

    <span data-ttu-id="5c684-125">O parâmetro *IdProp* será um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="5c684-125">The *IdProp* parameter will be one of the following.</span></span>

    

    | <span data-ttu-id="5c684-126">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5c684-126">Parameter</span></span>                   | <span data-ttu-id="5c684-127">Usado para</span><span class="sxs-lookup"><span data-stu-id="5c684-127">Used for</span></span>                                                |
    |-----------------------------|---------------------------------------------------------|
    | <span data-ttu-id="5c684-128">MSAAPROPID \_ ROLEMAP</span><span class="sxs-lookup"><span data-stu-id="5c684-128">MSAAPROPID\_ROLEMAP</span></span>         | <span data-ttu-id="5c684-129">Para definir um mapa de função para exibição de lista ou controles de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="5c684-129">To set a role map for list view or tree view controls.</span></span>  |
    | <span data-ttu-id="5c684-130">MSAAPROPID \_ STATEMAP</span><span class="sxs-lookup"><span data-stu-id="5c684-130">MSAAPROPID\_STATEMAP</span></span>        | <span data-ttu-id="5c684-131">Para definir um mapa de estado para exibição de lista ou controles de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="5c684-131">To set a state map for list view or tree view controls.</span></span> |
    | <span data-ttu-id="5c684-132">PROPID \_ ACC \_ DESCRIPTIONMAP</span><span class="sxs-lookup"><span data-stu-id="5c684-132">PROPID\_ACC\_DESCRIPTIONMAP</span></span> | <span data-ttu-id="5c684-133">Para definir um mapa de descrição para exibição de lista ou exibições de árvore.</span><span class="sxs-lookup"><span data-stu-id="5c684-133">To set a description map for list view or tree views.</span></span>   |
    | <span data-ttu-id="5c684-134">\_VALUEMAP MSAAPROPID</span><span class="sxs-lookup"><span data-stu-id="5c684-134">MSAAPROPID\_VALUEMAP</span></span>        | <span data-ttu-id="5c684-135">Para definir um mapa de valor em controles deslizantes.</span><span class="sxs-lookup"><span data-stu-id="5c684-135">To set a value map on slider controls.</span></span>                  |

    

     

4.  <span data-ttu-id="5c684-136">**Limpar.**</span><span class="sxs-lookup"><span data-stu-id="5c684-136">**Clean up.**</span></span>

    <span data-ttu-id="5c684-137">Antes de destruir qualquer controle de mapa de valor anotado (por exemplo, ao manipular o [WM \_ Destroy](../winmsg/wm-destroy.md)), você deve limpar as propriedades previamente registradas e liberar o Gerenciador de anotações.</span><span class="sxs-lookup"><span data-stu-id="5c684-137">Before you destroy any value map annotated controls (for example, when handling [WM\_DESTROY](../winmsg/wm-destroy.md)), you must clear previously registered properties and release the annotation manager.</span></span>

    <span data-ttu-id="5c684-138">Para fazer isso, chame [**IAccPropServices:: ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) conforme apropriado e solte o ponteiro para [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices).</span><span class="sxs-lookup"><span data-stu-id="5c684-138">To do this, call [**IAccPropServices::ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) as appropriate and release your pointer to [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices).</span></span>

<span data-ttu-id="5c684-139">Para o código de exemplo, consulte [exemplo de anotação de mapa de valor](value-map-annotation-sample.md).</span><span class="sxs-lookup"><span data-stu-id="5c684-139">For sample code, see [Value Map Annotation Sample](value-map-annotation-sample.md).</span></span>

 

 