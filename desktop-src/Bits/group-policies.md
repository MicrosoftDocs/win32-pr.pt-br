---
title: Políticas de grupo
description: Serviço de Transferência Inteligente em Segundo Plano bits (BITS) usa as políticas de grupo a seguir para definir transferências e configurações de BITS. Para obter mais informações sobre qual versão do BITS é usada por diferentes versões do Windows, consulte o tópico Novidades.
ms.assetid: 32c7e2b1-bac2-4708-a30c-f6b2a816c1a4
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: b8d09b87c1243c2a6e53d59166f611931ab572ca755ea2fde2e44e6ef15a4202
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118173730"
---
# <a name="group-policies"></a>Políticas de grupo

> [!NOTE]
> Para obter detalhes sobre como usar o MDM (gerenciamento de dispositivo móvel) para definir políticas para Serviço de Transferência Inteligente em Segundo Plano (BITS), consulte [CSP de política.](/windows/client-management/mdm/policy-configuration-service-provider)

Serviço de Transferência Inteligente em Segundo Plano bits (BITS) usa as políticas de grupo a seguir para definir transferências e configurações de BITS. Para obter mais informações sobre qual versão do BITS é usada por diferentes versões do Windows, consulte o tópico [Novidades.](what-s-new.md)

> [!NOTE]  
> Se o valor da política não for definido, o BITS usará o valor da política padrão.

**Para habilitar uma política de BITS**

1.  Abra Política de Grupo inserindo **gpedit.msc /gpcomputer:"**_ComputerName_  *_"_* na janela Executar ou no prompt de comando em uma janela do CMD.
2.  As políticas bits estão localizadas em **Configuração do** **Computador, Modelos Administrativos,** **Rede** **e Serviço de Transferência Inteligente em Segundo Plano**.
3.  Clique com o botão direito do mouse na política e **selecione Editar**.
4.  Siga as instruções para habilenciar e definir a política.

As políticas de grupo para BITS estão localizadas no Registro em **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **BITS**. Observe que apenas as políticas configuradas estão listadas no Registro.

|Política|Descrição|
|-|-|
|JobInactivityTimeout<br/>BITS 1.0|Por padrão, o BITS mantém informações sobre um trabalho por 90 dias. Se não houver nenhuma atividade em relação ao trabalho por esse período, o BITS cancelará o trabalho. O progresso da transferência ou as alterações de propriedade redefinem o temporizador.<br/> Talvez seja necessário ajustar essa política se o usuário não fizer logoff nem manter uma conexão de rede por longos períodos de tempo.|
|MaxInternetBandwidth<br/>BITS 2.0|Limita a largura de banda de rede que o BITS usa para transferências em segundo plano (essa política não afeta transferências em primeiro plano).<br/>Especifique um limite a ser usado durante um intervalo de tempo específico e um limite a ser usado em todos os outros momentos. Por exemplo, limite o uso da largura de banda de rede a 10 Kbps (quilobits por segundo) a partir das 8h às 17h e use toda a largura de banda não usada disponível o restante do tempo.<br/>**Observação:** alterar o relógio do sistema não afeta o intervalo de tempo de limitação de largura de banda. Por exemplo, se a hora atual for 14h e o intervalo de limitação de largura de banda começa às 15h, mover o relógio do sistema para frente uma hora não significa que o BITS imporá a limitação de largura de banda uma hora mais cedo, a limitação de largura de banda ainda ocorrerá em uma hora. Para refletir a alteração do relógio do sistema no BITS, você deve reiniciar o computador ou o serviço BITS.<br/>Especifique o limite em quilobits por segundo. Basear o limite no tamanho do link de rede, não no tamanho da NIC (placa de interface de rede) do computador. O BITS usará aproximadamente dois quilobits se você especificar um valor menor que dois quilobits. Para impedir que as transferências de BITS ocorram, especifique um limite de zero. Se você especificar um limite de zero, o BITS coloca todos os trabalhos em segundo plano em um estado de erro transitório. (O código de erro é definido como BG_E_BLOCKED_BY_POLICY.) O BITS coloca os trabalhos no estado na fila após o intervalo de tempo expirar.<br/> Se você desabilitar ou não configurar essa política, o BITS usará toda a largura de banda não utilizada disponível.<br/> Normalmente, você usa essa política para impedir que as transferências de BITS competem pela largura de banda de rede quando o cliente tem um adaptador de rede rápido (10 Mbps), mas está conectado à rede por meio de um link lento (56 Kbps).<br/> Para obter informações sobre como o BITS usa largura de banda de rede, consulte [Largura de banda de rede.](network-bandwidth.md)|
|MaxDownloadTime<br/>BITS 3.0|Determina o período de tempo que o BITS pode gastar transferindo ativamente os arquivos no trabalho. O padrão é 90 dias.<br/> Para substituir essa política para um trabalho específico, chame o [**método IBackgroundCopyJob4::SetMaximumDownloadTime.**](/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyjob4-setmaximumdownloadtime)|
|MaxJobsPerMachine<br/>BITS 3.0|Limita o número de trabalhos que os usuários podem criar no computador. O padrão é 300 trabalhos. Essa política não se aplica a um usuário com privilégios de administrador ou contas de serviço.|
|MaxJobsPerUser<br/>BITS 3.0|Limita o número de trabalhos que um usuário pode criar no computador. O padrão é 60 trabalhos por usuário. Essa política não se aplica a um usuário com privilégios de administrador ou contas de serviço.|
|MaxFilesPerJob<br/>BITS 3.0|Limita o número de arquivos que um usuário pode adicionar a um trabalho. O padrão é 200 arquivos por trabalho. Essa política não se aplica a um usuário com privilégios de administrador ou contas de serviço.|
|MaxRangesPerFile<br/>BITS 3.0|Limita o número de intervalos que um usuário pode especificar para um arquivo. O valor padrão é 500 intervalos. Essa política não se aplica a um usuário com privilégios de administrador ou contas de serviço.|

O BITS usa as políticas de grupo a seguir para habilitar e configurar como o BITS interage com o BranchCache.

|Política|Descrição|
|-|-|
|DisableBranchCache<br/>BITS 4.0|Por padrão, o Windows BranchCache está habilitado. De definir essa política para impedir que os clientes BITS transferam conteúdo usando o Windows BranchCache.<br/>**Observação:** essa configuração não afeta o uso de Windows BranchCache por aplicativos diferentes de BITS. Essa política não se aplica a transferências de BITS por SMB (Bloco de Mensagens do Servidor). Essa configuração não terá efeito se as configurações administrativas do computador para Windows Cache de Branch desabilitar totalmente seu uso.|

O BITS usa as políticas de grupo a seguir para configurar a limitação de largura de banda.

|Política|Descrição|
|-|-|
|EnableMaintenanceLimits<br/>BITS 4.0|Limita a largura de banda de rede que o BITS usa para transferências em segundo plano durante os dias e horas de manutenção. As agendas de manutenção limitam ainda mais a largura de banda de rede usada para transferências em segundo plano.<br/> Especifique um limite a ser usado para trabalhos em segundo plano durante um agendamento de manutenção. Por exemplo, se os trabalhos de prioridade normal atualmente estão limitados a 256 Kbps em um agendamento de trabalho, você pode limitar ainda mais a largura de banda de rede dos trabalhos de prioridade normal a 0 Kbps a partir das 8h. para 10h00. em um agendamento de manutenção.<br/>**Observação:** os limites de largura de banda definidos para o período de manutenção superam os limites definidos para o trabalho e outras agendas.|
|EnableBandwidthLimits<br/>BITS 4.0|Limita a largura de banda de rede que o BITS usa para transferências em segundo plano durante o trabalho e dias e horas não úteis. A agenda de trabalho é definida usando um calendário semanal, que consiste em dias da semana e horas do dia. Todas as horas e dias que não estão definidos em uma agenda de trabalho são consideradas horas não úteis.<br/> Especifique um limite a ser usado para trabalhos em segundo plano durante uma agenda de trabalho. Por exemplo, você pode limitar a largura de banda de rede de trabalhos de baixa prioridade a 128 Kbps a partir das 8h às 17h de segunda a sexta-feira e, em seguida, de definir o limite como 512 Kbps para horas não de trabalho.|


## <a name="related-topics"></a>Tópicos relacionados
* [CSP Policy](/windows/client-management/mdm/policy-configuration-service-provider)
