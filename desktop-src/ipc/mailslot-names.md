---
description: Nome de processadores e colocação de mensagens em processadores.
ms.assetid: 1ef522a4-9786-427c-a18a-ae1f0a05cc50
title: Nomes de processador de processadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf03718a7e603fe891e00d82c2b0b06fab63f8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646696"
---
# <a name="mailslot-names"></a><span data-ttu-id="8fcc4-103">Nomes de processador de processadores</span><span class="sxs-lookup"><span data-stu-id="8fcc4-103">Mailslot Names</span></span>

<span data-ttu-id="8fcc4-104">Quando um processo cria um processador de itens, o nome do processador de processadores deve ter o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="8fcc4-104">When a process creates a mailslot, the mailslot name must have the following form.</span></span>

<span data-ttu-id="8fcc4-105">\\\\.\\ nome do \\ \[ *caminho* \\ \]  do processador de processadores</span><span class="sxs-lookup"><span data-stu-id="8fcc4-105">\\\\.\\mailslot\\\[*path*\\\]*name*</span></span>

<span data-ttu-id="8fcc4-106">Um nome de processador de texto requer os seguintes elementos: duas barras invertidas para iniciar o nome, um ponto, uma barra invertida após o período, a palavra "processador de texto" e uma barra invertida à direita.</span><span class="sxs-lookup"><span data-stu-id="8fcc4-106">A mailslot name requires the following elements: two backslashes to begin the name, a period, a backslash following the period, the word "mailslot", and a trailing backslash.</span></span> <span data-ttu-id="8fcc4-107">Os nomes não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8fcc4-107">Names are not case sensitive.</span></span> <span data-ttu-id="8fcc4-108">Um nome de processador de itens pode ser precedido por um caminho que consiste nos nomes de um ou mais diretórios, separados por barras invertidas.</span><span class="sxs-lookup"><span data-stu-id="8fcc4-108">A mailslot name can be preceded by a path consisting of the names of one or more directories, separated by backslashes.</span></span> <span data-ttu-id="8fcc4-109">Por exemplo, se um usuário espera mensagens no assunto de impostos de Bob, Pete e Suzana, o aplicativo do processador de mensagens do usuário pode permitir que o usuário crie processadores de mensagens individuais para cada remetente, como mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="8fcc4-109">For example, if a user expects messages on the subject of taxes from Bob, Pete, and Sue, the user's mailslot application might allow the user to create individual mailslots for each sender, as shown here:</span></span><dl> <span data-ttu-id="8fcc4-110">\\\\.\\ \\ \\ comentários bobs de taxas de processador de processadores \_</span><span class="sxs-lookup"><span data-stu-id="8fcc4-110">\\\\.\\mailslot\\taxes\\bobs\_comments</span></span>  
<span data-ttu-id="8fcc4-111">\\\\.\\ os impostos do processador de \\ taxas \\ petem \_ comentários</span><span class="sxs-lookup"><span data-stu-id="8fcc4-111">\\\\.\\mailslot\\taxes\\petes\_comments</span></span>  
<span data-ttu-id="8fcc4-112">\\\\.\\ \\ \\ comentários sues de taxas de processador de processadores \_</span><span class="sxs-lookup"><span data-stu-id="8fcc4-112">\\\\.\\mailslot\\taxes\\sues\_comments</span></span>  
</dl>

<span data-ttu-id="8fcc4-113">Para colocar uma mensagem em um processador de mensagens, um processo abre um processador por nome.</span><span class="sxs-lookup"><span data-stu-id="8fcc4-113">To put a message into a mailslot, a process opens a mailslot by name.</span></span> <span data-ttu-id="8fcc4-114">Para gravar em um processador de processadores no computador local, um processo pode usar um nome de processador de processadores que tenha a mesma forma usada para criar um processador de processadores.</span><span class="sxs-lookup"><span data-stu-id="8fcc4-114">To write to a mailslot on the local computer, a process can use a mailslot name that has the same form used for creating a mailslot.</span></span> <span data-ttu-id="8fcc4-115">No entanto, essa situação é relativamente incomum.</span><span class="sxs-lookup"><span data-stu-id="8fcc4-115">This situation, however, is relatively uncommon.</span></span> <span data-ttu-id="8fcc4-116">Com mais frequência, você usaria o seguinte formulário para gravar em um processador de processadores em um computador remoto específico:</span><span class="sxs-lookup"><span data-stu-id="8fcc4-116">More frequently, you would use the following form to write to a mailslot on a specific remote computer:</span></span>

<span data-ttu-id="8fcc4-117">\\\\*ComputerName* \\ nome do \\ \[ *caminho* \\ \]  do processador de processadores</span><span class="sxs-lookup"><span data-stu-id="8fcc4-117">\\\\*ComputerName*\\mailslot\\\[*path*\\\]*name*</span></span>

<span data-ttu-id="8fcc4-118">Para colocar uma mensagem em cada processador de mensagens no domínio especificado com um determinado nome, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="8fcc4-118">To put a message into every mailslot in the specified domain with a given name, use the following form:</span></span>

<span data-ttu-id="8fcc4-119">\\\\*Nome_do_domínio* \\ nome do \\ \[ *caminho* \\ \]  do processador de processadores</span><span class="sxs-lookup"><span data-stu-id="8fcc4-119">\\\\*DomainName*\\mailslot\\\[*path*\\\]*name*</span></span>

<span data-ttu-id="8fcc4-120">Para colocar uma mensagem em cada processador de mensagens com um nome específico no domínio primário do sistema, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="8fcc4-120">To put a message into every mailslot with a given name in the system's primary domain, use the following form:</span></span>

<span data-ttu-id="8fcc4-121">\\\\\*\\nome do \\ \[ *caminho* \\ \]  do processador de processadores</span><span class="sxs-lookup"><span data-stu-id="8fcc4-121">\\\\\*\\mailslot\\\[*path*\\\]*name*</span></span>

 

 



