---
title: Concluindo e cancelando um trabalho
description: Para concluir um trabalho de transferência, chame o método método ibackgroundcopyjob Complete.
ms.assetid: 8f96ed59-b038-4047-bea4-c63b9e84c209
keywords:
- transferir BITS de trabalho, cancelando
- Cancelando um trabalho BITS
- transferir BITS de trabalho, concluindo
- Concluindo um trabalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb5cd6a33cf8cefa8749a1802c922dc80518722
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453530"
---
# <a name="completing-and-canceling-a-job"></a>Concluindo e cancelando um trabalho

Para concluir um trabalho de transferência, chame o método [**método ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) . Para baixar trabalhos, você pode chamar o método **Complete** antes que todos os arquivos no trabalho tenham sido transferidos (antes de o estado do trabalho ser BG, o \_ estado do trabalho é \_ \_ transferido). Somente os arquivos que o BITS transferiu com êxito para o cliente antes de você ter chamado o método **Complete** estão disponíveis para o usuário.

Para trabalhos de carregamento, chame o método [**completo**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) somente se o estado do trabalho for BG, \_ estado de trabalho \_ \_ transferido. Para determinar quando o estado do trabalho é BG, o estado do trabalho é \_ \_ \_ transferido, [sondar](polling-for-the-status-of-the-job.md) a propriedade de estado do trabalho ou registrar-se para receber a notificação de evento de recebimento de \_ tarefa de notificação BG \_ \_ . [](registering-a-com-callback.md)

Para cancelar um trabalho de transferência, chame o método [**método ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) . O método **Cancel** remove o trabalho da fila de transferência e remove os arquivos temporários do cliente. Normalmente, você chamará esse método se não for possível resolver um erro associado ao trabalho.

O método [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) cancela um upload se o carregamento não for concluído. Se o upload for concluído e o trabalho for do tipo BG \_ resposta de carregamento do tipo de trabalho \_ \_ \_ , o método cancelará a resposta.

Se você não chamar o método [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) ou o método [**método ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) dentro de 90 dias ( [JobInactivityTimeout](group-policies.md) padrão política de grupo), o serviço cancelará o trabalho. Se o serviço cancelar o trabalho, os arquivos baixados e o arquivo de resposta não estarão disponíveis para o cliente; o cancelamento do trabalho não afeta os arquivos que foram carregados com êxito. Você sempre deve chamar o método **Complete** ou **Cancel** e não confiar na política JobInactivityTimeout para limpar seus trabalhos. Os trabalhos restantes na fila podem impedir que os usuários criem outros trabalhos se o limite da política MaxJobsPerUser ou MaxJobsPerMachine for atingido.

 

 




