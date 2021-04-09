---
description: Tarefas de transações COM+
ms.assetid: fe4374f1-2452-4316-be57-b866c438404d
title: Tarefas de transações COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70aaebd3e788e1ff12e86b7831979f055367fea7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089373"
---
# <a name="com-transactions-tasks"></a><span data-ttu-id="3175e-103">Tarefas de transações COM+</span><span class="sxs-lookup"><span data-stu-id="3175e-103">COM+ Transactions Tasks</span></span>

<span data-ttu-id="3175e-104">Embora o processamento automático de transações no COM+ permita que você gaste um tempo de desenvolvimento mais produtivo na criação e configuração de objetos que você deseja participar de transações automáticas, há algumas tarefas de programação que você pode executar para personalizar o comportamento da transação para os requisitos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3175e-104">While automatic transaction processing in COM+ allows you to spend more productive development time in creating and configuring objects that you want to participate in automatic transactions, there are some programming tasks you can perform to tailor transaction behavior to your application requirements.</span></span>

<span data-ttu-id="3175e-105">Os tópicos a seguir discutem opções de programação específicas relacionadas ao processamento de transações.</span><span class="sxs-lookup"><span data-stu-id="3175e-105">The following topics discuss specific programming options related to transaction processing.</span></span>



| <span data-ttu-id="3175e-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="3175e-106">Topic</span></span>                                                                                             | <span data-ttu-id="3175e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3175e-107">Description</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3175e-108">Configurando o atributo de transação</span><span class="sxs-lookup"><span data-stu-id="3175e-108">Setting the Transaction Attribute</span></span>](setting-the-transaction-attribute.md)<br/>             | <span data-ttu-id="3175e-109">Descreve como definir valores de atributo de transação para seus objetos de transação.</span><span class="sxs-lookup"><span data-stu-id="3175e-109">Describes how to set transaction attribute values for your transaction objects.</span></span><br/>         |
| [<span data-ttu-id="3175e-110">Configurar o nível de isolamento da transação</span><span class="sxs-lookup"><span data-stu-id="3175e-110">Setting the Transaction Isolation Level</span></span>](setting-the-transaction-isolation-level.md)<br/> | <span data-ttu-id="3175e-111">Descreve como definir os níveis de isolamento da transação para seus objetos de transação.</span><span class="sxs-lookup"><span data-stu-id="3175e-111">Describes how to set the transaction isolation levels for your transaction objects.</span></span><br/>     |
| [<span data-ttu-id="3175e-112">Definindo o tempo limite da transação</span><span class="sxs-lookup"><span data-stu-id="3175e-112">Setting the Transaction Time-Out</span></span>](setting-the-transaction-time-out.md)<br/>               | <span data-ttu-id="3175e-113">Descreve como definir intervalos de tempo limite para suas transações.</span><span class="sxs-lookup"><span data-stu-id="3175e-113">Describes how to set time-out intervals for your transactions.</span></span><br/>                          |
| [<span data-ttu-id="3175e-114">Definindo os sinalizadores consistentes e concluídos</span><span class="sxs-lookup"><span data-stu-id="3175e-114">Setting the Consistent and Done Flags</span></span>](setting-the-consistent-and-done-flags.md)<br/>     | <span data-ttu-id="3175e-115">Mostra como usar os sinalizadores consistentes e concluídos para controlar o resultado de uma transação.</span><span class="sxs-lookup"><span data-stu-id="3175e-115">Shows how to use the consistent and done flags to control the outcome of a transaction.</span></span><br/> |
| [<span data-ttu-id="3175e-116">Criando objetos BYOT</span><span class="sxs-lookup"><span data-stu-id="3175e-116">Creating BYOT Objects</span></span>](creating-byot-objects.md)<br/>                                     | <span data-ttu-id="3175e-117">Descreve como criar objetos para que você possa trazer sua própria transação (BYOT).</span><span class="sxs-lookup"><span data-stu-id="3175e-117">Describes how to create objects so you can Bring Your Own Transaction (BYOT).</span></span><br/>           |



 

> [!Note]  
> <span data-ttu-id="3175e-118">Como regra geral, qualquer componente que atualize o estado persistente deve dar suporte a transações.</span><span class="sxs-lookup"><span data-stu-id="3175e-118">As a general rule, any component that updates persistent state should support transactions.</span></span> <span data-ttu-id="3175e-119">Os componentes que combinam as operações de dois ou mais objetos em uma única tarefa devem usar transações para simplificar a recuperação de erros.</span><span class="sxs-lookup"><span data-stu-id="3175e-119">Components that combine the operations of two or more objects into a single task should use transactions to simplify error recovery.</span></span> <span data-ttu-id="3175e-120">Além disso, para liberar recursos, como conexões de banco de dados, as transações em COM+ devem ser tão curtas quanto você pode fazer.</span><span class="sxs-lookup"><span data-stu-id="3175e-120">Also, to release resources, such as database connections, transactions in COM+ should be as short as you can make them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3175e-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3175e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3175e-122">Conceitos de transações COM+</span><span class="sxs-lookup"><span data-stu-id="3175e-122">COM+ Transactions Concepts</span></span>](com--transactions-concepts.md)
</dt> </dl>

 

 




