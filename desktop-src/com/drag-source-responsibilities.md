---
title: Arrastar responsabilidades de origem
description: Arrastar responsabilidades de origem
ms.assetid: bafef0c1-f78e-424a-9ed0-07764a60b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ce91a795815148f442c19530a552cf7c843332
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105781317"
---
# <a name="drag-source-responsibilities"></a><span data-ttu-id="b28ab-103">Arrastar responsabilidades de origem</span><span class="sxs-lookup"><span data-stu-id="b28ab-103">Drag Source Responsibilities</span></span>

<span data-ttu-id="b28ab-104">A fonte de arrastar é responsável pelas seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="b28ab-104">The drag source is responsible for the following tasks:</span></span>

-   <span data-ttu-id="b28ab-105">Fornecer um objeto de transferência de dados para o destino de soltura que expõe as interfaces [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) .</span><span class="sxs-lookup"><span data-stu-id="b28ab-105">Providing a data-transfer object for the drop target that exposes the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) and [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) interfaces.</span></span>
-   <span data-ttu-id="b28ab-106">Gerando comentários de origem e ponteiro.</span><span class="sxs-lookup"><span data-stu-id="b28ab-106">Generating pointer and source feedback.</span></span>
-   <span data-ttu-id="b28ab-107">Determinando quando a operação de arrastar foi cancelada ou uma operação de remoção ocorreu.</span><span class="sxs-lookup"><span data-stu-id="b28ab-107">Determining when the drag operation has been canceled or a drop operation has occurred.</span></span>
-   <span data-ttu-id="b28ab-108">Executar qualquer ação nos dados originais causados pela operação de remoção, como excluir os dados ou criar um link para ele.</span><span class="sxs-lookup"><span data-stu-id="b28ab-108">Performing any action on the original data caused by the drop operation, such as deleting the data or creating a link to it.</span></span>

<span data-ttu-id="b28ab-109">A tarefa principal é criar um objeto de transferência de dados que expõe as interfaces [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) .</span><span class="sxs-lookup"><span data-stu-id="b28ab-109">The main task is creating a data-transfer object that exposes the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) and [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) interfaces.</span></span> <span data-ttu-id="b28ab-110">A origem de arrastar pode ou não incluir uma cópia dos dados selecionados.</span><span class="sxs-lookup"><span data-stu-id="b28ab-110">The drag source might or might not include a copy of the selected data.</span></span> <span data-ttu-id="b28ab-111">Incluí-lo não é obrigatório, mas isso ajuda a proteger contra alterações inadvertidas e permite que o código de operações da área de transferência seja idêntico ao código de arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="b28ab-111">Including it is not mandatory, but doing so helps protect against inadvertent changes and allows the Clipboard operations code to be identical to the drag and drop code.</span></span>

<span data-ttu-id="b28ab-112">Enquanto uma operação de arrastar está em andamento, a fonte de arrastar é responsável por definir o ponteiro do mouse e, se apropriado, para fornecer comentários de origem adicionais ao usuário.</span><span class="sxs-lookup"><span data-stu-id="b28ab-112">While a drag operation is in progress, the drag source is responsible for setting the mouse pointer and, if appropriate, for providing additional source feedback to the user.</span></span> <span data-ttu-id="b28ab-113">A fonte de arrastar não pode fornecer comentários que acompanhem a posição do mouse além de definir realmente o ponteiro real (consulte a função [**SetCursor**](/windows/win32/api/winuser/nf-winuser-setcursor) ).</span><span class="sxs-lookup"><span data-stu-id="b28ab-113">The drag source cannot provide any feedback that tracks the mouse position other than by actually setting the real pointer (see the [**SetCursor**](/windows/win32/api/winuser/nf-winuser-setcursor) function).</span></span> <span data-ttu-id="b28ab-114">Essa regra deve ser imposta para evitar conflitos com os comentários fornecidos pelo destino de soltura.</span><span class="sxs-lookup"><span data-stu-id="b28ab-114">This rule must be enforced to avoid conflicts with the feedback provided by the drop target.</span></span> <span data-ttu-id="b28ab-115">(Uma fonte de arrastar também pode ser um destino de soltura.</span><span class="sxs-lookup"><span data-stu-id="b28ab-115">(A drag source can also be a drop target.</span></span> <span data-ttu-id="b28ab-116">Ao descartar, a origem/destino pode, naturalmente, fornecer comentários de destino para acompanhar a posição do mouse.</span><span class="sxs-lookup"><span data-stu-id="b28ab-116">When dropping on itself, the source/target can, of course, provide target feedback to track the mouse position.</span></span> <span data-ttu-id="b28ab-117">Nesse caso, no entanto, é a interface "soltar" controlando o mouse, não a origem.) Com base nos comentários oferecidos pelo destino de soltura, a fonte define um ponteiro apropriado.</span><span class="sxs-lookup"><span data-stu-id="b28ab-117">In this case, however, it is the drop target tracking the mouse, not the source.) Based on the feedback offered by the drop target, the source sets an appropriate pointer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b28ab-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b28ab-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b28ab-119">Arrastar e soltar</span><span class="sxs-lookup"><span data-stu-id="b28ab-119">Drag and Drop</span></span>](drag-and-drop.md)
</dt> </dl>

 

 