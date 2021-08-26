---
description: AcEs específicas do objeto têm suporte para objetos DS (serviço de diretório). Uma ACE específica a um objeto contém um par de GUIDs que expandem as maneiras pelas quais a ACE pode proteger um objeto.
ms.assetid: 37d353c0-ac22-430f-b5f3-15deb69be24b
title: ACEs específicas do objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4212a0f7fe4eff7e38b41fe2636643c457cfeb51
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469573"
---
# <a name="object-specific-aces"></a>ACEs específicas do objeto

AcEs específicas [*do objeto*](/windows/desktop/SecGloss/a-gly) têm suporte para objetos DS (serviço de diretório). Uma ACE específica a um objeto contém um par de GUIDs que expandem as maneiras pelas quais a ACE pode proteger um objeto.




| GUID | Descrição | 
|------|-------------|
| <strong>ObjectType</strong> | Identifica um dos seguintes:<ul><li>Um tipo de objeto filho. A ACE controla o direito de criar um tipo especificado de objeto filho. Para obter mais informações, consulte <a href="controlling-child-object-creation-in-c--.md">Controlando a criação de objeto filho em C++.</a></li><li>Um conjunto de propriedades ou propriedade. A ACE controla o direito de ler ou gravar a propriedade ou o conjunto de propriedades. Para obter mais informações, <a href="aces-to-control-access-to-an-object-s-properties.md">consulte ACEs para controlar o acesso às propriedades de um objeto</a>.</li><li>Um direito estendido. A ACE controla o direito de executar a operação associada ao direito estendido.</li><li>Uma gravação validada. A ACE controla o direito de executar determinadas operações de gravação. Essas permissões de gravação validadas, definidas e expostas no Editor de ACL, fornecem permissões para gravações validadas de propriedades em vez de gravações de baixo nível desmarcadas de qualquer valor em uma propriedade que é concedida com uma permissão de "propriedade de gravação".</li></ul> | 
| <strong>Inheritedobjecttype</strong> | Indica o tipo de objeto filho que pode herdar a ACE. A herança também é controlada pelos sinalizadores de herança <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>no ACE_HEADER</strong></a>, bem como por qualquer proteção contra herança colocada nos objetos filho. Para obter mais informações, consulte <a href="ace-inheritance.md">Herança ace</a>. | 




 

Há suporte para três tipos de ACEs específicas do objeto.

> [!Note]  
> Atualmente, não há suporte para ACEs de objeto de alarme do sistema.

 



| Type                      | Descrição                                                                                                                                                                                                                                       |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACE do objeto de acesso negado  | Usado em uma DACL para negar acesso de um objeto de confiança a uma propriedade ou propriedade definida no objeto ou para limitar a herança ACE a um tipo especificado de objeto filho. Usa a [**estrutura ACCESS \_ DENIED OBJECT \_ \_ ACE.**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace)         |
| ACE do objeto permitido para acesso | Usado em uma DACL para permitir que um objeto de confiança acesse uma propriedade ou propriedade definida no objeto ou para limitar a herança ACE a um tipo especificado de objeto filho. Usa a [**estrutura ACCESS ALLOWED OBJECT \_ \_ \_ ACE.**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace)      |
| ACE do objeto de auditoria do sistema   | Usado em uma SACL para registrar as tentativas de um objeto de confiança de acessar uma propriedade ou propriedade definida no objeto ou para limitar a herança ACE a um tipo especificado de objeto filho. Usa a [**estrutura SYSTEM AUDIT OBJECT \_ \_ \_ ACE.**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) |



 

Qualquer ACL que contenha uma ACE específica a um objeto deve usar a revisão ACL \_ REVISION \_ DS.

 

 
