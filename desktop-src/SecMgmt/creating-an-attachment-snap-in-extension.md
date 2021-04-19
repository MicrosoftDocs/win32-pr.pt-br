---
description: Uma extensão de snap-in de anexo fornece uma interface que os usuários podem usar para alterar as definições de configuração específicas do serviço.
ms.assetid: 6f2dc372-dee4-4793-b943-395c0587ed5e
title: Criando uma extensão de snap-in de anexo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513c982acc7e5285f3b4d1510f18b7eb6c9fe1d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779346"
---
# <a name="creating-an-attachment-snap-in-extension"></a>Criando uma extensão de snap-in de anexo

Uma extensão de snap-in de anexo fornece uma interface que os usuários podem usar para alterar as definições de configuração específicas do serviço. A extensão do snap-in de anexos deve atender aos requisitos do MMC para ser uma extensão de snap-in válida. Para obter mais informações sobre esses requisitos, consulte a documentação do [console de gerenciamento Microsoft](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .

Além das interfaces exigidas pelo MMC, uma extensão de snap-in de anexos deve implementar a interface COM [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo). Os snap-ins de configuração de segurança chamam métodos dessa interface para determinar se os dados de configuração foram alterados e, nesse caso, para atualizar o banco de dado de segurança. O snap-in de anexo deve armazenar quaisquer alterações de configuração até que os snap-ins de configuração de segurança recuperem esses dados.

Uma extensão de snap-in de anexo deve fornecer a seguinte funcionalidade:

-   [Exibir informações de configuração e análise](displaying-configuration-and-analysis-information.md)
-   [Modificar as informações de configuração na interface do usuário](modifying-configuration-information-in-the-user-interface.md)
-   [Modificar informações de configuração no banco de dados de segurança](modifying-configuration-information-in-the-database.md)

Para auxiliar sua extensão de snap-in na execução dessas tarefas, os snap-ins de configuração de segurança implementam uma interface COM, [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), que fornece métodos que sua extensão de snap-in pode chamar para se inicializar e consultar informações do banco de dados de segurança.

Depois de criar sua extensão de snap-in de anexo, você deve registrá-la com os snap-ins de configuração de segurança, conforme descrito em [registrando uma extensão de snap-in de anexo](registering-an-attachment-snap-in-extension.md).

 

 
