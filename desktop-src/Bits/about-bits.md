---
title: Sobre BITS
description: Use Serviço de Transferência Inteligente em Segundo Plano (BITS) para transferir arquivos de forma assíncrona entre um cliente e um servidor.
ms.assetid: 056007f4-6a71-4f8e-bf7d-17ed87088edf
keywords:
- Serviço de Transferência Inteligente em Segundo Plano, descrito
- transferir BITS da fila
- transferir BITS da fila, limitação
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: b1ac0f587b496692ec1c2e62be06c0e64766a205
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084583"
---
# <a name="about-bits"></a>Sobre BITS

Use Serviço de Transferência Inteligente em Segundo Plano (BITS) para baixar arquivos do ou carregar arquivos em servidores Web HTTP ou servidores de arquivos SMB. 

O BITS continua a transferir arquivos depois que um aplicativo é encerrado, desde que o usuário que iniciou a transferência permaneça conectado e uma conexão de rede seja mantida. O BITS não forçará uma conexão de rede. O BITS retoma as transferências depois que uma conexão de rede perdida é restabelecida ou depois de um usuário que fez logoff de logs novamente. Para obter mais informações, consulte [usuários e conexões de rede](users-and-network-connections.md).

O BITS está atento ao custo e ao congestionamento da rede atual para que um trabalho em segundo plano interfira no mínimo possível com a experiência de primeiro plano do usuário. O BITS usa a [largura de banda de rede](network-bandwidth.md) ociosa para transferir os arquivos e aumentar ou diminuir a taxa na qual os arquivos são transferidos com base na quantidade de largura de banda de rede ociosa disponível. Se um aplicativo de rede começar a consumir mais largura de banda, o BITS reduzirá sua taxa de transferência para preservar a experiência interativa do usuário. O BITS usa políticas de [transferência](how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md) especificadas pelo aplicativo para impedir que arquivos sejam transferidos em conexões de rede com custo.

O BITS também está atento ao uso de energia. A partir do Windows 10 de maio de 2019 atualização, o BITS transferirá arquivos quando o computador estiver no modo de [espera moderno](/windows-hardware/design/device-experiences/modern-standby) e o computador estiver conectado.

O aplicativo BITS pode usar os diferentes [níveis de prioridade](/windows/desktop/api/Bits/ne-bits-bg_job_priority) do bits para permitir que os bits escolham de forma inteligente quais trabalhos de transferência são executados. Os trabalhos com prioridade mais alta estão à frente dos trabalhos de prioridade mais baixa. Os trabalhos com o mesmo nível de prioridade compartilham o tempo de transferência, o que impede um trabalho grande de bloquear trabalhos pequenos na fila de transferência. Os trabalhos com prioridade mais baixa não recebem o tempo de transferência até que os trabalhos com prioridade mais alta estejam concluídos ou em um estado de erro.

O BITS usa o Windows BranchCache para cache de sistemas pares. Para obter mais informações, consulte a [visão geral do BranchCache](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10)).

Plataforma Universal do Windows (UWP) os desenvolvedores devem usar a API [Windows. Networking. BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) e não a API bits.

Há três tipos de [**trabalhos de transferência**](/windows/desktop/api/Bits/ne-bits-bg_job_type). Um trabalho de download baixa arquivos para o cliente, um trabalho de upload carrega um arquivo no servidor e um trabalho de resposta de upload carrega um arquivo no servidor e recebe um arquivo de resposta do aplicativo de servidor.

Os tópicos a seguir fornecem informações mais detalhadas sobre o BITS:

-   [Autenticação](authentication.md)
-   [Ciclo de vida de um trabalho do BITS](life-cycle-of-a-bits-job.md)
-   [Usuários e conexões de rede](users-and-network-connections.md)
-   [Largura de banda da rede](network-bandwidth.md)
-   [Políticas de grupo](group-policies.md)
-   [Contas de serviço e BITS](service-accounts-and-bits.md)
-   [Tokens auxiliares para trabalhos de transferência de BITS](helper-tokens-for-bits-transfer-jobs.md)
-   [Consistência de transferência de arquivo](file-transfer-consistency.md)
-   [Requisitos de HTTP para downloads de BITS](http-requirements-for-bits-downloads.md)
-   [Requisitos do IIS para carregamentos do BITS](iis-requirements-for-bits-uploads.md)
-   [Limpeza do diretório virtual](virtual-directory-cleanup.md)
-   [Restauração de BITS e do sistema](bits-and-system-restore.md)
-   [Tipo de inicialização do BITS](bits-startup-type.md)
-   [Compartilhamento de Conexão com a Internet](internet-connection-sharing.md)
-   [Cache de pares](peer-caching.md)
-   [Segurança de BITS, tokens e contas de administrador](user-account-control-and-bits.md)
-   [BITS Compact Server](bits-compact-server.md)

Use as [interfaces](bits-interfaces.md) bits para gravar aplicativos que criam e monitoram trabalhos de transferência. Para obter detalhes sobre como usar as interfaces BITS, consulte [usando o bits](using-bits.md).