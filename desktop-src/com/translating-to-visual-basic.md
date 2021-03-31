---
title: Convertendo para Visual Basic
description: Convertendo para Visual Basic
ms.assetid: 48672d0c-b0d7-4820-91d4-d985030396f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c45e7beedaaa3983b1be1503b5ce443a3adf4d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822760"
---
# <a name="translating-to-visual-basic"></a><span data-ttu-id="3a625-103">Convertendo para Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3a625-103">Translating to Visual Basic</span></span>

<span data-ttu-id="3a625-104">Você pode adicionar um objeto COM ao seu Visual Basic projeto como uma referência ou um componente.</span><span class="sxs-lookup"><span data-stu-id="3a625-104">You can add a COM object to your Visual Basic project either as a reference or a component.</span></span> <span data-ttu-id="3a625-105">Depois que o objeto for adicionado ao seu projeto, seu aplicativo poderá acessar suas classes e interfaces.</span><span class="sxs-lookup"><span data-stu-id="3a625-105">Once the object is added to your project, your application can access its classes and interfaces.</span></span> <span data-ttu-id="3a625-106">Em seguida, você pode usar o pesquisador de objetos de Visual Basic para exibir as informações da biblioteca de tipos do objeto na sintaxe Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3a625-106">You can then use the Visual Basic Object Browser to view the object's type library information in Visual Basic syntax.</span></span>

<span data-ttu-id="3a625-107">Normalmente, os controles são adicionados a um projeto, pois os componentes e os não controlados são adicionados como referências.</span><span class="sxs-lookup"><span data-stu-id="3a625-107">Typically, controls are added to a project as a components and noncontrols are added as references.</span></span> <span data-ttu-id="3a625-108">Quando um objeto COM é adicionado como um componente, ele aparece na caixa de ferramentas Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3a625-108">When a COM object is added as a component, it appears in the Visual Basic toolbox.</span></span> <span data-ttu-id="3a625-109">Novas instâncias desse objeto são criadas arrastando o ícone de objeto da caixa de ferramentas para um formulário Visual Basic ou outro tipo de contêiner.</span><span class="sxs-lookup"><span data-stu-id="3a625-109">New instances of that object are created by dragging the object icon from the toolbox onto a Visual Basic form or other type of container.</span></span> <span data-ttu-id="3a625-110">Novas instâncias de objetos COM adicionados como referências são criadas usando a **nova** palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="3a625-110">New instances of COM objects added as references are created using the **new** keyword.</span></span>

<span data-ttu-id="3a625-111">A distinção entre usar uma classe como referência versus um componente é sutil, mas importante.</span><span class="sxs-lookup"><span data-stu-id="3a625-111">The distinction between using a class as a reference versus a component is subtle but important.</span></span> <span data-ttu-id="3a625-112">Quando você adiciona um objeto como uma referência, você pode usar apenas a biblioteca de tipos que o controle fornece ou a biblioteca de tipos "RAW".</span><span class="sxs-lookup"><span data-stu-id="3a625-112">When you add an object as a reference, you can use only the type library that the control provides, or the "raw" type library.</span></span>

<span data-ttu-id="3a625-113">Se você adicionar um controle como um componente, o Visual Basic mesclará as propriedades e os métodos do extensor do formulário no qual o controle é inserido com a biblioteca de tipos do controle, fornecendo assim uma versão estendida e encapsulada da biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="3a625-113">If you add a control as a component, Visual Basic merges the extender properties and methods of the form in which the control is embedded with the control's type library, thus providing a wrapped, extended version of the type library.</span></span> <span data-ttu-id="3a625-114">Com essa versão da biblioteca de tipos, você pode usar propriedades do extensor, como Top e Left, como se fossem parte do controle, em vez do contêiner do controle.</span><span class="sxs-lookup"><span data-stu-id="3a625-114">With this version of the type library, you can use extender properties such as Top and Left as if they were part of the control, instead of the control's container.</span></span>

<span data-ttu-id="3a625-115">Atualmente, o Visual Basic não dá suporte a várias bibliotecas de tipos criadas em um único arquivo. dll.</span><span class="sxs-lookup"><span data-stu-id="3a625-115">Visual Basic does not currently support multiple type libraries built into a single .dll file.</span></span> <span data-ttu-id="3a625-116">Se você encontrar uma DLL que incorpora várias bibliotecas de tipos, deverá obter cópias autônomas das bibliotecas de tipos da fonte que forneceu o objeto para usar o objeto com Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3a625-116">If you run into a DLL that incorporates multiple type libraries, you should get stand-alone copies of the type libraries from the source that supplied the object in order to use the object with Visual Basic.</span></span>

<span data-ttu-id="3a625-117">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="3a625-117">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="3a625-118">Convertendo para Visual Basic do C++</span><span class="sxs-lookup"><span data-stu-id="3a625-118">Translating to Visual Basic from C++</span></span>](translating-to-visual-basic-from-c--.md)
-   [<span data-ttu-id="3a625-119">Convertendo para Visual Basic do Java</span><span class="sxs-lookup"><span data-stu-id="3a625-119">Translating to Visual Basic from Java</span></span>](translating-to-visual-basic-from-java.md)
-   [<span data-ttu-id="3a625-120">Adicionando um componente a um projeto Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3a625-120">Adding a Component to a Visual Basic Project</span></span>](adding-a-component-to-a-visual-basic-project.md)
-   [<span data-ttu-id="3a625-121">Adicionando uma referência a um projeto Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3a625-121">Adding a Reference to a Visual Basic Project</span></span>](adding-a-reference-to-a-visual-basic-project.md)
-   [<span data-ttu-id="3a625-122">Pesquisador de objetos do Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3a625-122">Visual Basic Object Browser</span></span>](visual-basic-object-browser.md)

## <a name="related-topics"></a><span data-ttu-id="3a625-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3a625-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a625-124">Convertendo para C++</span><span class="sxs-lookup"><span data-stu-id="3a625-124">Translating to C++</span></span>](translating-to-c--.md)
</dt> <dt>

[<span data-ttu-id="3a625-125">Convertendo para Java</span><span class="sxs-lookup"><span data-stu-id="3a625-125">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




