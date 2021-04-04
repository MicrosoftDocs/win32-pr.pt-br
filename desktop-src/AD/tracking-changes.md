---
title: Controlando alterações
description: Alguns aplicativos devem manter a consistência entre dados específicos armazenados no serviço de diretório Active Directory e outros dados.
ms.assetid: f4539482-1170-4c0c-b817-b39e58049d39
ms.tgt_platform: multiple
keywords:
- Active Directory, usando, controlando alterações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dc772f883b97eb4e7305b39f0a582448a8bc021
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103917098"
---
# <a name="tracking-changes"></a>Controlando alterações

Alguns aplicativos devem manter a consistência entre dados específicos armazenados no serviço de diretório Active Directory e outros dados. Os outros dados podem ser armazenados no diretório, em uma tabela SQL Server, em um arquivo ou no registro. Quando os dados armazenados no diretório são alterados, os outros dados podem precisar ser alterados para permanecerem consistentes. Os aplicativos que têm esse requisito incluem:

Esta seção não aborda os mecanismos usados pelos aplicativos de monitoramento. Esses são aplicativos que monitoram as alterações de diretório sem a finalidade de manter dados consistentes entre repositórios separados, mas como uma ferramenta de gerenciamento de sistema. Embora os aplicativos de monitoramento possam usar os mesmos mecanismos que oferecem suporte a aplicativos de controle de alterações, os mecanismos a seguir são projetados especificamente para monitorar aplicativos:

-   Auditoria de segurança. Ao modificar a parte da SACL (lista de controle de acesso) do sistema de um descritor de segurança de objeto, você pode fazer com que os acessos ao objeto em um determinado controlador de domínio gerem registros de auditoria no log de eventos de segurança nesse DC. Você pode auditar leituras, gravações ou ambos; Você pode auditar o objeto inteiro ou os atributos específicos. Para obter mais informações, consulte [recuperando a SACL e a geração de auditoria de um objeto](retrieving-an-objectampaposs-sacl.md) . [](/windows/desktop/SecAuthZ/audit-generation)
-   Log de eventos. Ao modificar as configurações do registro em um determinado controlador de domínio, você pode alterar os tipos de eventos registrados no log de eventos do serviço de diretório. Especificamente, para registrar todas as modificações, defina o valor de **8 acesso ao diretório** na seguinte chave do registro para 4.

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                NTDS
                   Diagnostics
    ```

    Para obter mais informações, consulte [log de eventos](/windows/desktop/EventLog/event-logging).

-   Rastreamento de eventos. O Windows 2000 introduziu uma API de rastreamento de eventos para rastreamento e registro em log de eventos interessantes em software ou hardware. O sistema operacional Windows, e Active Directory Domain Services em particular, dão suporte ao uso de rastreamento de eventos para planejamento de capacidade e análise de desempenho detalhada. Para obter mais informações, consulte [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) e [rastreamento de eventos em ADSI](/windows/desktop/ADSI/adsi-and-etw).

Esta seção inclui os tópicos a seguir:

-   [Visão geral das técnicas de Controle de Alterações](overview-of-change-tracking-techniques.md)
-   [Notificações de alteração no Active Directory Domain Services](change-notifications-in-active-directory-domain-services.md)
-   [Sondando alterações usando o controle DirSync](polling-for-changes-using-the-dirsync-control.md)
-   [Sondando alterações usando USNChanged](polling-for-changes-using-usnchanged.md)

 

 