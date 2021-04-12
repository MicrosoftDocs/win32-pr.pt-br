---
description: Sinalizadores consistentes e concluídos
ms.assetid: a641fa95-5587-4362-9869-e5c27c6dd2ce
title: Sinalizadores consistentes e concluídos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a61d1f715d06e6bfb6632b9bbb59276074c4d7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501130"
---
# <a name="consistent-and-done-flags"></a><span data-ttu-id="ffde7-103">Sinalizadores consistentes e concluídos</span><span class="sxs-lookup"><span data-stu-id="ffde7-103">Consistent and Done Flags</span></span>

<span data-ttu-id="ffde7-104">O COM+ sempre cria um objeto de contexto antes de ativar um objeto transacional.</span><span class="sxs-lookup"><span data-stu-id="ffde7-104">COM+ always creates a context object before activating a transactional object.</span></span> <span data-ttu-id="ffde7-105">O objeto de contexto contém informações relacionadas a objeto, como seu criador e seu identificador de transação.</span><span class="sxs-lookup"><span data-stu-id="ffde7-105">The context object holds object-related information, such as its creator and its transaction identifier.</span></span> <span data-ttu-id="ffde7-106">Cada objeto de contexto também contém um *sinalizador consistente* e um *sinalizador Done*.</span><span class="sxs-lookup"><span data-stu-id="ffde7-106">Each context object also contains a *consistent flag* and a *done flag*.</span></span> <span data-ttu-id="ffde7-107">Juntos, esses sinalizadores determinam o status do objeto transacional.</span><span class="sxs-lookup"><span data-stu-id="ffde7-107">Together these flags determine the status of the transactional object.</span></span>

<span data-ttu-id="ffde7-108">O sinalizador consistente indica que o objeto transacional é consistente ou inconsistente.</span><span class="sxs-lookup"><span data-stu-id="ffde7-108">The consistent flag indicates that the transactional object is either consistent or inconsistent.</span></span> <span data-ttu-id="ffde7-109">Os detalhes específicos do que tornam o estado do objeto consistente é o programador.</span><span class="sxs-lookup"><span data-stu-id="ffde7-109">The specific details of what makes an object's state consistent is up to the programmer.</span></span> <span data-ttu-id="ffde7-110">Quando uma chamada de método define esse sinalizador como true, o objeto é consistente.</span><span class="sxs-lookup"><span data-stu-id="ffde7-110">When a method call sets this flag to True, the object is consistent.</span></span> <span data-ttu-id="ffde7-111">False indica que o objeto está inconsistente.</span><span class="sxs-lookup"><span data-stu-id="ffde7-111">False indicates that the object is inconsistent.</span></span> <span data-ttu-id="ffde7-112">COM+ define o sinalizador como true quando ele cria uma instância de objeto.</span><span class="sxs-lookup"><span data-stu-id="ffde7-112">COM+ sets the flag to True when it creates an object instance.</span></span> <span data-ttu-id="ffde7-113">Um objeto consistente está pronto para prosseguir com a transação.</span><span class="sxs-lookup"><span data-stu-id="ffde7-113">A consistent object is ready to proceed with the transaction.</span></span> <span data-ttu-id="ffde7-114">Enquanto um objeto permanece ativo, as chamadas de método subsequentes podem alternar repetidamente o sinalizador consistente de verdadeiro para falso e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="ffde7-114">While an object remains active, subsequent method calls can repeatedly switch the consistent flag from True to False and vice versa.</span></span>

<span data-ttu-id="ffde7-115">O sinalizador Done determina a duração de uma transação.</span><span class="sxs-lookup"><span data-stu-id="ffde7-115">The done flag determines the duration of a transaction.</span></span> <span data-ttu-id="ffde7-116">Quando uma chamada de método retorna, o COM+ inspeciona o sinalizador done.</span><span class="sxs-lookup"><span data-stu-id="ffde7-116">When a method call returns, COM+ inspects the done flag.</span></span> <span data-ttu-id="ffde7-117">Se o método definir esse sinalizador como true, o COM+ desativará o objeto e notará o sinalizador consistente.</span><span class="sxs-lookup"><span data-stu-id="ffde7-117">If the method sets this flag to True, COM+ deactivates the object and notes the consistent flag.</span></span> <span data-ttu-id="ffde7-118">Quando o sinalizador Done é false, COM+ não desativa o objeto nem anota o sinalizador consistente.</span><span class="sxs-lookup"><span data-stu-id="ffde7-118">When the done flag is False, COM+ neither deactivates the object nor notes the consistent flag.</span></span> <span data-ttu-id="ffde7-119">COM+ define o sinalizador Done como false quando ele cria uma instância de objeto.</span><span class="sxs-lookup"><span data-stu-id="ffde7-119">COM+ sets the done flag to False when it creates an object instance.</span></span>

<span data-ttu-id="ffde7-120">O sinalizador consistente converte um voto para confirmar ou anular a transação na qual ele é executado, e o sinalizador concluído finaliza o voto.</span><span class="sxs-lookup"><span data-stu-id="ffde7-120">The consistent flag casts a vote to commit or abort the transaction in which it executes, and the done flag finalizes the vote.</span></span> <span data-ttu-id="ffde7-121">O COM+ inspeciona o sinalizador consistente quando o sinalizador Done é definido como true em um retorno de chamada de método ou quando o objeto é desativado.</span><span class="sxs-lookup"><span data-stu-id="ffde7-121">COM+ inspects the consistent flag when the done flag is set to True on a method call return or when the object deactivates.</span></span> <span data-ttu-id="ffde7-122">Embora o sinalizador consistente de um objeto possa ser alterado repetidamente dentro de cada chamada de método, somente as últimas contagens de alteração.</span><span class="sxs-lookup"><span data-stu-id="ffde7-122">Although an object's consistent flag can change repeatedly within each method call, only the last change counts.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffde7-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ffde7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffde7-124">Gerenciando transações automáticas no COM+</span><span class="sxs-lookup"><span data-stu-id="ffde7-124">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> <dt>

[<span data-ttu-id="ffde7-125">Definindo os sinalizadores consistentes e concluídos</span><span class="sxs-lookup"><span data-stu-id="ffde7-125">Setting the Consistent and Done Flags</span></span>](setting-the-consistent-and-done-flags.md)
</dt> </dl>

 

 



