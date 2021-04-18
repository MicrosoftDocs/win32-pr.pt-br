---
description: Conceitos de componentes em fila do COM+
ms.assetid: ff11e251-311f-4612-8f0d-a4cbc5b4d872
title: Conceitos de componentes em fila do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729d1a8983e84d817e402454392ce95fc2b07a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762995"
---
# <a name="com-queued-components-concepts"></a><span data-ttu-id="f4388-103">Conceitos de componentes em fila do COM+</span><span class="sxs-lookup"><span data-stu-id="f4388-103">COM+ Queued Components Concepts</span></span>

<span data-ttu-id="f4388-104">Com base nos serviços de [enfileiramento de mensagens](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) , o serviço de componentes em fila do com+ fornece uma maneira fácil de invocar e executar componentes de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="f4388-104">Based on [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) services, the COM+ queued components service provides an easy way to invoke and execute components asynchronously.</span></span> <span data-ttu-id="f4388-105">O processamento pode ocorrer sem considerar a disponibilidade ou a acessibilidade do remetente ou do receptor.</span><span class="sxs-lookup"><span data-stu-id="f4388-105">Processing can occur without regard to the availability or accessibility of either the sender or the receiver.</span></span>

<span data-ttu-id="f4388-106">Em termos de COM, uma *fila* é uma área de armazenamento que salva as mensagens para recuperação posterior.</span><span class="sxs-lookup"><span data-stu-id="f4388-106">In COM terms, a *queue* is a storage area that saves messages for later retrieval.</span></span> <span data-ttu-id="f4388-107">O enfileiramento fornece um mecanismo de comunicação sem conexão.</span><span class="sxs-lookup"><span data-stu-id="f4388-107">Queuing provides a mechanism for connectionless communication.</span></span> <span data-ttu-id="f4388-108">Ou seja, o remetente e o destinatário não estão conectados diretamente e se comunicam somente por meio de filas.</span><span class="sxs-lookup"><span data-stu-id="f4388-108">That is, the sender and receiver are not connected directly and communicate only through queues.</span></span> <span data-ttu-id="f4388-109">O enfileiramento fornece uma maneira de manter as informações até que o receptor esteja pronto para obtê-la.</span><span class="sxs-lookup"><span data-stu-id="f4388-109">Queuing provides a way to hold the information until the receiver is ready to obtain it.</span></span> <span data-ttu-id="f4388-110">O remetente e o destinatário estão se comunicando indiretamente para que cada um possa operar de forma independente, não afetado pelo outro.</span><span class="sxs-lookup"><span data-stu-id="f4388-110">The sender and receiver are indirectly communicating so that each can operate independently, unaffected by the other.</span></span>

<span data-ttu-id="f4388-111">No passado, um conhecimento profundo do marshaling era necessário para enfileirar, enviar e receber mensagens assíncronas.</span><span class="sxs-lookup"><span data-stu-id="f4388-111">In the past, an in-depth knowledge of marshaling was necessary to queue, send, and receive asynchronous messages.</span></span> <span data-ttu-id="f4388-112">Agora, usando chamadas de método que são facilmente compreendidas e usadas por desenvolvedores de componentes, o serviço de componentes em fila COM+ realiza marshaling de dados automaticamente na forma de uma mensagem de enfileiramento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f4388-112">Now, using method calls that are easily understood and used by component developers, the COM+ queued components service automatically marshals data in the form of a Message Queuing message.</span></span> <span data-ttu-id="f4388-113">E como o serviço de componentes em fila oferece suporte interno para transações, um estado inconsistente não poderá comprometer os dados se ocorrer uma falha de servidor.</span><span class="sxs-lookup"><span data-stu-id="f4388-113">And because the queued components service offers built-in support for transactions, an inconsistent state cannot compromise data if a server failure occurs.</span></span>

<span data-ttu-id="f4388-114">Os tópicos a seguir nesta seção contêm informações básicas sobre como criar e gravar componentes enfileirados.</span><span class="sxs-lookup"><span data-stu-id="f4388-114">The following topics in this section contain background information about designing and writing queued components.</span></span>



| <span data-ttu-id="f4388-115">Tópico</span><span class="sxs-lookup"><span data-stu-id="f4388-115">Topic</span></span>                                                                           | <span data-ttu-id="f4388-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4388-116">Description</span></span>                                                                                                           |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4388-117">Benefícios do processamento em fila</span><span class="sxs-lookup"><span data-stu-id="f4388-117">Benefits of Queued Processing</span></span>](benefits-of-queued-processing.md)<br/>   | <span data-ttu-id="f4388-118">Descreve os benefícios da programação com os componentes em fila do COM+.</span><span class="sxs-lookup"><span data-stu-id="f4388-118">Describes the benefits of programming with COM+ queued components.</span></span><br/>                                         |
| [<span data-ttu-id="f4388-119">Arquitetura de componentes na fila</span><span class="sxs-lookup"><span data-stu-id="f4388-119">Queued Components Architecture</span></span>](queued-components-architecture.md)<br/> | <span data-ttu-id="f4388-120">Descreve a arquitetura do serviço de componentes em fila do COM+.</span><span class="sxs-lookup"><span data-stu-id="f4388-120">Describes the architecture of the COM+ queued components service.</span></span><br/>                                          |
| [<span data-ttu-id="f4388-121">Enfileiramento de mensagens transacionais</span><span class="sxs-lookup"><span data-stu-id="f4388-121">Transactional Message Queuing</span></span>](transactional-message-queuing.md)<br/>   | <span data-ttu-id="f4388-122">Descreve como as transações são manipuladas pelo serviço de componentes em fila do COM+.</span><span class="sxs-lookup"><span data-stu-id="f4388-122">Describes how transactions are handled by the COM+ queued components service.</span></span><br/>                              |
| [<span data-ttu-id="f4388-123">Segurança de componentes na fila</span><span class="sxs-lookup"><span data-stu-id="f4388-123">Queued Components Security</span></span>](queued-components-security.md)<br/>         | <span data-ttu-id="f4388-124">Descreve as opções de política para autenticação de mensagens do cliente e suas implicações.</span><span class="sxs-lookup"><span data-stu-id="f4388-124">Describes the policy options for authentication of client messages and their implications.</span></span><br/>                 |
| [<span data-ttu-id="f4388-125">Desenvolvendo componentes em fila</span><span class="sxs-lookup"><span data-stu-id="f4388-125">Developing Queued Components</span></span>](developing-queued-components.md)<br/>     | <span data-ttu-id="f4388-126">Descreve considerações de programação ao escrever componentes queuable.</span><span class="sxs-lookup"><span data-stu-id="f4388-126">Describes programming considerations when writing queuable components.</span></span><br/>                                     |
| [<span data-ttu-id="f4388-127">Erros de componentes na fila</span><span class="sxs-lookup"><span data-stu-id="f4388-127">Queued Components Errors</span></span>](queued-components-errors.md)<br/>             | <span data-ttu-id="f4388-128">Descreve os tipos mais comuns de erros que você pode encontrar ao usar o serviço de componentes na fila do COM+.</span><span class="sxs-lookup"><span data-stu-id="f4388-128">Describes the most common types of errors you may encounter when using the COM+ queued components service.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="f4388-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f4388-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4388-130">Tarefas de componentes em fila COM+</span><span class="sxs-lookup"><span data-stu-id="f4388-130">COM+ Queued Components Tasks</span></span>](com--queued-components-tasks.md)
</dt> </dl>

 

 




