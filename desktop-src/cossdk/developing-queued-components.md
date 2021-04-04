---
description: Desenvolvendo componentes em fila
ms.assetid: 867b7512-82ad-4877-8675-aa2d7e62ff8a
title: Desenvolvendo componentes em fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8808ef3e6cba8ff561dd94473fca8f00631081f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646285"
---
# <a name="developing-queued-components"></a><span data-ttu-id="0dd58-103">Desenvolvendo componentes em fila</span><span class="sxs-lookup"><span data-stu-id="0dd58-103">Developing Queued Components</span></span>

<span data-ttu-id="0dd58-104">O serviço de componentes na fila do COM+ requer que todos os métodos de aplicativo contenham somente \[ \] parâmetros de parâmetro, sem valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="0dd58-104">The COM+ queued components service requires all application methods to contain only \[in\] parameters, with no return values.</span></span> <span data-ttu-id="0dd58-105">Como o objeto Server não está necessariamente disponível quando o cliente faz a chamada, os resultados do servidor podem ser retornados enviando uma mensagem que cria outro objeto.</span><span class="sxs-lookup"><span data-stu-id="0dd58-105">Because the server object is not necessarily available when the client makes the call, server results can be returned by sending a message that creates another object.</span></span> <span data-ttu-id="0dd58-106">Dessa forma, a comunicação bidirecional não ocorre em todos os casos, mas apenas quando ela é necessária, por uma série de mensagens unidirecionais entre objetos.</span><span class="sxs-lookup"><span data-stu-id="0dd58-106">In this way, two-way communication occurs not in every case but only when it is required, by a series of one-way messages between objects.</span></span>

<span data-ttu-id="0dd58-107">Para usar o serviço de componentes na fila COM+, você deve ter o serviço de [enfileiramento de mensagens](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) já instalado.</span><span class="sxs-lookup"><span data-stu-id="0dd58-107">To use the COM+ queued components service, you must have the [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) service already installed.</span></span> <span data-ttu-id="0dd58-108">O enfileiramento de mensagens não é instalado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="0dd58-108">Message Queuing is not installed automatically.</span></span> <span data-ttu-id="0dd58-109">O enfileiramento de mensagens deve ser selecionado durante a configuração do sistema operacional ou usando **Adicionar/remover programas**.</span><span class="sxs-lookup"><span data-stu-id="0dd58-109">Message Queuing must be selected during the operating system setup or by using **Add/Remove programs**.</span></span> <span data-ttu-id="0dd58-110">Um certificado interno do enfileiramento de mensagens é criado automaticamente no logon.</span><span class="sxs-lookup"><span data-stu-id="0dd58-110">An internal Message Queuing certificate is created automatically at logon.</span></span>

<span data-ttu-id="0dd58-111">Os tópicos descritos na tabela a seguir fornecem considerações adicionais para situações mais especializadas.</span><span class="sxs-lookup"><span data-stu-id="0dd58-111">The topics described in the following table provide additional considerations for more specialized situations.</span></span>



| <span data-ttu-id="0dd58-112">Tópico</span><span class="sxs-lookup"><span data-stu-id="0dd58-112">Topic</span></span>                                                                                           | <span data-ttu-id="0dd58-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="0dd58-113">Description</span></span>                                                                                            |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dd58-114">[Passando objetos como parâmetros](passing-objects-as-parameters.md)s</span><span class="sxs-lookup"><span data-stu-id="0dd58-114">[Passing Objects as Parameter](passing-objects-as-parameters.md)s</span></span><br/>                   | <span data-ttu-id="0dd58-115">Descreve como transmitir objetos como \[ parâmetros em \] componentes em fila.</span><span class="sxs-lookup"><span data-stu-id="0dd58-115">Describes how to pass objects as \[in\] parameters to queued components.</span></span><br/>                    |
| [<span data-ttu-id="0dd58-116">Limitações de segurança no modo de grupo de trabalho</span><span class="sxs-lookup"><span data-stu-id="0dd58-116">Security Limitations in Workgroup Mode</span></span>](security-limitations-in-workgroup-mode.md)<br/> | <span data-ttu-id="0dd58-117">Descreve as limitações no uso da autenticação do serviço de enfileiramento de mensagens no modo de grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0dd58-117">Describes limitations on the use of Message Queuing authentication in workgroup mode.</span></span><br/>       |
| [<span data-ttu-id="0dd58-118">Considerações de thread</span><span class="sxs-lookup"><span data-stu-id="0dd58-118">Threading Considerations</span></span>](threading-considerations.md)<br/>                             | <span data-ttu-id="0dd58-119">Descreve as preocupações específicas relacionadas à passagem de ponteiros de interface do gravador entre threads.</span><span class="sxs-lookup"><span data-stu-id="0dd58-119">Describes specific concerns related to passing recorder interface pointers between threads.</span></span><br/> |
| [<span data-ttu-id="0dd58-120">Recebendo uma resposta</span><span class="sxs-lookup"><span data-stu-id="0dd58-120">Receiving a Response</span></span>](receiving-a-response.md)<br/>                                     | <span data-ttu-id="0dd58-121">Descreve como construir uma resposta a uma chamada de componente enfileirada.</span><span class="sxs-lookup"><span data-stu-id="0dd58-121">Describes how to construct a response to a queued component call.</span></span><br/>                           |



 

 

 




