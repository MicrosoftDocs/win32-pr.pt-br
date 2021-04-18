---
title: Arrastar e soltar
description: Arrastar e soltar refere-se a transferências de dados nas quais um mouse ou outro dispositivo apontador é usado para especificar a fonte de dados e seu destino.
ms.assetid: bba0ddf8-fcf9-4827-bf85-7ac597d33b4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc4b425637432024d097acb8afdc5e169467c6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105763336"
---
# <a name="drag-and-drop"></a><span data-ttu-id="ec0d6-103">Arrastar e soltar</span><span class="sxs-lookup"><span data-stu-id="ec0d6-103">Drag and Drop</span></span>

<span data-ttu-id="ec0d6-104">*Arrastar e soltar* refere-se a transferências de dados nas quais um mouse ou outro dispositivo apontador é usado para especificar a fonte de dados e seu destino.</span><span class="sxs-lookup"><span data-stu-id="ec0d6-104">*Drag and drop* refers to data transfers in which a mouse or other pointing device is used to specify both the data source and its destination.</span></span> <span data-ttu-id="ec0d6-105">Em uma operação típica de arrastar e soltar, um usuário seleciona o objeto a ser transferido movendo o ponteiro do mouse para ele e mantendo o botão esquerdo ou algum outro botão designado para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="ec0d6-105">In a typical drag and drop operation, a user selects the object to be transferred by moving the mouse pointer to it and holding down either the left button or some other button designated for this purpose.</span></span> <span data-ttu-id="ec0d6-106">Enquanto continua mantendo o botão, o usuário inicia a transferência arrastando o objeto para seu destino, que pode ser qualquer contêiner OLE.</span><span class="sxs-lookup"><span data-stu-id="ec0d6-106">While continuing to hold down the button, the user initiates the transfer by dragging the object to its destination, which can be any OLE container.</span></span> <span data-ttu-id="ec0d6-107">O recurso arrastar e soltar fornece exatamente a mesma funcionalidade da cópia e colagem da área de transferência OLE, mas adiciona comentários visuais e elimina a necessidade de menus.</span><span class="sxs-lookup"><span data-stu-id="ec0d6-107">Drag and drop provides exactly the same functionality as the OLE clipboard copy and paste but adds visual feedback and eliminates the need for menus.</span></span> <span data-ttu-id="ec0d6-108">Na verdade, se um aplicativo der suporte para copiar e colar da área de transferência, será necessário um pouco mais de suporte para arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="ec0d6-108">In fact, if an application supports clipboard copy and paste, little extra is needed to support drag and drop.</span></span>

<span data-ttu-id="ec0d6-109">Durante uma operação de arrastar e soltar OLE, são usadas as três partes separadas de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="ec0d6-109">During an OLE drag and drop operation, the following three separate pieces of code are used.</span></span>



| <span data-ttu-id="ec0d6-110">Fonte de código do tipo "arrastar e soltar"</span><span class="sxs-lookup"><span data-stu-id="ec0d6-110">Drag-and-drop code source</span></span>                               | <span data-ttu-id="ec0d6-111">Implementação e uso</span><span class="sxs-lookup"><span data-stu-id="ec0d6-111">Implementation and use</span></span>                                                                                                                                                                      |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec0d6-112">Interface [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)</span><span class="sxs-lookup"><span data-stu-id="ec0d6-112">[**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) interface</span></span><br/> | <span data-ttu-id="ec0d6-113">Implementado pelo objeto que contém os dados arrastados, chamados de *fonte de arrastar*.</span><span class="sxs-lookup"><span data-stu-id="ec0d6-113">Implemented by the object containing the dragged data, referred to as the *drag source*.</span></span><br/>                                                                                         |
| <span data-ttu-id="ec0d6-114">Interface [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)</span><span class="sxs-lookup"><span data-stu-id="ec0d6-114">[**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) interface</span></span><br/> | <span data-ttu-id="ec0d6-115">Implementado pelo objeto que se destina a aceitar o drop, chamado de *destino de soltura*.</span><span class="sxs-lookup"><span data-stu-id="ec0d6-115">Implemented by the object that is intended to accept the drop, referred to as the *drop target*.</span></span><br/>                                                                                 |
| <span data-ttu-id="ec0d6-116">Função [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)</span><span class="sxs-lookup"><span data-stu-id="ec0d6-116">[**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) function</span></span><br/>    | <span data-ttu-id="ec0d6-117">Implementado pelo OLE e usado para iniciar uma operação de arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="ec0d6-117">Implemented by OLE and used to initiate a drag and drop operation.</span></span> <span data-ttu-id="ec0d6-118">Depois que a operação estiver em andamento, ela facilitará a comunicação entre a origem de arrastar e o destino de soltar.</span><span class="sxs-lookup"><span data-stu-id="ec0d6-118">After the operation is in progress, it facilitates communication between the drag source and the drop target.</span></span><br/> |



 

<span data-ttu-id="ec0d6-119">As interfaces [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) e [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) podem ser implementadas em um contêiner ou em um aplicativo de objeto.</span><span class="sxs-lookup"><span data-stu-id="ec0d6-119">The [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) and [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) interfaces can be implemented in either a container or in an object application.</span></span> <span data-ttu-id="ec0d6-120">A função de arrastar origem ou soltar destino não está limitada a nenhum tipo de aplicativo OLE.</span><span class="sxs-lookup"><span data-stu-id="ec0d6-120">The role of drag source or drop target is not limited to any one type of OLE application.</span></span>

<span data-ttu-id="ec0d6-121">A função OLE [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) implementa um loop que controla o movimento do mouse e do teclado até o momento em que a operação de arrastar é cancelada ou uma queda ocorre.</span><span class="sxs-lookup"><span data-stu-id="ec0d6-121">The OLE function [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) implements a loop that tracks mouse and keyboard movement until such time as the drag is canceled or a drop occurs.</span></span> <span data-ttu-id="ec0d6-122">**DoDragDrop** é a função fundamental no processo de arrastar e soltar, facilitando a comunicação entre a origem de arrastar e o destino de soltar.</span><span class="sxs-lookup"><span data-stu-id="ec0d6-122">**DoDragDrop** is the key function in the drag and drop process, facilitating communication between the drag source and drop target.</span></span>

<span data-ttu-id="ec0d6-123">Durante uma operação de arrastar e soltar, três tipos de comentários podem ser exibidos para o usuário.</span><span class="sxs-lookup"><span data-stu-id="ec0d6-123">During a drag and drop operation, three types of feedback can be displayed to the user.</span></span>



| <span data-ttu-id="ec0d6-124">Tipo de comentário</span><span class="sxs-lookup"><span data-stu-id="ec0d6-124">Type of feedback</span></span>            | <span data-ttu-id="ec0d6-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec0d6-125">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec0d6-126">Comentários de origem</span><span class="sxs-lookup"><span data-stu-id="ec0d6-126">Source feedback</span></span><br/>  | <span data-ttu-id="ec0d6-127">Fornecido pela fonte de arrastar, os comentários de origem indicam que os dados estão sendo arrastados e não são alterados durante a operação de arrastar.</span><span class="sxs-lookup"><span data-stu-id="ec0d6-127">Provided by the drag source, the source feedback indicates the data is being dragged and does not change during the course of the drag.</span></span> <span data-ttu-id="ec0d6-128">Normalmente, os dados são realçados para sinalizar que ele foi selecionado.</span><span class="sxs-lookup"><span data-stu-id="ec0d6-128">Typically, the data is highlighted to signal it has been selected.</span></span><br/>                                                                                                                                            |
| <span data-ttu-id="ec0d6-129">Comentários do ponteiro</span><span class="sxs-lookup"><span data-stu-id="ec0d6-129">Pointer feedback</span></span><br/> | <span data-ttu-id="ec0d6-130">Fornecido pela fonte de arrastar, o feedback do ponteiro indica o que acontece se o mouse for liberado em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="ec0d6-130">Provided by the drag source, the pointer feedback indicates what happens if the mouse is released at any given moment.</span></span> <span data-ttu-id="ec0d6-131">Os comentários do ponteiro são alterados continuamente conforme o usuário move o mouse e/ou pressiona uma tecla modificadora.</span><span class="sxs-lookup"><span data-stu-id="ec0d6-131">Pointer feedback changes continually as the user moves the mouse and/or presses a modifier key.</span></span> <span data-ttu-id="ec0d6-132">Por exemplo, se o ponteiro for movido para uma janela que não aceita um drop, o ponteiro muda para o símbolo "não permitido".</span><span class="sxs-lookup"><span data-stu-id="ec0d6-132">For example, if the pointer is moved into a window that cannot accept a drop, the pointer changes to the "not allowed" symbol.</span></span><br/> |
| <span data-ttu-id="ec0d6-133">Comentários de destino</span><span class="sxs-lookup"><span data-stu-id="ec0d6-133">Target feedback</span></span><br/>  | <span data-ttu-id="ec0d6-134">Fornecido pelo destino de soltar, os comentários de destino indicam onde a queda deve ocorrer.</span><span class="sxs-lookup"><span data-stu-id="ec0d6-134">Provided by the drop target, target feedback indicates where the drop is to occur.</span></span><br/>                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="ec0d6-135">Para obter mais informações, consulte [arrastar responsabilidades de origem](drag-source-responsibilities.md).</span><span class="sxs-lookup"><span data-stu-id="ec0d6-135">For more information, see [Drag Source Responsibilities](drag-source-responsibilities.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec0d6-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ec0d6-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec0d6-137">Transferência de Dados</span><span class="sxs-lookup"><span data-stu-id="ec0d6-137">Data Transfer</span></span>](data-transfer.md)
</dt> </dl>

 

 





