---
description: Transações COM+
ms.assetid: 40eccce1-a362-4adc-8060-f6923b9162c9
title: Transações COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef51f4c8ed5e37101f64d36af385c93ac7e69ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370457"
---
# <a name="com-transactions"></a><span data-ttu-id="9dece-103">Transações COM+</span><span class="sxs-lookup"><span data-stu-id="9dece-103">COM+ Transactions</span></span>

<span data-ttu-id="9dece-104">Ao comprar um livro de uma livraria online, você usa um cartão de crédito para comercializar dinheiro para um livro.</span><span class="sxs-lookup"><span data-stu-id="9dece-104">When you purchase a book from an online bookstore, you use a credit card to trade money for a book.</span></span> <span data-ttu-id="9dece-105">Depois de enviar seu pedido, uma série de operações relacionadas (validação do seu cartão de crédito, verificação da disponibilidade do inventário e assim por diante) garante que você obtenha o livro e que a livraridade receba seu dinheiro.</span><span class="sxs-lookup"><span data-stu-id="9dece-105">After you submit your order, a series of related operations (validation of your credit card, verification of inventory availability, and so forth) ensures that you get the book and that the bookstore gets your money.</span></span> <span data-ttu-id="9dece-106">Se uma única operação na série falhar durante a troca, todo o Exchange falhará.</span><span class="sxs-lookup"><span data-stu-id="9dece-106">If a single operation in the series fails during the exchange, the entire exchange fails.</span></span> <span data-ttu-id="9dece-107">Você não obtém o livro, e a livraria não recebe seu dinheiro.</span><span class="sxs-lookup"><span data-stu-id="9dece-107">You do not get the book, and the bookstore does not get your money.</span></span>

<span data-ttu-id="9dece-108">A tecnologia responsável por tornar essa troca online balanceada e previsível é chamada de *processamento de transações*.</span><span class="sxs-lookup"><span data-stu-id="9dece-108">The technology responsible for making this online exchange balanced and predictable is called *transaction processing*.</span></span> <span data-ttu-id="9dece-109">Programaticamente, uma *transação* é uma unidade de trabalho na qual ocorrem uma série de operações.</span><span class="sxs-lookup"><span data-stu-id="9dece-109">Programmatically, a *transaction* is a unit of work in which a series of operations occur.</span></span> <span data-ttu-id="9dece-110">O COM+ usa transações programáticas para garantir que os recursos não sejam permanentemente atualizados, a menos que todas as operações na transação sejam concluídas com êxito.</span><span class="sxs-lookup"><span data-stu-id="9dece-110">COM+ uses programmatic transactions to ensure that resources are not permanently updated unless all operations within the transaction complete successfully.</span></span> <span data-ttu-id="9dece-111">Ao associar um conjunto de operações relacionadas em uma transação COM+ que seja completamente bem-sucedida ou completamente malsucedida, você pode simplificar muito a recuperação de erros.</span><span class="sxs-lookup"><span data-stu-id="9dece-111">By binding a set of related operations together in a COM+ transaction that either completely succeeds or completely fails, you can vastly simplify error recovery.</span></span>

<span data-ttu-id="9dece-112">Os tópicos a seguir apresentam teoria geral de processamento de transações, fornecem uma análise mais detalhada das transações no COM+ e apresentam dicas práticas para escrever componentes transacionais.</span><span class="sxs-lookup"><span data-stu-id="9dece-112">The following topics introduce general transaction processing theory, provide a closer look at transactions in COM+, and present practical tips for writing transactional components.</span></span>



| <span data-ttu-id="9dece-113">Tópico</span><span class="sxs-lookup"><span data-stu-id="9dece-113">Topic</span></span>                                                                   | <span data-ttu-id="9dece-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="9dece-114">Description</span></span>                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="9dece-115">Conceitos de transações COM+</span><span class="sxs-lookup"><span data-stu-id="9dece-115">COM+ Transactions Concepts</span></span>](com--transactions-concepts.md)<br/> | <span data-ttu-id="9dece-116">Apresenta os termos e conceitos básicos.</span><span class="sxs-lookup"><span data-stu-id="9dece-116">Presents basic terms and concepts.</span></span><br/>                                  |
| [<span data-ttu-id="9dece-117">Tarefas de transações COM+</span><span class="sxs-lookup"><span data-stu-id="9dece-117">COM+ Transactions Tasks</span></span>](com--transactions-tasks.md)<br/>       | <span data-ttu-id="9dece-118">Fornece informações práticas sobre como escrever componentes transacionais.</span><span class="sxs-lookup"><span data-stu-id="9dece-118">Provides practical information on writing transactional components.</span></span><br/> |



 

 

 




