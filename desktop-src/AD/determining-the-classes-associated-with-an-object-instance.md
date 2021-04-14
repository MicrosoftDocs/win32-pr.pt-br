---
title: Determinando as classes associadas a uma instância de objeto
description: Cada objeto no Active Directory Domain Services tem dois atributos cujos valores identificam a hierarquia de classes de objeto da qual o objeto é uma instância.
ms.assetid: bb46f165-8c6e-4af1-b387-e0e30a4c6226
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67bc3fe900170e4a856d996f7e373918f242df2e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453518"
---
# <a name="determining-the-classes-associated-with-an-object-instance"></a><span data-ttu-id="f26c1-103">Determinando as classes associadas a uma instância de objeto</span><span class="sxs-lookup"><span data-stu-id="f26c1-103">Determining the Classes Associated With an Object Instance</span></span>

<span data-ttu-id="f26c1-104">Cada objeto no Active Directory Domain Services tem dois atributos cujos valores identificam a hierarquia de classes de objeto da qual o objeto é uma instância.</span><span class="sxs-lookup"><span data-stu-id="f26c1-104">Every object in Active Directory Domain Services has two attributes whose values identify the hierarchy of object classes of which the object is an instance.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f26c1-105">Atributo</span><span class="sxs-lookup"><span data-stu-id="f26c1-105">Attribute</span></span></th>
<th><span data-ttu-id="f26c1-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f26c1-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f26c1-107"><strong>structuralObjectClass</strong></span><span class="sxs-lookup"><span data-stu-id="f26c1-107"><strong>structuralObjectClass</strong></span></span></td>
<td><span data-ttu-id="f26c1-108">Identifica as classes estruturais e abstratas das quais o objeto é uma instância.</span><span class="sxs-lookup"><span data-stu-id="f26c1-108">Identifies the structural and abstract classes of which the object is an instance.</span></span> <span data-ttu-id="f26c1-109">Por exemplo, os valores de um objeto de usuário podem ser:</span><span class="sxs-lookup"><span data-stu-id="f26c1-109">For example, the values for a user object can be:</span></span>
<ul>
<li><span data-ttu-id="f26c1-110"><strong>início</strong></span><span class="sxs-lookup"><span data-stu-id="f26c1-110"><strong>top</strong></span></span></li>
<li><span data-ttu-id="f26c1-111"><strong>person</strong></span><span class="sxs-lookup"><span data-stu-id="f26c1-111"><strong>person</strong></span></span></li>
<li><span data-ttu-id="f26c1-112"><strong>organizationalPerson</strong></span><span class="sxs-lookup"><span data-stu-id="f26c1-112"><strong>organizationalPerson</strong></span></span></li>
<li><span data-ttu-id="f26c1-113"><strong>user</strong></span><span class="sxs-lookup"><span data-stu-id="f26c1-113"><strong>user</strong></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f26c1-114"><strong>objectClass</strong></span><span class="sxs-lookup"><span data-stu-id="f26c1-114"><strong>objectClass</strong></span></span></td>
<td><span data-ttu-id="f26c1-115">Identifica as classes incluídas no <strong>structuralObjectClass</strong>, além de todas as classes auxiliares que são conectadas dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="f26c1-115">Identifies the classes included in <strong>structuralObjectClass</strong>, plus any auxiliary classes that are dynamically attached.</span></span> <span data-ttu-id="f26c1-116">Por exemplo, se uma &quot; &quot; classe auxiliar de veículo for anexada a um objeto de usuário, os valores poderão ser:</span><span class="sxs-lookup"><span data-stu-id="f26c1-116">For example, if a &quot;vehicle&quot; auxiliary class is attached to a user object, the values can be:</span></span>
<ul>
<li><span data-ttu-id="f26c1-117"><strong>início</strong></span><span class="sxs-lookup"><span data-stu-id="f26c1-117"><strong>top</strong></span></span></li>
<li><span data-ttu-id="f26c1-118"><strong>veículo</strong></span><span class="sxs-lookup"><span data-stu-id="f26c1-118"><strong>vehicle</strong></span></span></li>
<li><span data-ttu-id="f26c1-119"><strong>person</strong></span><span class="sxs-lookup"><span data-stu-id="f26c1-119"><strong>person</strong></span></span></li>
<li><span data-ttu-id="f26c1-120"><strong>organizationalPerson</strong></span><span class="sxs-lookup"><span data-stu-id="f26c1-120"><strong>organizationalPerson</strong></span></span></li>
<li><span data-ttu-id="f26c1-121"><strong>user</strong></span><span class="sxs-lookup"><span data-stu-id="f26c1-121"><strong>user</strong></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f26c1-122">Lembre-se de que nenhum desses atributos inclui classes auxiliares que são vinculadas estaticamente com as classes de objeto das quais o objeto é uma instância.</span><span class="sxs-lookup"><span data-stu-id="f26c1-122">Be aware that neither of these attributes include auxiliary classes that are statically linked with the object classes of which the object is an instance.</span></span> <span data-ttu-id="f26c1-123">Por exemplo, a classe auxiliar **SecurityPrincipal** é estaticamente vinculada à classe **User** porque está incluída nos valores **systemAuxiliaryClass** do objeto **classSchema** do usuário; Ele não está incluído nos atributos **objectClass** ou **structuralObjectClass** das instâncias da classe User.</span><span class="sxs-lookup"><span data-stu-id="f26c1-123">For example, the **securityPrincipal** auxiliary class is statically linked with the **user** class because it is included in the **systemAuxiliaryClass** values of the user **classSchema** object; it is not included in either the **objectClass** or **structuralObjectClass** attributes of instances of the user class.</span></span>

 

 




