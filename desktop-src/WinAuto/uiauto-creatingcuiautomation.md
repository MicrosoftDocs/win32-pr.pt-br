---
title: Criando o objeto CUIAutomation
description: Esta seção descreve como começar a escrever um aplicativo cliente de automação da interface do usuário da Microsoft instanciando um objeto que implementa o IUIAutomation.
ms.assetid: 9b90da60-0204-48c1-bb16-ff4a843bac67
keywords:
- clientes, criando objeto CUIAutomation
- clientes, objeto CUIAutomation
- Automação da interface do usuário, objeto CUIAutomation
- Automação da interface do usuário, criando objeto CUIAutomation
- Criando objeto CUIAutomation
- Objeto CUIAutomation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8162dac5276bbb22d00413276482cca34334fda5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917362"
---
# <a name="creating-the-cuiautomation-object"></a><span data-ttu-id="48c11-109">Criando o objeto CUIAutomation</span><span class="sxs-lookup"><span data-stu-id="48c11-109">Creating the CUIAutomation Object</span></span>

<span data-ttu-id="48c11-110">Esta seção descreve como começar a escrever um aplicativo cliente de automação da interface do usuário da Microsoft instanciando um objeto que implementa o [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span><span class="sxs-lookup"><span data-stu-id="48c11-110">This section describes how to get started writing a Microsoft UI Automation client application by instantiating an object that implements [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span></span>

<span data-ttu-id="48c11-111">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="48c11-111">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="48c11-112">O objeto CUIAutomation</span><span class="sxs-lookup"><span data-stu-id="48c11-112">The CUIAutomation Object</span></span>](#the-cuiautomation-object)
-   [<span data-ttu-id="48c11-113">Criando o objeto</span><span class="sxs-lookup"><span data-stu-id="48c11-113">Creating the Object</span></span>](#creating-the-object)
-   [<span data-ttu-id="48c11-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="48c11-114">Related topics</span></span>](#related-topics)

## <a name="the-cuiautomation-object"></a><span data-ttu-id="48c11-115">O objeto CUIAutomation</span><span class="sxs-lookup"><span data-stu-id="48c11-115">The CUIAutomation Object</span></span>

<span data-ttu-id="48c11-116">A primeira etapa no uso da automação da interface do usuário é criar um objeto da classe [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="48c11-116">The first step in using UI Automation is to create an object of the [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) class.</span></span> <span data-ttu-id="48c11-117">Esse objeto expõe a interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) , que é o gateway para todos os outros objetos e interfaces que são usados por aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="48c11-117">This object exposes the [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface, which is the gateway to all the other objects and interfaces that are used by client applications.</span></span> <span data-ttu-id="48c11-118">Entre outras coisas, o **IUIAutomation** é usado para as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="48c11-118">Among other things, **IUIAutomation** is used for the following tasks:</span></span>

-   <span data-ttu-id="48c11-119">Inscrevendo-se em eventos.</span><span class="sxs-lookup"><span data-stu-id="48c11-119">Subscribing to events.</span></span>
-   <span data-ttu-id="48c11-120">Criando condições.</span><span class="sxs-lookup"><span data-stu-id="48c11-120">Creating conditions.</span></span> <span data-ttu-id="48c11-121">Condições são objetos usados para restringir o escopo de pesquisas para elementos de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="48c11-121">Conditions are objects used to narrow the scope of searches for UI Automation elements.</span></span>
-   <span data-ttu-id="48c11-122">Obter elementos de automação da interface do usuário diretamente da área de trabalho (o elemento raiz) ou de coordenadas de tela ou identificadores de janela.</span><span class="sxs-lookup"><span data-stu-id="48c11-122">Obtaining UI Automation elements directly from the desktop (the root element), or from screen coordinates or window handles.</span></span>
-   <span data-ttu-id="48c11-123">Criação de objetos Tree Walker que podem ser usados para navegar pela hierarquia de elementos de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="48c11-123">Creating tree walker objects that can be used to navigate the hierarchy of UI Automation elements.</span></span>
-   <span data-ttu-id="48c11-124">Convertendo tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="48c11-124">Converting data types.</span></span>

## <a name="creating-the-object"></a><span data-ttu-id="48c11-125">Criando o objeto</span><span class="sxs-lookup"><span data-stu-id="48c11-125">Creating the Object</span></span>

<span data-ttu-id="48c11-126">Para começar a usar a automação de interface do usuário em seu aplicativo, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="48c11-126">To get started using UI Automation in your application, take the following steps:</span></span>

-   <span data-ttu-id="48c11-127">Inclua automação da IU. h em seus cabeçalhos de projeto.</span><span class="sxs-lookup"><span data-stu-id="48c11-127">Include UIAutomation.h in your project headers.</span></span> <span data-ttu-id="48c11-128">Automação da IU. h traz os outros cabeçalhos que definem a API.</span><span class="sxs-lookup"><span data-stu-id="48c11-128">UIAutomation.h brings in the other headers that define the API.</span></span>
-   <span data-ttu-id="48c11-129">Declare um ponteiro para [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span><span class="sxs-lookup"><span data-stu-id="48c11-129">Declare a pointer to [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span></span>
-   <span data-ttu-id="48c11-130">Inicialize a Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="48c11-130">Initialize the Component Object Model (COM).</span></span>
-   <span data-ttu-id="48c11-131">Crie uma instância de [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) e recupere a interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) em seu ponteiro.</span><span class="sxs-lookup"><span data-stu-id="48c11-131">Create an instance of [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) and retrieve the [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface in your pointer.</span></span>

<span data-ttu-id="48c11-132">A função de exemplo a seguir inicializa COM e, em seguida, cria o objeto [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) , recuperando a interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) no ponteiro *ppAutomation* .</span><span class="sxs-lookup"><span data-stu-id="48c11-132">The following example function initializes COM, and then creates the [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) object, retrieving the [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface in the *ppAutomation* pointer.</span></span>


```C++
#include <uiautomation.h>

// CoInitialize must be called before calling this function, and the  
// caller must release the returned pointer when finished with it.
// 
HRESULT InitializeUIAutomation(IUIAutomation **ppAutomation)
{
    return CoCreateInstance(CLSID_CUIAutomation, NULL,
        CLSCTX_INPROC_SERVER, IID_IUIAutomation, 
        reinterpret_cast<void**>(ppAutomation));
}
```



## <a name="related-topics"></a><span data-ttu-id="48c11-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="48c11-133">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="48c11-134">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="48c11-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="48c11-135">Visão geral sobre eventos de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="48c11-135">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

[<span data-ttu-id="48c11-136">Obtendo elementos da automação interface do usuário</span><span class="sxs-lookup"><span data-stu-id="48c11-136">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
</dt> </dl>

 

 