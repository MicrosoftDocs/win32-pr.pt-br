---
title: Métodos IPaper
description: Fornece objetos de copapel que são controlados principalmente por sua interface IPaper nativa.
ms.assetid: 3b77a6b3-8ec3-4a91-82cd-1f08d10fbf73
keywords:
- IPaper
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84153c9fcec021d9084807d73d46198e3a56482
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160355"
---
# <a name="ipaper-methods"></a><span data-ttu-id="2c41a-104">Métodos IPaper</span><span class="sxs-lookup"><span data-stu-id="2c41a-104">IPaper Methods</span></span>

<span data-ttu-id="2c41a-105">O **StoServe** fornece objetos de copapel que são controlados principalmente por sua interface **IPaper** nativa.</span><span class="sxs-lookup"><span data-stu-id="2c41a-105">**StoServe** provides COPaper objects that are controlled primarily by their native **IPaper** interface.</span></span>

<span data-ttu-id="2c41a-106">A tabela a seguir lista os métodos **IPaper** de IPaper. H no diretório irmão \\ Inc.</span><span class="sxs-lookup"><span data-stu-id="2c41a-106">The following table lists **IPaper** methods from IPAPER.H in the sibling \\INC directory.</span></span>



| <span data-ttu-id="2c41a-107">Método</span><span class="sxs-lookup"><span data-stu-id="2c41a-107">Method</span></span>    | <span data-ttu-id="2c41a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2c41a-108">Description</span></span>                                                         |
|-----------|---------------------------------------------------------------------|
| <span data-ttu-id="2c41a-109">InitPaper</span><span class="sxs-lookup"><span data-stu-id="2c41a-109">InitPaper</span></span> | <span data-ttu-id="2c41a-110">Inicializa o objeto de papel e cria uma matriz de dados de tinta.</span><span class="sxs-lookup"><span data-stu-id="2c41a-110">Initializes paper object and create ink data array.</span></span>                 |
| <span data-ttu-id="2c41a-111">Bloqueio</span><span class="sxs-lookup"><span data-stu-id="2c41a-111">Lock</span></span>      | <span data-ttu-id="2c41a-112">Fornece controle de cliente do papel e bloqueia outros clientes.</span><span class="sxs-lookup"><span data-stu-id="2c41a-112">Gives client control of the paper and locks out other clients.</span></span>      |
| <span data-ttu-id="2c41a-113">Unlock</span><span class="sxs-lookup"><span data-stu-id="2c41a-113">Unlock</span></span>    | <span data-ttu-id="2c41a-114">Abandona o controle de cliente do documento.</span><span class="sxs-lookup"><span data-stu-id="2c41a-114">Relinquishes client control of the paper.</span></span>                           |
| <span data-ttu-id="2c41a-115">Carregar</span><span class="sxs-lookup"><span data-stu-id="2c41a-115">Load</span></span>      | <span data-ttu-id="2c41a-116">Carrega o conteúdo em papel do arquivo composto do cliente e notifica os coletores.</span><span class="sxs-lookup"><span data-stu-id="2c41a-116">Loads paper content from client's compound file and notifies sinks.</span></span> |
| <span data-ttu-id="2c41a-117">Salvar</span><span class="sxs-lookup"><span data-stu-id="2c41a-117">Save</span></span>      | <span data-ttu-id="2c41a-118">Salva o conteúdo do papel no arquivo composto do cliente.</span><span class="sxs-lookup"><span data-stu-id="2c41a-118">Saves paper content to client's compound file.</span></span>                      |
| <span data-ttu-id="2c41a-119">InkStart</span><span class="sxs-lookup"><span data-stu-id="2c41a-119">InkStart</span></span>  | <span data-ttu-id="2c41a-120">Inicia o desenho de tinta colorida na superfície do papel.</span><span class="sxs-lookup"><span data-stu-id="2c41a-120">Starts color ink drawing to the paper surface.</span></span>                      |
| <span data-ttu-id="2c41a-121">InkDraw</span><span class="sxs-lookup"><span data-stu-id="2c41a-121">InkDraw</span></span>   | <span data-ttu-id="2c41a-122">Coloca pontos de dados de tinta na superfície de papel eletrônico.</span><span class="sxs-lookup"><span data-stu-id="2c41a-122">Puts ink data points on the electronic paper surface.</span></span>               |
| <span data-ttu-id="2c41a-123">InkStop</span><span class="sxs-lookup"><span data-stu-id="2c41a-123">InkStop</span></span>   | <span data-ttu-id="2c41a-124">Interrompe o desenho de tinta na superfície do papel.</span><span class="sxs-lookup"><span data-stu-id="2c41a-124">Stops ink drawing to the paper surface.</span></span>                             |
| <span data-ttu-id="2c41a-125">Apagar</span><span class="sxs-lookup"><span data-stu-id="2c41a-125">Erase</span></span>     | <span data-ttu-id="2c41a-126">Apague o conteúdo do papel atual e notifique os coletores.</span><span class="sxs-lookup"><span data-stu-id="2c41a-126">Erase the current paper content and notifies sinks.</span></span>                 |
| <span data-ttu-id="2c41a-127">Redimensionar</span><span class="sxs-lookup"><span data-stu-id="2c41a-127">Resize</span></span>    | <span data-ttu-id="2c41a-128">Redimensiona o tamanho do retângulo do papel de desenho e notifica os coletores.</span><span class="sxs-lookup"><span data-stu-id="2c41a-128">Resizes the drawing paper rectangle size and notifies sinks.</span></span>        |
| <span data-ttu-id="2c41a-129">Emiti</span><span class="sxs-lookup"><span data-stu-id="2c41a-129">Redraw</span></span>    | <span data-ttu-id="2c41a-130">Redesenha o conteúdo do objeto de papel e notifica os coletores.</span><span class="sxs-lookup"><span data-stu-id="2c41a-130">Redraws contents of paper object and notifies sinks.</span></span>                |



 

<span data-ttu-id="2c41a-131">Os métodos de interesse deste exemplo de código em arquivos compostos são [**carregar**](ipaper--load.md), [**salvar**](ipaper--save.md)e [**redesenhar**](ipaper--redraw.md).</span><span class="sxs-lookup"><span data-stu-id="2c41a-131">Methods of interest for this code sample on compound files are [**Load**](ipaper--load.md), [**Save**](ipaper--save.md), and [**Redraw**](ipaper--redraw.md).</span></span>

<span data-ttu-id="2c41a-132">[**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md)e [**InkStop**](cguipaper-methods.md) são métodos usados por clientes para o copapel de comando para gravar sequências de desenho de tinta.</span><span class="sxs-lookup"><span data-stu-id="2c41a-132">[**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) are methods used by clients to command COPaper to record ink drawing sequences.</span></span> <span data-ttu-id="2c41a-133">Normalmente, o cliente responderá a uma \_ mensagem do WM LBUTTONDOWN como o início de uma sequência de desenho de tinta chamando **InkStart** no copaper.</span><span class="sxs-lookup"><span data-stu-id="2c41a-133">The client will typically respond to a WM\_LBUTTONDOWN message as the start of an ink drawing sequence by calling **InkStart** on COPaper.</span></span> <span data-ttu-id="2c41a-134">À medida que o usuário move o mouse ou a caneta para desenhar enquanto mantém pressionado o botão esquerdo, o cliente responderá às mensagens do WM MOUSEMOVE repetidas \_ com chamadas correspondentes a **InkDraw**.</span><span class="sxs-lookup"><span data-stu-id="2c41a-134">As the user moves the mouse or pen to draw while holding down the left button, the client will respond to repeated WM\_MOUSEMOVE messages with corresponding calls to **InkDraw**.</span></span> <span data-ttu-id="2c41a-135">Quando o usuário libera o botão esquerdo do mouse, o cliente responderá a uma \_ mensagem do WM LBUTTONUP com uma chamada para **InkStop**, que marca o final da sequência de desenho de tinta.</span><span class="sxs-lookup"><span data-stu-id="2c41a-135">When the user releases the left mouse button, the client will respond to a WM\_LBUTTONUP message with a call to **InkStop**, which marks the end of the ink drawing sequence.</span></span>

<span data-ttu-id="2c41a-136">[**InkStart**](inkstart-method.md) informa ao copaper a posição inicial da sequência de desenho nas coordenadas da janela do cliente.</span><span class="sxs-lookup"><span data-stu-id="2c41a-136">[**InkStart**](inkstart-method.md) tells COPaper the start position for the drawing sequence in client window coordinates.</span></span> <span data-ttu-id="2c41a-137">Ele também passa a cor e a largura da tinta selecionada no momento.</span><span class="sxs-lookup"><span data-stu-id="2c41a-137">It also passes the currently selected ink color and width.</span></span> <span data-ttu-id="2c41a-138">O cliente mantém essas seleções; O copaper apenas os registra quando a chamada **InkStart** é feita.</span><span class="sxs-lookup"><span data-stu-id="2c41a-138">The client maintains these selections; COPaper merely records them when the **InkStart** call is made.</span></span> <span data-ttu-id="2c41a-139">[**InkDraw**](inkdraw-method.md) é chamado repetidamente para informar o sucesso das coordenadas da janela que representam o movimento de desenho do mouse ou da caneta.</span><span class="sxs-lookup"><span data-stu-id="2c41a-139">[**InkDraw**](inkdraw-method.md) is called repeatedly to tell COPaper the succession of window coordinates that represent the drawing motion of the mouse or pen.</span></span> <span data-ttu-id="2c41a-140">[**InkStop**](cguipaper-methods.md) instrui o copapel para marcar o final de uma sequência de desenho.</span><span class="sxs-lookup"><span data-stu-id="2c41a-140">[**InkStop**](cguipaper-methods.md) instructs COPaper to mark the end of a drawing sequence.</span></span>

 

 




