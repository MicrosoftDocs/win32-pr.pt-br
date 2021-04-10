---
title: Chaves e valores do registro para backup e restauração
ms.assetid: 83449f78-cca1-449b-8c5f-3c8a91c8b3e7
description: 'Saiba mais sobre: chaves e valores do registro para backup e restauração'
keywords:
- backup de backup, chaves do registro
- Backup de chaves do registro
- Backup do CustomPerformanceSettings
- Backup do DisableMonitoring
- Backup do FilesNotToBackup
- Backup do FilesNotToSnapshot
- Backup do KeysNotToRestore
- Backup do LastInstance
- Backup do LastRestoreId
- Backup do MaxShadowCopies
- Backup do MinDiffAreaFileSize
- Backup do OverallPerformanceSetting
- Backup do SYSVOL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef9796ff96efbc20ac90de6d26a0c1bac7b17633
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089626"
---
# <a name="registry-keys-and-values-for-backup-and-restore"></a>Chaves e valores do registro para backup e restauração

Os aplicativos que solicitam ou executam operações de backup e restauração devem usar as seguintes chaves de registro e valores para se comunicarem entre si ou com recursos como o [serviço de cópias de sombra de volume (VSS)](/windows/desktop/VSS/volume-shadow-copy-service-portal) e o backup do Windows:

-   [CustomPerformanceSettings](#customperformancesettings)
-   [DisableMonitoring](#disablemonitoring)
-   [FilesNotToBackup](#filesnottobackup)
-   [FilesNotToSnapshot](#filesnottosnapshot)
-   [IdleTimeout](#idletimeout)
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

Em plataformas de cliente Windows que começam com o Windows 7, os usuários são automaticamente solicitados a configurar o recurso de backup do Windows, caso ainda não tenham feito isso. Essas notificações aparecem no momento da inicialização do computador, começando nos sete dias após a instalação do sistema operacional. Eles também aparecem quando o usuário se conecta a uma unidade de disco rígido; Nesse caso, as notificações são exibidas imediatamente.

Os OEMs e desenvolvedores de aplicativos de backup de terceiros podem usar o valor do registro **DisableMonitoring** para desativar essas notificações automáticas.

Esse valor não existe por padrão, portanto, deve ser criado na seguinte chave do registro:

**HKEY \_ SOFTWARE do \_ computador local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **WindowsBackup**

O valor do registro **DisableMonitoring** tem o tipo de dados reg \_ DWORD e é interpretado da seguinte maneira:

-   Se os dados do valor estiverem definidos como 1 e se os usuários ainda não tiverem configurado o recurso de backup do Windows, as notificações automáticas serão desativadas. Se uma notificação automática já estiver presente na central de ações, definir esse valor do registro fará com que a notificação seja removida às 10:00 da manhã seguinte.
-   Se o valor não existir, se seus dados não estiverem definidos ou se seus dados estiverem definidos como zero, as notificações automáticas não serão desativadas.

**Windows Vista e Windows XP:** Não há suporte para esse valor de registro.

## <a name="filesnottobackup"></a>FilesNotToBackup

A chave do registro **FilesNotToBackup** especifica os nomes dos arquivos e diretórios nos quais os aplicativos de backup não devem fazer backup ou restaurar. Cada uma das entradas dessa chave é uma cadeia de \_ caracteres reg multi \_ sz no seguinte formato:

\[ \] Unidade \[ *Caminho do* \] \\ *Nome do arquivo* \[ /s\]

-   *Unidade* especifica a unidade e é opcional. Por exemplo, c:. Para especificar todas as unidades, use uma barra invertida ( \) ; nenhuma letra de unidade é necessária.
-   *Caminho* especifica o caminho e é opcional. Ele não pode conter caracteres curinga.
-   *Filename* especifica o arquivo ou diretório e é necessário. Ele pode conter caracteres curinga.
-   /s especifica que todos os subdiretórios do caminho especificado devem ser incluídos.
-   Variáveis de ambiente como% SystemRoot% podem ser substituídas por toda ou parte da cadeia de caracteres inteira.

A tabela a seguir mostra algumas entradas típicas.

| Nome da entrada                             | Valor padrão                                                                             |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| Internet Explorer                      | Arquivos temporários                                                                           |
| Arquivo de página de memória                       | \\Pagefile.sys                                                                            |
| MS Coordenador de Transações Distribuídas | C: \\ Windows \\ System32 \\ MSDTC \\ MSDTC. LOG C: \\ Windows \\ System32 \\ MSDtc \\ trace \\ dtctrace. log |
| Cache Arquivos Offline                    | % SystemRoot% \\ CSC \\ \* /s                                                                  |
| Gerenciamento de energia                       | \\hiberfil.sys                                                                            |
| Armazenamento de instância única                | \\Repositório comum do SIS \\ \* . \* /s                                                              |
| Arquivos temporários                        | % TEMP% \\ \* /s                                                                             |



 

> [!Note]  
> Os aplicativos que executam backups em nível de volume geralmente fazem isso copiando o volume inteiro no nível de bloco, para que eles não aceitem a chave do registro **FilesNotToBackup** no momento do backup. Em vez disso, eles esperam até que o tempo de restauração exclua os arquivos cujo backup não foi feito. Na maioria dos casos, essa é uma estratégia razoável. No entanto, no caso de arquivos de armazenamento de instância única, os arquivos de repositório comuns do SIS não devem ser excluídos no momento da restauração.

 

Para backups de volume em nível de bloco, Backup do Windows Server e o utilitário Windows Wbadmin honram a chave do registro **FilesNotToBackup** excluindo os arquivos apropriados no momento da restauração. A restauração do sistema e o backup do estado do sistema não respeitam a chave do registro **FilesNotToBackup** .

**Windows XP:** A restauração do sistema honra a chave do registro **FilesNotToBackup** .

## <a name="filesnottosnapshot"></a>FilesNotToSnapshot

O VSS dá suporte à chave do registro **FilesNotToSnapshot** . Aplicativos e serviços podem usar essa chave para especificar arquivos a serem excluídos de cópias de sombra recém-criadas. Para obter mais informações, consulte [excluindo arquivos de cópias de sombra](/windows/desktop/VSS/excluding-files-from-shadow-copies).

**Windows Server 2003 e Windows XP:** Não há suporte para essa chave do registro.

Para backups de volume em nível de bloco, Backup do Windows Server honra a chave do registro **FilesNotToSnapshot** excluindo os arquivos apropriados no momento da restauração.

## <a name="idletimeout"></a>IdleTimeout

O valor do registro **IdleTimeout** especifica a quantidade de tempo, em segundos, que o serviço VSS aguardará quando estiver ocioso. Se esse valor de tempo limite for atingido e não houver tarefas a serem executadas, o serviço VSS será desligado.

Esse valor de registro pode ser encontrado na seguinte chave do registro:

**HKEY \_ \_** Configurações de \\  \\  \\  \\ **VSS** \\  dos serviços do sistema de computador local CurrentControlSet

Se esse valor de registro não existir:

-   O valor de tempo limite real que é usado é de 180 segundos (3 minutos) por padrão.
-   Você pode criar um valor com o nome **IdleTimeout** e o tipo DWORD e defini-lo como o valor desejado.

Se esse valor de registro for definido como 0 segundos:

-   O valor de tempo limite real que é usado é de 180 segundos (3 minutos).

Se você definir esse valor de registro:

-   O VSS usa o valor de tempo limite que você definiu.
-   Você pode especificar qualquer valor entre 1 e FFFFFFFF segundos. No entanto, é recomendável que você escolha um valor entre 1 e 180 segundos.

**Windows Server 2003 e Windows XP:** Não há suporte para essa chave do registro.

## <a name="keysnottorestore"></a>KeysNotToRestore

A chave do registro **KeysNotToRestore** especifica os nomes das subchaves do registro e os valores que os aplicativos de backup não devem restaurar. Para obter mais informações, consulte [KeysNotToRestore](/previous-versions/windows/it-pro/windows-server-2003/cc737538(v=ws.10)). Não é necessário respeitar a chave do registro **KeysNotToRestore** .

**Windows Server 2003 e Windows XP:** Você deve respeitar a chave do registro **KeysNotToRestore** .

Para backups de volume em nível de bloco, Backup do Windows Server honra a chave do registro **KeysNotToRestore** excluindo os arquivos apropriados no momento da restauração.

O backup do estado do sistema honra a chave do registro **KeysNotToRestore** .

## <a name="lastinstance"></a>LastInstance

O valor do registro **LastInstance** indica que uma operação de Restauração bare-metal foi executada e que os volumes foram substituídos, mas não formatados. Para obter mais informações, consulte [usando a recuperação automatizada do sistema VSS para recuperação de desastre](/windows/desktop/VSS/using-vss-automated-system-recovery-for-disaster-recovery).

**Windows Server 2003 e Windows XP:** Não há suporte para esse valor de registro.

## <a name="lastrestoreid"></a>LastRestoreId

Quando um aplicativo de backup executa uma restauração de estado do sistema, ele deve indicar que ele fez isso definindo o valor do registro **LastRestoreId** . "Restauração do estado do sistema", nesse caso, refere-se a qualquer restauração que restaura de forma seletiva os binários e drivers do sistema operacional.

Se toda a inicialização e o volume do sistema forem restaurados no nível do volume, esse valor não deverá ser definido.

Se o valor do registro **LastRestoreId** não existir, o aplicativo de backup deverá criá-lo na seguinte chave do registro:

**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Control** \\ **BackupRestore** \\ **SystemStateRestore**

Crie um valor com o nome **LastRestoreId** e digite reg \_ sz. O valor deve ser um valor opaco exclusivo, como um GUID.

Sempre que uma nova restauração de estado do sistema é executada, o aplicativo de backup deve alterar os dados do valor **LastRestoreId** .

Outros aplicativos que precisam monitorar restaurações de estado do sistema devem armazenar os dados desse valor de registro. Esses dados podem ser comparados com os dados atuais do valor do registro **LastRestoreId** para determinar se uma nova restauração de estado do sistema foi executada.

**Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para esse valor de registro até o Windows Vista com Service Pack 1 (SP1) e o Windows Server 2008.

## <a name="maxshadowcopies"></a>MaxShadowCopies

O valor do registro **MaxShadowCopies** especifica o número máximo de [*cópias de sombra acessíveis ao cliente*](/windows/desktop/VSS/vssgloss-c) que podem ser armazenadas em cada volume do computador. Uma cópia de sombra acessível pelo cliente é uma cópia de sombra criada usando o **valor \_ \_ \_ acessível do cliente VSS CTX** da enumeração de [**\_ \_ \_ contexto de instantâneo do VSS**](/windows/desktop/api/vss/ne-vss-vss_snapshot_context) . As cópias de sombra acessíveis pelo cliente são usadas por Cópias de Sombra para Pastas Compartilhadas. Para obter mais informações sobre cópias de sombra, consulte a documentação do [VSS](/windows/desktop/VSS/volume-shadow-copy-service-portal) .

Se o valor do registro **MaxShadowCopies** não existir, o aplicativo de backup poderá criá-lo na seguinte chave do registro:

**HKEY \_ \_** Configurações de \\  \\  \\  \\ **VSS** \\  dos serviços do sistema de computador local CurrentControlSet

Crie um valor com o nome **MaxShadowCopies** e digite DWORD. Os dados padrão para esse valor são 64. O mínimo é 1. O máximo é 512.

> [!Note]  
> Para outros tipos de cópias de sombra, não há nenhum valor de registro que corresponda a **MaxShadowCopies**. O número máximo de cópias de sombra é de 512 por volume.

 

**Observação**  A configuração **MaxShadowCopies** tem suporte no Windows Server 2003 ou posterior.

**Windows Server 2003:** Em servidores de cluster, os dados do valor do registro **MaxShadowCopies** podem precisar ser definidos como um número mais baixo. Para obter mais informações, consulte "quando você usa o Serviço de Cópias de Sombra de Volume em computadores com base no Windows Server 2003 que executam várias operações de e/s, os volumes de disco levam mais tempo para ficar online" na base de dados de conhecimento de ajuda e suporte em [https://support.microsoft.com/kb/945058](https://support.microsoft.com/kb/945058) .

**Windows XP:** Não há suporte para esse valor de registro.

## <a name="mindiffareafilesize"></a>MinDiffAreaFileSize

O [VSS](/windows/desktop/VSS/volume-shadow-copy-service-portal) aloca uma área de armazenamento de cópia de sombra (ou "área de comparação") para armazenar dados para cópias de sombra. O tamanho mínimo da área de armazenamento de cópia de sombra é uma configuração por computador que pode ser especificada usando o valor do registro **MinDiffAreaFileSize** .

Se o valor do registro **MinDiffAreaFileSize** não for definido, o tamanho mínimo da área de armazenamento de cópia de sombra será de 32 MB para volumes menores que 500 mb e 320 MB para volumes maiores que 500 MB.

**Windows server 2008, Windows server 2003 com SP1 e Windows Vista:** Se o valor do registro **MinDiffAreaFileSize** não for definido, a área de armazenamento de cópia de sombra terá um tamanho mínimo de 300 MB. Se o valor do registro **MinDiffAreaFileSize** for definido, seus dados deverão estar entre 300 mb e 3000 MB (3 GB) e deve ser um múltiplo de 300 MB.

**Windows Server 2003:** Se o valor do registro **MinDiffAreaFileSize** não for definido, o tamanho mínimo da área de armazenamento de cópia de sombra será de 100 MB.

**Windows XP:** Não há suporte para esse valor de registro.

Se o valor do registro **MinDiffAreaFileSize** não existir, o aplicativo de backup poderá criá-lo na seguinte chave do registro:

**HKEY \_ Sistema de \_ computador local** \\  \\ **CurrentControlSet** \\ **Serviços** de \\ **VolSnap**

Crie um valor com o nome **MinDiffAreaFileSize** e digite reg \_ DWORD. Os dados dessa chave são especificados em megabytes. 320 é igual a 320 MB e 3200 é igual a 3,2 GB. Você deve especificar um número que seja um múltiplo de 32. Se você especificar um valor que não seja um múltiplo de 32, o próximo múltiplo de 32 será usado.

As cópias de sombra podem não funcionar corretamente se o valor do registro **MinDiffAreaFileSize** especifica um tamanho mínimo maior que o tamanho máximo da área de armazenamento de cópia de sombra. Para especificar o tamanho máximo da área de armazenamento de cópia de sombra, use o comando [vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) Add ShadowStorage ou vssadmin Resize ShadowStorage. Para ver o tamanho máximo atual, use o comando [VSSadmin list ShadowStorage](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) . Se você não tiver definido um tamanho máximo, não haverá nenhum limite para a quantidade de espaço que pode ser usada.

## <a name="overallperformancesetting-and-customperformancesettings"></a>OverallPerformanceSetting e CustomPerformanceSettings

Os valores do registro **OverallPerformanceSetting** e **CustomPerformanceSettings** são usados para especificar configurações de desempenho para backup do Windows Server. Esses valores de registro têm suporte apenas em sistemas operacionais Windows Server.

**Windows Server 2003:** Não há suporte para esses valores de registro.

Se esses valores de registro não existirem, o aplicativo de backup poderá criá-los na seguinte chave do registro:

**HKEY \_ SOFTWARE do \_ computador local** \\  \\ backup do nível de bloco **do Windows do Microsoft** \\ **Windows** \\ **CurrentVersion** \\ 

Para especificar configurações de desempenho para todos os volumes, crie um valor com o nome **OverallPerformanceSetting** e digite reg \_ DWORD. Os dados do valor devem ser definidos como um dos valores a seguir.

| Valor | Significado                                                                                                                                                                                                                                   |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Desempenho normal do backup (usando backups completos). Essa configuração corresponde à configuração de desempenho de backup normal descrita em [otimizando o backup e o desempenho do servidor](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11)).            |
| 2     | Desempenho de backup mais rápido (usando backups incrementais). Essa configuração corresponde à configuração de desempenho de backup mais rápida descrita em [otimizando o desempenho do backup e do servidor](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11)).     |
| 3     | Desempenho de backup personalizado (especificando uma configuração de desempenho para cada volume). Essa configuração corresponde à configuração personalizada descrita em [otimizando o backup e o desempenho do servidor](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11)). |



 

Se você definir **OverallPerformanceSetting** como 3, também deverá especificar as configurações de desempenho para cada volume individualmente. Para fazer isso, crie um valor com o nome **CustomPerformanceSettings** e digite reg \_ multi \_ sz. Os dados deste valor devem ser definidos da seguinte maneira:

-   Cada cadeia de caracteres na \_ \_ sequência de cadeias de caracteres reg de vários sz contém a configuração de um volume.
-   Cada cadeia de caracteres consiste em um GUID de volume, seguido por uma vírgula, seguida por um valor DWORD.
-   Cada um dos valores DWORD é 1 (backup completo) ou 2 (backup incremental).

Por exemplo, suponha que o computador tenha dois volumes da seguinte maneira:

-   Os dois volumes são C: \\ e D: \\ .
-   O GUID do volume C: \\ é 07c473ca4-2df8-11de-9d80-806e6f6e6963 e o GUID do volume D: \\ é 0ac22ea6c-712f-11de-adb0-00215a67606e.
-   Você deseja especificar o backup normal perfornance para o volume C: \\ e o desempenho de backup mais rápido para o volume D: \\ .

Para fazer isso, você definiria **OverallPerformanceSetting** como 3 e **CustomPerformanceSettings** como "07c473ca4-2df8-11de-9d80-806e6f6e6963, 1 \\ 00ac22ea6c-712f-11de-adb0-00215a67606e, 2".

Se você definir **OverallPerformanceSetting** como 1 ou 2, os dados no valor de **CustomPerformanceSettings** serão ignorados.

## <a name="sysvol"></a>SYSVOL

O valor do registro **SYSVOL** é uma maneira de notificar o serviço de replicação de sistema de arquivos distribuído (DFSR) que uma operação de restauração de estado do sistema foi iniciada. Qualquer aplicativo de backup que executa a restauração do estado do sistema do SYSVOL deve usar esse valor para indicar se a operação de restauração é autoritativa ou não autoritativa. Esse valor é lido pelo serviço DFSR. Se esse valor não for definido, a restauração do SYSVOL será executada de forma não autoritativa por padrão.

Se o valor do registro **SYSVOL** não existir, o aplicativo de backup deverá criá-lo na seguinte chave do registro:

**HKEY \_ Sistema de \_ computador local** \\  \\ **CurrentControlSet** \\ **Serviços** \\  \\ **restauração** de DFSR

Crie um valor com o nome **SYSVOL** e digite reg \_ sz. Os dados do valor devem ser definidos como "autoritativo" ou "não autoritativo" com base na solicitação do administrador do sistema.

**Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para esse valor de registro.

 

 
