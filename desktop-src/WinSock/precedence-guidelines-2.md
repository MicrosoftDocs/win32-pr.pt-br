---
description: Os dois (ou mais) descritores que fazem referência a um Soquete compartilhado podem ser usados de forma independente no que diz respeito à e/s.
ms.assetid: 25252552-4b62-441a-b564-e7f4a77cf68a
title: Diretrizes de precedência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c2086b2d640e2968c56082c2d8dfff99546fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090365"
---
# <a name="precedence-guidelines"></a><span data-ttu-id="71b51-103">Diretrizes de precedência</span><span class="sxs-lookup"><span data-stu-id="71b51-103">Precedence Guidelines</span></span>

<span data-ttu-id="71b51-104">Os dois (ou mais) descritores que fazem referência a um Soquete compartilhado podem ser usados de forma independente no que diz respeito à e/s.</span><span class="sxs-lookup"><span data-stu-id="71b51-104">The two (or more) descriptors that reference a shared socket may be used independently as far as I/O is concerned.</span></span> <span data-ttu-id="71b51-105">No entanto, a interface do Windows Sockets não implementa nenhum tipo de controle de acesso, portanto, cabe aos processos envolvidos coordenarem suas operações em um Soquete compartilhado.</span><span class="sxs-lookup"><span data-stu-id="71b51-105">However, the Windows Sockets interface does not implement any type of access control, so it is up to the processes involved to coordinate their operations on a shared socket.</span></span> <span data-ttu-id="71b51-106">Um uso típico para soquetes compartilhados é ter um processo responsável pela criação de soquetes e estabelecimento de conexões que entregam soquetes a outros processos responsáveis pela troca de informações.</span><span class="sxs-lookup"><span data-stu-id="71b51-106">A typical use for shared sockets is to have one process that is responsible for creating sockets and establishing connections hand off sockets to other processes that are responsible for information exchange.</span></span>

<span data-ttu-id="71b51-107">A diretriz geral para dar suporte a várias operações pendentes em soquetes compartilhados é que um provedor de serviços é incentivado a respeitar todas as operações simultâneas em soquetes compartilhados, especialmente a operação mais recente em um objeto de soquete.</span><span class="sxs-lookup"><span data-stu-id="71b51-107">The general guideline for supporting multiple outstanding operations on shared sockets is that a service provider is encouraged to honor all simultaneous operations on shared sockets, especially the most recent operation on a socket object.</span></span> <span data-ttu-id="71b51-108">Se necessário, isso pode ocorrer às custas de cancelar algumas das operações anteriores, mas ainda pendentes, que retornarão WSAEINTR nesse caso.</span><span class="sxs-lookup"><span data-stu-id="71b51-108">If need be, this may occur at the expense of canceling some of the previous but still pending operations, which will return WSAEINTR in this case.</span></span>

 

 



