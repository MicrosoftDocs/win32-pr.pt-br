---
description: As funções de instalação podem gerar caixas de diálogo para lidar com situações de instalação comuns e coletar informações do usuário.
ms.assetid: 0bff17a6-590d-4410-9ed1-0a655d94caad
title: Sobre solicitação de disco e tratamento de erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9aa7a43cc0efd81f066872a55cde20b66bb13d1c117153606f4b9fe2dd2e58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887959"
---
# <a name="about-disk-prompting-and-error-handling"></a>Sobre solicitação de disco e tratamento de erros

Embora as funções de instalação não forneçam uma interface do usuário, há quatro funções de instalação que geram caixas de diálogo para lidar com situações de instalação comuns e reunir informações do usuário. São eles: [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)e [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora).

As rotinas de retorno de chamada podem chamar essas funções para criar caixas de diálogo para auxiliar no processamento de notificações enviadas por outras funções de instalação, como [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) e [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea).

A função [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) solicita que o usuário insira mídia removível, especifique um novo caminho de origem ou cancele a instalação. O aplicativo pode oferecer opções adicionais ao usuário, dependendo dos sinalizadores especificados quando a função é chamada. Isso inclui ignorar o arquivo atual ou procurar um novo caminho de origem.

As três funções, [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)e [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora), criam caixas de diálogo que interagem com o usuário para coletar informações do usuário sobre como proceder quando ocorreu um erro.

A função [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora) gera uma caixa de diálogo que pergunta ao usuário como se recuperar de um erro de cópia. O usuário pode especificar um novo caminho de origem para a operação de cópia ou cancelar a instalação. Dependendo dos sinalizadores especificados durante a chamada para **SetupCopyError**, o usuário também poderá procurar um novo caminho de origem, exibir detalhes do erro ou ignorar o arquivo atual.

Uma caixa de diálogo que pergunta ao usuário como processar erros que ocorrem durante uma operação de renomeação de arquivo pode ser gerada chamando [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora). Com essa caixa de diálogo, o usuário tem a oportunidade de repetir a operação, ignorar a operação de renomeação atual ou anular.

A função [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora) gera uma caixa de diálogo que pode coletar informações sobre como o usuário deseja tratar um erro que ocorreu durante uma operação de exclusão de arquivo. O usuário recebe as opções para repetir a operação, ignorar a operação de exclusão atual ou anular.

A rotina de retorno de chamada de fila padrão, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), usa as quatro funções mencionadas anteriormente para gerar partes de sua interface do usuário e para lidar com erros e solicitar novas mídias.

 

 



