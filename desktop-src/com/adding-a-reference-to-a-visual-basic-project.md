---
title: Adicionando uma referência a um projeto Visual Basic
description: Adicionando uma referência a um projeto Visual Basic
ms.assetid: 635b1fe9-e592-42d7-a0ee-34fea205f412
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b29b99610464287f34e9c78e44319c16b4d47c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292035"
---
# <a name="adding-a-reference-to-a-visual-basic-project"></a><span data-ttu-id="81ec0-103">Adicionando uma referência a um projeto Visual Basic</span><span class="sxs-lookup"><span data-stu-id="81ec0-103">Adding a Reference to a Visual Basic Project</span></span>

<span data-ttu-id="81ec0-104">O procedimento a seguir descreve como adicionar uma referência a um objeto COM para um projeto Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="81ec0-104">The following procedure describes how to add a reference to a COM object to a Visual Basic project.</span></span> <span data-ttu-id="81ec0-105">Em seguida, seu aplicativo pode usar as classes desse objeto.</span><span class="sxs-lookup"><span data-stu-id="81ec0-105">Your application can then use the classes of that object.</span></span>

<span data-ttu-id="81ec0-106">Quando você adiciona um objeto como uma referência, só pode usar a biblioteca de tipos fornecida pelo controle ou a biblioteca de tipos "RAW".</span><span class="sxs-lookup"><span data-stu-id="81ec0-106">When you add an object as a reference, you can only use the type library provided by the control, or the "raw" type library.</span></span> <span data-ttu-id="81ec0-107">Por outro lado, a adição de um controle como um componente também expõe as propriedades e os métodos do extensor Visual Basic como se eles fossem parte do controle.</span><span class="sxs-lookup"><span data-stu-id="81ec0-107">In contrast, adding a control as a component also exposes the Visual Basic extender properties and methods as if they were part of the control.</span></span>

<span data-ttu-id="81ec0-108">**Para fazer uma referência de Visual Basic a um componente**</span><span class="sxs-lookup"><span data-stu-id="81ec0-108">**To make a Visual Basic reference to a component**</span></span>

1.  <span data-ttu-id="81ec0-109">No menu **Projeto**, clique em **Referências**.</span><span class="sxs-lookup"><span data-stu-id="81ec0-109">On the **Project** menu, click **References**.</span></span>
2.  <span data-ttu-id="81ec0-110">Clique para marcar a caixa de seleção ao lado do componente que você deseja adicionar.</span><span class="sxs-lookup"><span data-stu-id="81ec0-110">Click to select the check box next to the component you want to add.</span></span> <span data-ttu-id="81ec0-111">Se o componente não estiver listado, localize o arquivo. dll ou. ocx usando **procurar**.</span><span class="sxs-lookup"><span data-stu-id="81ec0-111">If the component is not listed, locate the .dll or .ocx file using **Browse**.</span></span>
3.  <span data-ttu-id="81ec0-112">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="81ec0-112">Click **OK**.</span></span>

<span data-ttu-id="81ec0-113">O componente agora faz parte do projeto.</span><span class="sxs-lookup"><span data-stu-id="81ec0-113">The component is now part of the project.</span></span> <span data-ttu-id="81ec0-114">Seu aplicativo pode criar instâncias de classe usando a **nova** palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="81ec0-114">Your application can create class instances using the **New** keyword.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81ec0-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="81ec0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81ec0-116">Adicionando um componente a um projeto Visual Basic</span><span class="sxs-lookup"><span data-stu-id="81ec0-116">Adding a Component to a Visual Basic Project</span></span>](adding-a-component-to-a-visual-basic-project.md)
</dt> <dt>

[<span data-ttu-id="81ec0-117">Convertendo para Visual Basic</span><span class="sxs-lookup"><span data-stu-id="81ec0-117">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
</dt> </dl>

 

 




