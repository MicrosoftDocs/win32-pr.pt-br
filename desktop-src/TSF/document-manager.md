---
title: Gerenciador de documentos
description: Gerenciador de documentos
ms.assetid: e30087b6-524a-481e-845d-0348bac3830a
keywords:
- TSF (estrutura de serviços de texto), Gerenciador de documentos
- TSF (estrutura de serviços de texto), Gerenciador de documentos
- serviços de texto, Gerenciador de documentos
- Aplicativos habilitados para TSF, Gerenciador de documentos
- Gerenciador de documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2182782218ad6a8aa0a70f296f639560307249
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635373"
---
# <a name="document-manager"></a><span data-ttu-id="6d37a-108">Gerenciador de documentos</span><span class="sxs-lookup"><span data-stu-id="6d37a-108">Document Manager</span></span>

## <a name="applications"></a><span data-ttu-id="6d37a-109">Aplicativos</span><span class="sxs-lookup"><span data-stu-id="6d37a-109">Applications</span></span>

<span data-ttu-id="6d37a-110">Para criar um objeto do Gerenciador de documentos, um aplicativo chama [ITfThreadMgr:: CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr).</span><span class="sxs-lookup"><span data-stu-id="6d37a-110">To create a document manager object an application calls [ITfThreadMgr::CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr).</span></span> <span data-ttu-id="6d37a-111">O aplicativo cria um objeto separado do Gerenciador de documentos para cada documento individual que o aplicativo mantém.</span><span class="sxs-lookup"><span data-stu-id="6d37a-111">The application creates a separate document manager object for each individual document that the application maintains.</span></span> <span data-ttu-id="6d37a-112">O aplicativo usa o Gerenciador de documentos para criar contextos de edição, adicionar um contexto à pilha de contexto e remover um contexto da pilha de contexto.</span><span class="sxs-lookup"><span data-stu-id="6d37a-112">The application uses the document manager to create edit contexts, add a context to the context stack and remove a context from the context stack.</span></span>

## <a name="text-services"></a><span data-ttu-id="6d37a-113">Serviços de texto</span><span class="sxs-lookup"><span data-stu-id="6d37a-113">Text Services</span></span>

<span data-ttu-id="6d37a-114">Um serviço de texto nunca cria um objeto do Gerenciador de documentos.</span><span class="sxs-lookup"><span data-stu-id="6d37a-114">A text service never creates a document manager object.</span></span> <span data-ttu-id="6d37a-115">Em vez disso, o serviço de texto Obtém o objeto do Gerenciador de documentos ativo no momento chamando [ITfThreadMgr:: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus).</span><span class="sxs-lookup"><span data-stu-id="6d37a-115">Instead, the text service obtains the currently active document manager object by calling [ITfThreadMgr::GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus).</span></span> <span data-ttu-id="6d37a-116">Um serviço de texto usa o Gerenciador de documentos para obter o contexto na parte superior da pilha.</span><span class="sxs-lookup"><span data-stu-id="6d37a-116">A text service uses the document manager to obtain the context at the top of the stack.</span></span>

<span data-ttu-id="6d37a-117">Um serviço de texto também pode usar o Gerenciador de documentos para criar seu próprio contexto e adicioná-lo e removê-lo da pilha de contexto.</span><span class="sxs-lookup"><span data-stu-id="6d37a-117">A text service can also use the document manager to create its own context and add and remove it from the context stack.</span></span> <span data-ttu-id="6d37a-118">Isso normalmente é feito quando o serviço de texto deve exibir uma interface do usuário modal, como quando uma lista de palavras é exibida para permitir que o usuário selecione uma palavra.</span><span class="sxs-lookup"><span data-stu-id="6d37a-118">This is normally done when the text service must display some modal user interface, such as when a list of words is displayed to enable the user to select a word.</span></span> <span data-ttu-id="6d37a-119">Quando a lista é exibida, o serviço de texto coloca seu próprio contexto na pilha.</span><span class="sxs-lookup"><span data-stu-id="6d37a-119">When the list is displayed, the text service places its own context on the stack.</span></span> <span data-ttu-id="6d37a-120">Quando a lista de palavras é ignorada, o serviço de texto remove seu contexto da pilha.</span><span class="sxs-lookup"><span data-stu-id="6d37a-120">When the word list is dismissed, the text service removes its context from the stack.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d37a-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6d37a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d37a-122">ITfDocumentMgr</span><span class="sxs-lookup"><span data-stu-id="6d37a-122">ITfDocumentMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[<span data-ttu-id="6d37a-123">ITfThreadMgr::CreateDocumentMgr</span><span class="sxs-lookup"><span data-stu-id="6d37a-123">ITfThreadMgr::CreateDocumentMgr</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr)
</dt> <dt>

[<span data-ttu-id="6d37a-124">ITfThreadMgr:: GetFocus</span><span class="sxs-lookup"><span data-stu-id="6d37a-124">ITfThreadMgr::GetFocus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> </dl>

 

 




