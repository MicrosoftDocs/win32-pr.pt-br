---
description: Esta seção discute os procedimentos de janela. Cada janela tem um procedimento de janela associado que processa todas as mensagens enviadas ou postadas em todas as janelas da classe.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowprocedures.htm
title: Procedimentos de janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ae68ba9b64557a6dc70d5c83788b8337648a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784634"
---
# <a name="window-procedures"></a><span data-ttu-id="83808-104">Procedimentos de janela</span><span class="sxs-lookup"><span data-stu-id="83808-104">Window Procedures</span></span>

<span data-ttu-id="83808-105">Cada janela tem um procedimento de janela associado — uma função que processa todas as mensagens enviadas ou postadas em todas as janelas da classe.</span><span class="sxs-lookup"><span data-stu-id="83808-105">Every window has an associated window procedure — a function that processes all messages sent or posted to all windows of the class.</span></span> <span data-ttu-id="83808-106">Todos os aspectos da aparência e do comportamento de uma janela dependem da resposta do procedimento da janela para essas mensagens.</span><span class="sxs-lookup"><span data-stu-id="83808-106">All aspects of a window's appearance and behavior depend on the window procedure's response to these messages.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="83808-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="83808-107">In This Section</span></span>



| <span data-ttu-id="83808-108">Nome</span><span class="sxs-lookup"><span data-stu-id="83808-108">Name</span></span>                                                         | <span data-ttu-id="83808-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="83808-109">Description</span></span>                                                                                                                                                                                                    |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83808-110">Sobre os procedimentos de janela</span><span class="sxs-lookup"><span data-stu-id="83808-110">About Window Procedures</span></span>](about-window-procedures.md)       | <span data-ttu-id="83808-111">Discute os procedimentos de janela.</span><span class="sxs-lookup"><span data-stu-id="83808-111">Discusses window procedures.</span></span> <span data-ttu-id="83808-112">Cada janela é um membro de uma determinada classe de janela.</span><span class="sxs-lookup"><span data-stu-id="83808-112">Each window is a member of a particular window class.</span></span> <span data-ttu-id="83808-113">A classe Window determina o procedimento de janela padrão que uma janela individual usa para processar suas mensagens.</span><span class="sxs-lookup"><span data-stu-id="83808-113">The window class determines the default window procedure that an individual window uses to process its messages.</span></span><br/> |
| [<span data-ttu-id="83808-114">Usando os procedimentos de janela</span><span class="sxs-lookup"><span data-stu-id="83808-114">Using Window Procedures</span></span>](using-window-procedures.md)       | <span data-ttu-id="83808-115">Aborda como executar as seguintes tarefas associadas a procedimentos de janela.</span><span class="sxs-lookup"><span data-stu-id="83808-115">Covers how to perform the following tasks associated with window procedures.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="83808-116">Referência de procedimento de janela</span><span class="sxs-lookup"><span data-stu-id="83808-116">Window Procedure Reference</span></span>](window-procedure-reference.md) | <span data-ttu-id="83808-117">Contém a referência de API.</span><span class="sxs-lookup"><span data-stu-id="83808-117">Contains the API reference.</span></span><br/>                                                                                                                                                                         |



 

### <a name="functions"></a><span data-ttu-id="83808-118">Funções</span><span class="sxs-lookup"><span data-stu-id="83808-118">Functions</span></span>



| <span data-ttu-id="83808-119">Nome</span><span class="sxs-lookup"><span data-stu-id="83808-119">Name</span></span>                                     | <span data-ttu-id="83808-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="83808-120">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83808-121">**CallWindowProc**</span><span class="sxs-lookup"><span data-stu-id="83808-121">**CallWindowProc**</span></span>](/windows/win32/api/winuser/nf-winuser-callwindowproca) | <span data-ttu-id="83808-122">Passa informações da mensagem para o procedimento de janela especificado.</span><span class="sxs-lookup"><span data-stu-id="83808-122">Passes message information to the specified window procedure.</span></span> <br/>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="83808-123">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="83808-123">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)   | <span data-ttu-id="83808-124">Chama o procedimento de janela padrão para fornecer o processamento padrão para qualquer mensagem de janela que um aplicativo não processar.</span><span class="sxs-lookup"><span data-stu-id="83808-124">Calls the default window procedure to provide default processing for any window messages that an application does not process.</span></span> <span data-ttu-id="83808-125">Essa função garante que cada mensagem seja processada.</span><span class="sxs-lookup"><span data-stu-id="83808-125">This function ensures that every message is processed.</span></span> <span data-ttu-id="83808-126">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) é chamado com os mesmos parâmetros recebidos pelo procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="83808-126">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) is called with the same parameters received by the window procedure.</span></span> <br/> |
| <span data-ttu-id="83808-127">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="83808-127">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span></span>           | <span data-ttu-id="83808-128">Uma função definida pelo aplicativo que processa as mensagens enviadas a uma janela.</span><span class="sxs-lookup"><span data-stu-id="83808-128">An application-defined function that processes messages sent to a window.</span></span> <span data-ttu-id="83808-129">O tipo **WndProc** define um ponteiro para essa função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="83808-129">The **WNDPROC** type defines a pointer to this callback function.</span></span> <span data-ttu-id="83808-130">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) é um espaço reservado para o nome da função definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="83808-130">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) is a placeholder for the application-defined function name.</span></span> <br/>                                                            |



 

 

 
