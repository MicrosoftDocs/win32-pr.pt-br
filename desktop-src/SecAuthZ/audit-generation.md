---
description: Os requisitos de segurança no nível de C2 especificam que os administradores de sistema devem ser capazes de auditar eventos relacionados à segurança e que o acesso a esses dados de auditoria deve ser limitado a administradores autorizados.
ms.assetid: 411001b1-94cd-465f-8558-c8aa119e4303
title: Geração de auditoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d00be8b6d94b29a42436fdabc63be8d2c05789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748121"
---
# <a name="audit-generation"></a>Geração de auditoria

Os requisitos de segurança no nível de C2 especificam que os administradores de sistema devem ser capazes de auditar eventos relacionados à segurança e que o acesso a esses dados de auditoria deve ser limitado a administradores autorizados. A API do Windows fornece funções que permitem que um administrador monitore eventos relacionados à segurança.

O descritor de segurança para um objeto protegível pode ter uma SACL ( [*lista de controle de acesso do sistema*](/windows/desktop/SecGloss/s-gly) ). Uma SACL contém ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) que especificam os tipos de tentativas de acesso que geram relatórios de auditoria. Cada ACE identifica um grupo de confiança, um conjunto de direitos de acesso e um conjunto de sinalizadores que indicam se o sistema gera mensagens de auditoria para tentativas de acesso com falha, tentativas de acesso bem-sucedidas ou ambos.

O sistema grava as mensagens de auditoria no log de eventos de segurança. Para obter informações sobre como acessar os registros em um log de eventos de segurança, consulte [log de eventos](/windows/desktop/EventLog/event-logging).

Para ler ou gravar a SACL de um objeto, um thread deve primeiro habilitar o \_ privilégio nome de segurança se \_ . Para obter mais informações, consulte [direitos de acesso à SACL](sacl-access-right.md).

A API do Windows também fornece suporte para aplicativos de servidor para gerar mensagens de auditoria quando um cliente tenta acessar um objeto particular. Para obter mais informações, consulte [auditando o acesso a objetos privados](auditing-access-to-private-objects.md).

 

 
