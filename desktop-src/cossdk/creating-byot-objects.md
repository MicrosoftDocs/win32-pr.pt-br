---
description: Criando objetos BYOT
ms.assetid: 16b68ce2-46b2-4e35-bf92-f132dcb354e3
title: Criando objetos BYOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544c5085061be5d1100706930a3e1617ec24890
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784583"
---
# <a name="creating-byot-objects"></a><span data-ttu-id="bdc3b-103">Criando objetos BYOT</span><span class="sxs-lookup"><span data-stu-id="bdc3b-103">Creating BYOT Objects</span></span>

<span data-ttu-id="bdc3b-104">Um novo objeto BYOT cria objetos com transações manuais.</span><span class="sxs-lookup"><span data-stu-id="bdc3b-104">A new BYOT object creates objects with manual transactions.</span></span> <span data-ttu-id="bdc3b-105">As duas interfaces, [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) e [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex), têm um único método, **CreateInstance**, que assumem um ponteiro de interface **ITransaction** e uma URL Tip, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="bdc3b-105">The two interfaces, [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) and [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex), have a single method, **CreateInstance**, which take an **ITransaction** interface pointer and TIP URL, respectively.</span></span> <span data-ttu-id="bdc3b-106">[**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) retorna um ponteiro de interface para o objeto recém-criado, que é inscrito na transação especificada.</span><span class="sxs-lookup"><span data-stu-id="bdc3b-106">[**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) returns an interface pointer to the newly created object, which is enlisted within the specified transaction.</span></span>

<span data-ttu-id="bdc3b-107">Quando um objeto com uma transação manual é liberado, o COM+ não tenta confirmar a transação.</span><span class="sxs-lookup"><span data-stu-id="bdc3b-107">When an object with a manual transaction is released, COM+ does not attempt to commit the transaction.</span></span> <span data-ttu-id="bdc3b-108">A transação é controlada explicitamente pelo Gerenciador de transações externas que dispensava a transação sob a qual esse objeto foi criado.</span><span class="sxs-lookup"><span data-stu-id="bdc3b-108">The transaction is controlled explicitly by the external transaction manager that dispensed the transaction under which this object had been created.</span></span>

> [!Note]  
> <span data-ttu-id="bdc3b-109">O objeto BYOT. ByotServerEx precisa ser importado para um aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="bdc3b-109">The Byot.ByotServerEx object needs to be imported into a COM+ application.</span></span>

 

 

 



