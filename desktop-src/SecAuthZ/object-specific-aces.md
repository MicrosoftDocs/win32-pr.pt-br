---
description: As ACEs específicas do objeto têm suporte para objetos do serviço de diretório (DS). Uma ACE específica de objeto contém um par de GUIDs que expandem as maneiras pelas quais a ACE pode proteger um objeto.
ms.assetid: 37d353c0-ac22-430f-b5f3-15deb69be24b
title: ACEs específicas do objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40760e5cd06af97e93f74c6ff8daff89cd5962f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011367"
---
# <a name="object-specific-aces"></a><span data-ttu-id="a48f0-104">ACEs específicas do objeto</span><span class="sxs-lookup"><span data-stu-id="a48f0-104">Object-specific ACEs</span></span>

<span data-ttu-id="a48f0-105">As [*ACEs*](/windows/desktop/SecGloss/a-gly) específicas do objeto têm suporte para objetos do serviço de diretório (DS).</span><span class="sxs-lookup"><span data-stu-id="a48f0-105">Object-specific [*ACEs*](/windows/desktop/SecGloss/a-gly) are supported for directory service (DS) objects.</span></span> <span data-ttu-id="a48f0-106">Uma ACE específica de objeto contém um par de GUIDs que expandem as maneiras pelas quais a ACE pode proteger um objeto.</span><span class="sxs-lookup"><span data-stu-id="a48f0-106">An object-specific ACE contains a pair of GUIDs that expand the ways in which the ACE can protect an object.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a48f0-107">GUID</span><span class="sxs-lookup"><span data-stu-id="a48f0-107">GUID</span></span></th>
<th><span data-ttu-id="a48f0-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a48f0-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a48f0-109"><strong>ObjectType</strong></span><span class="sxs-lookup"><span data-stu-id="a48f0-109"><strong>ObjectType</strong></span></span></td>
<td><span data-ttu-id="a48f0-110">Identifica um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="a48f0-110">Identifies one of the following:</span></span>
<ul>
<li><span data-ttu-id="a48f0-111">Um tipo de objeto filho.</span><span class="sxs-lookup"><span data-stu-id="a48f0-111">A type of child object.</span></span> <span data-ttu-id="a48f0-112">A ACE controla o direito de criar um tipo especificado de objeto filho.</span><span class="sxs-lookup"><span data-stu-id="a48f0-112">The ACE controls the right to create a specified type of child object.</span></span> <span data-ttu-id="a48f0-113">Para obter mais informações, consulte <a href="controlling-child-object-creation-in-c--.md">controlando a criação de objetos filho em C++</a>.</span><span class="sxs-lookup"><span data-stu-id="a48f0-113">For more information, see <a href="controlling-child-object-creation-in-c--.md">Controlling Child Object Creation in C++</a>.</span></span></li>
<li><span data-ttu-id="a48f0-114">Um conjunto de propriedades ou propriedade.</span><span class="sxs-lookup"><span data-stu-id="a48f0-114">A property set or property.</span></span> <span data-ttu-id="a48f0-115">A ACE controla o direito de ler ou gravar a propriedade ou o conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="a48f0-115">The ACE controls the right to read or write the property or property set.</span></span> <span data-ttu-id="a48f0-116">Para obter mais informações, consulte <a href="aces-to-control-access-to-an-object-s-properties.md">ACEs para controlar o acesso às propriedades de um objeto</a>.</span><span class="sxs-lookup"><span data-stu-id="a48f0-116">For more information, see <a href="aces-to-control-access-to-an-object-s-properties.md">ACEs to Control Access to an Object's Properties</a>.</span></span></li>
<li><span data-ttu-id="a48f0-117">Um direito estendido.</span><span class="sxs-lookup"><span data-stu-id="a48f0-117">An extended right.</span></span> <span data-ttu-id="a48f0-118">A ACE controla o direito de executar a operação associada ao direito estendido.</span><span class="sxs-lookup"><span data-stu-id="a48f0-118">The ACE controls the right to perform the operation associated with the extended right.</span></span></li>
<li><span data-ttu-id="a48f0-119">Uma gravação validada.</span><span class="sxs-lookup"><span data-stu-id="a48f0-119">A validated write.</span></span> <span data-ttu-id="a48f0-120">A ACE controla o direito de executar determinadas operações de gravação.</span><span class="sxs-lookup"><span data-stu-id="a48f0-120">The ACE controls the right to perform certain write operations.</span></span> <span data-ttu-id="a48f0-121">Essas permissões de gravação validadas, definidas e expostas no editor de ACL, fornecem permissões para gravações validadas de propriedades em vez de gravações de baixo nível desmarcadas de qualquer valor para uma propriedade que é concedida com uma &quot; permissão de propriedade de gravação &quot; .</span><span class="sxs-lookup"><span data-stu-id="a48f0-121">These validated write permissions, defined and exposed in the ACL Editor, provide permissions for validated writes of properties rather than unchecked low-level writes of any value to a property that is granted with a &quot;write property&quot; permission.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a48f0-122"><strong>InheritedObjectType</strong></span><span class="sxs-lookup"><span data-stu-id="a48f0-122"><strong>InheritedObjectType</strong></span></span></td>
<td><span data-ttu-id="a48f0-123">Indica o tipo de objeto filho que pode herdar a ACE.</span><span class="sxs-lookup"><span data-stu-id="a48f0-123">Indicates the type of child object that can inherit the ACE.</span></span> <span data-ttu-id="a48f0-124">A herança também é controlada pelos sinalizadores de herança no <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>ACE_HEADER</strong></a>, bem como por qualquer proteção contra herança colocada nos objetos filho.</span><span class="sxs-lookup"><span data-stu-id="a48f0-124">Inheritance is also controlled by the inheritance flags in the <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>ACE_HEADER</strong></a>, as well as by any protection against inheritance placed on the child objects.</span></span> <span data-ttu-id="a48f0-125">Para obter mais informações, consulte <a href="ace-inheritance.md">Ace Inheritance</a>.</span><span class="sxs-lookup"><span data-stu-id="a48f0-125">For more information, see <a href="ace-inheritance.md">ACE Inheritance</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a48f0-126">Há suporte para três tipos de ACEs específicas de objeto.</span><span class="sxs-lookup"><span data-stu-id="a48f0-126">Three types of object-specific ACEs are supported.</span></span>

> [!Note]  
> <span data-ttu-id="a48f0-127">No momento, não há suporte para ACEs de objeto de alarme do sistema.</span><span class="sxs-lookup"><span data-stu-id="a48f0-127">System-alarm object ACEs are not currently supported.</span></span>

 



| <span data-ttu-id="a48f0-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="a48f0-128">Type</span></span>                      | <span data-ttu-id="a48f0-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="a48f0-129">Description</span></span>                                                                                                                                                                                                                                       |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a48f0-130">ACE de objeto negado pelo acesso</span><span class="sxs-lookup"><span data-stu-id="a48f0-130">Access-denied object ACE</span></span>  | <span data-ttu-id="a48f0-131">Usado em uma DACL para negar um acesso de confiança a uma propriedade ou propriedade definida no objeto ou para limitar a herança de ACE a um tipo especificado de objeto filho.</span><span class="sxs-lookup"><span data-stu-id="a48f0-131">Used in a DACL to deny a trustee access to a property or property set on the object, or to limit ACE inheritance to a specified type of child object.</span></span> <span data-ttu-id="a48f0-132">Usa a estrutura [**ACE de objeto de acesso \_ negado \_ \_**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace) .</span><span class="sxs-lookup"><span data-stu-id="a48f0-132">Uses the [**ACCESS\_DENIED\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace) structure.</span></span>         |
| <span data-ttu-id="a48f0-133">ACE de objeto permitido pelo Access</span><span class="sxs-lookup"><span data-stu-id="a48f0-133">Access-allowed object ACE</span></span> | <span data-ttu-id="a48f0-134">Usado em uma DACL para permitir o acesso de confiança a uma propriedade ou propriedade definida no objeto ou para limitar a herança de ACE a um tipo especificado de objeto filho.</span><span class="sxs-lookup"><span data-stu-id="a48f0-134">Used in a DACL to allow a trustee access to a property or property set on the object, or to limit ACE inheritance to a specified type of child object.</span></span> <span data-ttu-id="a48f0-135">Usa a [**estrutura \_ \_ \_ ACE de objeto permitido de acesso**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace) .</span><span class="sxs-lookup"><span data-stu-id="a48f0-135">Uses the [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace) structure.</span></span>      |
| <span data-ttu-id="a48f0-136">ACE de objeto de auditoria do sistema</span><span class="sxs-lookup"><span data-stu-id="a48f0-136">System-audit object ACE</span></span>   | <span data-ttu-id="a48f0-137">Usado em uma SACL para registrar as tentativas de um objeto de confiança de ter acesso a uma propriedade ou propriedade definida no objetos, ou para limitar a herança de ACE a um tipo especificado de objeto filho.</span><span class="sxs-lookup"><span data-stu-id="a48f0-137">Used in a SACL to log a trustee's attempts to access a property or property set on the object, or to limit ACE inheritance to a specified type of child object.</span></span> <span data-ttu-id="a48f0-138">Usa a [**estrutura \_ \_ \_ Ace do objeto de auditoria do sistema**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) .</span><span class="sxs-lookup"><span data-stu-id="a48f0-138">Uses the [**SYSTEM\_AUDIT\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) structure.</span></span> |



 

<span data-ttu-id="a48f0-139">Qualquer ACL que contenha uma ACE específica de objeto deve usar a revisão de ACL de revisão \_ \_ DS.</span><span class="sxs-lookup"><span data-stu-id="a48f0-139">Any ACL that contains an object-specific ACE must use the revision ACL\_REVISION\_DS.</span></span>

 

 
