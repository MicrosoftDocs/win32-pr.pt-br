---
description: Uma ACE (entrada de controle de acesso) é um elemento em uma ACL (lista de controle de acesso).
ms.assetid: 9cf4d796-3955-456b-9db9-ae9fa83752f6
title: Entradas de controle de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8adcc382da130c57c55b869c47c8837c7780a7cff4e6dbdd881e55aa7b724dc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785646"
---
# <a name="access-control-entries"></a>Entradas de controle de acesso

Uma [*ACE (entrada de controle*](/windows/desktop/SecGloss/a-gly) de acesso) é um elemento em uma ACL (lista de controle [*de*](/windows/desktop/SecGloss/a-gly) acesso). Uma ACL pode ter zero ou mais ACEs. Cada ACE controla ou monitora o acesso a um objeto por um objeto de confiança especificado. Para obter informações sobre como adicionar, remover ou alterar as ACEs nas ACLs de um objeto, consulte Modificando as ACLs de um objeto [em C++.](modifying-the-acls-of-an-object-in-c--.md)

Há seis tipos de ACEs, três dos quais são suportados por todos os objetos de segurança. Os outros três tipos são [ACEs específicas do objeto com](object-specific-aces.md) suporte pelos objetos de serviço de diretório.

Todos os tipos de ACEs contêm as seguintes informações de controle de acesso:

-   Um [SID (identificador de](security-identifiers.md) segurança) que identifica o usuário [confiável](trustees.md) ao qual a ACE se aplica.
-   Uma [*máscara de*](/windows/desktop/SecGloss/a-gly) acesso que especifica os direitos de [acesso](access-rights-and-access-masks.md) controlados pela ACE.
-   Um sinalizador que indica o tipo de ACE.
-   Um conjunto de sinalizadores de bits que determinam se contêineres ou objetos filho podem herdar a ACE do objeto primário ao qual a ACL está anexada.

A tabela a seguir lista os três tipos ACE com suporte por todos os objetos de segurança.



| Tipo               | Descrição                                                                                                                                                                                                                                      |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACE negada ao acesso  | Usado em uma DACL [*(lista de controle de*](/windows/desktop/SecGloss/d-gly) acesso discricionário) para negar direitos de acesso a um confiável.                                       |
| ACE com permissão de acesso | Usado em uma DACL para permitir direitos de acesso a um confiável.                                                                                                                                                                                              |
| ACE de auditoria do sistema   | Usado em uma [*SACL*](/windows/desktop/SecGloss/s-gly) (lista de controle de acesso do sistema) para gerar um registro de auditoria quando o usuário confiável tenta exercício dos direitos de acesso especificados. |



 

Para uma tabela de ACEs específicas do objeto, consulte [ACEs específicas do objeto](object-specific-aces.md).

> [!Note]  
> Atualmente, não há suporte para ACEs de objeto de alarme do sistema.

 

 

 
