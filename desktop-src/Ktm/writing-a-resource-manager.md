---
description: Se você estiver escrevendo um serviço ou componente e precisar usar serviços transacionais ou se precisar monitorar o estado de uma transação de kernel, você precisará criar um RM (Gerenciador de recursos).
ms.assetid: 9b62ef58-9897-4573-bda4-8c3ec952b6d2
title: Escrevendo um Gerenciador de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c47f9a0704f6edaea02d752fe39f01fce61c0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758456"
---
# <a name="writing-a-resource-manager"></a><span data-ttu-id="a62d4-103">Escrevendo um Gerenciador de recursos</span><span class="sxs-lookup"><span data-stu-id="a62d4-103">Writing a Resource Manager</span></span>

<span data-ttu-id="a62d4-104">Se você estiver escrevendo um serviço ou componente e precisar usar serviços transacionais ou se precisar monitorar o estado de uma transação de kernel, você precisará criar um RM (Gerenciador de recursos).</span><span class="sxs-lookup"><span data-stu-id="a62d4-104">If you are writing a service or component and need to use transactional services or if you need to monitor the state of a kernel transaction, you need to create a resource manager (RM).</span></span>

<span data-ttu-id="a62d4-105">Para escrever um Gerenciador de recursos, você deve criar vários objetos kernel.</span><span class="sxs-lookup"><span data-stu-id="a62d4-105">To write a resource manager, you must create multiple kernel objects.</span></span> <span data-ttu-id="a62d4-106">Os objetos que um RM usa são:</span><span class="sxs-lookup"><span data-stu-id="a62d4-106">The objects that an RM uses are:</span></span>

-   <span data-ttu-id="a62d4-107">Objetos do Gerenciador de transações (TM)</span><span class="sxs-lookup"><span data-stu-id="a62d4-107">Transaction Manager (TM) objects</span></span>
-   <span data-ttu-id="a62d4-108">Objetos do Resource Manager</span><span class="sxs-lookup"><span data-stu-id="a62d4-108">Resource Manager objects</span></span>
-   <span data-ttu-id="a62d4-109">Objetos de inscrição</span><span class="sxs-lookup"><span data-stu-id="a62d4-109">Enlistment objects</span></span>

<span data-ttu-id="a62d4-110">Primeiro, crie um objeto TM.</span><span class="sxs-lookup"><span data-stu-id="a62d4-110">First, create a TM object.</span></span> <span data-ttu-id="a62d4-111">Há dois tipos de TMs:</span><span class="sxs-lookup"><span data-stu-id="a62d4-111">There are two types of TMs:</span></span>

-   <span data-ttu-id="a62d4-112">Volátil – esses TMs não têm um log e não podem recuperar seu estado</span><span class="sxs-lookup"><span data-stu-id="a62d4-112">Volatile – these TMs do not have a log and cannot recover their state</span></span>
-   <span data-ttu-id="a62d4-113">Durável – esses TMs têm um log</span><span class="sxs-lookup"><span data-stu-id="a62d4-113">Durable – these TMs have a log</span></span>

<span data-ttu-id="a62d4-114">Para criar um TM durável, você deve criar um log do CLFS e chamar [**Createtransactionmanager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) ou fazer com que o KTM o crie para você.</span><span class="sxs-lookup"><span data-stu-id="a62d4-114">To create a durable TM, you must either create a CLFS log and call [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) or have KTM create it for you.</span></span> <span data-ttu-id="a62d4-115">Depois que um TM durável é criado, você deve primeiro recuperar o TM chamando [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager).</span><span class="sxs-lookup"><span data-stu-id="a62d4-115">After a durable TM is created, you must first recover the TM by calling [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager).</span></span> <span data-ttu-id="a62d4-116">Depois que o TM for recuperado, ele estará disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="a62d4-116">After the TM is recovered, it is available for use.</span></span>

<span data-ttu-id="a62d4-117">Se você recuperou um TM existente, todo o RMs associado a este TM começará a receber mensagens de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a62d4-117">If you recovered an existing TM, all RMs associated with this TM will start receiving recovery messages.</span></span> <span data-ttu-id="a62d4-118">Para obter mais informações, consulte [processamento de recuperação](recovery-processing.md).</span><span class="sxs-lookup"><span data-stu-id="a62d4-118">For more information, see [Recovery Processing](recovery-processing.md).</span></span>

<span data-ttu-id="a62d4-119">Em seguida, você cria um Gerenciador de recursos chamando [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) com o identificador TM.</span><span class="sxs-lookup"><span data-stu-id="a62d4-119">Next, you create a resource manager by calling [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) with the TM handle.</span></span> <span data-ttu-id="a62d4-120">O RM pode ser volátil ou durável.</span><span class="sxs-lookup"><span data-stu-id="a62d4-120">The RM can be volatile or durable.</span></span> <span data-ttu-id="a62d4-121">Somente TMs duráveis podem ser usados com RMs durável.</span><span class="sxs-lookup"><span data-stu-id="a62d4-121">Only durable TMs can be used with durable RMs.</span></span>

<span data-ttu-id="a62d4-122">Ao trabalhar de forma transacional, você se inscreve na transação chamando [**Createalistaing**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)e especificando quais notificações receber.</span><span class="sxs-lookup"><span data-stu-id="a62d4-122">When working transactionally, you enlist in the transaction by calling [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)and specifying which notifications to receive.</span></span>

<span data-ttu-id="a62d4-123">**Observação**  Você pode começar a receber notificações antes que a chamada para [**createinscrita**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment) seja concluída.</span><span class="sxs-lookup"><span data-stu-id="a62d4-123">**Note**  You can start receiving notifications before the call to [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment) is completed.</span></span>

<span data-ttu-id="a62d4-124">Quando você receber uma notificação, chame a função "concluída \* " apropriada quando qualquer trabalho associado ao processamento da notificação for concluído.</span><span class="sxs-lookup"><span data-stu-id="a62d4-124">When you receive a notification, call the appropriate "Complete\*" function when any work associated with processing the notification is completed.</span></span> <span data-ttu-id="a62d4-125">As funções completas são:</span><span class="sxs-lookup"><span data-stu-id="a62d4-125">The complete functions are:</span></span>

-   [<span data-ttu-id="a62d4-126">**CommitComplete**</span><span class="sxs-lookup"><span data-stu-id="a62d4-126">**CommitComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [<span data-ttu-id="a62d4-127">**PrepareComplete**</span><span class="sxs-lookup"><span data-stu-id="a62d4-127">**PrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [<span data-ttu-id="a62d4-128">**PreprepareComplete**</span><span class="sxs-lookup"><span data-stu-id="a62d4-128">**PreprepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)

<span data-ttu-id="a62d4-129">Se, a qualquer momento, um Gerenciador de recursos não puder concluir o trabalho da transação, ou se continuar renderizando seu aplicativo para não conseguir desfazer o trabalho feito dentro da transação, você deverá reverter a transação chamando [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).</span><span class="sxs-lookup"><span data-stu-id="a62d4-129">If at any time a resource manager is unable to complete the work of the transaction, or if continuing would render your application unable to undo the work done within the transaction, you must roll back the transaction by calling [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).</span></span>

 

 



