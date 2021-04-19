---
description: Herdando transações manuais
ms.assetid: 3616275c-1e2d-4f9d-8adf-11ac9be132f1
title: Herdando transações manuais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a802bb392223742e0116d34a81a25fe9be54f220
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811641"
---
# <a name="inheriting-manual-transactions"></a><span data-ttu-id="c7aba-103">Herdando transações manuais</span><span class="sxs-lookup"><span data-stu-id="c7aba-103">Inheriting Manual Transactions</span></span>

<span data-ttu-id="c7aba-104">Se um objeto com uma transação de BYOT em seu contexto criar um segundo objeto, o objeto downstream poderá herdar a transação de BYOT (se configurada para herdar transações).</span><span class="sxs-lookup"><span data-stu-id="c7aba-104">If an object with a BYOT transaction in its context creates a second object, the downstream object can inherit the BYOT transaction (if configured to inherit transactions).</span></span> <span data-ttu-id="c7aba-105">O primeiro objeto criado usando o gateway BYOT precisa ser configurado para transações "exigir" ou "suporte".</span><span class="sxs-lookup"><span data-stu-id="c7aba-105">The first object created using the BYOT gateway needs to be configured to "require" or "support" transactions.</span></span> <span data-ttu-id="c7aba-106">Os objetos subsequentes na atividade podem ser configurados com base nos requisitos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7aba-106">Subsequent objects in the activity could be configured based on application requirements.</span></span>

<span data-ttu-id="c7aba-107">Para transações automáticas, o tempo de execução do COM+ não tenta confirmar a transação até que o objeto raiz indique que ele está pronto (chamando [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) antes de retornar de uma chamada).</span><span class="sxs-lookup"><span data-stu-id="c7aba-107">For automatic transactions, the COM+ runtime does not attempt to commit the transaction until the root object indicates that it is ready (by calling [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) before returning from a call).</span></span> <span data-ttu-id="c7aba-108">Os usuários devem estar cientes de que uma transação de BYOT pode ser confirmada prematuramente (pois o trabalho de objetos filho não foi concluído), porque a "raiz" não está sendo executada no ambiente de tempo de execução do COM+ e a semântica de confirmação não está vinculada ao tempo de vida do objeto.</span><span class="sxs-lookup"><span data-stu-id="c7aba-108">Users should be aware that a BYOT transaction could commit prematurely (in that the work of child objects has not been completed), because the "root" is not running under the COM+ runtime environment, and the commit semantics are not tied to the lifetime of the object.</span></span> <span data-ttu-id="c7aba-109">Em geral, o usuário deve tomar cuidado para não violar o limite de sincronização da transação.</span><span class="sxs-lookup"><span data-stu-id="c7aba-109">In general, the user should take care to not violate the synchronization boundary of the transaction.</span></span>

<span data-ttu-id="c7aba-110">Caso contrário, a semântica de confirmação COM+ se aplicará.</span><span class="sxs-lookup"><span data-stu-id="c7aba-110">Otherwise, COM+ commit semantics apply.</span></span> <span data-ttu-id="c7aba-111">O COM+ não tentará confirmar uma transação enquanto um objeto dentro de um limite de sincronização estiver em chamada.</span><span class="sxs-lookup"><span data-stu-id="c7aba-111">COM+ will not attempt to commit a transaction while an object within a synchronization boundary is in call.</span></span> <span data-ttu-id="c7aba-112">Além disso, os objetos podem indicar sua consistência usando [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit).</span><span class="sxs-lookup"><span data-stu-id="c7aba-112">Also, objects can indicate their consistency using [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit).</span></span> <span data-ttu-id="c7aba-113">Se for feita uma tentativa de confirmar uma transação que inclui o trabalho de um objeto chamado **DisableCommit**, a transação será anulada.</span><span class="sxs-lookup"><span data-stu-id="c7aba-113">If an attempt is made to commit a transaction which includes the work of an object that has called **DisableCommit**, the transaction will abort.</span></span>

 

 



