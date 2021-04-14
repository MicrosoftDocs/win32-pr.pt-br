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
# <a name="determining-the-classes-associated-with-an-object-instance"></a>Determinando as classes associadas a uma instância de objeto

Cada objeto no Active Directory Domain Services tem dois atributos cujos valores identificam a hierarquia de classes de objeto da qual o objeto é uma instância.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>structuralObjectClass</strong></td>
<td>Identifica as classes estruturais e abstratas das quais o objeto é uma instância. Por exemplo, os valores de um objeto de usuário podem ser:
<ul>
<li><strong>início</strong></li>
<li><strong>person</strong></li>
<li><strong>organizationalPerson</strong></li>
<li><strong>user</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>objectClass</strong></td>
<td>Identifica as classes incluídas no <strong>structuralObjectClass</strong>, além de todas as classes auxiliares que são conectadas dinamicamente. Por exemplo, se uma &quot; &quot; classe auxiliar de veículo for anexada a um objeto de usuário, os valores poderão ser:
<ul>
<li><strong>início</strong></li>
<li><strong>veículo</strong></li>
<li><strong>person</strong></li>
<li><strong>organizationalPerson</strong></li>
<li><strong>user</strong></li>
</ul></td>
</tr>
</tbody>
</table>



 

Lembre-se de que nenhum desses atributos inclui classes auxiliares que são vinculadas estaticamente com as classes de objeto das quais o objeto é uma instância. Por exemplo, a classe auxiliar **SecurityPrincipal** é estaticamente vinculada à classe **User** porque está incluída nos valores **systemAuxiliaryClass** do objeto **classSchema** do usuário; Ele não está incluído nos atributos **objectClass** ou **structuralObjectClass** das instâncias da classe User.

 

 




