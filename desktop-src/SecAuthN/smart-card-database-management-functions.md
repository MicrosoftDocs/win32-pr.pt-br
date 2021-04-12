---
description: Gerencie o banco de dados do cartão inteligente, atualizando o banco de dados usando um contexto do Gerenciador de recursos especificado.
ms.assetid: a2f457e1-c042-42e7-9071-cf0edd68e27a
title: Funções de gerenciamento de banco de dados de cartão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c424494a30c71e15647da773027311ed53a2599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297110"
---
# <a name="smart-card-database-management-functions"></a><span data-ttu-id="5ea50-103">Funções de gerenciamento de banco de dados de cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="5ea50-103">Smart Card Database Management Functions</span></span>

<span data-ttu-id="5ea50-104">As funções a seguir gerenciam o [*banco de dados do cartão inteligente*](../secgloss/s-gly.md), atualizando o banco de dados usando um [*contexto do Gerenciador de recursos*](../secgloss/r-gly.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="5ea50-104">The following functions manage the [*smart card database*](../secgloss/s-gly.md), updating the database by using a specified [*resource manager context*](../secgloss/r-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="5ea50-105">A segurança do banco de dados é mantida colocando restrições de acesso no banco de dados, em vez de adicionar mecanismos de segurança ao [*subsistema de cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5ea50-105">Database security is maintained by placing access restrictions on the database, rather than by adding security mechanisms to the [*smart card subsystem*](../secgloss/s-gly.md).</span></span>

 



| <span data-ttu-id="5ea50-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="5ea50-106">Topic</span></span>                                                            | <span data-ttu-id="5ea50-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ea50-107">Description</span></span>                                                                                                                                                             |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ea50-108">**SCardAddReaderToGroup**</span><span class="sxs-lookup"><span data-stu-id="5ea50-108">**SCardAddReaderToGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardaddreadertogroupa)           | <span data-ttu-id="5ea50-109">Adicione um [*leitor*](../secgloss/r-gly.md) a um [*grupo de leitores*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5ea50-109">Add a [*reader*](../secgloss/r-gly.md) to a [*reader group*](../secgloss/r-gly.md).</span></span> |
| [<span data-ttu-id="5ea50-110">**SCardForgetCardType**</span><span class="sxs-lookup"><span data-stu-id="5ea50-110">**SCardForgetCardType**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea)               | <span data-ttu-id="5ea50-111">Remova um cartão inteligente do sistema.</span><span class="sxs-lookup"><span data-stu-id="5ea50-111">Remove a smart card from the system.</span></span>                                                                                                                                    |
| [<span data-ttu-id="5ea50-112">**SCardForgetReader**</span><span class="sxs-lookup"><span data-stu-id="5ea50-112">**SCardForgetReader**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadera)                   | <span data-ttu-id="5ea50-113">Remova um leitor do sistema.</span><span class="sxs-lookup"><span data-stu-id="5ea50-113">Remove a reader from the system.</span></span>                                                                                                                                        |
| [<span data-ttu-id="5ea50-114">**SCardForgetReaderGroup**</span><span class="sxs-lookup"><span data-stu-id="5ea50-114">**SCardForgetReaderGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadergroupa)         | <span data-ttu-id="5ea50-115">Remova um grupo de leitores do sistema.</span><span class="sxs-lookup"><span data-stu-id="5ea50-115">Remove a reader group from the system.</span></span>                                                                                                                                  |
| [<span data-ttu-id="5ea50-116">**SCardIntroduceCardType**</span><span class="sxs-lookup"><span data-stu-id="5ea50-116">**SCardIntroduceCardType**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea)         | <span data-ttu-id="5ea50-117">Introduza um novo cartão para o sistema.</span><span class="sxs-lookup"><span data-stu-id="5ea50-117">Introduce a new card to the system.</span></span>                                                                                                                                     |
| [<span data-ttu-id="5ea50-118">**SCardIntroduceReader**</span><span class="sxs-lookup"><span data-stu-id="5ea50-118">**SCardIntroduceReader**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadera)             | <span data-ttu-id="5ea50-119">Introduza um novo leitor para o sistema.</span><span class="sxs-lookup"><span data-stu-id="5ea50-119">Introduce a new reader to the system.</span></span>                                                                                                                                   |
| [<span data-ttu-id="5ea50-120">**SCardIntroduceReaderGroup**</span><span class="sxs-lookup"><span data-stu-id="5ea50-120">**SCardIntroduceReaderGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadergroupa)   | <span data-ttu-id="5ea50-121">Introduza um novo grupo de leitores para o sistema.</span><span class="sxs-lookup"><span data-stu-id="5ea50-121">Introduce a new reader group to the system.</span></span>                                                                                                                             |
| [<span data-ttu-id="5ea50-122">**SCardRemoveReaderFromGroup**</span><span class="sxs-lookup"><span data-stu-id="5ea50-122">**SCardRemoveReaderFromGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardremovereaderfromgroupa) | <span data-ttu-id="5ea50-123">Remover um leitor de um grupo de leitores.</span><span class="sxs-lookup"><span data-stu-id="5ea50-123">Remove a reader from a reader group.</span></span>                                                                                                                                    |



 

 

 
