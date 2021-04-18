---
description: Descreve os conceitos básicos de e/s.
ms.assetid: 61b286a0-2f0d-48d1-a0b9-bb13f1ea1b0e
title: Conceitos de e/s
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727ae7f2b34b7938de444a82c9c4dfdf89f52ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761731"
---
# <a name="io-concepts"></a><span data-ttu-id="fce42-103">Conceitos de e/s</span><span class="sxs-lookup"><span data-stu-id="fce42-103">I/O Concepts</span></span>

<span data-ttu-id="fce42-104">Os seguintes conceitos de e/s são descritos nesta seção.</span><span class="sxs-lookup"><span data-stu-id="fce42-104">The following I/O concepts are described in this section.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fce42-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="fce42-105">In this section</span></span>



| <span data-ttu-id="fce42-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="fce42-106">Topic</span></span>                                                                               | <span data-ttu-id="fce42-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="fce42-107">Description</span></span>                                                                                                                                                         |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fce42-108">Buffer de arquivo</span><span class="sxs-lookup"><span data-stu-id="fce42-108">File Buffering</span></span>](file-buffering.md)<br/>                                     | <span data-ttu-id="fce42-109">Descreve as considerações sobre O controle de aplicativo do buffer de arquivo, também conhecido como e/s (entrada/saída) de arquivo sem buffer.</span><span class="sxs-lookup"><span data-stu-id="fce42-109">Describes considerations for application control of file buffering, also known as unbuffered file input/output (I/O).</span></span><br/>                                    |
| [<span data-ttu-id="fce42-110">Cache de arquivo</span><span class="sxs-lookup"><span data-stu-id="fce42-110">File Caching</span></span>](file-caching.md)<br/>                                         | <span data-ttu-id="fce42-111">O Windows armazena em cache os dados de arquivo que são lidos de discos e gravados em discos.</span><span class="sxs-lookup"><span data-stu-id="fce42-111">Windows caches file data that is read from disks and written to disks.</span></span><br/>                                                                                   |
| [<span data-ttu-id="fce42-112">E/s síncrona e síncrona</span><span class="sxs-lookup"><span data-stu-id="fce42-112">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)<br/> | <span data-ttu-id="fce42-113">Há dois tipos de sincronização de e/s (entrada/saída): e/s síncrona e e/SS assíncrona.</span><span class="sxs-lookup"><span data-stu-id="fce42-113">There are two types of input/output (I/O) synchronization: synchronous I/O and asynchronous I/O.</span></span> <span data-ttu-id="fce42-114">E/s assíncrona também é conhecida como e/s sobreposta.</span><span class="sxs-lookup"><span data-stu-id="fce42-114">Asynchronous I/O is also referred to as overlapped I/O.</span></span><br/> |
| [<span data-ttu-id="fce42-115">Cancelando operações de e/s pendentes</span><span class="sxs-lookup"><span data-stu-id="fce42-115">Canceling Pending I/O Operations</span></span>](canceling-pending-i-o-operations.md)<br/> | <span data-ttu-id="fce42-116">Permitir que os usuários cancelem solicitações de e/s lentas ou bloqueadas pode melhorar a usabilidade e a robustez do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fce42-116">Allowing users to cancel I/O requests that are slow or blocked can enhance the usability and robustness of your application.</span></span><br/>                             |
| [<span data-ttu-id="fce42-117">E/s alertável</span><span class="sxs-lookup"><span data-stu-id="fce42-117">Alertable I/O</span></span>](alertable-i-o.md)<br/>                                       | <span data-ttu-id="fce42-118">E/s de alerta é o método pelo qual os threads de aplicativo processam solicitações de e/s assíncronas somente quando estão em um estado de alerta.</span><span class="sxs-lookup"><span data-stu-id="fce42-118">Alertable I/O is the method by which application threads process asynchronous I/O requests only when they are in an alertable state.</span></span><br/>                     |
| [<span data-ttu-id="fce42-119">Portas de conclusão de e/s</span><span class="sxs-lookup"><span data-stu-id="fce42-119">I/O Completion Ports</span></span>](i-o-completion-ports.md)<br/>                         | <span data-ttu-id="fce42-120">As portas de conclusão de e/s fornecem um modelo de Threading eficiente para processar várias solicitações de e/s assíncronas em um sistema multiprocessador.</span><span class="sxs-lookup"><span data-stu-id="fce42-120">I/O completion ports provide an efficient threading model for processing multiple asynchronous I/O requests on a multiprocessor system.</span></span><br/>                  |



 

 

 




