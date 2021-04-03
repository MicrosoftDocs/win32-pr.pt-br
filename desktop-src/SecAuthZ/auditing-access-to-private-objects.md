---
description: Um servidor protegido pode usar as seguintes funções para gerar relatórios de auditoria no log de eventos de segurança.
ms.assetid: 4edee246-4fa7-4947-9737-34198f36e3ab
title: Auditoria de acesso a objetos privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3669841714fe9c24f6346404bc8634222bc4557e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922895"
---
# <a name="auditing-access-to-private-objects"></a>Auditoria de acesso a objetos privados

Um servidor protegido pode usar as seguintes funções para gerar relatórios de auditoria no log de eventos de segurança.



| Função                                                                                                     | Descrição                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma)                                                 | O mesmo que a função [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) , exceto que ela pode gerar mensagens de auditoria para tentativas de acesso com falha ou bem-sucedidas.                                                                            |
| [**AccessCheckByTypeAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytypeandauditalarma)                                     | O mesmo que a função [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype) , exceto que ela pode gerar mensagens de auditoria para tentativas de acesso com falha ou bem-sucedidas.                                                                |
| [**AccessCheckByTypeResultListAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma)                 | O mesmo que a função [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) , exceto que ela pode gerar mensagens de auditoria para tentativas de acesso com falha ou bem-sucedidas.                                            |
| [**AccessCheckByTypeResultListAndAuditAlarmByHandle**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarmbyhandlea) | O mesmo que a função [**AccessCheckByTypeResultListAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma) , exceto que ela permite que o thread de chamada Execute a verificação de acesso antes de representar o cliente. |
| [**ObjectCloseAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectcloseauditalarma)                                                       | Gera uma mensagem de auditoria para indicar que um cliente tentou fechar um objeto particular.                                                                                                                                   |
| [**ObjectDeleteAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma)                                                       | Gera uma mensagem de auditoria para indicar que um cliente tentou excluir um objeto particular.                                                                                                                                  |
| [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma)                                                         | Gera uma mensagem de auditoria para indicar que um cliente tentou abrir ou criar um objeto particular.                                                                                                                          |
| [**ObjectPrivilegeAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectprivilegeauditalarma)                                               | Gera uma mensagem de auditoria para indicar que um cliente tentou usar um conjunto especificado de privilégios em conjunto com uma tentativa de acessar um objeto particular.                                                              |
| [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma)                                           | Gera uma mensagem de auditoria para indicar que um cliente tentou usar um conjunto de privilégios especificado.                                                                                                                        |



 

 

 
