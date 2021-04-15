---
title: Sobre o DDEML
description: Este tópico discute a troca de dados dinâmicas.
ms.assetid: 155b4cb0-dfbb-42f5-9fa3-8129349a0754
keywords:
- Interface do usuário do Windows, troca dinâmica de dados (DDE)
- Troca dinâmica de dados (DDE), sobre
- DDE (troca dinâmica de dados), sobre
- troca de dados, troca dinâmica de dados (DDE)
- Interface do usuário do Windows, biblioteca de gerenciamento de troca dinâmica de dados (DDEML)
- Biblioteca de gerenciamento de troca dinâmica de dados (DDEML), sobre
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), sobre
- Data Exchange, biblioteca de gerenciamento de troca dinâmica de dados (DDEML)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ed77565c8b4e20841ad2ef80ae84c1f5c39724
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498810"
---
# <a name="about-the-ddeml"></a><span data-ttu-id="92790-111">Sobre o DDEML</span><span class="sxs-lookup"><span data-stu-id="92790-111">About the DDEML</span></span>

<span data-ttu-id="92790-112">O troca dinâmica de dados (DDE) difere do mecanismo de transferência de dados da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="92790-112">Dynamic Data Exchange (DDE) differs from the clipboard data-transfer mechanism.</span></span> <span data-ttu-id="92790-113">Uma diferença é que a área de transferência é quase sempre usada como uma resposta única para uma ação específica pelo usuário, como clicar em **colar** em um menu.</span><span class="sxs-lookup"><span data-stu-id="92790-113">One difference is that the clipboard is almost always used as a one-time response to a specific action by the user — such as clicking **Paste** from a menu.</span></span> <span data-ttu-id="92790-114">Embora o DDE também possa ser iniciado por um usuário, ele normalmente continua sem o envolvimento adicional do usuário.</span><span class="sxs-lookup"><span data-stu-id="92790-114">Although DDE can also be initiated by a user, it typically continues without the user's further involvement.</span></span>

<span data-ttu-id="92790-115">A biblioteca de gerenciamento de troca dinâmica de dados (DDEML) fornece uma interface que simplifica a tarefa de adicionar capacidade DDE a um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="92790-115">The Dynamic Data Exchange Management Library (DDEML) provides an interface that simplifies the task of adding DDE capability to an application.</span></span> <span data-ttu-id="92790-116">Em vez de enviar, postar e processar mensagens DDE diretamente, um aplicativo usa as funções fornecidas pelo DDEML para gerenciar conversas DDE.</span><span class="sxs-lookup"><span data-stu-id="92790-116">Instead of sending, posting, and processing DDE messages directly, an application uses the functions provided by the DDEML to manage DDE conversations.</span></span> <span data-ttu-id="92790-117">Uma conversa DDE é a interação entre aplicativos cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="92790-117">A DDE conversation is the interaction between client and server applications.</span></span> <span data-ttu-id="92790-118">O DDEML também fornece um meio para gerenciar as cadeias de caracteres e os dados compartilhados entre aplicativos DDE.</span><span class="sxs-lookup"><span data-stu-id="92790-118">The DDEML also provides a means for managing the strings and data shared among DDE applications.</span></span> <span data-ttu-id="92790-119">Em vez de usar Atoms e ponteiros para objetos de memória compartilhados, os aplicativos DDE criam e trocam identificadores de cadeias de caracteres, que identificam cadeias e identificadores de dados, que identificam objetos DDE.</span><span class="sxs-lookup"><span data-stu-id="92790-119">Instead of using atoms and pointers to shared memory objects, DDE applications create and exchange string handles, which identify strings, and data handles, which identify DDE objects.</span></span> <span data-ttu-id="92790-120">O DDEML fornece uma função ([**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) que permite que um aplicativo de servidor registre os nomes de serviço com suporte.</span><span class="sxs-lookup"><span data-stu-id="92790-120">The DDEML provides a function ([**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) that enables a server application to register the service names it supports.</span></span> <span data-ttu-id="92790-121">Os nomes de serviço são então difundidos para outros aplicativos no sistema, que usam os nomes para se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="92790-121">The service names are then broadcast to other applications in the system, which use the names to connect to the server.</span></span> <span data-ttu-id="92790-122">O DDEML também garante a compatibilidade entre aplicativos DDE, exigindo que eles implementem o protocolo DDE de maneira consistente.</span><span class="sxs-lookup"><span data-stu-id="92790-122">The DDEML also ensures compatibility among DDE applications by requiring them to implement the DDE protocol in a consistent manner.</span></span>

<span data-ttu-id="92790-123">Os aplicativos existentes que usam o protocolo DDE baseado em mensagem são totalmente compatíveis com aqueles que usam o DDEML; ou seja, um aplicativo que usa o DDE baseado em mensagem pode estabelecer conversas e executar transações com aplicativos usando o DDEML.</span><span class="sxs-lookup"><span data-stu-id="92790-123">Existing applications using the message-based DDE protocol are fully compatible with those that use the DDEML; that is, an application using message-based DDE can establish conversations and perform transactions with applications using the DDEML.</span></span> <span data-ttu-id="92790-124">Em vez de usar mensagens DDE em seu novo aplicativo, aproveite o DDEML e os vários aprimoramentos que ele oferece.</span><span class="sxs-lookup"><span data-stu-id="92790-124">Instead of using DDE messages in your new application, take advantage of the DDEML and the many improvements it offers.</span></span>

<span data-ttu-id="92790-125">Para usar o DDEML, você deve incluir o DDEML. Arquivo de cabeçalho H em seus arquivos de origem, vincule com o USER32. LIB e verifique se o arquivo de DDEML.DLL reside no caminho do sistema.</span><span class="sxs-lookup"><span data-stu-id="92790-125">To use the DDEML, you must include the DDEML.H header file in your source files, link with the USER32.LIB file, and ensure that the DDEML.DLL file resides in the system's path.</span></span>

<span data-ttu-id="92790-126">Sempre que uma função DDEML falha, um aplicativo pode chamar a função [**DdeGetLastError**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) para determinar a causa da falha.</span><span class="sxs-lookup"><span data-stu-id="92790-126">Whenever a DDEML function fails, an application can call the [**DdeGetLastError**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) function to determine the cause of the failure.</span></span> <span data-ttu-id="92790-127">**DdeGetLastError** retorna um valor de erro que especifica a causa do erro mais recente.</span><span class="sxs-lookup"><span data-stu-id="92790-127">**DdeGetLastError** returns an error value that specifies the cause of the most recent error.</span></span>

 

 




