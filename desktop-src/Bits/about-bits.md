---
title: Sobre BITS
description: Use Serviço de Transferência Inteligente em Segundo Plano bits (BITS) para transferir arquivos de forma assíncrona entre um cliente e um servidor.
ms.assetid: 056007f4-6a71-4f8e-bf7d-17ed87088edf
keywords:
- Serviço de Transferência Inteligente em Segundo Plano, descrito
- TRANSFERIR BITS da fila
- transferir bits da fila, aceleração
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: 53693b7087d647e8d6e89a8c81e09895dc3866b964642475466bbf8f52ddbae5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529276"
---
# <a name="about-bits"></a>Sobre BITS

Use Serviço de Transferência Inteligente em Segundo Plano bits (BITS) para baixar arquivos de ou carregar arquivos em servidores Web HTTP ou servidores de arquivos SMB. 

O BITS continua a transferir arquivos depois que um aplicativo é desligado, desde que o usuário que iniciou a transferência permaneça conectado e uma conexão de rede seja mantida. O BITS não força uma conexão de rede. O BITS retoma as transferências depois que uma conexão de rede que foi perdida é restabelecida ou depois que um usuário que fez logo login novamente. Para obter mais informações, consulte [Usuários e Conexões de rede](users-and-network-connections.md).

O BITS está atento ao custo e ao congestionamento de rede atuais para que um trabalho em segundo plano interfira o menor possível na experiência de primeiro plano do usuário. O BITS usa [largura](network-bandwidth.md) de banda de rede ociosa para transferir os arquivos e aumentará ou diminuirá a taxa na qual os arquivos são transferidos com base na quantidade de largura de banda de rede ociosa disponível. Se um aplicativo de rede começar a consumir mais largura de banda, o BITS reduzirá sua taxa de transferência para preservar a experiência interativa do usuário. O BITS usa políticas de transferência [especificadas pelo](how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md) aplicativo para impedir a transferência de arquivos em conexões de rede com custo.

O BITS também está atento ao uso de energia. A partir do Atualização de maio de 2019 para o Windows 10, o BITS transferirá arquivos [](/windows-hardware/design/device-experiences/modern-standby) quando o computador estiver no modo De espera moderno e o computador estiver conectado.

O aplicativo BITS pode usar os diferentes níveis de [prioridade bits para](/windows/desktop/api/Bits/ne-bits-bg_job_priority) permitir que o BITS escolha de forma inteligente quais trabalhos de transferência executar. Os trabalhos com prioridade mais alta estão à frente dos trabalhos de prioridade mais baixa. Os trabalhos com o mesmo nível de prioridade compartilham o tempo de transferência, o que impede um trabalho grande de bloquear trabalhos pequenos na fila de transferência. Os trabalhos com prioridade mais baixa não recebem o tempo de transferência até que os trabalhos com prioridade mais alta estejam concluídos ou em um estado de erro.

O BITS usa Windows BranchCache para cache de pares. Para obter mais informações, consulte a [Visão geral do BranchCache.](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10))

Os desenvolvedores da UWP (Plataforma Universal Windows) devem usar o [Windows. API Networking.BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) e não a API bits.

Há três tipos de trabalhos [**de transferência.**](/windows/desktop/api/Bits/ne-bits-bg_job_type) Um trabalho de download baixa arquivos para o cliente, um trabalho de upload carrega um arquivo no servidor e um trabalho de upload-resposta carrega um arquivo no servidor e recebe um arquivo de resposta do aplicativo do servidor.

Os tópicos a seguir fornecem informações mais detalhadas sobre o BITS:

-   [Autenticação](authentication.md)
-   [Ciclo de vida de um trabalho bits](life-cycle-of-a-bits-job.md)
-   [Usuários e conexões de rede](users-and-network-connections.md)
-   [Largura de banda da rede](network-bandwidth.md)
-   [Políticas de Grupo](group-policies.md)
-   [Contas de serviço e BITS](service-accounts-and-bits.md)
-   [Tokens auxiliares para trabalhos de transferência de BITS](helper-tokens-for-bits-transfer-jobs.md)
-   [Consistência de transferência de arquivo](file-transfer-consistency.md)
-   [Requisitos HTTP para downloads de BITS](http-requirements-for-bits-downloads.md)
-   [Requisitos do IIS para uploads de BITS](iis-requirements-for-bits-uploads.md)
-   [Limpeza de diretório virtual](virtual-directory-cleanup.md)
-   [BITS e Restauração do Sistema](bits-and-system-restore.md)
-   [Tipo de inicialização bits](bits-startup-type.md)
-   [Compartilhamento de Conexão com a Internet](internet-connection-sharing.md)
-   [Par Caching](peer-caching.md)
-   [Segurança bits, tokens e contas de administrador](user-account-control-and-bits.md)
-   [BITS Compact Server](bits-compact-server.md)

Use as interfaces BITS para escrever [aplicativos](bits-interfaces.md) que criam e monitoram trabalhos de transferência. Para obter detalhes sobre como usar as interfaces BITS, consulte [Usando BITS](using-bits.md).