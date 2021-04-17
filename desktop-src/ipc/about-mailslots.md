---
description: Um processador de processadores é um pseudofile que reside na memória e você usa funções de arquivo padrão para acessá-lo.
ms.assetid: 9a68905d-c235-4c72-bc71-1cccdf5cdadc
title: Sobre processadores de informações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bd83fc0d952577efdb149d4c7f25fffbab9784f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769261"
---
# <a name="about-mailslots"></a><span data-ttu-id="ee433-103">Sobre processadores de informações</span><span class="sxs-lookup"><span data-stu-id="ee433-103">About Mailslots</span></span>

<span data-ttu-id="ee433-104">Um processador de processadores é um pseudofile que reside na memória e você usa funções de arquivo padrão para acessá-lo.</span><span class="sxs-lookup"><span data-stu-id="ee433-104">A mailslot is a pseudofile that resides in memory, and you use standard file functions to access it.</span></span> <span data-ttu-id="ee433-105">Os dados em uma mensagem do processador de mensagens podem estar em qualquer formato, mas não podem ter mais de 424 bytes quando enviados entre computadores.</span><span class="sxs-lookup"><span data-stu-id="ee433-105">The data in a mailslot message can be in any form, but cannot be larger than 424 bytes when sent between computers.</span></span> <span data-ttu-id="ee433-106">Ao contrário dos arquivos de disco, os processadores são temporários.</span><span class="sxs-lookup"><span data-stu-id="ee433-106">Unlike disk files, mailslots are temporary.</span></span> <span data-ttu-id="ee433-107">Quando todos os identificadores para um processador de processadores são fechados, o processador de processadores e todos os dados que ele contém são excluídos.</span><span class="sxs-lookup"><span data-stu-id="ee433-107">When all handles to a mailslot are closed, the mailslot and all the data it contains are deleted.</span></span>

<span data-ttu-id="ee433-108">Um *servidor do processador de processadores* é um processo que cria e possui um processador de processadores.</span><span class="sxs-lookup"><span data-stu-id="ee433-108">A *mailslot server* is a process that creates and owns a mailslot.</span></span> <span data-ttu-id="ee433-109">Quando o servidor cria um processador de processadores, ele recebe um identificador de processador de processadores.</span><span class="sxs-lookup"><span data-stu-id="ee433-109">When the server creates a mailslot, it receives a mailslot handle.</span></span> <span data-ttu-id="ee433-110">Esse identificador deve ser usado quando um processo lê mensagens do processador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="ee433-110">This handle must be used when a process reads messages from the mailslot.</span></span> <span data-ttu-id="ee433-111">Somente o processo que cria um processador de processadores ou obteve o identificador por algum outro mecanismo (como a herança) pode ler do processador de itens.</span><span class="sxs-lookup"><span data-stu-id="ee433-111">Only the process that creates a mailslot or has obtained the handle by some other mechanism (such as inheritance) can read from the mailslot.</span></span> <span data-ttu-id="ee433-112">Todos os processadores são locais para o processo que os cria.</span><span class="sxs-lookup"><span data-stu-id="ee433-112">All mailslots are local to the process that creates them.</span></span> <span data-ttu-id="ee433-113">Um processo não pode criar um processador de processadores remoto.</span><span class="sxs-lookup"><span data-stu-id="ee433-113">A process cannot create a remote mailslot.</span></span>

<span data-ttu-id="ee433-114">Um *cliente do processador* de mensagens é um processo que grava uma mensagem em um processador de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ee433-114">A *mailslot client* is a process that writes a message to a mailslot.</span></span> <span data-ttu-id="ee433-115">Qualquer processo que tenha o nome de um processador de mensagens pode colocar uma mensagem lá.</span><span class="sxs-lookup"><span data-stu-id="ee433-115">Any process that has the name of a mailslot can put a message there.</span></span> <span data-ttu-id="ee433-116">Novas mensagens seguem qualquer mensagem existente no processador de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ee433-116">New messages follow any existing messages in the mailslot.</span></span>

<span data-ttu-id="ee433-117">Os processadores podem transmitir mensagens em um domínio.</span><span class="sxs-lookup"><span data-stu-id="ee433-117">Mailslots can broadcast messages within a domain.</span></span> <span data-ttu-id="ee433-118">Se vários processos em um domínio criarem um processador de mensagens usando o mesmo nome, cada mensagem que é endereçada a esse processador e enviado ao domínio é recebida pelos processos participantes.</span><span class="sxs-lookup"><span data-stu-id="ee433-118">If several processes in a domain each create a mailslot using the same name, every message that is addressed to that mailslot and sent to the domain is received by the participating processes.</span></span> <span data-ttu-id="ee433-119">Como um processo pode controlar tanto um identificador de processador de processadores quanto o identificador do cliente recuperado quando o processador de mensagens é aberto para uma operação de gravação, os aplicativos podem facilmente implementar uma facilidade de transmissão de mensagem simples em um domínio.</span><span class="sxs-lookup"><span data-stu-id="ee433-119">Because one process can control both a server mailslot handle and the client handle retrieved when the mailslot is opened for a write operation, applications can easily implement a simple message-passing facility within a domain.</span></span>

<span data-ttu-id="ee433-120">Para enviar mensagens com mais de 424 bytes entre computadores, use [pipes nomeados](named-pipes.md) ou [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="ee433-120">To send messages that are larger than 424 bytes between computers, use [named pipes](named-pipes.md) or [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2) instead.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee433-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ee433-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee433-122">Nomes de processador de processadores</span><span class="sxs-lookup"><span data-stu-id="ee433-122">Mailslot Names</span></span>](mailslot-names.md)
</dt> <dt>

[<span data-ttu-id="ee433-123">Operações de processador de processadores</span><span class="sxs-lookup"><span data-stu-id="ee433-123">Mailslot Operations</span></span>](mailslot-operations.md)
</dt> </dl>

 

 
