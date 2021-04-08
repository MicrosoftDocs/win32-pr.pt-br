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
# <a name="object-specific-aces"></a>ACEs específicas do objeto

As [*ACEs*](/windows/desktop/SecGloss/a-gly) específicas do objeto têm suporte para objetos do serviço de diretório (DS). Uma ACE específica de objeto contém um par de GUIDs que expandem as maneiras pelas quais a ACE pode proteger um objeto.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>ObjectType</strong></td>
<td>Identifica um dos seguintes:
<ul>
<li>Um tipo de objeto filho. A ACE controla o direito de criar um tipo especificado de objeto filho. Para obter mais informações, consulte <a href="controlling-child-object-creation-in-c--.md">controlando a criação de objetos filho em C++</a>.</li>
<li>Um conjunto de propriedades ou propriedade. A ACE controla o direito de ler ou gravar a propriedade ou o conjunto de propriedades. Para obter mais informações, consulte <a href="aces-to-control-access-to-an-object-s-properties.md">ACEs para controlar o acesso às propriedades de um objeto</a>.</li>
<li>Um direito estendido. A ACE controla o direito de executar a operação associada ao direito estendido.</li>
<li>Uma gravação validada. A ACE controla o direito de executar determinadas operações de gravação. Essas permissões de gravação validadas, definidas e expostas no editor de ACL, fornecem permissões para gravações validadas de propriedades em vez de gravações de baixo nível desmarcadas de qualquer valor para uma propriedade que é concedida com uma &quot; permissão de propriedade de gravação &quot; .</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>InheritedObjectType</strong></td>
<td>Indica o tipo de objeto filho que pode herdar a ACE. A herança também é controlada pelos sinalizadores de herança no <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>ACE_HEADER</strong></a>, bem como por qualquer proteção contra herança colocada nos objetos filho. Para obter mais informações, consulte <a href="ace-inheritance.md">Ace Inheritance</a>.</td>
</tr>
</tbody>
</table>



 

Há suporte para três tipos de ACEs específicas de objeto.

> [!Note]  
> No momento, não há suporte para ACEs de objeto de alarme do sistema.

 



| Tipo                      | Descrição                                                                                                                                                                                                                                       |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACE de objeto negado pelo acesso  | Usado em uma DACL para negar um acesso de confiança a uma propriedade ou propriedade definida no objeto ou para limitar a herança de ACE a um tipo especificado de objeto filho. Usa a estrutura [**ACE de objeto de acesso \_ negado \_ \_**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace) .         |
| ACE de objeto permitido pelo Access | Usado em uma DACL para permitir o acesso de confiança a uma propriedade ou propriedade definida no objeto ou para limitar a herança de ACE a um tipo especificado de objeto filho. Usa a [**estrutura \_ \_ \_ ACE de objeto permitido de acesso**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace) .      |
| ACE de objeto de auditoria do sistema   | Usado em uma SACL para registrar as tentativas de um objeto de confiança de ter acesso a uma propriedade ou propriedade definida no objetos, ou para limitar a herança de ACE a um tipo especificado de objeto filho. Usa a [**estrutura \_ \_ \_ Ace do objeto de auditoria do sistema**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) . |



 

Qualquer ACL que contenha uma ACE específica de objeto deve usar a revisão de ACL de revisão \_ \_ DS.

 

 
