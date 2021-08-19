---
description: Os requisitos de segurança no nível C2 especificam que os administradores do sistema devem ser capazes de auditar eventos relacionados à segurança e que o acesso a esses dados de auditoria deve ser limitado a administradores autorizados.
ms.assetid: 411001b1-94cd-465f-8558-c8aa119e4303
title: Geração de auditoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fb2c6ab4b43d169e1ca6f6317489921987d22b507489ef0a5fd289d8483c84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784692"
---
# <a name="audit-generation"></a>Geração de auditoria

Os requisitos de segurança no nível C2 especificam que os administradores do sistema devem ser capazes de auditar eventos relacionados à segurança e que o acesso a esses dados de auditoria deve ser limitado a administradores autorizados. A API Windows fornece funções que permitem que um administrador monitore eventos relacionados à segurança.

O descritor de segurança para um objeto seguro pode ter uma SACL [*(lista de controle de*](/windows/desktop/SecGloss/s-gly) acesso do sistema). Uma SACL contém [*ACEs*](/windows/desktop/SecGloss/a-gly) (entradas de controle de acesso) que especificam os tipos de tentativas de acesso que geram relatórios de auditoria. Cada ACE identifica um usuário confiável, um conjunto de direitos de acesso e um conjunto de sinalizadores que indicam se o sistema gera mensagens de auditoria para tentativas de acesso com falha, tentativas de acesso bem-sucedidas ou ambas.

O sistema grava mensagens de auditoria no log de eventos de segurança. Para obter informações sobre como acessar os registros em um log de eventos de segurança, consulte [Log de eventos](/windows/desktop/EventLog/event-logging).

Para ler ou gravar a SACL de um objeto, um thread deve primeiro habilitar o privilégio ES \_ SECURITY \_ NAME. Para obter mais informações, consulte [SACL Access Right](sacl-access-right.md).

A API Windows também dá suporte a aplicativos de servidor para gerar mensagens de auditoria quando um cliente tenta acessar um objeto privado. Para obter mais informações, consulte [Auditando o acesso a objetos privados](auditing-access-to-private-objects.md).

 

 
