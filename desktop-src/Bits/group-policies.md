---
title: Políticas de grupo
description: Serviço de Transferência Inteligente em Segundo Plano (BITS) usa as políticas de grupo a seguir para configurar as transferências e as configurações do BITS. Para obter mais informações sobre qual versão do BITS é usada por diferentes versões do Windows, consulte o tópico o que há de novo.
ms.assetid: 32c7e2b1-bac2-4708-a30c-f6b2a816c1a4
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: f3ff0070c489759055bdaae1d2e68d8718a7bae5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159361"
---
# <a name="group-policies"></a>Políticas de grupo

> [!NOTE]
> Para obter detalhes sobre como usar o MDM (gerenciamento de dispositivo móvel) para definir políticas para Serviço de Transferência Inteligente em Segundo Plano (BITS), consulte [CSP de política](/windows/client-management/mdm/policy-configuration-service-provider).

Serviço de Transferência Inteligente em Segundo Plano (BITS) usa as políticas de grupo a seguir para configurar as transferências e as configurações do BITS. Para obter mais informações sobre qual versão do BITS é usada por diferentes versões do Windows, consulte o tópico [o que](what-s-new.md) há de novo.

> [!NOTE]  
> Se o valor da política não for definido, o BITS usará o valor da política padrão.

**Para habilitar uma política de BITS**

1.  Abra Política de Grupo inserindo **gpedit. msc/gpcomputer: "***ComputerName***"** na janela **executar** ou no prompt de comando em uma janela cmd.
2.  As políticas de BITS estão localizadas em **configuração do computador**, **Modelos Administrativos**, **rede** **serviço de transferência inteligente em segundo plano**.
3.  Clique com o botão direito do mouse na política e selecione **Editar**.
4.  Siga as instruções para habilitar e definir a política.

As políticas de grupo para bits estão localizadas no registro em **HKEY \_ local \_ Machine** \\ **software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **bits**. Observe que somente as políticas configuradas são listadas no registro.

|Política|Descrição|
|-|-|
|JobInactivityTimeout<br/>BITS 1,0|Por padrão, o BITS mantém informações sobre um trabalho por 90 dias. Se não houver nenhuma atividade em relação ao trabalho durante esse período de tempo, o BITS cancelará o trabalho. As alterações de progresso ou de propriedade de transferência redefinem o temporizador.<br/> Talvez seja necessário ajustar essa política se o usuário não fizer logon ou manter uma conexão de rede por longos períodos de tempo.|
|MaxInternetBandwidth<br/>BITS 2,0|Limita a largura de banda de rede que o BITS usa para transferências em segundo plano (essa política não afeta transferências em primeiro plano).<br/>Especifique um limite a ser usado durante um intervalo de tempo específico e um limite a ser usado em todos os outros horários. Por exemplo, limite o uso da largura de banda de rede a 10 kilobits por segundo (Kbps) de 8:00 A.M. a 5:00 P.M. e usar toda a largura de banda não utilizada no restante do tempo.<br/>**Observação**: alterar o relógio do sistema não afeta o intervalo de tempo de limitação de largura de banda. Por exemplo, se a hora atual for 2:00 e o intervalo de limitação de largura de banda começa às 3:00, mover o relógio do sistema para frente uma hora não significa que os BITS imporão a limitação da largura de banda a uma hora antecipadamente, a limitação da largura de banda ainda ocorrerá em uma hora. Para refletir a alteração do relógio do sistema em BITS, você deve reiniciar o computador ou o serviço BITS.<br/>Especifique o limite em quilobits por segundo. Basear o limite no tamanho do link de rede, não o tamanho da NIC (placa de interface de rede) do computador. O BITS usa aproximadamente dois kilobits se você especificar um valor menor que dois kilobits. Para impedir que as transferências do BITS ocorram, especifique um limite de zero. Se você especificar um limite de zero, o BITS colocará todos os trabalhos em segundo plano em um estado de erro transitório. (O código de erro é definido como BG_E_BLOCKED_BY_POLICY.) O BITS coloca os trabalhos no estado na fila após o intervalo de tempo expirar.<br/> Se você desabilitar ou não configurar essa política, o BITS usará toda a largura de banda disponível não utilizada.<br/> Normalmente, você usa essa política para impedir que as transferências de BITS se conpetem para a largura de banda da rede quando o cliente tem um adaptador de rede rápido (10 Mbps), mas está conectado à rede por meio de um link lento (56 Kbps).<br/> Para obter informações sobre como o BITS usa largura de banda de rede, consulte [largura de banda de rede](network-bandwidth.md).|
|MaxDownloadTime<br/>BITS 3,0|Determina o período de tempo que o BITS pode gastar Transferindo ativamente os arquivos no trabalho. O padrão é 90 dias.<br/> Para substituir essa política para um trabalho específico, chame o método [**IBackgroundCopyJob4:: SetMaximumDownloadTime**](/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyjob4-setmaximumdownloadtime) .|
|MaxJobsPerMachine<br/>BITS 3,0|Limita o número de trabalhos que os usuários podem criar no computador. O padrão é 300 trabalhos. Essa política não se aplica a um usuário com privilégios de administrador ou contas de serviço.|
|MaxJobsPerUser<br/>BITS 3,0|Limita o número de trabalhos que um usuário pode criar no computador. O padrão é 60 trabalhos por usuário. Essa política não se aplica a um usuário com privilégios de administrador ou contas de serviço.|
|MaxFilesPerJob<br/>BITS 3,0|Limita o número de arquivos que um usuário pode adicionar a um trabalho. O padrão é 200 arquivos por trabalho. Essa política não se aplica a um usuário com privilégios de administrador ou contas de serviço.|
|MaxRangesPerFile<br/>BITS 3,0|Limita o número de intervalos que um usuário pode especificar para um arquivo. O valor padrão é 500 intervalos. Essa política não se aplica a um usuário com privilégios de administrador ou contas de serviço.|

O BITS usa as seguintes políticas de grupo para habilitar e configurar como o BITS interage com o BranchCache.

|Política|Descrição|
|-|-|
|DisableBranchCache<br/>BITS 4,0|Por padrão, o recurso Windows BranchCache está habilitado. Defina essa política para impedir que clientes BITS transfiram conteúdo usando o Windows BranchCache.<br/>**Observação**: essa configuração não afeta o uso do Windows BranchCache por aplicativos que não sejam bits. Essa política não se aplica a transferências de BITS por meio do protocolo SMB. Essa configuração não terá efeito se as configurações administrativas do computador para o cache de ramificação do Windows desabilitarem totalmente seu uso.|

O BITS usa as seguintes políticas de grupo para configurar a limitação da largura de banda.

|Política|Descrição|
|-|-|
|EnableMaintenanceLimits<br/>BITS 4,0|Limita a largura de banda de rede que o BITS usa para transferências em segundo plano durante os dias de manutenção e horas. As agendas de manutenção limitam ainda mais a largura de banda de rede usada para transferências em segundo plano.<br/> Especifique um limite a ser usado para trabalhos em segundo plano durante um agendamento de manutenção. Por exemplo, se os trabalhos de prioridade normal estiverem limitados a 256 kbps em uma agenda de trabalho, você poderá limitar ainda mais a largura de banda de rede de trabalhos de prioridade normal a 0 kbps da 8:00. para 10h00. em um agendamento de manutenção.<br/>**Observação**: os limites de largura de banda definidos para o período de manutenção substituem os limites definidos para o trabalho e outras agendas.|
|EnableBandwidthLimits<br/>BITS 4,0|Limita a largura de banda de rede que o BITS usa para transferências em segundo plano durante os dias de trabalho e não de trabalho e horas. A agenda de trabalho é definida usando um calendário semanal, que consiste em dias da semana e horas do dia. Todas as horas e dias não definidos em uma agenda de trabalho são considerados horas não úteis.<br/> Especifique um limite a ser usado para trabalhos em segundo plano durante uma agenda de trabalho. Por exemplo, você pode limitar a largura de banda de rede de trabalhos de baixa prioridade a 128 kbps da 8:00 A.M. a 5:00 P.M. de segunda a sexta-feira e defina o limite como 512 kbps para horas não úteis.|


## <a name="related-topics"></a>Tópicos relacionados
* [CSP Policy](/windows/client-management/mdm/policy-configuration-service-provider)
