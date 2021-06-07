---
title: Chaves e valores do Registro para backup e restauração
ms.assetid: 83449f78-cca1-449b-8c5f-3c8a91c8b3e7
description: 'Saiba mais sobre: Chaves e valores do Registro para backup e restauração'
keywords:
- backup Backup , chaves do Registro
- Backup de chaves do Registro
- CustomPerformanceSettings Backup
- DesabilitarMonitoramento de Backup
- FilesNotToBackup Backup
- FilesNotToSnapshot Backup
- KeysNotToRestore Backup
- LastInstance Backup
- LastRestoreId Backup
- MaxShadowCopies Backup
- MinDiffAreaFileSize Backup
- OverallPerformanceSetting Backup
- SYSVOL Backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7058378561072bdc0f51abb455c098a22a9ad5e
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386785"
---
# <a name="registry-keys-and-values-for-backup-and-restore"></a>Chaves e valores do Registro para backup e restauração

Os aplicativos que solicitam ou executam operações de backup e restauração devem usar as seguintes chaves e valores do Registro para se comunicar entre si ou com recursos como o [VSS (Serviço de Cópias de Sombra de Volume)](/windows/desktop/VSS/volume-shadow-copy-service-portal) e Backup do Windows:

-   [CustomPerformanceSettings](#customperformancesettings)
-   [DisableMonitoring](#disablemonitoring)
-   [FilesNotToBackup](#filesnottobackup)
-   [FilesNotToSnapshot](#filesnottosnapshot)
-   [Idletimeout](#idletimeout)
-   [KeysNotToRestore](#keysnottorestore)
-   [LastInstance](#lastinstance)
-   [LastRestoreId](#lastrestoreid)
-   [MaxShadowCopies](#maxshadowcopies)
-   [MinDiffAreaFileSize](#mindiffareafilesize)
-   [OverallPerformanceSetting e CustomPerformanceSettings](#overallperformancesetting-and-customperformancesettings)
-   [SYSVOL](#sysvol)

## <a name="customperformancesettings"></a>CustomPerformanceSettings

Consulte [OverallPerformanceSetting e CustomPerformanceSettings](#overallperformancesetting-and-customperformancesettings).

## <a name="disablemonitoring"></a>DisableMonitoring

Em plataformas cliente Windows a partir do Windows 7, os usuários serão solicitados automaticamente a configurar o recurso Backup do Windows se ainda não o fizeram. Essas notificações aparecem no momento da inicialização do computador, começando sete dias após a instalação do sistema operacional. Eles também aparecem quando o usuário conecta uma unidade de disco rígido; nesse caso, as notificações aparecem imediatamente.

Os OEMs e os desenvolvedores de aplicativos de backup de terceiros podem usar o valor do Registro **DisableMonitoring** para desativar essas notificações automáticas.

Esse valor não existe por padrão, portanto, ele deve ser criado sob a seguinte chave do Registro:

**HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **WindowsBackup**

O **valor do Registro DisableMonitoring** tem o tipo de dados REG DWORD e é interpretado da seguinte \_ maneira:

-   Se os dados do valor estão definidos como 1 e se os usuários ainda não configuraram o recurso Backup do Windows, as notificações automáticas serão desligadas. Se uma notificação automática já estiver presente na Central de Ações, definir esse valor do Registro faz com que a notificação seja removida às 10h da manhã seguinte.
-   Se o valor não existir, se seus dados não estão definidos ou se seus dados estão definidos como zero, as notificações automáticas não serão desligadas.

**Windows Vista e Windows XP:** Não há suporte para esse valor do Registro.

## <a name="filesnottobackup"></a>FilesNotToBackup

A **chave do Registro FilesNotToBackup** especifica os nomes dos arquivos e diretórios que os aplicativos de backup não devem fazer backup ou restaurar. Cada uma das entradas nessa chave é uma cadeia de caracteres REG \_ MULTI \_ SZ no seguinte formato:

\[ \] Unidade \[  \] Caminho \\ *FileName* \[ /s\]

-   *A* unidade especifica a unidade e é opcional. Por exemplo, c:. Para especificar todas as unidades, use uma faixa invertida ( \\ ); nenhuma letra da unidade é necessária.
-   *Path* especifica o caminho e é opcional. Ele não pode conter caracteres curinga.
-   *FileName* especifica o arquivo ou diretório e é necessário. Ele pode conter caracteres curinga.
-   /s especifica que todos os subdireários do caminho especificado devem ser incluídos.
-   Variáveis de ambiente como %Systemroot% podem ser substituídas por toda ou parte da cadeia de caracteres inteira.

A tabela a seguir mostra algumas entradas típicas.

| Nome da entrada                             | Valor padrão                                                                             |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| Internet Explorer                      | Arquivos temporários                                                                           |
| Arquivo de página memória                       | \\Pagefile.sys                                                                            |
| MS Coordenador de Transações Distribuídas | C: \\ Windows \\ system32 \\ MSDtc \\ MSDTC. LOG C: \\ Windows \\ system32 \\ MSDtc \\ trace \\ dtctrace.log |
| cache Arquivos Offline dados                    | %Systemroot% \\ CSC \\ \* /s                                                                  |
| Gerenciamento de energia                       | \\hiberfil.sys                                                                            |
| Armazenamento de instância única                | \\SIS Common Store \\ \* . \* /s                                                              |
| Arquivos temporários                        | %TEMP% \\ \* /s                                                                             |



 

> [!Note]  
> Os aplicativos que executam backups em nível de volume geralmente fazem isso copiando todo o volume no nível do bloco, portanto, eles não podem cumprir a chave do Registro **FilesNotToBackup** no momento do backup. Em vez disso, eles esperam até o tempo de restauração para excluir os arquivos que não devem ser armazenados em backup. Na maioria dos casos, essa é uma estratégia razoável. No entanto, no caso de arquivos de Armazenamento de Instância Única, os arquivos do Armazenamento Comum do SIS não devem ser excluídos no momento da restauração.

 

Para backups de volume no nível de bloco, Backup do Windows Server e o utilitário Wbadmin do Windows adem a chave do Registro **FilesNotToBackup** excluindo os arquivos apropriados no momento da restauração. Restauração do Sistema e o Backup de Estado do Sistema não são a chave do Registro **FilesNotToBackup.**

**Windows XP:** Restauração do Sistema a chave do **Registro FilesNotToBackup.**

## <a name="filesnottosnapshot"></a>FilesNotToSnapshot

O VSS dá suporte à chave do Registro **FilesNotToSnapshot.** Os aplicativos e serviços podem usar essa chave para especificar arquivos a serem excluídos de cópias de sombra recém-criadas. Para obter mais informações, consulte [Excluindo arquivos de cópias de sombra.](/windows/desktop/VSS/excluding-files-from-shadow-copies)

**Windows Server 2003 e Windows XP:** Não há suporte para essa chave do Registro.

Para backups de volume no nível do bloco, Backup do Windows Server a chave do Registro **FilesNotToSnapshot** excluindo os arquivos apropriados no momento da restauração.

## <a name="idletimeout"></a>IdleTimeout

O **valor do Registro IdleTimeout** especifica a quantidade de tempo, em segundos, que o serviço VSS aguardará quando estiver ocioso. Se esse valor de tempoout for atingido e não houver nenhuma tarefa a ser executada, o serviço VSS será desligado.

Esse valor do Registro pode ser encontrado na seguinte chave do Registro:

**HKEY \_ Configurações \_ do** \\  \\ VSS do Sistema LOCAL MACHINE **CurrentControlSet** \\ **Services** \\  \\ 

Se esse valor do Registro não existir:

-   O valor de tempo máximo real usado é de 180 segundos (3 minutos) por padrão.
-   Você pode criar um valor com o nome **IdleTimeout** e o tipo DWORD e defini-lo como o valor desejado.

Se esse valor do Registro for definido como 0 segundo:

-   O valor de tempo máximo real usado é de 180 segundos (3 minutos).

Se você definir esse valor do Registro:

-   O VSS usa o valor de tempoout que você definiu.
-   Você pode especificar qualquer valor entre 1 e FFFFFFFF segundos. No entanto, é recomendável que você escolha um valor entre 1 e 180 segundos.

**Windows Server 2003 e Windows XP:** Não há suporte para essa chave do Registro.

## <a name="keysnottorestore"></a>KeysNotToRestore

A **chave do Registro KeysNotToRestore** especifica os nomes das sub-chaves do Registro e os valores que os aplicativos de backup não devem restaurar. Para obter mais informações, [consulte KeysNotToRestore](/previous-versions/windows/it-pro/windows-server-2003/cc737538(v=ws.10)). Não é necessário manter a chave do **Registro KeysNotToRestore.**

**Windows Server 2003 e Windows XP:** Você deve seguir a **chave do Registro KeysNotToRestore.**

Para backups de volume no nível do bloco, Backup do Windows Server a chave do Registro **KeysNotToRestore** excluindo os arquivos apropriados no momento da restauração.

O Backup de Estado do Sistema reconhece a chave do Registro **KeysNotToRestore.**

## <a name="lastinstance"></a>LastInstance

O **valor do Registro LastInstance** indica que uma operação de restauração bare-metal foi executada e que os volumes foram substituídos, mas não formatados. Para obter mais informações, consulte [Using VSS Automated Recuperação do Sistema for Disaster Recovery](/windows/desktop/VSS/using-vss-automated-system-recovery-for-disaster-recovery).

**Windows Server 2003 e Windows XP:** Não há suporte para esse valor do Registro.

## <a name="lastrestoreid"></a>LastRestoreId

Quando um aplicativo de backup executa uma restauração de estado do sistema, ele deve indicar que ele fez isso definindo o valor do Registro **LastRestoreId.** "Restauração de estado do sistema" nesse caso refere-se a qualquer restauração que restaura seletivamente binários e drivers do sistema operacional.

Se a inicialização inteira e o volume do sistema são restaurados no nível do volume, esse valor não deve ser definido.

Se o valor do Registro **LastRestoreId** não existir, o aplicativo de backup deverá criar sob a seguinte chave do Registro:

**HKEY \_ Backup \_ do** \\ **controle** \\ **CurrentControlSet** do sistema LOCAL \\  \\ **MACHINERestore** \\ **SystemStateRestore**

Crie um valor com o nome **LastRestoreId** e digite REG \_ SZ. O valor deve ser um valor opaco exclusivo, como um GUID.

Sempre que uma nova restauração de estado do sistema for executada, o aplicativo de backup deverá alterar os dados do **valor LastRestoreId.**

Outros aplicativos que precisam monitorar restaurações de estado do sistema devem armazenar os dados desse valor do Registro. Esses dados podem ser comparados com os dados atuais do valor do Registro **LastRestoreId** para determinar se uma nova restauração de estado do sistema foi executada.

**Windows Vista, Windows Server 2003 e Windows XP:** Esse valor do Registro não é suportado até que o Windows Vista com Service Pack 1 (SP1) e Windows Server 2008.

## <a name="maxshadowcopies"></a>MaxShadowCopies

O valor do Registro **MaxShadowCopies** especifica o número máximo de cópias de sombra acessíveis pelo cliente que podem ser [*armazenadas*](/windows/desktop/VSS/vssgloss-c) em cada volume do computador. Uma cópia de sombra acessível pelo cliente é uma cópia de sombra criada usando o valor **\_ \_ \_ ACESSÍVEL DO VSS CTX CLIENT** da [**\_ enumeração VSS \_ SNAPSHOT \_ CONTEXT.**](/windows/desktop/api/vss/ne-vss-vss_snapshot_context) As cópias de sombra acessíveis pelo cliente são usadas por Cópias de Sombra para Pastas Compartilhadas. Para obter mais informações sobre cópias de sombra, consulte a [documentação do VSS.](/windows/desktop/VSS/volume-shadow-copy-service-portal)

Se o valor do Registro **MaxShadowCopies** não existir, o aplicativo de backup poderá criar sob a seguinte chave do Registro:

**HKEY \_ Configurações \_ do** \\  \\ VSS do Sistema LOCAL MACHINE **CurrentControlSet** \\ **Services** \\  \\ 

Crie um valor com o nome **MaxShadowCopies e** digite DWORD. Os dados padrão para esse valor são 64. O mínimo é 1. O máximo é 512.

> [!Note]  
> Para outros tipos de cópias de sombra, não há nenhum valor do Registro que corresponda a **MaxShadowCopies.** O número máximo de cópias de sombra é 512 por volume.

 

**Observação**  A **configuração MaxShadowCopies** tem suporte no Windows Server 2003 ou posterior.

**Windows Server 2003:** Em servidores de cluster, os dados do valor do Registro **MaxShadowCopies** talvez precisem ser definidos como um número menor. Para obter mais informações, consulte "Quando você usa o Serviço de Cópias de Sombra de Volume em computadores baseados no Windows Server 2003 que executem muitas operações de E/S, os volumes de disco levam mais tempo para ficar online" na Base de Dados de Conhecimento de Ajuda e Suporte em [https://support.microsoft.com/kb/945058](https://support.microsoft.com/kb/945058) .

**Windows XP:** Não há suporte para esse valor do Registro.

## <a name="mindiffareafilesize"></a>MinDiffAreaFileSize

[O VSS](/windows/desktop/VSS/volume-shadow-copy-service-portal) aloca uma área de armazenamento de cópia de sombra (ou "área de comparação") para armazenar dados para cópias de sombra. O tamanho mínimo da área de armazenamento de cópia de sombra é uma configuração por computador que pode ser especificada usando o valor do Registro **MinDiffAreaFileSize.**

Se o valor do Registro **MinDiffAreaFileSize** não estiver definido, o tamanho mínimo da área de armazenamento de cópia de sombra será de 32 MB para volumes menores que 500 MB e 320 MB para volumes maiores que 500 MB.

**Windows Server 2008, Windows Server 2003 com SP1 e Windows Vista:** Se o valor do Registro **MinDiffAreaFileSize** não estiver definido, a área de armazenamento de cópia de sombra terá um tamanho mínimo de 300 MB. Se o valor do Registro **MinDiffAreaFileSize** estiver definido, seus dados deverão estar entre 300 MB e 3000 MB (3 GB) e devem ser múltiplos de 300 MB.

**Windows Server 2003:** Se o valor do Registro **MinDiffAreaFileSize** não estiver definido, o tamanho mínimo da área de armazenamento de cópia de sombra será de 100 MB.

**Windows XP:** Não há suporte para esse valor do Registro.

Se o valor do Registro **MinDiffAreaFileSize** não existir, o aplicativo de backup poderá criar sob a seguinte chave do Registro:

**HKEY \_ Sistema \_ LOCAL** \\ **MACHINE** \\ **CurrentControlSet** \\ **Services** \\ **Volsnap**

Crie um valor com o nome **MinDiffAreaFileSize e** digite REG \_ DWORD. Os dados dessa chave são especificados em megabytes. 320 é igual a 320 MB e 3200 é igual a 3,2 GB. Você deve especificar um número que seja um múltiplo de 32. Se você especificar um valor que não seja um múltiplo de 32, o próximo múltiplo de 32 será usado.

Cópias de sombra poderão não funcionar corretamente se o valor do Registro **MinDiffAreaFileSize** especificar um tamanho mínimo maior que o tamanho máximo da área de armazenamento de cópia de sombra. Para especificar o tamanho máximo da área de armazenamento de cópia de sombra, use o [comando Vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) add shadowstorage ou o comando Vssadmin resize shadowstorage. Para ver o tamanho máximo atual, use o [comando Vssadmin list shadowstorage.](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) Se você não tiver definido um tamanho máximo, não haverá limite para a quantidade de espaço que pode ser usada.

## <a name="overallperformancesetting-and-customperformancesettings"></a>OverallPerformanceSetting e CustomPerformanceSettings

Os valores de registro **OverallPerformanceSetting** e **CustomPerformanceSettings** são usados para especificar as configurações de desempenho para Backup do Windows Server. Esses valores do Registro têm suporte apenas em sistemas operacionais Windows Server.

**Windows Server 2003:** Não há suporte para esses valores do Registro.

Se esses valores do Registro não existirem, o aplicativo de backup poderá crie-os na seguinte chave do Registro:

**HKEY \_ SOFTWARE \_ LOCAL** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion Backup em** Nível de Bloco do \\ **Windows**

Para especificar as configurações de desempenho para todos os volumes, crie um valor com o nome **OverallPerformanceSetting** e digite REG \_ DWORD. Os dados do valor devem ser definidos como um dos valores a seguir.

| Valor | Significado                                                                                                                                                                                                                                   |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Desempenho de backup normal (usando backups completos). Essa configuração corresponde à configuração De desempenho de backup normal descrita em [Otimizando o backup e o desempenho do servidor.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11))            |
| 2     | Desempenho de backup mais rápido (usando backups incrementais). Essa configuração corresponde à configuração desempenho de backup mais rápido descrita em [Otimizando o backup e o desempenho do servidor.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11))     |
| 3     | Desempenho de backup personalizado (especificando uma configuração de desempenho para cada volume). Essa configuração corresponde à configuração Personalizada descrita em [Otimizando o backup e o desempenho do servidor.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11)) |



 

Se você definir **OverallPerformanceSetting** como 3, também deverá especificar as configurações de desempenho para cada volume individualmente. Para fazer isso, crie um valor com o nome **CustomPerformanceSettings** e digite REG \_ MULTI \_ SZ. Os dados desse valor devem ser definidos da seguinte forma:

-   Cada cadeia de caracteres na sequência de cadeias de caracteres REG \_ MULTI \_ SZ contém a configuração de um volume.
-   Cada cadeia de caracteres consiste em um GUID de volume, seguido por uma vírgula, seguido por um valor DWORD.
-   Cada um dos valores DWORD é 1 (backup completo) ou 2 (backup incremental).

Por exemplo, suponha que o computador tenha dois volumes da seguinte forma:

-   Os dois volumes são C: \\ e D: \\ .
-   O GUID do volume C: é \\ 07c473ca4-2df8-11de-9d80-806e6f6e6963 e o GUID do volume D: \\ é 0ac22ea6c-712f-11de-adb0-00215a67606e.
-   Você deseja especificar a persistência de backup normal para o volume C: e o desempenho de \\ backup mais rápido para o volume D: \\ .

Para fazer isso, você definiria **OverallPerformanceSetting** como 3 e **CustomPerformanceSettings** como "07c473ca4-2df8-11de-9d80-806e6f6e6963,1 \\ 00ac22ea6c-712f-11de-adb0-00215a67606e,2".

Se você definir **OverallPerformanceSetting** como 1 ou 2, os dados no valor **CustomPerformanceSettings** serão ignorados.

## <a name="sysvol"></a>SYSVOL

O **valor do Registro SYSVOL** é uma maneira de notificar o serviço DFSR (replicação Sistema de Arquivos Distribuído) de que uma operação de restauração de estado do sistema foi iniciada. Qualquer aplicativo de backup que executa a restauração de estado do sistema do SYSVOL deve usar esse valor para indicar se a operação de restauração é autoritativa ou não autoritativa. Esse valor é lido pelo serviço DFSR. Se esse valor não for definido, a restauração SYSVOL será executada de forma não autorizada por padrão.

Se o **valor do Registro SYSVOL** não existir, o aplicativo de backup deverá criar sob a seguinte chave do Registro:

**HKEY \_ Restauração \_ DO** \\  \\  \\  \\ **DFSR** do Sistema LOCAL MACHINE CurrentControlSet \\ **Services**

Crie um valor com o nome **SYSVOL e** digite REG \_ SZ. Os dados do valor devem ser definidos como "autoritativos" ou "não autoritativos" com base na solicitação do administrador do sistema.

**Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para esse valor de registro.

 

 
