---
description: Um mecanismo de anexo é uma DLL que processa solicitações de análise e configuração específicas de serviço. Em outras palavras, ele manipula o processamento que não pode ser tratado pelo conjunto de ferramentas de configuração de segurança padrão.
ms.assetid: c04779f4-f1e9-40b0-9f00-0176afb1b839
title: Criando um mecanismo de anexo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96b16e768956e61fe76406777da2bce9affbfa2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778667"
---
# <a name="creating-an-attachment-engine"></a>Criando um mecanismo de anexo

Um mecanismo de anexo é uma DLL que processa solicitações de análise e configuração específicas de serviço. Em outras palavras, ele manipula o processamento que não pode ser tratado pelo conjunto de ferramentas de configuração de segurança padrão.

Para criar um mecanismo de anexo, você deve implementar as três funções a seguir:

-   [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md), que computa a diferença entre a configuração do serviço e a configuração armazenada no banco de dados de segurança. Essas diferenças são gravadas no banco de dados de segurança. Para obter mais informações, consulte [Implementing SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).
-   [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), que configura o serviço conforme especificado na interface do usuário do snap-in. Para obter mais informações, consulte [Implementing SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md).
-   [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), que atualiza a configuração de base e a análise de configuração para o serviço no banco de dados de segurança. Para obter mais informações, consulte [Implementing SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md).

O conjunto de ferramentas de configuração de segurança implementa um conjunto de funções de suporte que seu aplicativo pode chamar para consultar e definir informações no banco de dados de segurança. Para obter mais informações, consulte [funções de retorno de chamada de anexo](management-functions.md).

Depois de criar uma DLL do mecanismo de anexo, você deve registrá-la com o conjunto de ferramentas de configuração de segurança. Esse processo é descrito em [registrando um mecanismo de anexo](registering-an-attachment-engine.md).

Além de criar um mecanismo de anexo, você também deve criar uma extensão de snap-in de anexo. A extensão do snap-in fornece uma interface do usuário para tarefas específicas do serviço. Quando o usuário especifica uma nova configuração usando uma extensão de snap-in, a solicitação é passada para o mecanismo de anexo apropriado. Em seguida, o mecanismo se conecta ao serviço e altera sua configuração. Se você não implementar uma extensão de snap-in, os usuários não terão como alterar a configuração ou análise de serviço. Para obter mais informações sobre como criar uma extensão de snap-in de anexo, consulte [criando uma extensão de snap-in de anexo](creating-an-attachment-snap-in-extension.md).

 

 



