---
description: A API da AuthZ permite que os aplicativos executem verificações de acesso personalizáveis com melhor desempenho e desenvolvimento mais simplificado do que o controle de acesso de baixo nível.
ms.assetid: 83df96ff-f3d6-43f8-88b2-6387914b3503
title: Usando a API AuthZ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86394c0df408307ae4c49377af4a1ae8cc1f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297590"
---
# <a name="using-authz-api"></a><span data-ttu-id="5fb7f-103">Usando a API AuthZ</span><span class="sxs-lookup"><span data-stu-id="5fb7f-103">Using Authz API</span></span>

<span data-ttu-id="5fb7f-104">A API da AuthZ permite que os aplicativos executem verificações de acesso personalizáveis com melhor desempenho e desenvolvimento mais simplificado do que o [controle de acesso de baixo nível](low-level-access-control.md).</span><span class="sxs-lookup"><span data-stu-id="5fb7f-104">Authz API allows applications to perform customizable access checks with better performance and more simplified development than [Low-level Access Control](low-level-access-control.md).</span></span>

<span data-ttu-id="5fb7f-105">A API da AuthZ permite que os aplicativos armazenem em cache as verificações de desempenho para obter um aumento de performance, consultar e modificar contextos do cliente e definir regras de negócio que possam ser usadas para avaliar a permissão de acesso dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="5fb7f-105">Authz API allows applications to cache access checks for improved performance, to query and modify client contexts, and to define business rules that can be used to evaluate access permission dynamically.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5fb7f-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="5fb7f-106">In This Section</span></span>



| <span data-ttu-id="5fb7f-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="5fb7f-107">Topic</span></span>                                                                             | <span data-ttu-id="5fb7f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5fb7f-108">Description</span></span>                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5fb7f-109">Inicializando um contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="5fb7f-109">Initializing a Client Context</span></span>](initializing-a-client-context.md)<br/>     | <span data-ttu-id="5fb7f-110">Um aplicativo deve criar um contexto de cliente antes de poder usar a API AuthZ para executar verificações de acesso ou auditoria.</span><span class="sxs-lookup"><span data-stu-id="5fb7f-110">An application must create a client context before it can use Authz API to perform access checks or auditing.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="5fb7f-111">Consultando um contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="5fb7f-111">Querying a Client Context</span></span>](querying-a-client-context.md)<br/>             | <span data-ttu-id="5fb7f-112">Os aplicativos podem chamar a função [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) para consultar informações sobre um contexto de cliente existente.</span><span class="sxs-lookup"><span data-stu-id="5fb7f-112">Applications can call the [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) function to query information about an existing client context.</span></span><br/>                                                                                       |
| [<span data-ttu-id="5fb7f-113">Adicionando SIDs a um contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="5fb7f-113">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)<br/> | <span data-ttu-id="5fb7f-114">Um aplicativo pode adicionar SIDs ( [*identificadores de segurança*](/windows/desktop/SecGloss/s-gly) ) a um contexto de cliente existente chamando a função [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) .</span><span class="sxs-lookup"><span data-stu-id="5fb7f-114">An application can add [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) to an existing client context by calling the [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) function.</span></span><br/> |
| [<span data-ttu-id="5fb7f-115">Verificando o acesso com a API AuthZ</span><span class="sxs-lookup"><span data-stu-id="5fb7f-115">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)<br/>   | <span data-ttu-id="5fb7f-116">Os aplicativos determinam se devem ser concedidos acesso a objetos protegíveis chamando a função [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="5fb7f-116">Applications determine whether to grant access to securable objects by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="5fb7f-117">Cache de verificações de acesso</span><span class="sxs-lookup"><span data-stu-id="5fb7f-117">Caching Access Checks</span></span>](caching-access-checks.md)<br/>                     | <span data-ttu-id="5fb7f-118">Quando um aplicativo executa uma verificação de acesso chamando a função [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) , os resultados dessa verificação de acesso podem ser armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="5fb7f-118">When an application performs an access check by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function, the results of that access check can be cached.</span></span><br/>                                                                                       |



 

 

