---
title: Adicionando um componente a um projeto Visual Basic
description: Adicionando um componente a um projeto Visual Basic
ms.assetid: 7e78853a-b134-46d7-a230-3ee8d80d05c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd64b8367b33590b972adc2439af3a2479ee920e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292036"
---
# <a name="adding-a-component-to-a-visual-basic-project"></a><span data-ttu-id="19b0c-103">Adicionando um componente a um projeto Visual Basic</span><span class="sxs-lookup"><span data-stu-id="19b0c-103">Adding a Component to a Visual Basic Project</span></span>

<span data-ttu-id="19b0c-104">O procedimento a seguir descreve como adicionar um objeto COM como um componente a um projeto Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="19b0c-104">The following procedure describes how to add a COM object as a component to a Visual Basic project.</span></span> <span data-ttu-id="19b0c-105">Em seguida, seu aplicativo pode usar as classes desse objeto.</span><span class="sxs-lookup"><span data-stu-id="19b0c-105">Your application can then use the classes of that object.</span></span>

<span data-ttu-id="19b0c-106">Adicionar um controle como um componente expõe as propriedades e os métodos do extensor Visual Basic como se eles fossem parte do controle.</span><span class="sxs-lookup"><span data-stu-id="19b0c-106">Adding a control as a component exposes the Visual Basic extender properties and methods as if they were part of the control.</span></span> <span data-ttu-id="19b0c-107">Por outro lado, quando você adiciona um objeto como uma referência, só pode usar a biblioteca de tipos fornecida pelo controle ou a biblioteca de tipos "RAW".</span><span class="sxs-lookup"><span data-stu-id="19b0c-107">In contrast, when you add an object as a reference you can only use the type library provided by the control, or the "raw" type library.</span></span>

<span data-ttu-id="19b0c-108">**Para inserir um controle em um projeto Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="19b0c-108">**To insert a control into a Visual Basic project**</span></span>

1.  <span data-ttu-id="19b0c-109">No menu **projeto** , clique em **componentes**.</span><span class="sxs-lookup"><span data-stu-id="19b0c-109">On the **Project** menu, click **Components**.</span></span>
2.  <span data-ttu-id="19b0c-110">Clique para marcar a caixa de seleção ao lado do componente que você deseja adicionar.</span><span class="sxs-lookup"><span data-stu-id="19b0c-110">Click to select the check box next to the component you want to add.</span></span> <span data-ttu-id="19b0c-111">Se o componente não estiver listado, localize o arquivo. dll ou. ocx usando **procurar**.</span><span class="sxs-lookup"><span data-stu-id="19b0c-111">If the component is not listed, locate the .dll or .ocx file using **Browse**.</span></span>
3.  <span data-ttu-id="19b0c-112">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="19b0c-112">Click **OK**.</span></span>

<span data-ttu-id="19b0c-113">O componente agora faz parte do projeto e aparece na barra de ferramentas do objeto.</span><span class="sxs-lookup"><span data-stu-id="19b0c-113">The component is now part of the project and appears in the object toolbar.</span></span> <span data-ttu-id="19b0c-114">Seu aplicativo pode criar instâncias do controle arrastando o controle da barra de ferramentas e soltando-o em um formulário ou caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="19b0c-114">Your application can create instances of the control by dragging the control from the toolbar and dropping it onto a form or dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19b0c-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="19b0c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19b0c-116">Adicionando uma referência a um projeto Visual Basic</span><span class="sxs-lookup"><span data-stu-id="19b0c-116">Adding a Reference to a Visual Basic Project</span></span>](adding-a-reference-to-a-visual-basic-project.md)
</dt> <dt>

[<span data-ttu-id="19b0c-117">Convertendo para Visual Basic</span><span class="sxs-lookup"><span data-stu-id="19b0c-117">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
</dt> </dl>

 

 




