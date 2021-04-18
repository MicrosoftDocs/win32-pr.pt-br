---
description: Um aplicativo de backup e recuperação VSS que executa a recuperação de desastre (também chamada de recuperação bare-metal) pode usar o gravador ASR (recuperação automatizada do sistema) junto com o Ambiente de Pré-Instalação do Windows (Windows PE) para fazer backup e restaurar volumes críticos e outros componentes do estado do sistema inicializável. O aplicativo de backup é implementado como um solicitante do VSS.
ms.assetid: 13adfd79-f26a-4385-9b59-129d06fa72eb
title: Usando a recuperação automatizada do sistema do VSS para recuperação de desastre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e31ef8ba223f40928e2422fa92240656f94592d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813214"
---
# <a name="using-vss-automated-system-recovery-for-disaster-recovery"></a>Usando a recuperação automatizada do sistema do VSS para recuperação de desastre

Um aplicativo de backup e recuperação VSS que executa a recuperação de desastre (também chamada de recuperação bare-metal) pode usar o gravador ASR (recuperação automatizada do sistema) junto com o Ambiente de Pré-Instalação do Windows (Windows PE) para fazer backup e restaurar volumes críticos e outros componentes do estado do sistema inicializável. O aplicativo de backup é implementado como um solicitante do VSS.

**Observação**  Os aplicativos que usam a ASR devem licenciar o Windows PE.

**Windows Server 2003 e Windows XP:** A ASR não é implementada como um gravador VSS.

Para obter informações sobre as ferramentas de rastreamento que você pode usar com o ASR, consulte [usando ferramentas de rastreamento com aplicativos ASR do VSS](using-tracing-tools-with-vss-asr-applications.md).

**Neste artigo:**

-   [Visão geral das tarefas da fase de backup](#overview-of-backup-phase-tasks)
-   [Escolhendo quais componentes críticos fazer backup](#choosing-which-critical-components-to-back-up)
-   [Visão geral das tarefas da fase de restauração](#overview-of-restore-phase-tasks)
-   [Excluindo todos os discos de um volume](#excluding-all-disks-for-a-volume)

## <a name="overview-of-backup-phase-tasks"></a>Visão geral das tarefas da fase de backup

No momento do backup, o solicitante executa as etapas a seguir.

> [!Note]  
> Todas as etapas são necessárias, a menos que indicado de outra forma.

 

1.  Chame a função [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) para criar uma instância da interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) e chame o método [**IVssBackupComponents:: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) para inicializar a instância para gerenciar um backup.
2.  Chame [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) para definir o contexto para a operação de cópia de sombra.
3.  Chame [**IVssBackupComponents:: Setbackupstate**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) para configurar o backup. Defina o parâmetro *bBackupBootableSystemState* como **true** para indicar que o backup incluirá um estado do sistema inicializável.
4.  Escolha os componentes críticos no documento de metadados do gravador do gravador de ASR para fazer backup e chamar o [**componente IVssBackupComponents::**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) Addpara cada um deles.
5.  Chame [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) para criar um conjunto de cópias de sombra novo e vazio.
6.  Chame [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) para iniciar o contato assíncrono com gravadores.
7.  Chame [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) para recuperar o documento de metadados do gravador do gravador de ASR. A ID do gravador para o gravador de ASR é BE000CBE-11FE-4426-9C58-531AA6355FC4 e a cadeia de caracteres do nome do gravador é "gravador ASR".
8.  Chame [**IVssExamineWriterMetadata:: SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml) para salvar uma cópia do documento de metadados do gravador do gravador de ASR.
9.  Chame [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) para cada volume que possa participar de cópias de sombra para adicionar o volume ao conjunto de cópias de sombra.
10. Chame [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) para notificar os gravadores para se preparar para uma operação de backup.
11. Chame [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) (ou [**IVssBackupComponentsEx3:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex3-getwriterstatusex)) para verificar o status do gravador de ASR.
12. Neste ponto, você pode consultar as mensagens de falha que foram definidas pelo gravador em seu método [**CVssWriter:: OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) . Por exemplo, código que mostra como exibir essas mensagens, consulte [**IVssComponentEx:: GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg).
13. Chame [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) para criar uma cópia de sombra de volume.
14. Chame [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) para verificar o status do gravador de ASR.
15. Faça backup dos dados.
16. Indique se a operação de backup foi bem-sucedida chamando [**IVssBackupComponents:: SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded).
17. Chame [**IVssBackupComponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) para indicar que a operação de backup foi concluída.
18. Chame [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus). A memória de estado da sessão do gravador é um recurso limitado e os gravadores devem eventualmente reutilizar Estados de sessão. Esta etapa marca o estado da sessão de backup do gravador como concluída e notifica o VSS de que esse slot de sessão de backup pode ser reutilizado por uma operação de backup subsequente.
    > [!Note]  
    > Isso só é necessário no Windows Server 2008 com Service Pack 2 (SP2) e versões anteriores.

     

19. Chame [**IVssBackupComponents:: SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) para salvar uma cópia do documento de componentes de backup do solicitante. As informações no documento componentes de backup são usadas no momento da restauração quando o solicitante chama o método [**IVssBackupComponents:: InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) .

## <a name="choosing-which-critical-components-to-back-up"></a>Escolhendo quais componentes críticos fazer backup

Na fase de inicialização de backup, o gravador de ASR relata os seguintes tipos de componentes em seu documento de metadados do gravador:

-   Volumes críticos, como os volumes de inicialização, sistema e ambiente de recuperação do Windows (Windows RE) e a partição do Windows RE que está associada à instância do Windows Vista ou Windows Server 2008 que está sendo executada no momento. Um volume é um *volume crítico* se ele contiver informações de estado do sistema. Os volumes de inicialização e de sistema são incluídos automaticamente. O solicitante deve incluir todos os volumes que contêm componentes críticos do sistema relatados por gravadores, como os volumes que contêm o Active Directory. Os componentes críticos do sistema são marcados como "não selecionável para backup". No VSS, "não selecionável" significa "não opcional". Assim, o solicitante precisa fazer o backup como parte do estado do sistema. Para obter mais informações, consulte [fazendo backup e restaurando o estado do sistema](locating-additional-system-files.md). Os componentes para os quais o sinalizador de estado do sistema do VSS \_ CF \_ não \_ \_ são definidos não são críticos para o sistema.
    > [!Note]  
    > O componente ASR é um componente crítico do sistema que é relatado pelo gravador ASR.

     

-   Discos. Cada disco fixo no computador é exposto como um componente no ASR. Se um disco não tiver sido excluído durante o backup, ele será atribuído durante a restauração e poderá ser recriado e reformatado. Observe que durante a restauração, o solicitante ainda pode recriar um disco que foi excluído durante o backup chamando o método [**IVssBackupComponents:: setrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) . Se um disco em um pacote de disco dinâmico for selecionado, todos os outros discos nesse pacote também deverão ser selecionados. Se um volume for selecionado porque é um volume crítico (ou seja, um volume que contém informações de estado do sistema), todos os discos que contêm uma extensão para esse volume também devem ser selecionados. Para localizar as extensões de um volume, use o código de controle [**\_ \_ obter \_ \_ \_ extensões de disco de volume do IOCTL**](/windows/win32/api/winioctl/ni-winioctl-ioctl_volume_get_volume_disk_extents) .

    > [!Note]  
    > Durante o backup, o solicitante deve incluir todos os discos fixos. Se o disco que contém o conjunto de backup do solicitante for um disco local, esse disco deverá ser incluído. Durante a restauração, o solicitante deve excluir o disco que contém o conjunto de backup do solicitante para impedir que ele seja substituído.

     

    Em um ambiente de clustering, o ASR não recria o layout dos discos compartilhados do cluster. Esses discos devem ser restaurados online depois que o sistema operacional é restaurado no Windows RE.

-   Repositório de Dados de Configuração da Inicialização (BCD). Esse componente especifica o caminho do diretório que contém o repositório BCD. O solicitante deve especificar esse componente e fazer backup de todos os arquivos no diretório de repositório BCD. Para obter mais informações sobre o repositório BCD, consulte [sobre o BCD](/previous-versions/windows/desktop/bcd/about-bcd).
    > [!Note]  
    > Em computadores que usam a interface de firmware estendido (EFI), a partição do sistema EFI (ESP) é sempre oculta e não pode ser incluída em uma cópia de sombra de volume. O solicitante deve fazer backup do conteúdo desta partição. Como essa partição não pode ser incluída em uma cópia de sombra de volume, o backup só pode ser executado a partir do volume ativo, não da cópia de sombra. Para obter mais informações sobre EFI e ESP, consulte [Guia de acompanhamento](/windows-hardware/drivers/bringup/).

Os nomes dos componentes usam os seguintes formatos:

-   Para componentes de disco, o formato é

    <COMPONENT logicalPath="Disks" componentName="harddisk*n*" componentType="filegroup" />

    em que *n* é o número do disco. Somente o número do disco é registrado. Para obter o número do disco, use o código de controle do [**número de dispositivo de obtenção de armazenamento do IOCTL \_ \_ \_ \_**](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) .

-   Para componentes de volume, o formato é

    <COMPONENT logicalPath="Volumes" componentName="Volume{*GUID*}" componentType="filegroup" />

    em que *GUID* é o GUID do volume.

-   Para o componente de repositório BCD, o formato é

    <COMPONENT logicalPath="BCD" componentName="BCD" componentType="filegroup" componentCaption = "This is the path to the boot BCD store and the boot managers...All the files in this directory need to be backed up...">

    Se a partição do sistema tiver um nome de GUID de volume, esse componente será selecionável. Caso contrário, ele não será selecionável.

    > [!Note]  
    > O ASR adiciona os arquivos ao grupo de arquivos do componente de repositório BCD da seguinte maneira:
    >
    > -   Para discos EFI, o ASR adiciona
    >
    >     *SystemPartitionPath* \\ Inicialização da EFI da \\ Microsoft \\ \\ \* .\*
    >
    >     em que *SystemPartitionPath* é o caminho para a partição do sistema.
    >
    > -   Para discos GPT, o ASR adiciona
    >
    >     *SystemPartitionPath* \\ Inicialização \\ \* .\*
    >
    >     em que *SystemPartitionPath* é o caminho para a partição do sistema.
    >
    > -   O caminho da partição do sistema pode ser encontrado na seguinte chave do registro: **HKEY \_ local \_ Machine** \\ **System** \\ **Setup** \\ **SystemPartition**

     

Na restauração, todos os componentes marcados como volumes críticos devem ser restaurados. Se um ou mais volumes críticos não puderem ser restaurados, a operação de restauração falhará.

Na fase de [**Prerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) da sequência de restauração, os discos que não foram excluídos durante o backup são recriados e reformatados por padrão. No entanto, eles não serão recriados ou reformatados se atenderem às seguintes condições:

-   Um disco básico não será recriado se o layout do disco estiver intacto ou se apenas alterações aditivas forem feitas a ele. O layout do disco estará intacto se as seguintes condições forem verdadeiras:
    -   A assinatura de disco, o estilo de disco (GPT ou MBR), o tamanho do setor lógico e o deslocamento de início do volume não são alterados.
    -   O tamanho do volume não é reduzido.
    -   Para discos GPT, o identificador de partição não é alterado.
-   Um disco dinâmico não será recriado se o layout do disco estiver intacto ou se apenas alterações aditivas forem feitas a ele. Para que um disco dinâmico fique intacto, todas as condições para um disco básico devem ser atendidas. Além disso, a estrutura de volume do pacote de disco inteiro deve estar intacta. A estrutura de volume do pacote de disco estará intacta se atender às seguintes condições, que se aplicam aos discos MBR e GPT:
    -   O número de volumes que estão disponíveis no pacote físico durante a restauração deve ser maior ou igual ao número de volumes que foram especificados nos metadados do gravador ASR durante o backup.
    -   O número de [*plexes*](../vds/virtual-disk-service-glossary-all.md) por volume deve ser inalterado.
    -   O número de [*Membros*](../vds/virtual-disk-service-glossary-all.md) deve ser inalterado.
    -   O número de extensões de disco físico deve ser maior que o número de extensões de disco especificado nos metadados do gravador ASR.
    -   Um pacote intacto permanece intacto quando volumes adicionais são adicionados ou se um volume no pacote é estendido (por exemplo, de um volume simples para um volume estendido).
        > [!Note]  
        > Se um volume simples for espelhado, o pacote não estará intacto e será recriado para garantir que o estado do volume BCD e de inicialização permaneça consistente após a restauração. Se os volumes forem excluídos, o pacote será recriado.

         
-   Se a estrutura de volume do pacote de disco dinâmico estiver intacta e apenas alterações aditivas tiverem sido feitas, os discos no pacote não serão recriados.

    **Windows Vista:** Discos dinâmicos são sempre recriados. Observe que esse comportamento foi alterado com o Windows Server 2008 e o Windows Vista com Service Pack 1 (SP1).

A qualquer momento antes do início da fase de restauração, o solicitante pode especificar que os discos devem ser formatados rapidamente definindo a chave do registro **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession** . Nessa chave, há um valor chamado **QuickFormat** com o tipo de dados reg \_ DWORD. Se esse valor não existir, você deverá criá-lo. Defina os dados do valor **QuickFormat** como 1 para formatação rápida ou 0 para formatação lenta.

Se o valor de **QuickFormat** não existir, os discos serão formatados com lentidão.

A formatação rápida é significativamente mais rápida do que a formatação lenta (também chamada de formatação completa). No entanto, a formatação rápida não verifica cada setor no volume.

## <a name="overview-of-restore-phase-tasks"></a>Visão geral das tarefas da fase de restauração

No momento da restauração, o solicitante executa as seguintes etapas:

> [!Note]  
> Todas as etapas são necessárias, a menos que indicado de outra forma.

 

1.  Chame a função [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) para criar uma instância da interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) e chame o método [**IVssBackupComponents:: InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) para inicializar a instância para restauração carregando o documento de componentes de backup do solicitante na instância.
2.  \[Esta etapa será necessária somente se o solicitante precisar alterar se "IncludeDisk" ou "ExcludeDisk" está especificado para um ou mais discos. \] Chame [**IVssBackupComponents:: setrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) para definir as opções de restauração para os componentes do gravador ASR. O gravador ASR oferece suporte às seguintes opções: "IncludeDisk" permite que o solicitante inclua um disco no sistema de destino para ser considerado para restauração, mesmo que ele não tenha sido selecionado durante a fase de backup. "ExcludeDisk" permite que o solicitante impeça que um disco no sistema de destino seja recriado. Observe que, se "ExcludeDisk" for especificado para um disco que contém um volume crítico, a chamada subsequente para [**IVssBackupComponents::P Rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) falhará.

    O exemplo a seguir mostra como usar [**setrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) para impedir que disco 0 e disco 1 sejam recriados e injetam drivers de terceiros no volume de inicialização restaurado.

    **Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para a injeção de drivers de terceiros.

    O exemplo supõe que o ponteiro [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) , m \_ pBackupComponents, é válido.

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

    

    Para excluir todos os discos de um volume especificado, consulte o seguinte "excluindo todos os discos de um volume".

3.  Chame [**IVssBackupComponents::P Rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) para notificar o gravador de ASR para se preparar para uma operação de restauração. Chame [**IVssAsync:: QueryStatus**](/windows/desktop/api/Vss/nf-vss-ivssasync-querystatus) quantas vezes forem necessárias até que o valor de status retornado no parâmetro *PHRRESULT* não seja VSS \_ S \_ Async \_ Pending.
4.  Restaurar os dados. Na fase de restauração, o ASR reconfigura o caminho do GUID do volume ( \\ \\ ? \\ Volume {GUID}) para cada volume para corresponder ao caminho do GUID do volume que foi usado durante a fase de backup. No entanto, as letras das unidades não são preservadas, pois isso causaria colisões com as letras da unidade que são atribuídas automaticamente no ambiente de recuperação. Portanto, ao restaurar dados, o solicitante deve usar caminhos de GUID de volume, não letras de unidade, para acessar os volumes.
5.  Defina a  \\  \\ chave do Registro HKLM Software **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession** para indicar o conjunto de volumes que foram restaurados ou reformatados.

    Nessa chave, há um valor chamado **RestoredVolumes** com o tipo de dados reg \_ multi \_ sz. Se esse valor não existir, você deverá criá-lo. Sob esse valor, seu solicitante deve criar uma entrada de GUID de volume para cada volume que foi restaurado. Essa entrada deve estar no seguinte formato: \\ \\ ? \\ Volume {78618c8f-aefd-11da-a898-806e6f6e6963}. Cada vez que uma recuperação bare-metal é executada, o ASR define o valor **RestoredVolumes** para o conjunto de volumes que o ASR restaurou. Se o solicitante tiver restaurado volumes adicionais, ele deverá definir esse valor como a União do conjunto de volumes que o solicitante restaurou e o conjunto de volumes que o ASR restaurou. Se o solicitante não usou a ASR, ele deve substituir a lista de volumes.

    Você também deve criar um valor chamado **LastInstance** com o tipo de dados reg \_ sz. Essa chave deve conter um cookie aleatório que identifica exclusivamente a operação de restauração atual. Esse cookie pode ser criado usando as funções [**UuidCreate**](/windows/win32/api/rpcdce/nf-rpcdce-uuidcreate) e [**UuidToString**](/windows/win32/api/rpcdce/nf-rpcdce-uuidtostring) . Cada vez que uma recuperação bare-metal é executada, o ASR redefine esse valor de registro para notificar os solicitantes e os aplicativos de backup não VSS que a recuperação ocorreu.

6.  Chame [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) para indicar o fim da operação de restauração. Chame [**IVssAsync:: QueryStatus**](/windows/desktop/api/Vss/nf-vss-ivssasync-querystatus) quantas vezes forem necessárias até que o valor de status retornado no parâmetro *PHRRESULT* não seja VSS \_ S \_ Async \_ Pending.

Na fase de restauração, o ASR pode criar ou remover partições para restaurar o computador ao estado anterior. Os solicitantes não devem tentar mapear os números de disco da fase de backup para a fase de restauração.

Na restauração, o solicitante deve excluir o disco que contém o conjunto de backup do solicitante. Caso contrário, o conjunto de backup pode ser substituído pela operação de restauração.

Na restauração, um disco será excluído se não tiver sido selecionado como um componente durante o backup ou se ele for explicitamente excluído chamando [**IVssBackupComponents:: setrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) com a opção "ExcludeDisk" durante a restauração.

É importante observar que durante a recuperação de desastres do WinPE, a funcionalidade do gravador ASR está presente, mas nenhum outro gravador está disponível e o serviço VSS não está em execução. Após a recuperação de desastres do WinPE ser concluída, o computador foi reiniciado e o sistema operacional Windows está em execução normalmente, o serviço VSS pode ser iniciado e o solicitante pode executar qualquer operação de restauração adicional que exija a participação de gravadores diferentes do gravador de ASR.

Se, durante a sessão de restauração, o aplicativo de backup detectar que as IDs exclusivas de volume estão inalteradas e, portanto, todos os volumes da hora do backup estarão presentes e intactos no WinPE, o aplicativo de backup poderá continuar restaurando apenas o conteúdo dos volumes, sem envolver o ASR. Nesse caso, o aplicativo de backup deve indicar que o computador foi restaurado definindo a seguinte chave do registro no sistema operacional restaurado: **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession**

Sob essa chave, especifique **LastInstance** para o nome do valor, Reg \_ sz para o tipo de valor e um cookie aleatório (como um GUID criado pela função [**UuidCreate**](/windows/win32/api/rpcdce/nf-rpcdce-uuidcreate) ) para os dados do valor.

Se, durante a sessão de restauração, o aplicativo de backup detectar que um ou mais volumes foram alterados ou ausentes, o aplicativo de backup deverá usar a ASR para executar a restauração. O ASR recriará os volumes exatamente como estavam no momento do backup e definiu a chave do registro **RestoreSession** .

## <a name="excluding-all-disks-for-a-volume"></a>Excluindo todos os discos de um volume

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



 

 
