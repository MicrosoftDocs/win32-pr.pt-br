---
description: Quando um processo tenta acessar um objeto protegível, o sistema percorre as ACEs (entradas de controle de acesso) na DACL (lista de controle de acesso discricional) dos objetos até encontrar as ACEs que permitem ou negam o acesso solicitado.
ms.assetid: fccf043e-e769-4f3f-b18c-252be20190d8
title: Ordem das ACEs em uma DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc45d6fd286bb06bd4311a8a02010c68832735ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769193"
---
# <a name="order-of-aces-in-a-dacl"></a><span data-ttu-id="88de1-103">Ordem das ACEs em uma DACL</span><span class="sxs-lookup"><span data-stu-id="88de1-103">Order of ACEs in a DACL</span></span>

<span data-ttu-id="88de1-104">Quando um [*processo*](/windows/desktop/SecGloss/p-gly) tenta acessar um objeto protegível, o sistema percorre as ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) na DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) do objeto até encontrar ACEs que permitam ou negue o acesso solicitado.</span><span class="sxs-lookup"><span data-stu-id="88de1-104">When a [*process*](/windows/desktop/SecGloss/p-gly) tries to access a securable object, the system steps through the [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) in the object's [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) until it finds ACEs that allow or deny the requested access.</span></span> <span data-ttu-id="88de1-105">Os direitos de acesso que uma DACL permite que um usuário variem dependendo da ordem das ACEs na DACL.</span><span class="sxs-lookup"><span data-stu-id="88de1-105">The access rights that a DACL allows a user could vary depending on the order of ACEs in the DACL.</span></span> <span data-ttu-id="88de1-106">Consequentemente, o sistema operacional Windows XP define uma ordem preferida para ACEs na DACL de um objeto protegível.</span><span class="sxs-lookup"><span data-stu-id="88de1-106">Consequently, the Windows XP operating system defines a preferred order for ACEs in the DACL of a securable object.</span></span> <span data-ttu-id="88de1-107">A ordem preferida fornece uma estrutura simples que garante que uma ACE de acesso negado realmente negue acesso.</span><span class="sxs-lookup"><span data-stu-id="88de1-107">The preferred order provides a simple framework that ensures that an access-denied ACE actually denies access.</span></span> <span data-ttu-id="88de1-108">Para obter mais informações sobre o algoritmo do sistema para verificar o acesso, consulte [como as DACLs controlam o acesso a um objeto](how-dacls-control-access-to-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="88de1-108">For more information about the system's algorithm for checking access, see [How DACLs Control Access to an Object](how-dacls-control-access-to-an-object.md).</span></span>

<span data-ttu-id="88de1-109">Para o Windows Server 2003 e o Windows XP, a ordem correta das ACEs é complicada pela introdução de ACEs específicas de objeto e herança automática.</span><span class="sxs-lookup"><span data-stu-id="88de1-109">For Windows Server 2003 and Windows XP, the proper order of ACEs is complicated by the introduction of object-specific ACEs and automatic inheritance.</span></span>

<span data-ttu-id="88de1-110">As etapas a seguir descrevem a ordem preferida:</span><span class="sxs-lookup"><span data-stu-id="88de1-110">The following steps describe the preferred order:</span></span>

1.  <span data-ttu-id="88de1-111">Todas as ACEs explícitas são colocadas em um grupo antes de quaisquer ACEs herdadas.</span><span class="sxs-lookup"><span data-stu-id="88de1-111">All explicit ACEs are placed in a group before any inherited ACEs.</span></span>
2.  <span data-ttu-id="88de1-112">Dentro do grupo de ACEs explícitas, ACEs com acesso negado são colocadas antes das ACEs permitidas pelo Access.</span><span class="sxs-lookup"><span data-stu-id="88de1-112">Within the group of explicit ACEs, access-denied ACEs are placed before access-allowed ACEs.</span></span>
3.  <span data-ttu-id="88de1-113">As ACEs herdadas são colocadas na ordem em que são herdadas.</span><span class="sxs-lookup"><span data-stu-id="88de1-113">Inherited ACEs are placed in the order in which they are inherited.</span></span> <span data-ttu-id="88de1-114">As ACEs herdadas do pai do objeto filho aparecem primeiro, então as ACEs herdadas do avô e assim por diante na árvore de objetos.</span><span class="sxs-lookup"><span data-stu-id="88de1-114">ACEs inherited from the child object's parent come first, then ACEs inherited from the grandparent, and so on up the tree of objects.</span></span>
4.  <span data-ttu-id="88de1-115">Para cada nível de ACEs herdadas, as ACEs de acesso negado são colocadas antes das ACEs permitidas pelo Access.</span><span class="sxs-lookup"><span data-stu-id="88de1-115">For each level of inherited ACEs, access-denied ACEs are placed before access-allowed ACEs.</span></span>

<span data-ttu-id="88de1-116">É claro que nem todos os tipos de ACE são necessários em uma ACL.</span><span class="sxs-lookup"><span data-stu-id="88de1-116">Of course, not all ACE types are required in an ACL.</span></span>

<span data-ttu-id="88de1-117">Funções como [**AddAccessAllowedAceEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) e [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) adicionam uma ACE ao final de uma ACL.</span><span class="sxs-lookup"><span data-stu-id="88de1-117">Functions such as [**AddAccessAllowedAceEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) and [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) add an ACE to the end of an ACL.</span></span> <span data-ttu-id="88de1-118">É responsabilidade do chamador garantir que as ACEs sejam adicionadas na ordem correta.</span><span class="sxs-lookup"><span data-stu-id="88de1-118">It is the caller's responsibility to ensure that the ACEs are added in the proper order.</span></span>

 

 
