---
description: O Coordenador de Transações Distribuídas (DTC) permite transações distribuídas ou transações que estão sob o controle de vários gerenciadores de recursos em um ou mais sistemas. O KTM e o DTC trabalham juntos para fazer isso.
ms.assetid: 468379e2-c5f6-479f-9d5d-42afb395ec9b
title: Interoperabilidade com outros recursos do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa3aeac3d920b408a9a18c32eab83cf747525e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780131"
---
# <a name="interoperability-with-other-windows-features"></a><span data-ttu-id="5c55e-104">Interoperabilidade com outros recursos do Windows</span><span class="sxs-lookup"><span data-stu-id="5c55e-104">Interoperability With Other Windows Features</span></span>

<span data-ttu-id="5c55e-105">O [Coordenador de transações distribuídas](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) permite *transações distribuídas* ou transações que estão sob o controle de vários gerenciadores de recursos em um ou mais sistemas.</span><span class="sxs-lookup"><span data-stu-id="5c55e-105">The [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) enables *distributed transactions*, or transactions that are under the control of multiple resource managers on one or more systems.</span></span> <span data-ttu-id="5c55e-106">O KTM e o DTC trabalham juntos para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="5c55e-106">KTM and DTC work closely together to accomplish this.</span></span>

<span data-ttu-id="5c55e-107">O COM+ expõe um modelo declarativo para programação transacional.</span><span class="sxs-lookup"><span data-stu-id="5c55e-107">COM+ exposes a declarative model for transactional programming.</span></span> <span data-ttu-id="5c55e-108">Em outras palavras, o programador declara a extensão até a qual um objeto pode tirar proveito das transações, e o tempo de execução do COM+ gerencia as transações em nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="5c55e-108">In other words, the programmer declares the extent to which an object can take advantage of transactions, and the COM+ runtime manages the transactions on the object's behalf.</span></span> <span data-ttu-id="5c55e-109">Por exemplo, um objeto pode ser declarado para participar de uma transação somente se já existir uma, para exigir uma transação (uma é criada se ela ainda não existir), para exigir uma nova transação (uma é criada independentemente de se já existir) ou não é transacional.</span><span class="sxs-lookup"><span data-stu-id="5c55e-109">For example, an object can be declared to participate in a transaction only if one already exists, to require a transaction (one is created if it does not already exist), to require a new transaction (one is created regardless of whether one already exists), or is not transactional.</span></span> <span data-ttu-id="5c55e-110">Essas transações gerenciadas declarativamente são usadas automaticamente em conexões de banco de dados criadas por objetos COM+ que estão sendo executados no contexto de uma transação.</span><span class="sxs-lookup"><span data-stu-id="5c55e-110">These declaratively-managed transactions are automatically used on database connections created by COM+ objects that are executing in the context of a transaction.</span></span>

 

 
