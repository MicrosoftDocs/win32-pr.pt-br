---
description: Consulte o banco de dados do cartão inteligente. Eles podem fornecer uma lista de cartões inteligentes fornecidos por um usuário específico, as interfaces e o provedor de serviços primário de um cartão específico, os grupos de leitores definidos para o sistema e os leitores em um conjunto de grupos de leitores.
ms.assetid: a30cbb99-522c-4752-bfcd-75be608785f1
title: Funções de consulta de banco de dados de cartão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd74c15eb475d5de9ccce84ba5936b724c0d8d82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170946"
---
# <a name="smart-card-database-query-functions"></a><span data-ttu-id="e60b8-104">Funções de consulta de banco de dados de cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="e60b8-104">Smart Card Database Query Functions</span></span>

<span data-ttu-id="e60b8-105">As funções a seguir consultam o [*banco de dados do cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e60b8-105">The following functions query the [*smart card database*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="e60b8-106">Eles podem fornecer uma lista de cartões inteligentes fornecidos por um usuário específico, as interfaces e o [*provedor de serviços primário*](../secgloss/p-gly.md) de um cartão específico, os [*grupos de leitores*](../secgloss/r-gly.md) definidos para o sistema e os [*leitores*](../secgloss/r-gly.md) em um conjunto de grupos de leitores.</span><span class="sxs-lookup"><span data-stu-id="e60b8-106">They can provide a list of smart cards supplied by a specific user, the interfaces and [*primary service provider*](../secgloss/p-gly.md) of a specific card, the [*reader groups*](../secgloss/r-gly.md) defined for the system, and the [*readers*](../secgloss/r-gly.md) within a set of reader groups.</span></span>

<span data-ttu-id="e60b8-107">Ao usar essas funções, você pode consultar o banco de dados completo do cartão inteligente ou pode restringir a pesquisa definindo o [*contexto do Gerenciador de recursos*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e60b8-107">When you use these functions, you can query the complete smart card database, or you can narrow the search by setting the [*resource manager context*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="e60b8-108">O contexto do Gerenciador de recursos é definido chamando [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) antes de chamar uma função de consulta.</span><span class="sxs-lookup"><span data-stu-id="e60b8-108">The resource manager context is set by calling [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) before calling a query function.</span></span>

> [!Note]  
> <span data-ttu-id="e60b8-109">Sem um contexto especificado, algumas informações ainda podem estar inacessíveis devido a restrições de segurança.</span><span class="sxs-lookup"><span data-stu-id="e60b8-109">Without a specified context, some information may still be inaccessible due to security restrictions.</span></span>

 



| <span data-ttu-id="e60b8-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="e60b8-110">Topic</span></span>                                                  | <span data-ttu-id="e60b8-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="e60b8-111">Description</span></span>                                                                                                                                                                          |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e60b8-112">**SCardGetProviderId**</span><span class="sxs-lookup"><span data-stu-id="e60b8-112">**SCardGetProviderId**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardgetproviderida)       | <span data-ttu-id="e60b8-113">Recupere o identificador (GUID) do [*provedor de serviços primário*](../secgloss/p-gly.md) para o cartão fornecido.</span><span class="sxs-lookup"><span data-stu-id="e60b8-113">Retrieve the identifier (GUID) of the [*primary service provider*](../secgloss/p-gly.md) for the given card.</span></span> |
| [<span data-ttu-id="e60b8-114">**SCardListCards**</span><span class="sxs-lookup"><span data-stu-id="e60b8-114">**SCardListCards**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistcardsa)               | <span data-ttu-id="e60b8-115">Recupere uma lista de cartões introduzidos anteriormente no sistema por um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="e60b8-115">Retrieve a list of cards previously introduced to the system by a specific user.</span></span>                                                                                                     |
| [<span data-ttu-id="e60b8-116">**SCardListInterfaces**</span><span class="sxs-lookup"><span data-stu-id="e60b8-116">**SCardListInterfaces**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistinterfacesa)     | <span data-ttu-id="e60b8-117">Recupere os identificadores (GUIDs) das interfaces fornecidas por um determinado cartão.</span><span class="sxs-lookup"><span data-stu-id="e60b8-117">Retrieve the identifiers (GUIDs) of the interfaces supplied by a given card.</span></span>                                                                                                         |
| [<span data-ttu-id="e60b8-118">**SCardListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="e60b8-118">**SCardListReaderGroups**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistreadergroupsa) | <span data-ttu-id="e60b8-119">Recupere uma lista de grupos de leitores que foram introduzidos anteriormente no sistema.</span><span class="sxs-lookup"><span data-stu-id="e60b8-119">Retrieve a list of reader groups that have previously been introduced to the system.</span></span>                                                                                                 |
| [<span data-ttu-id="e60b8-120">**SCardListReaders**</span><span class="sxs-lookup"><span data-stu-id="e60b8-120">**SCardListReaders**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistreadersa)           | <span data-ttu-id="e60b8-121">Recupere a lista de leitores em um conjunto de grupos de leitores nomeados.</span><span class="sxs-lookup"><span data-stu-id="e60b8-121">Retrieve the list of readers within a set of named reader groups.</span></span>                                                                                                                    |



 

 

 
