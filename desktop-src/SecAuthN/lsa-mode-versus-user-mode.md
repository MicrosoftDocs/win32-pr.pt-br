---
description: Quando um pacote de segurança SSP/AP está funcionando como um pacote de autenticação, ele é carregado no espaço de processo da autoridade de segurança local (LSA) e é considerado no modo LSA.
ms.assetid: ff4e61be-dbaa-4cfa-8c72-43e99fe1c3cb
title: Modo LSA versus modo de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8fadde30fe60c38a2b8ccb1f158d94ec7d5603
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011524"
---
# <a name="lsa-mode-vs-user-mode"></a><span data-ttu-id="51372-103">Modo LSA versus modo de usuário</span><span class="sxs-lookup"><span data-stu-id="51372-103">LSA Mode vs. User Mode</span></span>

<span data-ttu-id="51372-104">Quando um [*pacote de segurança*](../secgloss/s-gly.md) SSP/AP está funcionando como um [*pacote de autenticação*](../secgloss/a-gly.md), ele é carregado no espaço de processo da [*autoridade de segurança local*](../secgloss/l-gly.md) (LSA) e é considerado no modo LSA.</span><span class="sxs-lookup"><span data-stu-id="51372-104">When an SSP/AP [*security package*](../secgloss/s-gly.md) is functioning as an [*authentication package*](../secgloss/a-gly.md), it is loaded into the process space of the [*Local Security Authority*](../secgloss/l-gly.md) (LSA) and is said to be in LSA mode.</span></span> <span data-ttu-id="51372-105">Os aplicativos de logon acessam a funcionalidade do pacote de autenticação usando as [funções de logon LSA](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="51372-105">Logon applications access authentication package functionality using the [LSA Logon Functions](authentication-functions.md).</span></span> <span data-ttu-id="51372-106">Os desenvolvedores podem usar as funções de suporte do LSA disponíveis somente para os pacotes de segurança do modo LSA para implementar pacotes de autenticação mais sofisticados do que o suportado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="51372-106">Developers can use LSA support functions available only to LSA-mode security packages to implement more sophisticated authentication packages than previously supported.</span></span>

<span data-ttu-id="51372-107">Quando um [*pacote de segurança*](../secgloss/s-gly.md) fornece serviços de segurança para um aplicativo cliente/servidor, ele é carregado nos processos de cliente e servidor e é considerado no modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="51372-107">When a [*security package*](../secgloss/s-gly.md) provides security services to a client/server application, it is loaded into the client and server processes and is said to be in user mode.</span></span> <span data-ttu-id="51372-108">Os aplicativos cliente/servidor acessam os serviços de suporte de segurança do pacote de segurança usando o SSPI (Microsoft [*Security Support Provider interface*](../secgloss/s-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="51372-108">Client/server applications access the security package's security support services using Microsoft [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI).</span></span>

<span data-ttu-id="51372-109">O suporte de LSA para SSP/APs inclui funções que as instâncias de modo LSA e de modo de usuário de um pacote de segurança podem usar para se comunicar.</span><span class="sxs-lookup"><span data-stu-id="51372-109">LSA support for SSP/APs includes functions that the LSA-mode and user-mode instances of a security package can use to communicate.</span></span> <span data-ttu-id="51372-110">Além disso, a instância do modo de usuário de um pacote de segurança pode delegar solicitações selecionadas para informações para a instância do modo LSA do pacote.</span><span class="sxs-lookup"><span data-stu-id="51372-110">Additionally, the user-mode instance of a security package can delegate selected requests for information to the LSA-mode instance of the package.</span></span>

<span data-ttu-id="51372-111">Para obter detalhes sobre como os pacotes de segurança são inicializados para cada modo, consulte [inicialização do modo LSA](lsa-mode-initialization.md) e [inicialização do modo de usuário](user-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="51372-111">For details about how security packages are initialized for each mode, see [LSA-mode Initialization](lsa-mode-initialization.md) and [User-mode Initialization](user-mode-initialization.md).</span></span>

 

 
