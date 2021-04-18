---
description: O sistema operacional Windows inclui um conjunto de gravadores do VSS responsáveis por enumerar os dados exigidos por vários recursos do Windows. Eles são chamados de &\# 0034;&s in box \# 0034; gravadores.
ms.assetid: e20a303d-9440-42be-b383-85f6fad89157
title: Gravadores do VSS In-Box
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc256cfe72f3653d4af282148c87c2b45bcac51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763415"
---
# <a name="in-box-vss-writers"></a>Gravadores do VSS In-Box

O sistema operacional Windows inclui um conjunto de gravadores do VSS responsáveis por enumerar os dados exigidos por vários recursos do Windows. Eles são chamados de gravadores "in-box".

> [!Note]  
> O gravador in-box do MSDE não está disponível no Windows Vista, no Windows Server 2008 e posterior. Em vez disso, o gravador do SQL deve ser usado para fazer backup de bancos de dados do SQL Server. Somente SQL Server 2005 SP2 e posterior têm suporte no Windows Vista, no Windows Server 2008 e posterior.

 

-   [Gravador VSS do Active Directory Domain Services (NTDS)](#active-directory-domain-services-ntds-vss-writer)
-   [Gravador de Serviços de Federação do Active Directory (AD FS)](#active-directory-federation-services-writer)
-   [Gravador VSS do serviços AD LDS (LDS)](#active-directory-lightweight-directory-services-lds-vss-writer)
-   [Gravador de Active Directory Rights Management Services (AD RMS)](#active-directory-rights-management-services-ad-rms-writer)
-   [Gravador ASR (recuperação automatizada do sistema)](#automated-system-recovery-asr-writer)
-   [Gravador de Serviço de Transferência Inteligente em Segundo Plano (BITS)](#background-intelligent-transfer-service-bits-writer)
-   [Gravador de autoridade de certificação](#certificate-authority-writer)
-   [Gravador do serviço de cluster](#cluster-service-writer)
-   [Gravador VSS de Volume Compartilhado Clusterizado (CSV)](#cluster-shared-volume-csv-vss-writer)
-   [Gravador de banco de dados de registro de classe COM+](#com-class-registration-database-writer)
-   [Gravador de eliminação de duplicação de dados](#data-deduplication-writer)
-   [Replicação de Sistema de Arquivos Distribuído (DFSR)](#distributed-file-system-replication-dfsr)
-   [Gravador DHCP (protocolo de configuração dinâmica de hosts)](#dynamic-host-configuration-protocol-dhcp-writer)
-   [FRS (Serviço de Replicação de Arquivos)](#file-replication-service-frs)
-   [Gravador FSRM (Gerenciador de recursos de servidor de arquivos)](#file-server-resource-manager-fsrm-writer)
-   [Gravador do Hyper-V](#hyper-v-writer)
-   [Gravador de configuração do IIS](#iis-configuration-writer)
-   [Gravador de metabase do IIS](#iis-metabase-writer)
-   [Gravador MSMQ (enfileiramento de mensagens da Microsoft)](#microsoft-message-queuing-msmq-writer)
-   [Gravador de serviço MSSearch](#mssearch-service-writer)
-   [Gravador VSS do NPS](#nps-vss-writer)
-   [Gravador de contadores de desempenho](#performance-counters-writer)
-   [Gravador do registro](#registry-writer)
-   [Gravador VSS do gateway de Serviços de Área de Trabalho Remota (serviços de terminal)](#remote-desktop-services-terminal-services-gateway-vss-writer)
-   [Gravador VSS de licenciamento do Serviços de Área de Trabalho Remota (serviços de terminal)](#remote-desktop-services-terminal-services-licensing-vss-writer)
-   [Gravador de otimização de cópia de sombra](#shadow-copy-optimization-writer)
-   [Gravador do serviço de compartilhamento de sincronização](#sync-share-service-writer)
-   [Gravador do sistema](#system-writer)
-   [Gravador de Agendador de Tarefas](#task-scheduler-writer)
-   [Gravador de repositório de metadados do VSS](#vss-metadata-store-writer)
-   [Gravador do WDS (serviços de implantação do Windows)](#windows-deployment-services-wds-writer)
-   [Gravador do banco de dados interno do Windows (WID)](#windows-internal-database-wid-writer)
-   [Gravador WINS (serviço de cadastramento na Internet do Windows)](#windows-internet-name-service-wins-writer)
-   [Gravador WMI](#wmi-writer)

## <a name="active-directory-domain-services-ntds-vss-writer"></a>Gravador VSS do Active Directory Domain Services (NTDS)

Esse gravador relata o arquivo de banco de dados NTDS (Ntds. dit) e os arquivos de log associados. Esses arquivos são necessários para restaurar o Active Directory corretamente.

Há apenas um arquivo NTDS. dit por controlador de domínio e é relatado nos metadados do gravador, como no exemplo a seguir:

``` syntax
    <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
```

Aqui está um exemplo que mostra como listar os componentes nos metadados do gravador:

``` syntax
    <BACKUP_LOCATIONS>
        <DATABASE logicalPath="C:_Windows_NTDS" 
                     componentName="ntds" 
                     caption="" restoreMetadata="no" 
                     notifyOnBackupComplete="no" 
                     selectable="no" 
                     selectableForRestore="no" 
                     componentFlags="3">
        <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Windows\NTDS" 
                     filespec="edb*.log" 
                     filespecBackupType="3855"/> 
        <DATABASE_LOGFILES path="C:\Windows\NTDS" 
                     filespec="edb.chk" 
                     filespecBackupType="3855"/>
        </DATABASE>
    </BACKUP_LOCATIONS>
```

No momento do backup, o gravador define o tempo de expiração de backup nos metadados de backup do gravador. Os solicitantes devem recuperar esses metadados usando [**IVssComponent:: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) para determinar se o banco de dados expirou. Bancos de dados expirados não podem ser restaurados.

Se o computador que contém o banco de dados NTDS for um controlador de domínio, o aplicativo de backup sempre deverá executar um backup de estado do sistema em todos os volumes que contenham informações críticas do estado do sistema. No momento da restauração, o aplicativo deve primeiro reiniciar o computador em Modo de Restauração dos Serviços de Diretório e, em seguida, executar uma restauração de estado do sistema.

A cadeia de caracteres do nome do gravador para esse gravador é "NTDS".

A ID do gravador para este gravador é B2014C9E-8711-4C5C-A5A9-3CF384484757.

## <a name="active-directory-federation-services-writer"></a>Gravador de Serviços de Federação do Active Directory (AD FS)

Esse gravador relata os arquivos de dados do Serviços de Federação do Active Directory (AD FS) (ADFS).

**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para esse gravador.

A cadeia de caracteres do nome do gravador para esse gravador é "gravador VSS do ADFS".

A ID do gravador para este gravador é 772C45F8-AE01-4F94-940C-94961864ACAD.

## <a name="active-directory-lightweight-directory-services-lds-vss-writer"></a>Gravador VSS do serviços AD LDS (LDS)

Esse gravador relata o arquivo de banco de dados ADAM (Adamntds. dit) e os arquivos de log associados para cada instância em% Program Files% \\ Microsoft Adam \\ Instance *n* \\ data, em que *N* é o número da instância do Adam. Esses arquivos de log de banco de dados são necessários para restaurar instâncias do ADAM.

**Windows XP:** Não há suporte para esse gravador.

Aqui está um exemplo que mostra como listar os componentes nos metadados do gravador:

``` syntax
    <BACKUP_LOCATIONS>
        <DATABASE logicalPath="C:_Program Files_Microsoft ADAM_instance1_data" 
                     componentName="adamntds" 
                     caption="" 
                     restoreMetadata="no" 
                     notifyOnBackupComplete="no" 
                     selectable="no" 
                     selectableForRestore="no" 
                     componentFlags="3">
        <DATABASE_FILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="adamntds.dit" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="edb*.log" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="edb.chk" 
                     filespecBackupType="3855"/>
        </DATABASE>
    </BACKUP_LOCATIONS>
```

No momento do backup, o gravador define o tempo de expiração de backup nos metadados de backup. Os aplicativos de backup devem recuperar esses metadados usando o método [**IVssComponent:: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) para determinar se o banco de dados expirou. Bancos de dados expirados não podem ser restaurados.

A cadeia de caracteres do nome do gravador para esse gravador é "ADAM (Instance *N*) Writer", em que *N* é o número da instância do Adam, por exemplo, "Adam (instance1) Writer", "Adam (Instance2) Writer" e assim por diante.

A ID do gravador para este gravador é DD846AAA-A1B6-42A8-AAF8-03DCB6114BFD. Essa ID de gravador é a mesma para todas as instâncias.

## <a name="active-directory-rights-management-services-ad-rms-writer"></a>Gravador de Active Directory Rights Management Services (AD RMS)

Esse gravador relata os arquivos de dados do AD RMS (serviço de Active Directory Rights Management).

**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para esse gravador.

A cadeia de caracteres do nome do gravador para este gravador é "gravador de AD RMS".

A ID do gravador para este gravador é 886C43B1-D455-4428-A37F-4D6B9E43F50F.

## <a name="automated-system-recovery-asr-writer"></a>Gravador ASR (recuperação automatizada do sistema)

O gravador ASR armazena a configuração de discos no sistema. Esse gravador relata o banco de dados de configuração de inicialização (BCD) e também é responsável por desmontar o hive do registro que representa o BCD durante a criação da cópia de sombra. O gravador ASR deve ser incluído em todos os backups necessários para a recuperação bare-metal. Para obter mais informações sobre o ASR, consulte [usando a recuperação automatizada do sistema VSS para recuperação de desastre](using-vss-automated-system-recovery-for-disaster-recovery.md).

**Windows Server 2003 e Windows XP:** Não há suporte para esse gravador.

A cadeia de caracteres do nome do gravador para este gravador é "gravador ASR".

A ID do gravador para o gravador de ASR é BE000CBE-11FE-4426-9C58-531AA6355FC4.

## <a name="background-intelligent-transfer-service-bits-writer"></a>Gravador de Serviço de Transferência Inteligente em Segundo Plano (BITS)

O gravador BITS usa a chave do registro **FilesNotToBackup** para excluir arquivos da pasta de cache bits. O local do cache padrão é% AllUsersProfile% \\ do cache do Microsoft \\ Network \\ Downloader \\ .

**Windows Server 2003 e Windows XP:** Não há suporte para esse gravador.

Além disso, o gravador BITS exclui os seguintes arquivos do backup: os arquivos de estado do BITS (Qmgr0. dat e Qmgr1. dat), o arquivo de log de depuração BITS e os arquivos parcialmente baixados do BITS.

Se o arquivo de destino do download do BITS for um arquivo SMB, a conta do cliente deverá ter uma relação de confiança com o servidor ou os backups poderão falhar.

A cadeia de caracteres do nome do gravador para este gravador é "gravador BITS".

A ID do gravador para o gravador BITS é 4969D978-BE47-48B0-B100-F328F07AC1E0.

## <a name="certificate-authority-writer"></a>Gravador de autoridade de certificação

Esse gravador é responsável por enumerar os arquivos de dados para o servidor de certificado.

A cadeia de caracteres do nome do gravador para esse gravador é "autoridade de certificação".

**Windows XP:** A cadeia de caracteres do nome do gravador para esse gravador é "gravador do servidor de certificado".

A ID do gravador para o gravador é 6F5B15B5-DA24-4D88-B737-63063E3A1F86.

## <a name="cluster-service-writer"></a>Gravador do serviço de cluster

O gravador VSS do serviço de cluster está documentado na documentação da API do [serviço de cluster](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) .

**Windows Vista, Windows Server 2003 e Windows XP:** Esse gravador não tem suporte até o Windows Vista com Service Pack 1 (SP1) e o Windows Server 2008.

## <a name="cluster-shared-volume-csv-vss-writer"></a>Gravador VSS de Volume Compartilhado Clusterizado (CSV)

Esse gravador relata os arquivos de dados de Volume Compartilhado Clusterizado (CSV). Esse gravador é um gravador in-box para versões do sistema operacional Windows Server; Ele não é fornecido no Windows Client.

**Windows server 2008 R2, Windows server 2008 e Windows server 2003:** Não há suporte para esse gravador.

A cadeia de caracteres do nome do gravador para este gravador é "Volume Compartilhado Clusterizado gravador VSS".

A ID do gravador para o gravador é 1072AE1C-E5A7-4EA1-9E4A-6F7964656570.

## <a name="com-class-registration-database-writer"></a>Gravador de banco de dados de registro de classe COM+

Esse gravador é responsável pelo conteúdo do diretório de registro% SystemRoot% \\ . O catálogo COM+ é um arquivo no registro de% SystemRoot% \\ com um nome que segue o padrão R *xxxxxxxxxxxx*. CLB, em que *xxxxxxxxxxxx* é um número hexadecimal de 12 dígitos. Potencialmente, pode haver vários arquivos desse tipo se os aplicativos COM+ tiverem sido configurados no computador. O arquivo que contém o catálogo COM+ atual é o arquivo com o maior valor de *xxxxxxxxxxxx*.

**Windows Server 2003 e Windows XP:** Não há suporte para esse gravador.

O banco de dados de registro de classe COM+ depende de uma chave de registro que está sendo submetida a backup e, portanto, precisa de backup e restauração junto com o registro.

Para restaurar o banco de dados de registro do COM+, um aplicativo de backup (solicitante) deve chamar o método [**ICOMAdminCatalog:: RestoreREGDB**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) .

A cadeia de caracteres do nome do gravador para este gravador é "COM+ REGDB Writer".

A ID do gravador do gravador de banco de dados de registro de classe COM+ é 542DA469-D3E1-473C-9F4F-7847F01FC64F.

## <a name="data-deduplication-writer"></a>Gravador de eliminação de duplicação de dados

O gravador VSS de eliminação de duplicação de dados está documentado na documentação da API de [eliminação de duplicação de dados](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) . Esse gravador é um gravador in-box para versões do sistema operacional Windows Server; Ele não é fornecido no Windows Client.

**Windows server 2008 R2, Windows server 2008 e Windows server 2003:** Não há suporte para esse gravador.

## <a name="distributed-file-system-replication-dfsr"></a>Replicação de Sistema de Arquivos Distribuído (DFSR)

O componente a seguir inclui um gravador VSS: [replicação de sistema de arquivos distribuído (DFSR)](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)

**Windows Vista, Windows Server 2003 e Windows XP:** Esse gravador não tem suporte até o Windows Vista com SP1 e o Windows Server 2008.

## <a name="dynamic-host-configuration-protocol-dhcp-writer"></a>Gravador DHCP (protocolo de configuração dinâmica de hosts)

Esse gravador é responsável por enumerar os arquivos necessários para a função de servidor DHCP. Esse gravador é um gravador in-box para versões do sistema operacional Windows Server; Ele não é fornecido no Windows Client.

A cadeia de caracteres do nome do gravador para este gravador é "gravador Jet do DHCP".

A ID do gravador para este gravador é BE9AC81E-3619-421F-920F-4C6FEA9E93AD.

## <a name="file-replication-service-frs"></a>FRS (Serviço de Replicação de Arquivos)

O gravador do serviço de replicação de arquivo está documentado em [backup e restauração de uma pasta FRS-Replicated SYSVOL](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md).

**Windows Vista, Windows Server 2003 e Windows XP:** Esse gravador não tem suporte até o Windows Vista com SP1 e o Windows Server 2008.

## <a name="file-server-resource-manager-fsrm-writer"></a>Gravador FSRM (Gerenciador de recursos de servidor de arquivos)

Esse gravador enumera os arquivos de configuração do FSRM que são usados para o backup do estado do sistema. Durante as operações de restauração, ela impede alterações na configuração do FSRM e interrompe temporariamente a imposição de cotas e de triagens de arquivos. Depois que a restauração for concluída, o gravador atualizará o FSRM com a configuração restaurada. Esse gravador só está presente quando o FSRM (parte da função de serviços de arquivos) está instalado e em execução. Esse gravador é um gravador in-box para versões do sistema operacional Windows Server; Ele não é fornecido no Windows Client.

**Windows Server 2003:** Esse gravador não tem suporte até o Windows Server 2003 R2.

A cadeia de caracteres do nome do gravador para esse gravador é "gravador FSRM".

A ID do gravador para este gravador é 12CE4370-5BB7-4C58-A76A-E5D5097E3674.

## <a name="hyper-v-writer"></a>Gravador do Hyper-V

O gravador VSS do Hyper-V está documentado na documentação da API do [Hyper-v](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines) . Esse gravador é um gravador in-box para versões do sistema operacional Windows Server; Ele não é fornecido no Windows Client.

**Windows Server 2003:** Esse gravador não tem suporte até o Windows Server 2008.

## <a name="iis-configuration-writer"></a>Gravador de configuração do IIS

O gravador de configuração do IIS é responsável por enumerar os arquivos de configuração do IIS.

**Windows Vista, Windows Server 2003 e Windows XP:** Esse gravador não tem suporte até o Windows Vista com SP1 e o Windows Server 2008. Os solicitantes são necessários para fazer backup dos arquivos de configuração do IIS, incluindo o arquivo de machine.config do .NET FX ou o arquivo de web.config raiz do ASP.NET.

Esse gravador não faz backup do arquivo de machine.config do .NET FX ou do arquivo de web.config raiz ASP.NET porque esses arquivos são enumerados pelo gravador do sistema.

Esse gravador faz backup de todos os arquivos que estão nos diretórios de configuração% windir% \\ System32 \\ inetsrv \\ \\ e% WINDIR% \\ System32 \\ inetsrv \\ , exceto pelos arquivos enumerados pelo gravador do sistema.

A ID do gravador para o gravador de configuração do IIS é 2A40FD15-DFCA-4aa8-A654-1F8C654603F6.

## <a name="iis-metabase-writer"></a>Gravador de metabase do IIS

O gravador de metabase do IIS (servidor de informações da Internet) é responsável por enumerar o arquivo de metabase do IIS.

**Windows Vista, Windows Server 2003 e Windows XP:** Esse gravador não tem suporte até o Windows Vista com SP1 e o Windows Server 2008. Os solicitantes são necessários para fazer backup do arquivo da metabase do IIS.

A ID do gravador para o gravador da metabase do IIS é 59B1f0CF-90EF-465F-9609-6CA8B2938366.

## <a name="microsoft-message-queuing-msmq-writer"></a>Gravador MSMQ (enfileiramento de mensagens da Microsoft)

Esse gravador relata os arquivos de dados do MSMQ (enfileiramento de mensagens da Microsoft).

**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para esse gravador.

A cadeia de caracteres do nome do gravador para esse gravador é "MSMQ Writer (*SvcName*)", em que *SvcName* é o nome do serviço MSMQ ao qual o gravador está associado. Para a instalação padrão, o nome do serviço é "MSMQ". Para instâncias clusterizadas, o nome do serviço é MSMQ $*resourceName*, em que *resourceName* é o nome do recurso MSMQ clusterizado.

A ID do gravador para este gravador é 7E47B561-971A-46E6-96B9-696EEAA53B2A.

## <a name="mssearch-service-writer"></a>Gravador de serviço MSSearch

Esse gravador existe para excluir arquivos de índice de pesquisa de cópias de sombra após a criação. Isso é feito para minimizar o impacto da e/s de cópia em gravação durante e/s regular nesses arquivos no volume copiado por sombra.

**Windows Server 2003:** Não há suporte para esse gravador.

Para instalar esse gravador no servidor, você deve instalar a função serviços de arquivo e habilitar a Serviço de Pesquisa do Windows.

A cadeia de caracteres do nome do gravador para esse gravador é "gravador de serviço MSSearch".

A ID do gravador para o gravador de serviço MSSearch é CD3F2362-8BEF-46C7-9181-D62844CDC0B2.

## <a name="nps-vss-writer"></a>Gravador VSS do NPS

O gravador do NPS é responsável por enumerar os arquivos de configuração do NPS (servidor de diretivas de rede) para servidores que têm a função de serviços de acesso e política de rede instalada.

**Windows Vista, Windows Server 2003 e Windows XP:** Esse gravador não tem suporte até o Windows Vista com SP1 e o Windows Server 2008.

A cadeia de caracteres do nome do gravador para esse gravador é "gravador VSS do NPS".

A ID do gravador para o gravador VSS do NPS é 0x35E81631-13E1-48DB-97FC-D5BC721BB18A.

## <a name="performance-counters-writer"></a>Gravador de contadores de desempenho

Esse gravador relata os arquivos de configuração do contador de desempenho. Esses arquivos são modificados apenas durante a instalação do aplicativo e devem ser armazenados em backup e restaurados durante as restaurações e backups de estado do sistema.

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para esse gravador. Os solicitantes são necessários para fazer backup desses arquivos manualmente. (Consulte [fazendo backup e restaurando o estado do sistema](locating-additional-system-files.md).)

A cadeia de caracteres do nome do gravador para esse gravador é "gravador de contadores de desempenho".

A ID do gravador para o gravador de contadores de desempenho é 0BADA1DE-01A9-4625-8278-69E735F39DD2.

## <a name="registry-writer"></a>Gravador do registro

O gravador do registro informa os arquivos de registro do Windows para habilitar backups in-loco e restaurações do registro. Ele não relata hives de usuário.

**Windows Server 2003:** No Windows Server 2003, esse gravador usa um arquivo de repositório intermediário (às vezes chamado de "arquivo saliva") para armazenar os dados do registro. (Consulte [operações de backup e restauração do registro em VSS](registry-backup-and-restore-operations-under-vss.md).)

**Windows XP:** Não há suporte para esse gravador. (Consulte [operações de backup e restauração do registro em VSS](registry-backup-and-restore-operations-under-vss.md).)

A cadeia de caracteres do nome do gravador para esse gravador é "gravador do registro".

A ID do gravador para o gravador do registro é AFBAB4A2-367D-4D15-A586-71DBB18F8485.

## <a name="remote-desktop-services-terminal-services-gateway-vss-writer"></a>Gravador VSS do gateway de Serviços de Área de Trabalho Remota (serviços de terminal)

Esse gravador é responsável por enumerar os arquivos de gateway de Serviços de Área de Trabalho Remota (serviços de terminal) para servidores que têm Área de Trabalho Remota gateway, uma subfunção de Serviços de Área de Trabalho Remota função, instalada.

**Windows Server 2003:** Não há suporte para esse gravador.

Esse gravador é um gravador in-box para versões do sistema operacional Windows Server; Ele não é fornecido no Windows Client.

O gateway de Serviços de Área de Trabalho Remota depende de várias chaves do registro cujo backup está sendo feito e, portanto, precisa de backup e restauração junto com o registro.

A cadeia de caracteres do nome do gravador para esse gravador é "gravador de Gateway TS".

A ID do gravador para este gravador é 368753EC-572E-4FC7-B4B9-CCD9BDC624CB.

## <a name="remote-desktop-services-terminal-services-licensing-vss-writer"></a>Gravador VSS de licenciamento do Serviços de Área de Trabalho Remota (serviços de terminal)

Esse gravador é responsável por enumerar os arquivos de licenciamento de Serviços de Área de Trabalho Remota (Licenciamento RD) ou licenciamento de serviços de terminal (Licenciamento TS) para servidores que têm Área de Trabalho Remota licenciamento, uma subfunção de Serviços de Área de Trabalho Remota função instalada.

**Windows Server 2003:** Não há suporte para esse gravador.

Esse gravador é um gravador in-box para versões do sistema operacional Windows Server; Ele não é fornecido no Windows Client.

Serviços de Área de Trabalho Remota licenciamento depende de várias chaves do registro cujo backup está sendo feito e, portanto, precisa de backup e restauração junto com o registro.

A cadeia de caracteres do nome do gravador para este gravador é "TermServLicensing".

A ID do gravador para este gravador é 5382579C-98DF-47A7-AC6C-98A6D7106E09.

## <a name="shadow-copy-optimization-writer"></a>Gravador de otimização de cópia de sombra

Esse gravador exclui determinados arquivos de cópias de sombra de volume. Isso é feito para minimizar o impacto da e/s de cópia em gravação durante e/s regular nesses arquivos no volume copiado por sombra. Os arquivos que são excluídos normalmente são arquivos temporários ou arquivos que não contêm o estado do sistema ou do usuário.

**Windows Server 2003 e Windows XP:** Não há suporte para esse gravador.

A cadeia de caracteres do nome do gravador para este gravador é "gravador de otimização de cópia de sombra".

A ID do gravador para o gravador de otimização de cópia de sombra é 4DC3BDD4-AB48-4D07-ADB0-3BEE2926FD7F.

## <a name="sync-share-service-writer"></a>Gravador do serviço de compartilhamento de sincronização

**Windows Server 2012 R2:** Esse gravador está incluído no Windows Server 2012 R2 e nas versões mais recentes do servidor. Ele não é compatível com as versões da área de trabalho.

Esse gravador é responsável por enumerar os compartilhamentos de sincronização em servidores que têm o serviço de compartilhamento de sincronização instalado e para garantir que seus metadados e dados permaneçam consistentes durante o backup e a restauração.

Esse gravador só estará presente quando o serviço de compartilhamento de sincronização estiver instalado e em execução.

Haverá um componente do gravador VSS para cada compartilhamento de sincronização. Isso inclui os metadados e os caminhos de dados. Esses backups devem ser feitos juntos para fins de consistência.

A cadeia de caracteres do nome do gravador é "gravador VSS do serviço de compartilhamento de sincronização".

A ID do gravador é D46BF321-FDBA-4A35-8EC3-454DF03BC86A.

## <a name="system-writer"></a>Gravador do sistema

O gravador do sistema enumera todos os binários do sistema operacional e do driver e é necessário para um backup do estado do sistema.

**Windows Server 2003 e Windows XP:** Não há suporte para esse gravador.

Esse gravador é executado como parte do serviço de serviços de criptografia (CryptSvc). O gravador do sistema gera uma lista de arquivos que contém os seguintes arquivos:

-   Todos os arquivos estáticos que foram instalados. Um arquivo estático é um arquivo listado no manifesto do componente com o atributo de arquivo **writeableType** definido como "Static" ou "". Os arquivos estáticos incluem todos os arquivos protegidos pelo Proteção de Recursos do Windows (WRP). No entanto, nem todos os arquivos estáticos são arquivos protegidos por WRP. Por exemplo, os arquivos de jogos são estáticos, mas não protegidos por WRP para que os administradores possam alterar as configurações de controle dos pais.
-   O conteúdo do diretório do Windows lado a lado (WinSxS), incluindo todos os manifestos, componentes opcionais e arquivos Win32 de terceiros.
    > [!Note]  
    > Muitos dos arquivos no diretório% windir% \\ System32 são links físicos para arquivos no diretório WinSxS.

     

-   Todos os arquivos PnP para drivers instalados (pertencentes a PnP).
-   Todos os serviços de modo de usuário e drivers não-PnP.
-   Todos os catálogos de propriedade de CryptSvc.

O aplicativo de restauração é responsável por dispor os arquivos e o registro e definir as ACLs para corresponder à cópia de sombra do sistema. Os links físicos apropriados também devem ser criados para que uma restauração de estado do sistema seja realizada com sucesso.

A cadeia de caracteres do nome do gravador para este gravador é "gravador do sistema".

A ID do gravador para o gravador do sistema é E8132975-6F93-4464-A53E-1050253AE220.

## <a name="task-scheduler-writer"></a>Gravador de Agendador de Tarefas

Esse gravador relata os arquivos de tarefa do Agendador de tarefas.

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para esse gravador. Os solicitantes são necessários para fazer backup desses arquivos manualmente. (Consulte [fazendo backup e restaurando o estado do sistema](locating-additional-system-files.md).)

A cadeia de caracteres do nome do gravador para este gravador é "gravador de Agendador de Tarefas".

A ID do gravador para o gravador é D61D61C8-D73A-4EEE-8CDD-F6F9786B7124.

## <a name="vss-metadata-store-writer"></a>Gravador de repositório de metadados do VSS

Esse gravador relata os arquivos de metadados do gravador para todos os gravadores Express do VSS.

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para esse gravador.

A cadeia de caracteres do nome do gravador para esse gravador é "gravador do repositório de metadados do VSS Express Writer".

A ID do gravador para o gravador é 75DFB225-E2E4-4D39-9AC9-FFAFF65DDF06.

## <a name="windows-deployment-services-wds-writer"></a>Gravador do WDS (serviços de implantação do Windows)

Esse gravador relata os arquivos de dados do WDS (serviços de implantação do Windows).

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para esse gravador.

A cadeia de caracteres do nome do gravador para esse gravador é "gravador VSS do WDS".

A ID do gravador para este gravador é 82CB5521-68DB-4626-83A4-7FC6F88853E9.

## <a name="windows-internal-database-wid-writer"></a>Gravador do banco de dados interno do Windows (WID)

Esse gravador relata os arquivos de dados do banco de dados interno do Windows (WID).

**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para esse gravador.

A cadeia de caracteres do nome do gravador para este gravador é "WIDWriter".

A ID do gravador para este gravador é 8D5194E1-E455-434A-B2E5-51296CCE67DF.

## <a name="windows-internet-name-service-wins-writer"></a>Gravador WINS (serviço de cadastramento na Internet do Windows)

Esse gravador é responsável por enumerar os arquivos necessários para o WINS.

**Windows XP:** Não há suporte para esse gravador.

A cadeia de caracteres do nome do gravador para este gravador é "gravador Jet do WINS".

A ID do gravador para este gravador é F08C1483-8407-4A26-8C26-6C267A629741.

## <a name="wmi-writer"></a>Gravador WMI

Esse gravador é usado para identificar dados e estado específicos do WMI durante operações de backup. Os dados incluem arquivos do repositório do WBEM.

**Windows Server 2003 e Windows XP:** Não há suporte para esse gravador.

A cadeia de caracteres do nome do gravador para este gravador é "gravador WMI".

A ID do gravador para este gravador é A6AD56C2-B509-4E6C-BB19-49D8F43532F0.

 

 
