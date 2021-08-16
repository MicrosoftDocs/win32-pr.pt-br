---
title: Concluindo e cancelando um trabalho
description: Para concluir um trabalho de transferência, chame o método IBackgroundCopyJob Complete.
ms.assetid: 8f96ed59-b038-4047-bea4-c63b9e84c209
keywords:
- transferir bits de trabalho , cancelando
- cancelando um BITS de trabalho
- transferir bits de trabalho, concluindo
- concluindo um BITS de trabalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 348ee7c4ad4b9a38350e6a1f25d8d05d206b299518cf25197b643dbcb15cb4a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835051"
---
# <a name="completing-and-canceling-a-job"></a>Concluindo e cancelando um trabalho

Para concluir um trabalho de transferência, chame [**o método IBackgroundCopyJob::Complete.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) Para trabalhos de download, você pode chamar o método **Complete** antes que todos os arquivos no trabalho tenham sido transferidos (antes que o estado do trabalho seja BG \_ JOB STATE \_ \_ TRANSFERRED). Somente os arquivos que o BITS transferiu com êxito para o cliente antes de você chamar o **método Complete** estão disponíveis para o usuário.

Para trabalhos de upload, chame [**o método Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) somente se o estado do trabalho for BG JOB STATE \_ \_ \_ TRANSFERRED. Para determinar quando o estado do trabalho é BG JOB STATE TRANSFERRED, sondar a propriedade de estado do trabalho ou registrar para receber a notificação de evento \_ \_ \_ BG NOTIFY JOB TRANSFERRED [](polling-for-the-status-of-the-job.md) \_ \_ \_ . [](registering-a-com-callback.md)

Para cancelar um trabalho de transferência, chame o [**método IBackgroundCopyJob::Cancel.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) O **método Cancel** remove o trabalho da fila de transferência e remove os arquivos temporários do cliente. Normalmente, você chamará esse método se não conseguir resolver um erro associado ao trabalho.

O [**método Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) cancela um upload se o upload não for concluído. Se o upload for concluído e o trabalho for do tipo BG JOB TYPE UPLOAD REPLY, o método \_ \_ \_ \_ cancelará a resposta.

Se você não chamar o método [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) ou o método [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) dentro de 90 dias (jobInactivityTimeout [padrão](group-policies.md) Política de Grupo), o serviço cancelará o trabalho. Se o serviço cancelar o trabalho, os arquivos baixados e o arquivo de resposta não estarão disponíveis para o cliente; O cancelamento do trabalho não afeta os arquivos que foram carregados com êxito. Você sempre deve chamar o **método Complete** ou **Cancel** e não contar com a política JobInactivityTimeout para limpar seus trabalhos. Os trabalhos deixados na fila poderão impedir que os usuários criarem outros trabalhos se o limite de política MaxJobsPerUser ou MaxJobsPerMachine for atingido.

 

 




