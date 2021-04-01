---
description: Um mecanismo de anexo é uma DLL que manipula solicitações de análise e configuração específicas do serviço.
ms.assetid: bbca486a-9eec-4510-b5fd-435972182a69
title: Mecanismos de anexo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af0711caa5ceada7c16ae11b6470568a76d16ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829311"
---
# <a name="attachment-engines"></a>Mecanismos de anexo

Um mecanismo de anexo é uma DLL que manipula solicitações de análise e configuração específicas do serviço.

O usuário faz uma solicitação de configuração e análise específica do serviço usando a extensão de snap-in de anexo. Essa solicitação é passada por meio dos snap-ins de configuração de segurança para o mecanismo de configuração de segurança geral que, por sua vez, passa o processamento específico do serviço para o mecanismo de anexo apropriado. Em seguida, o mecanismo de anexo se conecta ao serviço e altera sua configuração. Em outras palavras, o mecanismo de anexo fornece o processamento de back-end que dá suporte à extensão de snap-in de anexo.

Um mecanismo de anexo deve implementar as três funções a seguir:

-   [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md), que computa a diferença entre a configuração do serviço e a configuração armazenada no banco de dados de segurança. As diferenças são gravadas no banco de dados de segurança.
-   [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), que configura o serviço conforme especificado na interface do usuário do snap-in.
-   [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), que atualiza a configuração de base e a análise de configuração para o serviço no banco de dados de segurança.

Para simplificar a implementação das funções anteriores, o conjunto de ferramentas de configuração de segurança oferece suporte a funções e estruturas que seu aplicativo pode usar para consultar e definir informações no banco de dados de segurança. Para obter mais informações, consulte [funções de retorno de chamada de anexo](management-functions.md).

Ao criar uma DLL do mecanismo de anexo, você deve instalá-la e registrá-la no mecanismo de configuração de segurança. Para registrar a DLL, você adiciona uma chave específica ao registro. Quando o mecanismo de configuração de segurança é iniciado, ele verifica o registro e carrega todas as DLLs do mecanismo de anexo registrado. Em seguida, ele passa as solicitações de análise e configuração específicas do serviço para o mecanismo de anexo apropriado. As solicitações de análise e configuração padrão, aquelas que não são específicas do serviço, são tratadas pelo mecanismo de configuração de segurança.

 

 



