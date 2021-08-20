---
description: Um aplicativo de backup e recuperação do VSS que executa a recuperação de desastre (também chamado de recuperação bare-metal) pode usar o asrador asR (automated Recuperação do Sistema) junto com o ambiente de pré-instalação do Windows (Windows PE) para fazer backup e restaurar volumes críticos e outros componentes do estado inicializável do sistema. O aplicativo de backup é implementado como um solicitante vss.
ms.assetid: 13adfd79-f26a-4385-9b59-129d06fa72eb
title: Usando o VSS Automated Recuperação do Sistema para recuperação de desastre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6813f0f746600fa665ed20bb208f3241cb1a88a12de721d53a8afa77be4a4c35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998056"
---
# <a name="using-vss-automated-system-recovery-for-disaster-recovery"></a>Usando o VSS Automated Recuperação do Sistema para recuperação de desastre

Um aplicativo de backup e recuperação do VSS que executa a recuperação de desastre (também chamado de recuperação bare-metal) pode usar o asrador asR (automated Recuperação do Sistema) junto com o ambiente de pré-instalação do Windows (Windows PE) para fazer backup e restaurar volumes críticos e outros componentes do estado inicializável do sistema. O aplicativo de backup é implementado como um solicitante vss.

**Observação**  Os aplicativos que usam ASR devem licenciar Windows PE.

**Windows Server 2003 e Windows XP:** O ASR não é implementado como um vss writer.

Para obter informações sobre ferramentas de rastreamento que podem ser usadas com o ASR, consulte [Using Tracing Tools with VSS ASR Applications](using-tracing-tools-with-vss-asr-applications.md).

**Neste artigo:**

-   [Visão geral das tarefas da fase de backup](#overview-of-backup-phase-tasks)
-   [Escolhendo quais componentes críticos fazer o back-up](#choosing-which-critical-components-to-back-up)
-   [Visão geral das tarefas da fase de restauração](#overview-of-restore-phase-tasks)
-   [Excluindo todos os discos para um volume](#excluding-all-disks-for-a-volume)

## <a name="overview-of-backup-phase-tasks"></a>Visão geral das tarefas da fase de backup

No momento do backup, o solicitante executa as etapas a seguir.

> [!Note]  
> Todas as etapas são necessárias, a menos que indicado de outra forma.

 

1.  Chame a função [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) para criar uma instância da interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) e chame o método [**IVssBackupComponents::InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) para inicializar a instância para gerenciar um backup.
2.  Chame [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) para definir o contexto para a operação de cópia de sombra.
3.  Chame [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) para configurar o backup. De definir *o parâmetro bBackupBootableSystemState* como **true** para indicar que o backup incluirá um estado inicializável do sistema.
4.  Escolha quais componentes críticos no Documento de Metadados do Autor do asR para fazer o back-up e chamar [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) para cada um deles.
5.  Chame [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) para criar um novo conjunto de cópias de sombra vazio.
6.  Chame [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) para iniciar o contato assíncrono com os autores.
7.  Chame [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) para recuperar o documento de metadados do autor do ASR. A ID do autor do ASR é BE000CBE-11FE-4426-9C58-531AAA6355FC4 e a cadeia de caracteres de nome do autor é "AsR Writer".
8.  Chame [**IVssExamineWriterMetadata::SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml) para salvar uma cópia do documento de metadados do autor do ASR.
9.  Chame [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) para cada volume que pode participar de cópias de sombra para adicionar o volume ao conjunto de cópias de sombra.
10. Chame [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) para notificar os autores a se prepararem para uma operação de backup.
11. Chame [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) (ou [**IVssBackupComponentsEx3::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex3-getwriterstatusex)) para verificar o status do asr writer.
12. Neste ponto, você pode consultar mensagens de falha que foram definidas pelo autor em seu [**método CVssWriter::OnPrepareBackup.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) Para obter um código de exemplo que mostra como exibir essas mensagens, consulte [**IVssComponentEx::GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg).
13. Chame [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) para criar uma cópia de sombra de volume.
14. Chame [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) para verificar o status do asr writer.
15. Fazer o back-up dos dados.
16. Indique se a operação de backup foi bem-sucedida chamando [**IVssBackupComponents::SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded).
17. Chame [**IVssBackupComponents::BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) para indicar que a operação de backup foi concluída.
18. Chame [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus). A memória de estado da sessão do autor é um recurso limitado e os autores devem, eventualmente, reutilizar estados de sessão. Esta etapa marca o estado de sessão de backup do autor como concluído e notifica o VSS de que esse slot de sessão de backup pode ser reutilizado por uma operação de backup subsequente.
    > [!Note]  
    > Isso só é necessário no Windows Server 2008 com Service Pack 2 (SP2) e anteriores.

     

19. Chame [**IVssBackupComponents::SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) para salvar uma cópia do documento Componentes de Backup do solicitante. As informações no Documento de Componentes de Backup são usadas no momento da restauração quando o solicitante chama o método [**IVssBackupComponents::InitializeForRestore.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore)

## <a name="choosing-which-critical-components-to-back-up"></a>Escolhendo quais componentes críticos fazer o back-up

Na fase de inicialização de backup, o asr writer relata os seguintes tipos de componentes em seu Documento de Metadados do Writer:

-   Volumes críticos, como os volumes de inicialização, sistema e ambiente de recuperação do Windows (Windows RE) e a partição Windows RE associada à instância do Windows Vista ou Windows Server 2008 em execução no momento. Um volume será um *volume crítico se* contiver informações de estado do sistema. Os volumes de inicialização e do sistema são incluídos automaticamente. O solicitante deve incluir todos os volumes que contêm componentes críticos do sistema relatados por autores, como os volumes que contêm o Active Directory. Os componentes críticos do sistema são marcados como "não selecionáveis para backup". No VSS, "não selecionável" significa "não opcional". Portanto, o solicitante é necessário para fazer o back-up como parte do estado do sistema. Para obter mais informações, [consulte Backing Up and Restoring System State](locating-additional-system-files.md). Os componentes para os quais o sinalizador NOT SYSTEM STATE do VSS \_ CF está definido não são \_ \_ \_ críticos para o sistema.
    > [!Note]  
    > O componente ASR é um componente crítico do sistema relatado pelo asr writer.

     

-   Discos. Cada disco fixo no computador é exposto como um componente no ASR. Se um disco não tiver sido excluído durante o backup, ele será atribuído durante a restauração e poderá ser criado e reformatado. Observe que, durante a restauração, o solicitante ainda pode criar um disco que foi excluído durante o backup chamando o método [**IVssBackupComponents::SetRestoreOptions.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) Se um disco em um pacote de disco dinâmico estiver selecionado, todos os outros discos nesse pacote também deverão ser selecionados. Se um volume for selecionado porque é um volume crítico (ou seja, um volume que contém informações de estado do sistema), todos os discos que contêm uma extensão para esse volume também deverão ser selecionados. Para encontrar as extensão de um volume, use o código de controle [**IOCTL \_ VOLUME GET VOLUME DISK \_ \_ \_ \_ EXTENTS.**](/windows/win32/api/winioctl/ni-winioctl-ioctl_volume_get_volume_disk_extents)

    > [!Note]  
    > Durante o backup, o solicitante deve incluir todos os discos fixos. Se o disco que contém o conjunto de backup do solicitante for um disco local, esse disco deverá ser incluído. Durante a restauração, o solicitante deve excluir o disco que contém o conjunto de backup do solicitante para impedir que ele seja substituído.

     

    Em um ambiente de clustering, o ASR não cria o layout dos discos compartilhados do cluster. Esses discos devem ser restaurados online depois que o sistema operacional for restaurado no Windows RE.

-   Dados de Configuração da Inicialização (BCD). Esse componente especifica o caminho do diretório que contém o armazenamento BCD. O solicitante deve especificar esse componente e fazer o back-up de todos os arquivos no diretório do armazenamento BCD. Para obter mais informações sobre o armazenamento BCD, consulte [Sobre BCD](/previous-versions/windows/desktop/bcd/about-bcd).
    > [!Note]  
    > Em computadores que usam a EFI (Interface de Firmware Estendida), a ESP (Partição do Sistema EFI) está sempre oculta e não pode ser incluída em uma cópia de sombra de volume. O solicitante deve fazer o back-up do conteúdo dessa partição. Como essa partição não pode ser incluída em uma cópia de sombra de volume, o backup só pode ser executado do volume ao vivo, não da cópia de sombra. Para obter mais informações sobre EFI e ESP, consulte [Guia de adoção.](/windows-hardware/drivers/bringup/)

Os nomes dos componentes usam os seguintes formatos:

-   Para componentes de disco, o formato é

    <COMPONENT logicalPath="Disks" componentName="harddisk*n*" componentType="filegroup" />

    em *que n* é o número do disco. Somente o número do disco é registrado. Para obter o número do disco, use o código [**de controle IOCTL \_ STORAGE GET DEVICE \_ \_ \_ NUMBER.**](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_get_device_number)

-   Para componentes de volume, o formato é

    <COMPONENT logicalPath="Volumes" componentName="Volume{*GUID*}" componentType="filegroup" />

    em *que GUID* é o GUID do volume.

-   Para o componente do armazenamento BCD, o formato é

    <COMPONENT logicalPath="BCD" componentName="BCD" componentType="filegroup" componentCaption = "This is the path to the boot BCD store and the boot managers...All the files in this directory need to be backed up...">

    Se a partição do sistema tiver um nome GUID de volume, esse componente será selecionável. Caso contrário, não será selecionável.

    > [!Note]  
    > O ASR adiciona os arquivos ao grupo de arquivos do componente do armazenamento BCD da seguinte forma:
    >
    > -   Para discos EFI, o ASR adiciona
    >
    >     *SystemPartitionPath* \\ Inicialização \\ da Microsoft EFI \\ \\ \* .\*
    >
    >     em *que SystemPartitionPath é* o caminho para a partição do sistema.
    >
    > -   Para discos GPT, o ASR adiciona
    >
    >     *SystemPartitionPath* \\ Inicializar \\ \* .\*
    >
    >     em *que SystemPartitionPath é* o caminho para a partição do sistema.
    >
    > -   O caminho de partição do sistema pode ser encontrado na seguinte chave do Registro: Sistema de Instalação do Sistema de COMPUTADOR **\_ LOCAL \_** \\  \\  \\ **HKEYPartition**

     

Na restauração, todos os componentes marcados como volumes críticos devem ser restaurados. Se um ou mais volumes críticos não puderem ser restaurados, a operação de restauração falhará.

Na fase [**Pré-repositório**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) da sequência de restauração, os discos que não foram excluídos durante o backup são criados e reformatados por padrão. No entanto, eles não serão criados ou reformatados se atenderem às seguintes condições:

-   Um disco básico não será criado se o layout do disco estiver intacto ou apenas alterações aditivas foram feitas nele. O layout do disco está intacto se as seguintes condições são verdadeiras:
    -   A assinatura de disco, o estilo de disco (GPT ou MBR), o tamanho do setor lógico e o deslocamento de início do volume não são alterados.
    -   O tamanho do volume não é reduzido.
    -   Para discos GPT, o identificador de partição não é alterado.
-   Um disco dinâmico não será criado se seu layout de disco estiver intacto ou apenas alterações aditivas foram feitas nele. Para que um disco dinâmico esteja intacto, todas as condições para um disco básico devem ser atendidas. Além disso, toda a estrutura de volume do pacote de disco deve estar intacta. A estrutura de volume do pacote de discos está intacta se atender às seguintes condições, que se aplicam a discos MBR e GPT:
    -   O número de volumes disponíveis no pacote físico durante a restauração deve ser maior ou igual ao número de volumes especificados nos metadados do asR writer durante o backup.
    -   O número de [*plexes*](../vds/virtual-disk-service-glossary-all.md) por volume deve ser inalterado.
    -   O número de [*membros*](../vds/virtual-disk-service-glossary-all.md) deve permanecer inalterado.
    -   O número de extensão de disco físico deve ser maior que o número de extensão de disco especificado nos metadados do asR writer.
    -   Um pacote intacto permanece intacto quando volumes adicionais são adicionados ou se um volume no pacote é estendido (por exemplo, de um volume simples para um volume estendido).
        > [!Note]  
        > Se um volume simples for espelhado, o pacote não estará intacto e será criado de novo para garantir que o estado do volume de inicialização e BCD permaneça consistente após a restauração. Se os volumes são excluídos, o pacote é re-criado.

         
-   Se a estrutura de volume do pacote de disco dinâmico estiver intacta e apenas alterações aditivas foram feitas nele, os discos no pacote não serão criados.

    **Windows Vista:** Discos dinâmicos são sempre re-criados. Observe que esse comportamento foi alterado com Windows Server 2008 e Windows Vista com Service Pack 1 (SP1).

A qualquer momento antes do início da fase de restauração, o solicitante pode especificar que os discos devem ser formatados rapidamente definindo a chave do Registro **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\  \\ **RestoreSession.** Nessa chave, há um valor chamado **QuickFormat** com o tipo de dados REG \_ DWORD. Se esse valor não existir, você deverá crie-o. De definir os dados do **valor QuickFormat** como 1 para formatação rápida ou 0 para formatação lenta.

Se o **valor QuickFormat** não existir, os discos serão formatados lentamente.

A formatação rápida é significativamente mais rápida do que a formatação lenta (também chamada de formatação completa). No entanto, a formatação rápida não verifica cada setor no volume.

## <a name="overview-of-restore-phase-tasks"></a>Visão geral das tarefas da fase de restauração

No momento da restauração, o solicitante executa as seguintes etapas:

> [!Note]  
> Todas as etapas são necessárias, a menos que indicado de outra forma.

 

1.  Chame a função [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) para criar uma instância da interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) e chame o método [**IVssBackupComponents::InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) para inicializar a instância para restauração carregando o Documento de Componentes de Backup do solicitante na instância.
2.  \[Essa etapa será necessária somente se o solicitante precisar alterar se "IncludeDisk" ou "ExcludeDisk" for especificado para um ou mais discos. \] Chame [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) para definir as opções de restauração para os componentes do asR writer. O assertor ASR dá suporte às seguintes opções: "IncludeDisk" permite que o solicitante inclua um disco no sistema de destino a ser considerado para restauração, mesmo se ele não tiver sido selecionado durante a fase de backup. "ExcludeDisk" permite que o solicitante impeça que um disco no sistema de destino seja criado. Observe que, se "ExcludeDisk" for especificado para um disco que contém um volume crítico, a chamada subsequente para [**IVssBackupComponents::P reRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) falhará.

    O exemplo a seguir mostra como usar [**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) para impedir que o disco 0 e o disco 1 são criados e injetar drivers de terceiros no volume de inicialização restaurado.

    **Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para a injeção de drivers de terceiros.

    O exemplo pressupõe que o ponteiro [**IVssBackupComponents,**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) m \_ pBackupComponents, é válido.

    ```C++
        m_pBackupComponents->SetRestoreOptions(
            AsrWriterId,
            VSS_CT_FILEGROUP,
            NULL,
            TEXT("ASR"),
            TEXT("\"ExcludeDisk\"=\"0\", \"ExcludeDisk\"=\"1\" "),
            TEXT("\"InjectDrivers\"=\"1\" ")
            );
    ```

    

    Para excluir todos os discos de um volume especificado, consulte o seguinte "Excluindo todos os discos para um volume".

3.  Chame [**IVssBackupComponents::P reRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) para notificar o asr writer para se preparar para uma operação de restauração. Chame [**IVssAsync::QueryStatus**](/windows/desktop/api/Vss/nf-vss-ivssasync-querystatus) quantas vezes for necessário até que o valor de status retornado no parâmetro *pHrResult* não seja \_ VSS S \_ ASYNC \_ PENDING.
4.  Restaurar os dados. Na fase de restauração, o ASR reconfigura o caminho guid do volume ( \\ \\ ? \\ Volume{GUID}) para cada volume corresponder ao caminho guid do volume que foi usado durante a fase de backup. No entanto, as letras da unidade não são preservadas, pois isso causaria colisões com as letras da unidade atribuídas automaticamente no ambiente de recuperação. Portanto, ao restaurar dados, o solicitante deve usar caminhos GUID de volume, não letras de unidade, para acessar os volumes.
5.  Defina a chave do Registro **HKLM** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\  \\ **RestoreSession** para indicar o conjunto de volumes que foram restaurados ou reformatados.

    Nessa chave, há um valor chamado **RestoredVolumes com** o tipo de dados REG \_ MULTI \_ SZ. Se esse valor não existir, você deverá crie-o. Sob esse valor, o solicitante deve criar uma entrada GUID de volume para cada volume que foi restaurado. Essa entrada deve estar no seguinte formato: \\ \\ ? \\ Volume{78618c8f-aefd-11da-a898-806e6f6e6963}. Sempre que uma recuperação bare-metal é executada, o ASR define o valor **RestoredVolumes** para o conjunto de volumes restaurados pelo ASR. Se o solicitante restaurou volumes adicionais, ele deve definir esse valor como a união do conjunto de volumes que o solicitante restaurou e o conjunto de volumes restaurados pelo ASR. Se o solicitante não usou o ASR, ele deve substituir a lista de volumes.

    Você também deve criar um valor chamado **LastInstance com** o tipo de dados REG \_ SZ. Essa chave deve conter um cookie aleatório que identifica exclusivamente a operação de restauração atual. Esse cookie pode ser criado usando as [**funções UuidCreate**](/windows/win32/api/rpcdce/nf-rpcdce-uuidcreate) e [**UuidToString.**](/windows/win32/api/rpcdce/nf-rpcdce-uuidtostring) Sempre que uma recuperação bare-metal é executada, o ASR redefine esse valor do Registro para notificar solicitantes e aplicativos de backup não VSS de que a recuperação ocorreu.

6.  Chame [**IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) para indicar o final da operação de restauração. Chame [**IVssAsync::QueryStatus**](/windows/desktop/api/Vss/nf-vss-ivssasync-querystatus) quantas vezes for necessário até que o valor de status retornado no parâmetro *pHrResult* não seja \_ VSS S \_ ASYNC \_ PENDING.

Na fase de restauração, o ASR pode criar ou remover partições para restaurar o computador para seu estado anterior. Os solicitantes não devem tentar mapear números de disco da fase de backup para a fase de restauração.

Na restauração, o solicitante deve excluir o disco que contém o conjunto de backup do solicitante. Caso contrário, o conjunto de backup pode ser substituído pela operação de restauração.

Na restauração, um disco será excluído se ele não tiver sido selecionado como um componente durante o backup ou se for excluído explicitamente chamando [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) com a opção "ExcludeDisk" durante a restauração.

É importante observar que, durante a recuperação de desastre do WinPE, a funcionalidade do asr writer está presente, mas nenhum outro autor está disponível e o serviço VSS não está em execução. Após a conclusão da recuperação de desastre do WinPE, o computador foi reiniciado e o sistema operacional Windows está em execução normalmente, o serviço VSS pode ser iniciado e o solicitante pode executar operações de restauração adicionais que exigem a participação de autores que não sejam o asSertor.

Se, durante a sessão de restauração, o aplicativo de backup detectar que as IDs exclusivas do volume estão inalteradas e, portanto, todos os volumes do momento do backup estão presentes e intactos no WinPE, o aplicativo de backup pode continuar a restaurar apenas o conteúdo dos volumes, sem envolver o ASR. Nesse caso, o aplicativo de backup deve indicar que o computador foi restaurado definindo a seguinte chave do Registro no sistema operacional restaurado: **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AsR** \\ **RestoreSession**

Sob essa chave, especifique **LastInstance** para o nome do valor, REG SZ para o tipo de valor e um cookie aleatório (como um GUID criado pela \_ [**função UuidCreate)**](/windows/win32/api/rpcdce/nf-rpcdce-uuidcreate) para os dados de valor.

Se, durante a sessão de restauração, o aplicativo de backup detectar que um ou mais volumes foram alterados ou ausentes, o aplicativo de backup deverá usar o ASR para executar a restauração. O ASR criará os volumes exatamente como estavam no momento do backup e definirá a chave do Registro **RestoreSession.**

## <a name="excluding-all-disks-for-a-volume"></a>Excluindo todos os discos para um volume

O exemplo a seguir mostra como excluir todos os discos de um volume especificado.


```C++
HRESULT BuildRestoreOptionString
(
    const WCHAR             *pwszVolumeNamePath,
    CMyString               *pstrExclusionList
)
{
    HANDLE                  hVolume           = INVALID_HANDLE_VALUE;
    DWORD                   cbSize            = 0;
    VOLUME_DISK_EXTENTS     * pExtents        = NULL;
    DISK_EXTENT             * pExtent         = NULL;
    ULONG                   i                 = 0;
    BOOL                    fIoRet            = FALSE;
    WCHAR                   wszDest[MAX_PATH] = L"";
    CMyString               strVolumeName;
    CMyString               strRestoreOption;

    // Open a handle to the volume device.
    strVolumeName.Set( pwszVolumeNamePath );
    // If the volume name contains a trailing backslash, remove it.
    strVolumeName.UnTrailing( L'\\' );
    hVolume = ::CreateFile(strVolumeName, 0, FILE_SHARE_READ | FILE_SHARE_WRITE, NULL, OPEN_EXISTING, NULL, 0);
    // Check whether the call to CreateFile succeeded.

    // Get the list of disks used by this volume.
    cbSize = sizeof(VOLUME_DISK_EXTENTS);
    pExtents = (VOLUME_DISK_EXTENTS *)::CoTaskMemAlloc(cbSize);

    ::ZeroMemory(pExtents, cbSize);

    fIoRet = ::DeviceIoControl(hVolume, IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS, NULL, 0, pExtents, cbSize, &cbSize, 0);
    if ( !fIoRet && GetLastError() == ERROR_MORE_DATA )
    {
        // Allocate more memory.
        cbSize = FIELD_OFFSET(VOLUME_DISK_EXTENTS, Extents) + pExtents->NumberOfDiskExtents * sizeof(DISK_EXTENT);
        ::CoTaskMemFree(pExtents);
        pExtents = NULL;

        pExtents = (VOLUME_DISK_EXTENTS *) ::CoTaskMemAlloc(cbSize);
        // Check whether CoTaskMemAlloc returned an out-of-memory error.
        ::ZeroMemory(pExtents, cbSize);

        // Now the buffer should be big enough.
        ::DeviceIoControl(hVolume, IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS, NULL, 0, pExtents, cbSize, &cbSize, 0);
        // Check whether the IOCTL succeeded.
    }
    // Check for errors; note that the IOCTL can fail for a reason other than insufficient memory.

    // For each disk, mark it to be excluded in the Restore Option string.
    for (i = 0; i < pExtents->NumberOfDiskExtents; i++)
    {
        pExtent = &pExtents->Extents[i];

        *wszDest = L'\0';
        StringCchPrintf(wszDest, MAX_PATH, L"\"ExcludeDisk\"=\"%d\", ", pExtent->DiskNumber); // check errors

        strRestoreOption.Append(wszDest);
        // Check for an out-of-memory error.
    }

    // Remove the trailing comma.
    strRestoreOption.TrimRight();
    strRestoreOption.UnTrailing(',');

    // Set the output parameter.
    strRestoreOption.Transfer( pstrExclusionList );

Exit:
    if( pExtents )
    {
        ::CoTaskMemFree(pExtents);
        pExtents = NULL;
    }

    if( hVolume != INVALID_HANDLE_VALUE )
    {
        ::CloseHandle(hVolume);
        hVolume = INVALID_HANDLE_VALUE;
    }

    return ( hr );
}

```



 

 
