---
description: O Gerenciador de Autorização oferece uma estrutura flexível para a integração entre o controle de acesso com base na função e os aplicativos Isso permite aos administradores que usam esses aplicativos fornecer acesso por meio de funções atribuídas de usuário relativas a funções de trabalho.
ms.assetid: c6d37b2e-b149-43e2-8155-cb2f669e421c
title: Modelo do Gerenciador de autorização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3455c9577f24b260bd02f947d0af99ec85570bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297771"
---
# <a name="authorization-manager-model"></a><span data-ttu-id="42ed1-104">Modelo do Gerenciador de autorização</span><span class="sxs-lookup"><span data-stu-id="42ed1-104">Authorization Manager Model</span></span>

<span data-ttu-id="42ed1-105">O Gerenciador de Autorização oferece uma estrutura flexível para a integração entre o controle de acesso com base na função e os aplicativos</span><span class="sxs-lookup"><span data-stu-id="42ed1-105">Authorization Manager provides a flexible framework for integrating role-based access control into applications.</span></span> <span data-ttu-id="42ed1-106">Isso permite aos administradores que usam esses aplicativos fornecer acesso por meio de funções atribuídas de usuário relativas a funções de trabalho.</span><span class="sxs-lookup"><span data-stu-id="42ed1-106">It enables administrators who use those applications to provide access through assigned user roles that relate to job functions.</span></span>

<span data-ttu-id="42ed1-107">Os aplicativos do Gerenciador de autorização armazenam a política de autorização na forma de armazenamentos de autorização armazenados em arquivos Active Directory ou XML e aplicam a política de autorização em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="42ed1-107">Authorization Manager applications store authorization policy in the form of authorization stores that are stored in Active Directory or XML files and apply authorization policy at run time.</span></span>

<span data-ttu-id="42ed1-108">Em seguida, os aplicativos chamam um método de verificação de acesso em tempo de execução que verifica o acesso às informações de política no repositório de autorização.</span><span class="sxs-lookup"><span data-stu-id="42ed1-108">Applications then call a run-time access check method that checks access against the policy information in the authorization store.</span></span>

<span data-ttu-id="42ed1-109">A política de autorização inclui as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="42ed1-109">Authorization policy includes the following parts:</span></span>

-   [<span data-ttu-id="42ed1-110">Repositórios de política, aplicativos e escopos</span><span class="sxs-lookup"><span data-stu-id="42ed1-110">Policy Stores, Applications, and Scopes</span></span>](policy-stores--applications--and-scopes.md)
-   [<span data-ttu-id="42ed1-111">Usuários e grupos</span><span class="sxs-lookup"><span data-stu-id="42ed1-111">Users and Groups</span></span>](users-and-groups.md)
-   [<span data-ttu-id="42ed1-112">Operações e tarefas</span><span class="sxs-lookup"><span data-stu-id="42ed1-112">Operations and Tasks</span></span>](operations-and-tasks.md)
-   [<span data-ttu-id="42ed1-113">Funções</span><span class="sxs-lookup"><span data-stu-id="42ed1-113">Roles</span></span>](roles.md)
-   [<span data-ttu-id="42ed1-114">Regras de negócios</span><span class="sxs-lookup"><span data-stu-id="42ed1-114">Business Rules</span></span>](business-rules.md)
-   [<span data-ttu-id="42ed1-115">Coleções</span><span class="sxs-lookup"><span data-stu-id="42ed1-115">Collections</span></span>](collections.md)

 

 



