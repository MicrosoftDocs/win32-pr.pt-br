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
# <a name="access-control-entries"></a>Entradas de controle de acesso

Uma ACE ( [*entrada de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) é um elemento em uma ACL (lista de controle de [*acesso*](/windows/desktop/SecGloss/a-gly) ). Uma ACL pode ter zero ou mais ACEs. Cada ACE controla ou monitora o acesso a um objeto por uma confiança especificada. Para obter informações sobre como adicionar, remover ou alterar as ACEs nas ACLs de um objeto, consulte [modificando as ACLs de um objeto em C++](modifying-the-acls-of-an-object-in-c--.md).

Há seis tipos de ACEs, três dos quais há suporte para todos os objetos protegíveis. Os outros três tipos são [ACEs específicas de objeto](object-specific-aces.md) com suporte dos objetos de serviço de diretório.

Todos os tipos de ACEs contêm as seguintes informações de controle de acesso:

-   Um SID ( [identificador de segurança](security-identifiers.md) ) que identifica o [confiável](trustees.md) ao qual a Ace se aplica.
-   Uma [*máscara de acesso*](/windows/desktop/SecGloss/a-gly) que especifica os [direitos de acesso](access-rights-and-access-masks.md) controlados pela Ace.
-   Um sinalizador que indica o tipo de ACE.
-   Um conjunto de sinalizadores de bits que determinam se os contêineres ou objetos filho podem herdar a ACE do objeto primário ao qual a ACL está anexada.

A tabela a seguir lista os três tipos de ACE com suporte de todos os objetos protegíveis.



| Tipo               | Descrição                                                                                                                                                                                                                                      |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACE com acesso negado  | Usado em uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) para negar direitos de acesso a um confiável.                                       |
| ACE permitida pelo acesso | Usado em uma DACL para permitir direitos de acesso a um confiável.                                                                                                                                                                                              |
| ACE de auditoria do sistema   | Usado em uma SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema para gerar um registro de auditoria quando o confiável tenta exercitar os direitos de acesso especificados. |



 

Para obter uma tabela de ACEs específicas de objeto, consulte [ACEs específicas de objeto](object-specific-aces.md).

> [!Note]  
> No momento, não há suporte para ACEs de objeto de alarme do sistema.

 

 

 
