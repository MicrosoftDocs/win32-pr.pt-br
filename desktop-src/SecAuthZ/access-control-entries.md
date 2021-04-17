---
description: Uma ACE (entrada de controle de acesso) é um elemento em uma ACL (lista de controle de acesso).
ms.assetid: 9cf4d796-3955-456b-9db9-ae9fa83752f6
title: Entradas de controle de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fe98cf1c1c4d5fb23091a6539564ff964202cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811301"
---
# <a name="access-control-entries"></a><span data-ttu-id="f6110-103">Entradas de controle de acesso</span><span class="sxs-lookup"><span data-stu-id="f6110-103">Access Control Entries</span></span>

<span data-ttu-id="f6110-104">Uma ACE ( [*entrada de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) é um elemento em uma ACL (lista de controle de [*acesso*](/windows/desktop/SecGloss/a-gly) ).</span><span class="sxs-lookup"><span data-stu-id="f6110-104">An [*access control entry*](/windows/desktop/SecGloss/a-gly) (ACE) is an element in an [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL).</span></span> <span data-ttu-id="f6110-105">Uma ACL pode ter zero ou mais ACEs.</span><span class="sxs-lookup"><span data-stu-id="f6110-105">An ACL can have zero or more ACEs.</span></span> <span data-ttu-id="f6110-106">Cada ACE controla ou monitora o acesso a um objeto por uma confiança especificada.</span><span class="sxs-lookup"><span data-stu-id="f6110-106">Each ACE controls or monitors access to an object by a specified trustee.</span></span> <span data-ttu-id="f6110-107">Para obter informações sobre como adicionar, remover ou alterar as ACEs nas ACLs de um objeto, consulte [modificando as ACLs de um objeto em C++](modifying-the-acls-of-an-object-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="f6110-107">For information about adding, removing, or changing the ACEs in an object's ACLs, see [Modifying the ACLs of an Object in C++](modifying-the-acls-of-an-object-in-c--.md).</span></span>

<span data-ttu-id="f6110-108">Há seis tipos de ACEs, três dos quais há suporte para todos os objetos protegíveis.</span><span class="sxs-lookup"><span data-stu-id="f6110-108">There are six types of ACEs, three of which are supported by all securable objects.</span></span> <span data-ttu-id="f6110-109">Os outros três tipos são [ACEs específicas de objeto](object-specific-aces.md) com suporte dos objetos de serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="f6110-109">The other three types are [Object-specific ACEs](object-specific-aces.md) supported by directory service objects.</span></span>

<span data-ttu-id="f6110-110">Todos os tipos de ACEs contêm as seguintes informações de controle de acesso:</span><span class="sxs-lookup"><span data-stu-id="f6110-110">All types of ACEs contain the following access control information:</span></span>

-   <span data-ttu-id="f6110-111">Um SID ( [identificador de segurança](security-identifiers.md) ) que identifica o [confiável](trustees.md) ao qual a Ace se aplica.</span><span class="sxs-lookup"><span data-stu-id="f6110-111">A [security identifier](security-identifiers.md) (SID) that identifies the [trustee](trustees.md) to which the ACE applies.</span></span>
-   <span data-ttu-id="f6110-112">Uma [*máscara de acesso*](/windows/desktop/SecGloss/a-gly) que especifica os [direitos de acesso](access-rights-and-access-masks.md) controlados pela Ace.</span><span class="sxs-lookup"><span data-stu-id="f6110-112">An [*access mask*](/windows/desktop/SecGloss/a-gly) that specifies the [access rights](access-rights-and-access-masks.md) controlled by the ACE.</span></span>
-   <span data-ttu-id="f6110-113">Um sinalizador que indica o tipo de ACE.</span><span class="sxs-lookup"><span data-stu-id="f6110-113">A flag that indicates the type of ACE.</span></span>
-   <span data-ttu-id="f6110-114">Um conjunto de sinalizadores de bits que determinam se os contêineres ou objetos filho podem herdar a ACE do objeto primário ao qual a ACL está anexada.</span><span class="sxs-lookup"><span data-stu-id="f6110-114">A set of bit flags that determine whether child containers or objects can inherit the ACE from the primary object to which the ACL is attached.</span></span>

<span data-ttu-id="f6110-115">A tabela a seguir lista os três tipos de ACE com suporte de todos os objetos protegíveis.</span><span class="sxs-lookup"><span data-stu-id="f6110-115">The following table lists the three ACE types supported by all securable objects.</span></span>



| <span data-ttu-id="f6110-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6110-116">Type</span></span>               | <span data-ttu-id="f6110-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6110-117">Description</span></span>                                                                                                                                                                                                                                      |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6110-118">ACE com acesso negado</span><span class="sxs-lookup"><span data-stu-id="f6110-118">Access-denied ACE</span></span>  | <span data-ttu-id="f6110-119">Usado em uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) para negar direitos de acesso a um confiável.</span><span class="sxs-lookup"><span data-stu-id="f6110-119">Used in a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) to deny access rights to a trustee.</span></span>                                       |
| <span data-ttu-id="f6110-120">ACE permitida pelo acesso</span><span class="sxs-lookup"><span data-stu-id="f6110-120">Access-allowed ACE</span></span> | <span data-ttu-id="f6110-121">Usado em uma DACL para permitir direitos de acesso a um confiável.</span><span class="sxs-lookup"><span data-stu-id="f6110-121">Used in a DACL to allow access rights to a trustee.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="f6110-122">ACE de auditoria do sistema</span><span class="sxs-lookup"><span data-stu-id="f6110-122">System-audit ACE</span></span>   | <span data-ttu-id="f6110-123">Usado em uma SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema para gerar um registro de auditoria quando o confiável tenta exercitar os direitos de acesso especificados.</span><span class="sxs-lookup"><span data-stu-id="f6110-123">Used in a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL) to generate an audit record when the trustee attempts to exercise the specified access rights.</span></span> |



 

<span data-ttu-id="f6110-124">Para obter uma tabela de ACEs específicas de objeto, consulte [ACEs específicas de objeto](object-specific-aces.md).</span><span class="sxs-lookup"><span data-stu-id="f6110-124">For a table of object-specific ACEs, see [Object-specific ACEs](object-specific-aces.md).</span></span>

> [!Note]  
> <span data-ttu-id="f6110-125">No momento, não há suporte para ACEs de objeto de alarme do sistema.</span><span class="sxs-lookup"><span data-stu-id="f6110-125">System-alarm object ACEs are not currently supported.</span></span>

 

 

 
