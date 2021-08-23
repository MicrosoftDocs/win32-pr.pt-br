---
description: A categoria sistema operacional agrupa classes que representam objetos relacionados ao sistema operacional.
ms.assetid: D0756D8C-A3D3-4C75-96A3-8C7F05300B39
ms.tgt_platform: multiple
title: Classes do sistema operacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc5cbb168b2a322b5ceae8a2bd73985d14a74b4f1df227fd3e6cce384c554742
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588286"
---
# <a name="operating-system-classes"></a>Classes do sistema operacional

A categoria sistema operacional agrupa classes que representam objetos relacionados ao sistema operacional. Elas denotam as várias configurações e configurações que definem um ambiente de computação. Os exemplos incluem: a configuração de inicialização, configurações de Component Object Model (COM), configurações de ambiente da área de trabalho, Drivers, configurações de segurança, configurações do usuário e configurações do registro.

A categoria do sistema operacional é agrupada nas seguintes subcategorias:

-   [INTERFACES](#com)
-   [Área de trabalho](#desktop)
-   [Drivers](#drivers)
-   [Log de eventos](#windows-event-log)
-   [Sistema de Arquivos](#file-system)
-   [Objetos de trabalho](#job-objects)
-   [Memória e arquivos de paginação](#memory-and-page-files)
-   [Áudio ou Visual de multimídia](#multimedia-audio-or-visual)
-   [Rede](#networking)
-   [Eventos do sistema operacional](#operating-system-events)
-   [Configurações do sistema operacional](#operating-system-settings)
-   [Processos](#processes)
-   [Registro](#registry)
-   [Trabalhos do Agendador](#scheduler-jobs)
-   [Segurança](#security)
-   [Serviços](#services)
-   [Compartilhamentos](#shares)
-   [menu Iniciar](#start-menu)
-   [Storage](#storage)
-   [Usuários](#users)
-   [ativação do produto Windows](#windows-product-activation)

## <a name="com"></a>COM

A subcategoria do COM agrupa classes que representam configurações de COM e DCOM, classes e configurações de aplicativo cliente.



| Classe                                                                                           | Descrição                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ClassicCOMApplicationClasses Win32**](win32-classiccomapplicationclasses.md)               | Classe de associação<br/> Relaciona um aplicativo DCOM e um componente COM agrupado sob ele.<br/>                                                                             |
| [**\_ClassicCOMClass Win32**](win32-classiccomclass.md)                                         | Classe de instância<br/> Representa as propriedades de um componente COM.<br/>                                                                                                   |
| [**\_ClassicCOMClassSettings Win32**](win32-classiccomclasssettings.md)                         | Classe de associação<br/> Relaciona uma classe COM e as configurações usadas para configurar instâncias da classe COM.<br/>                                                           |
| [**\_ClientApplicationSetting Win32**](win32-clientapplicationsetting.md)                       | Classe de associação<br/> Relaciona um executável e um aplicativo DCOM que contém as opções de configuração do DCOM para o arquivo executável.<br/>                           |
| [**\_Aplicativo Win32**](win32-comapplication.md)                                           | Classe de instância<br/> Representa um aplicativo COM.<br/>                                                                                                                   |
| [**\_COMApplicationClasses Win32**](win32-comapplicationclasses.md)                             | Classe de associação<br/> Relaciona um componente COM e o aplicativo COM onde ele reside.<br/>                                                                            |
| [**\_COMApplicationSettings Win32**](win32-comapplicationsettings.md)                           | Classe de associação<br/> Relaciona um aplicativo DCOM e suas definições de configuração.<br/>                                                                                   |
| [**\_COMClass Win32**](win32-comclass.md)                                                       | Classe de instância<br/> Representa as propriedades de um componente COM.<br/>                                                                                                   |
| [**\_ComClassAutoEmulator Win32**](win32-comclassautoemulator.md)                               | Classe de associação<br/> Relaciona uma classe COM e outra classe COM que ela emula automaticamente.<br/>                                                                    |
| [**\_ComClassEmulator Win32**](win32-comclassemulator.md)                                       | Classe de associação<br/> Relaciona duas versões de uma classe COM.<br/>                                                                                                         |
| [**\_ComponentCategory Win32**](win32-componentcategory.md)                                     | Classe de instância<br/> Representa uma categoria de componente.<br/>                                                                                                                |
| [**Configuração do Win32 \_**](win32-comsetting.md)                                                   | Classe de instância<br/> Representa as configurações associadas a um componente COM ou a um aplicativo COM.<br/>                                                                     |
| [**\_DCOMApplication Win32**](win32-dcomapplication.md)                                         | Classe de instância<br/> Representa as propriedades de um aplicativo DCOM.<br/>                                                                                                |
| [**\_DCOMApplicationAccessAllowedSetting Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-dcomapplicationaccessallowedsetting) | Classe de associação<br/> Relaciona a instância do [**Win32 \_ DCOMApplication**](win32-dcomapplication.md) e as identificações de segurança do usuário (SID) que podem acessá-la.<br/> |
| [**\_DCOMApplicationLaunchAllowedSetting Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-dcomapplicationlaunchallowedsetting) | Classe de associação<br/> Relaciona a instância [**\_ DCOMApplication do Win32**](win32-dcomapplication.md) e os SIDs de usuário que podem iniciá-lo.<br/>                           |
| [**\_DCOMApplicationSetting Win32**](win32-dcomapplicationsetting.md)                           | Classe de instância<br/> Representa as configurações de um aplicativo DCOM.<br/>                                                                                                  |
| [**\_ImplementedCategory Win32**](win32-implementedcategory.md)                                 | Classe de associação<br/> Relaciona uma categoria de componente e a classe COM usando suas interfaces.<br/>                                                                         |



 

## <a name="desktop"></a>Desktop

A subcategoria da área de trabalho agrupa classes que representam objetos que definem uma configuração de área de trabalho específica.



| Classe                                           | Descrição                                                                                                                        |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Área de trabalho Win32**](win32-desktop.md)         | Classe de instância<br/> Representa as características comuns da área de trabalho de um usuário.<br/>                                    |
| [**\_Ambiente Win32**](win32-environment.md) | Classe de instância<br/> Representa uma configuração de ambiente do sistema ou ambiente em um sistema de computador que executa o Windows.<br/> |
| [**\_Fuso horário do Win32**](win32-timezone.md)       | Classe de instância<br/> Representa as informações de fuso horário de um sistema de computador executando Windows.<br/>                   |
| [**Userdesktop Win32 \_**](win32-userdesktop.md) | Classe de associação<br/> Relaciona uma conta de usuário e as configurações da área de trabalho que são específicas a ela.<br/>                   |



 

## <a name="drivers"></a>Drivers

A subcategoria drivers agrupa classes que representam drivers de dispositivo virtual e drivers de sistema para serviços base.



| Classe                                             | Descrição                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [**Systemdrive do Win32 \_**](win32-systemdriver.md) | Classe de instância<br/> Representa o driver do sistema para um serviço base.<br/> |



 

## <a name="file-system"></a>Sistema de Arquivos

A subcategoria sistema de arquivos agrupa classes que representam a maneira como um disco rígido é organizado logicamente. Isso inclui o tipo de sistema de arquivos usado, a estrutura de diretório e a maneira como o disco é particionado.



| Classe                                                                               | Descrição                                                                                                                                                                          |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CIMLogicalDeviceCIMDataFile Win32**](win32-cimlogicaldevicecimdatafile.md)     | Classe de associação<br/> Relaciona os dispositivos lógicos e os arquivos de dados, indicando os arquivos de driver usados pelo dispositivo.<br/>                                                      |
| [**\_Diretório Win32**](win32-directory.md)                                         | Classe de instância<br/> Representa uma entrada de diretório em um sistema de computador que executa o Windows.<br/>                                                                              |
| [**\_DirectorySpecification Win32**](/previous-versions/windows/desktop/msiprov/win32-directoryspecification)               | Classe de instância<br/> Representa o layout do diretório do produto.<br/>                                                                                                |
| [**\_DiskDriveToDiskPartition Win32**](win32-diskdrivetodiskpartition.md)           | Classe de associação<br/> Relaciona uma unidade de disco e uma partição existente nela.<br/>                                                                                         |
| [**\_DiskPartition Win32**](win32-diskpartition.md)                                 | Classe de instância<br/> Representa os recursos e a capacidade de gerenciamento de uma área particionada de um disco físico em um sistema de computador que executa o Windows.<br/>              |
| [**\_DiskQuota Win32**](/previous-versions/windows/desktop/wmipdskq/win32-diskquota)                                    | Classe de associação<br/> Controla o uso de espaço em disco para volumes do sistema de arquivos NTFS.<br/>                                                                                        |
| [**Disco \_ lógico do Win32**](win32-logicaldisk.md)                                     | Representa uma fonte de dados que é resolvida para um dispositivo de armazenamento local real em um sistema de computador que executa o Windows.<br/>                                                            |
| [**\_LogicalDiskRootDirectory Win32**](win32-logicaldiskrootdirectory.md)           | Classe de associação<br/> Relaciona um disco lógico e sua estrutura de diretórios.<br/>                                                                                          |
| [**\_LogicalDiskToPartition Win32**](win32-logicaldisktopartition.md)               | Classe de associação<br/> Relaciona uma unidade de disco lógico e a partição de disco em que ela reside.<br/>                                                                           |
| [**\_MappedLogicalDisk Win32**](win32-mappedlogicaldisk.md)                         | Representa os dispositivos de armazenamento em rede que são mapeados como discos lógicos no sistema de computador que executa o Windows.<br/>                                                               |
| [**\_OperatingSystemAutochkSetting Win32**](/previous-versions//aa394240(v=vs.85)) | Classe de associação<br/> Representa a associação entre uma [**instância \_ ManagedSystemElement do CIM**](cim-managedsystemelement.md) e as configurações definidas para ela.<br/> |
| [**\_QuotaSetting Win32**](/previous-versions/windows/desktop/wmipdskq/win32-quotasetting)                              | Classe de instância<br/> Contém informações de configuração para cotas de disco em um volume.<br/>                                                                                       |
| [**Atalho do Win32 \_**](win32-shortcutfile.md)                                   | Classe de instância<br/> Representa os arquivos que são atalhos para outros arquivos, diretórios e comandos.<br/>                                                                  |
| [**Subdiretório Win32 \_**](win32-subdirectory.md)                                   | Classe de associação<br/> Relaciona um diretório (pasta) e um de seus subdiretórios (subpastas).<br/>                                                                     |
| [**\_SystemPartitions Win32**](win32-systempartitions.md)                           | Classe de associação<br/> Relaciona um sistema de computador e uma partição de disco nesse sistema.<br/>                                                                               |
| [**Volume do Win32 \_**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85))                                               | Classe de instância<br/> Representa uma área de armazenamento em um disco rígido.<br/>                                                                                                   |
| [**\_VolumeQuota Win32**](/previous-versions/windows/desktop/vdswmi/win32-volumequota)                                     | Classe de associação<br/> Relaciona um volume às configurações de cota por volume.<br/>                                                                                           |
| [**\_VolumeQuotaSetting Win32**](/previous-versions/windows/desktop/wmipdskq/win32-volumequotasetting)                  | Classe de associação<br/> Relaciona as configurações de cota de disco com um volume de disco específico.<br/>                                                                                     |
| [**\_VolumeUserQuota Win32**](/previous-versions/windows/desktop/vdswmi/win32-volumeuserquota)                             | Classe de associação<br/> Relaciona cotas por usuário a volumes habilitados para cotas.<br/>                                                                                            |



 

## <a name="job-objects"></a>Objetos de trabalho

A subcategoria objetos de trabalho agrupa classes que representam classes que fornecem o meio de instrumentação de objetos de trabalho nomeados. Um objeto de trabalho sem nome não pode ser instrumentado.



| Classe                                                                               | Descrição                                                                                                                                                                                |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CollectionStatistics Win32**](/previous-versions/windows/desktop/cimwin32a/win32-collectionstatistics)                   | Classe de associação<br/> Relaciona uma coleção de elementos do sistema gerenciado e a classe que representa informações estatísticas sobre a coleção.<br/>                               |
| [**LUID do Win32 \_**](/previous-versions/windows/desktop/wmipjobobjprov/win32-luid)                                                   | Classe de instância<br/> Representa um identificador local exclusivo (LUID)<br/>                                                                                                         |
| [**\_LUIDandAttributes Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-luidandattributes)                         | Classe de instância<br/> Representa um LUID e seus atributos.<br/>                                                                                                                 |
| [**\_NamedJobObject Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobject)                               | Classe de instância<br/> Representa um objeto de kernel que é usado para agrupar processos para controlar a vida útil e os recursos dos processos dentro do objeto de trabalho.<br/> |
| [**\_NamedJobObjectActgInfo Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectactginfo)               | Classe de instância<br/> Representa as informações de contabilidade de e/s de um objeto de trabalho.<br/>                                                                                           |
| [**\_NamedJobObjectLimit Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectlimit)                     | Classe de instância<br/> Representa uma associação entre um objeto de trabalho e as configurações de limite de objeto de trabalho.<br/>                                                                     |
| [**\_NamedJobObjectLimitSetting Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectlimitsetting)       | Classe de instância<br/> Representa as configurações de limite para um objeto de trabalho.<br/>                                                                                                       |
| [**\_NamedJobObjectProcess Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectprocess)                 | Classe de instância<br/> Relaciona um objeto de trabalho e o processo contido no objeto de trabalho.<br/>                                                                                     |
| [**\_NamedJobObjectSecLimit Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectseclimit)               | Classe de instância<br/> Relaciona um objeto de trabalho e as configurações de limite de segurança de objeto de trabalho.<br/>                                                                                      |
| [**\_NamedJobObjectSecLimitSetting Win32**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectseclimitsetting) | Classe de instância<br/> Representa as configurações de limite de segurança para um objeto de trabalho.<br/>                                                                                              |
| [**Win32 \_ NamedJobObjectStatistics**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectstatistics)           | Classe de instância<br/> Representa uma associação entre um objeto de trabalho e a classe de informações de contabilidade de E/S do objeto de trabalho.<br/>                                                   |
| [**Win32 \_ SIDandAttributes**](/previous-versions/windows/desktop/wmipjobobjprov/win32-sidandattributes)                           | Classe de instância<br/> Representa um SID (identificador de segurança) e seus atributos.<br/>                                                                                            |
| [**Win32 \_ TokenGroups**](/previous-versions/windows/desktop/wmipjobobjprov/win32-tokengroups)                                     | Classe de eventos<br/> Representa informações sobre os SIDs de grupo em um token de acesso.<br/>                                                                                          |
| [**TokenPrivileges do Win32 \_**](/previous-versions/windows/desktop/wmipjobobjprov/win32-tokenprivileges)                             | Classe de eventos<br/> Representa informações sobre um conjunto de privilégios para um token de acesso.<br/>                                                                                    |



 

## <a name="memory-and-page-files"></a>Arquivos de memória e página

A subcategoria Arquivos de memória e página grupos classes que representam definições de configuração de arquivo de página.



| Classe                                                                 | Descrição                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ PageFile**](win32-pagefile.md)                             | Classe de instância<br/> Representa o arquivo usado para lidar com a troca de arquivos de memória virtual em um Windows sistema.<br/>                  |
| [**Win32 \_ PageFileElementSetting**](win32-pagefileelementsetting.md) | Classe de associação<br/> Relaciona as configurações iniciais de um arquivo de página e o estado dessas configurações durante o uso normal.<br/>        |
| [**Win32 \_ PageFileSetting**](win32-pagefilesetting.md)               | Classe de instância<br/> Representa as configurações de um arquivo de página.<br/>                                                                  |
| [**Win32 \_ PageFileUsage**](win32-pagefileusage.md)                   | Classe de instância<br/> Representa o arquivo usado para lidar com a troca de arquivos de memória virtual em um sistema de computador executando Windows.<br/> |



 

## <a name="multimedia-audio-or-visual"></a>Áudio multimídia ou visual

A classe na subcategoria Audio multimídia ou Visual representa propriedades do codec de áudio ou vídeo instalado no sistema de computador.



| Classe                                       | Descrição                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**CodecFile do Win32 \_**](win32-codecfile.md) | Classe de instância<br/> Representa o codec de áudio ou vídeo instalado no sistema de computador.<br/> |



 

## <a name="networking"></a>Rede

A subcategoria Rede grupos classes que representam conexões de rede, clientes de rede e configurações de conexão de rede, como o protocolo usado.



| Classe                                                                            | Descrição                                                                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ActiveRoute**](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)                       | Classe de associação<br/> Relaciona a rota IP4 atual à tabela de rotas de IP persistente.<br/>                           |
| [**Win32 \_ IP4PersistedRouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable) | Classe de instância<br/> Representa rotas DE IP persistentes.<br/>                                                             |
| [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)                   | Classe de instância<br/> Representa informações que regem o roteamento de pacotes de dados de rede.<br/>                    |
| [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)         | Classe de eventos<br/> Representa eventos de alteração de rota de IP.<br/>                                                             |
| [**Win32 \_ NetworkClient**](win32-networkclient.md)                              | Classe de instância<br/> Representa um cliente de rede em um sistema de computador executando Windows.<br/>                           |
| [**Win32 \_ NetworkConnection**](win32-networkconnection.md)                      | Classe de instância<br/> Representa uma conexão de rede ativa em um Windows ambiente.<br/>                           |
| [**Win32 \_ NetworkProtocol**](win32-networkprotocol.md)                          | Classe de instância<br/> Representa um protocolo e suas características de rede em um sistema de computador executando Windows.<br/> |
| [**Win32 \_ NTDomain**](/previous-versions/windows/desktop/cimwin32a/win32-ntdomain)                                        | Classe de instância<br/> Representa um Windows NT domínio.<br/>                                                             |
| [**Win32 \_ PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)                               | Classe de instância<br/> Representa os valores retornados pelo comando **ping** padrão.<br/>                            |
| [**Win32 \_ ProtocolBinding**](win32-protocolbinding.md)                          | Classe de associação<br/> Relaciona um driver de nível de sistema, protocolo de rede e adaptador de rede.<br/>                    |



 

## <a name="operating-system-events"></a>Eventos do Sistema Operacional

A subcategoria Eventos do Sistema Operacional grupos classes que representam eventos no sistema operacional relacionados a processos, threads e desligamento do sistema.



| Classe                                                                                 | Descrição                                                                                                                                                              |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ComputerShutdownEvent**](/previous-versions/windows/desktop/cimwin32a/win32-computershutdownevent)                   | Classe de eventos<br/> Representa eventos de desligamento do computador.<br/>                                                                                                   |
| [**Win32 \_ ComputerSystemEvent**](/previous-versions/windows/desktop/cimwin32a/win32-computersystemevent)                       | Classe de eventos<br/> Representa eventos relacionados a um sistema de computador.<br/>                                                                                        |
| [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md)                           | Classe de eventos<br/> Representa eventos de alteração de dispositivo resultantes da adição, remoção ou modificação de dispositivos no sistema de computador.<br/>               |
| [**Win32 \_ ModuleLoadTrace**](/previous-versions/windows/desktop/krnlprov/win32-moduleloadtrace)                               | Classe de eventos<br/> Indica que um processo carregou um novo módulo.<br/>                                                                                      |
| [**Win32 \_ ModuleTrace**](/previous-versions/windows/desktop/krnlprov/win32-moduletrace)                                       | Classe de eventos<br/> Evento base para eventos de módulo.<br/>                                                                                                          |
| [**Win32 \_ ProcessStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstarttrace)                           | Classe de eventos<br/> Indica que um novo processo foi iniciado.<br/>                                                                                              |
| [**Win32 \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace)                             | Classe de eventos<br/> Indica que um processo foi encerrado.<br/>                                                                                               |
| [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace)                                     | Classe de eventos<br/> Evento base para eventos de processo.<br/>                                                                                                         |
| [**Win32 \_ SystemConfigurationChangeEvent**](win32-systemconfigurationchangeevent.md) | Classe de eventos<br/> Indica que a lista de dispositivos no sistema foi atualizada (um dispositivo foi adicionado ou removido ou a configuração foi alterada).<br/>    |
| [**Win32 \_ SystemTrace**](/previous-versions/windows/desktop/krnlprov/win32-systemtrace)                                       | Classe de eventos<br/> Classe base para todos os eventos de rastreamento do sistema, incluindo rastreamentos de módulo, processo e thread.<br/>                                                  |
| [**Win32 \_ ThreadStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-threadstarttrace)                             | Classe de eventos<br/> Indica que um novo thread foi iniciado.<br/>                                                                                                    |
| [**Win32 \_ ThreadStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-threadstoptrace)                               | Classe de eventos<br/> Indica que um thread foi interrompido.<br/>                                                                                                   |
| [**Win32 \_ ThreadTrace**](/previous-versions/windows/desktop/krnlprov/win32-threadtrace)                                       | Classe de eventos<br/> Classe de evento base para eventos de thread.<br/>                                                                                                    |
| [**Win32 \_ VolumeChangeEvent**](win32-volumechangeevent.md)                           | Classe de eventos<br/> Representa um evento de unidade mapeada em rede resultante da adição de uma letra da unidade de rede ou unidade montada no sistema de computador.<br/> |



 

## <a name="operating-system-settings"></a>configurações do sistema operacional

O sistema operacional Configurações classes de subcategoria que representam o Sistema Operacional e suas configurações.



| Classe                                                                                       | Descrição                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ BootConfiguration**](win32-bootconfiguration.md)                                 | Classe de instância<br/> Representa a configuração de inicialização de um sistema de computador executando Windows.<br/>                                                                       |
| [**Win32 \_ ComputerSystem**](win32-computersystem.md)                                       | Classe de instância<br/> Representa um sistema de computador que opera em um Windows ambiente.<br/>                                                                              |
| [**Win32 \_ ComputerSystemProcessor**](win32-computersystemprocessor.md)                     | Classe de associação<br/> Relaciona um sistema de computador e um processador em execução nesse sistema.<br/>                                                                          |
| [**Win32 \_ ComputerSystemProduct**](win32-computersystemproduct.md)                         | Classe de instância<br/> Representa um produto.<br/>                                                                                                                         |
| [**Win32 \_ DependentService**](win32-dependentservice.md)                                   | Classe de associação<br/> Relaciona dois serviços base interdependentes.<br/>                                                                                                  |
| [**Win32 \_ LoadOrderGroup**](win32-loadordergroup.md)                                       | Classe de instância<br/> Representa um grupo de serviços do sistema que definem dependências de execução.<br/>                                                                     |
| [**Win32 \_ LoadOrderGroupServiceDependencies**](win32-loadordergroupservicedependencies.md) | Classe de instância<br/> Representa uma associação entre um serviço base e um grupo de ordem de carregamento do que o serviço depende para iniciar a execução.<br/>                         |
| [**Win32 \_ LoadOrderGroupServiceMembers**](win32-loadordergroupservicemembers.md)           | Classe de associação<br/> Relaciona um grupo de ordem de carregamento e um serviço base.<br/>                                                                                             |
| [**Sistema operacional \_ Win32**](win32-operatingsystem.md)                                     | Classe de instância<br/> Representa um sistema operacional instalado em um sistema de computador executando Windows.<br/>                                                                |
| [**Win32 \_ OperatingSystemQFE**](win32-operatingsystemqfe.md)                               | Classe de associação<br/> Relaciona um sistema operacional e atualizações de produto aplicadas conforme representado em [**Win32 \_ QuickFixEngineering.**](win32-quickfixengineering.md)<br/> |
| [**Win32 \_ OSRecoveryConfiguration**](win32-osrecoveryconfiguration.md)                     | Classe de instância<br/> Representa os tipos de informações que serão coletadas da memória quando o sistema operacional falhar.<br/>                                        |
| [**QuickFixEngineering do Win32 \_**](win32-quickfixengineering.md)                             | Classe de instância<br/> Representa o QFE (engenharia Correção Rápida todo o sistema) ou atualizações que foram aplicadas ao sistema operacional atual.<br/>                         |
| [**Win32 \_ StartupCommand**](win32-startupcommand.md)                                       | Classe de instância<br/> Representa um comando que é executado automaticamente quando um usuário faz logor no sistema de computador.<br/>                                                       |
| [**Win32 \_ SystemBootConfiguration**](win32-systembootconfiguration.md)                     | Classe de associação<br/> Relaciona um sistema de computador e sua configuração de inicialização.<br/>                                                                                      |
| [**Win32 \_ SystemDesktop**](win32-systemdesktop.md)                                         | Classe de associação<br/> Relaciona um sistema de computador e sua configuração de área de trabalho.<br/>                                                                                   |
| [**Win32 \_ SystemDevices**](win32-systemdevices.md)                                         | Classe de associação<br/> Relaciona um sistema de computador e um dispositivo lógico instalado nesse sistema.<br/>                                                                   |
| [**Win32 \_ SystemLoadOrderGroups**](win32-systemloadordergroups.md)                         | Classe de associação<br/> Relaciona um sistema de computador e um grupo de ordem de carregamento.<br/>                                                                                          |
| [**Win32 \_ SystemNetworkConnections**](win32-systemnetworkconnections.md)                   | Classe de associação<br/> Relaciona uma conexão de rede e o sistema de computador no qual ela reside.<br/>                                                                  |
| [**Sistema \_ Win32OperatingSystem**](win32-systemoperatingsystem.md)                         | Classe de associação<br/> Relaciona um sistema de computador e seu sistema operacional.<br/>                                                                                        |
| [**Win32 \_ SystemProcesses**](win32-systemprocesses.md)                                     | Classe de associação <br/> Relaciona um sistema de computador e um processo em execução nesse sistema.<br/>                                                                           |
| [**Win32 \_ SystemProgramGroups**](win32-systemprogramgroups.md)                             | Classe de associação<br/> Relaciona um sistema de computador e um grupo de programas lógicos.<br/>                                                                                     |
| [**Win32 \_ SystemResources**](win32-systemresources.md)                                     | Classe de associação<br/> Relaciona um recurso do sistema e o sistema de computador em que ele reside.<br/>                                                                           |
| [**Win32 \_ SystemServices**](win32-systemservices.md)                                       | Classe de associação<br/> Relaciona um sistema de computador e um programa de serviço que existe no sistema.<br/>                                                                 |
| [**SystemSetting do Win32 \_**](win32-systemsetting.md)                                         | Classe de associação<br/> Relaciona um sistema de computador e uma configuração geral nesse sistema.<br/>                                                                            |
| [**Win32 \_ SystemSystemDriver**](win32-systemsystemdriver.md)                               | Classe de associação<br/> Relaciona um sistema de computador e um driver do sistema em execução nesse sistema de computador.<br/>                                                             |
| [**Win32 \_ SystemTimeZone**](win32-systemtimezone.md)                                       | Classe de associação<br/> Relaciona um sistema de computador e um fuso horário.<br/>                                                                                                 |
| [**Win32 \_ SystemUsers**](win32-systemusers.md)                                             | Classe de associação<br/> Relaciona um sistema de computador e uma conta de usuário nesse sistema.<br/>                                                                               |



 

## <a name="processes"></a>Processos

A subcategoria Processes agrupa classes que representam processos e threads do sistema.



| Classe                                                 | Descrição                                                                                                     |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**\_Processo Win32**](win32-process.md)               | Classe de instância<br/> Representa uma sequência de eventos em um sistema de computador que executa o Windows.<br/>      |
| [**\_ProcessStartup Win32**](win32-processstartup.md) | Classe de instância<br/> Representa a configuração de inicialização de um sistema de computador que executa o Windows.<br/> |
| [**\_Thread Win32**](win32-thread.md)                 | Classe de instância<br/> Representa um thread de execução.<br/>                                          |



 

## <a name="registry"></a>Registro

a classe na subcategoria do registro representa o conteúdo do registro de Windows.



| Classe                                     | Descrição                                                                                               |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**\_Registro do Win32**](win32-registry.md) | Classe de instância<br/> Representa o registro do sistema em um sistema de computador que executa o Windows.<br/> |



 

## <a name="scheduler-jobs"></a>Trabalhos do Agendador

A subcategoria trabalhos do Agendador agrupa as classes que representam as configurações de trabalho agendadas.



| Classe                                                | Descrição                                                                                                                                                                                                                                                           |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CurrentTime Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) | Classe abstrata<br/> Representa uma instância no tempo como segundos de componente, minutos, dia da semana e assim por diante.<br/>                                                                                                                                        |
| [**\_ScheduledJob Win32**](win32-scheduledjob.md)    | Classe de instância<br/> representa um trabalho agendado usando o serviço agendamento de Windows.<br/>                                                                                                                                                                   |
| [**Local do Win32 \_**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime)     | Classe de instância<br/> Representa um ponto no tempo retornado como [**objetos \_ locais do Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) que resultam de uma consulta. A propriedade **Hour** é retornada como a hora local em um relógio de 24 horas.<br/>                                |
| [**\_UTCTime Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)         | Classe de instância<br/> Representa um ponto no tempo que é retornado como [**objetos \_ UTCTime do Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) que resultam de uma consulta. A propriedade **Hour** é retornada como a hora UTC (tempo Universal Coordenado) em um relógio de 24 horas.<br/> |



 

## <a name="security"></a>Segurança

A subcategoria de segurança agrupa as classes que representam as configurações de segurança do sistema.



| Classe                                                                               | Descrição                                                                                                                                                  |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AccountId Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-accountsid)                                       | Classe de associação<br/> Relaciona uma instância de conta de segurança com uma instância de descritor de segurança.<br/>                                             |
| [**Ace do Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)                                                     | Classe de instância<br/> Representa uma ACE (entrada de controle de acesso).<br/>                                                                               |
| [**\_LogicalFileAccess Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileaccess)                         | Classe de associação<br/> Relaciona as configurações de segurança de um arquivo ou diretório e um membro de sua DACL (lista de controle de acesso discricionário).<br/> |
| [**\_LogicalFileAuditing Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileauditing)                     | Classe de associação<br/> Relaciona as configurações de segurança de um arquivo ou diretório de um membro de sua SACL (lista de controle de acesso) do sistema.<br/>            |
| [**\_LogicalFileGroup Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilegroup)                           | Classe de associação<br/> Relaciona as configurações de segurança de um arquivo ou diretório e seu grupo.<br/>                                                  |
| [**\_LogicalFileOwner Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileowner)                           | Classe de associação<br/> Relaciona as configurações de segurança de um arquivo ou diretório e seu proprietário.<br/>                                                  |
| [**\_LogicalFileSecuritySetting Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)       | Classe de instância<br/> Representa as configurações de segurança de um arquivo lógico.<br/>                                                                        |
| [**\_LogicalShareAccess Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalshareaccess)                       | Classe de associação<br/> Relaciona as configurações de segurança de um compartilhamento e um membro de sua DACL.<br/>                                                 |
| [**\_LogicalShareAuditing Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalshareauditing)                   | Classe de associação<br/> Relaciona as configurações de segurança de um compartilhamento e um membro de sua SACL.<br/>                                                 |
| [**\_LogicalShareSecuritySetting Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting)     | Classe de instância<br/> Representa as configurações de segurança de um arquivo lógico.<br/>                                                                        |
| [**\_PrivilegesStatus Win32**](win32-privilegesstatus.md)                           | Classe de instância<br/> Representa informações sobre os privilégios necessários para concluir uma operação.<br/>                                          |
| [**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)                       | Classe de instância<br/> Representa uma representação estrutural de um [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor).<br/>                   |
| [**\_SecuritySetting Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysetting)                             | Classe de instância<br/> Representa as configurações de segurança para um elemento gerenciado.<br/>                                                                     |
| [**\_SecuritySettingAccess Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingaccess)                 | Classe de instância<br/> Representa os direitos concedidos e negados a um objeto de confiança para um determinado Object.<br/>                                               |
| [**\_SecuritySettingAuditing Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingauditing)             | Classe de instância<br/> Representa a auditoria de um determinado objeto de confiança em um determinado Object.<br/>                                                          |
| [**\_SecuritySettingGroup Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettinggroup)                   | Classe de associação<br/> Relaciona a segurança de um objeto e seu grupo.<br/>                                                                     |
| [**\_SecuritySettingOfLogicalFile Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingoflogicalfile)   | Classe de instância<br/> Representa as configurações de segurança de um objeto de arquivo ou diretório.<br/>                                                             |
| [**\_SecuritySettingOfLogicalShare Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingoflogicalshare) | Classe de instância<br/> Representa as configurações de segurança de um objeto compartilhado.<br/>                                                                        |
| [**\_SecuritySettingOfObject Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingofobject)             | Classe de associação<br/> Relaciona um objeto a suas configurações de segurança.<br/>                                                                          |
| [**\_SecuritySettingOwner Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingowner)                   | Classe de associação<br/> Relaciona as configurações de segurança de um objeto e seu proprietário.<br/>                                                            |
| [**Sid do Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-sid)                                                     | Classe de instância<br/> Representa um SID arbitrário.<br/>                                                                                            |
| [**Confiança do Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)                                             | Classe de instância<br/> Representa um Trustee.<br/>                                                                                                   |



 

## <a name="services"></a>Serviços

A subcategoria de serviços agrupa classes que representam serviços e serviços base.



| Classe                                           | Descrição                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_BaseService Win32**](win32-baseservice.md) | Classe de instância<br/> Representa os objetos executáveis instalados em um banco de dados de registro mantido pelo Gerenciador de controle de serviço.<br/> |
| [**\_Serviço Win32**](win32-service.md)         | Classe de instância<br/> Representa um serviço em um sistema de computador que executa o Windows.<br/>                                                         |



 

## <a name="shares"></a>Compartilhamentos

A subcategoria compartilhamentos agrupa classes que representam detalhes de recursos compartilhados, como impressoras e pastas.



| Classe                                                       | Descrição                                                                                                                                                                                          |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_DFSNode Win32**](/previous-versions/windows/desktop/wmipdfs/win32-dfsnode)                     | Classe de associação<br/> Representa um nó raiz ou junção de um sistema de arquivos distribuído (DFS) baseado em domínio ou autônomo.<br/>                                                           |
| [**\_DFSNodeTarget Win32**](/previous-versions/windows/desktop/wmipdfs/win32-dfsnodetarget)         | Classe de associação<br/> Representa a relação de um nó DFS com um de seus destinos.<br/>                                                                                             |
| [**\_DFSTarget Win32**](/previous-versions/windows/desktop/wmipdfs/win32-dfstarget)                 | Classe de associação<br/> Representa o destino de um nó DFS.<br/>                                                                                                                         |
| [**\_ServerConnection Win32**](/previous-versions/windows/desktop/wmipsess/win32-serverconnection)   | Classe de instância<br/> Representa as conexões feitas de um computador remoto para um recurso compartilhado no computador local.<br/>                                                              |
| [**\_ServerSession Win32**](/previous-versions/windows/desktop/wmipsess/win32-serversession)         | Classe de instância<br/> Representa as sessões estabelecidas com o computador local por usuários em um computador remoto.<br/>                                                             |
| [**\_ConnectionShare Win32**](/previous-versions/windows/desktop/wmipsess/win32-connectionshare)     | Classe de associação<br/> Relaciona um recurso compartilhado no computador e a conexão feita ao recurso compartilhado.<br/>                                                                    |
| [**\_PrinterShare Win32**](win32-printershare.md)           | Classe de associação<br/> Relaciona uma impressora local e o compartilhamento que a representa à medida que ela é exibida em uma rede.<br/>                                                                     |
| [**\_SessionConnection Win32**](/previous-versions/windows/desktop/wmipsess/win32-sessionconnection) | Classe de associação<br/> Representa uma associação entre uma sessão estabelecida com o servidor local por um usuário em um computador remoto e as conexões que dependem da sessão.<br/> |
| [**\_SessionProcess Win32**](win32-sessionprocess.md)       | Classe de associação<br/> Representa uma associação entre uma sessão de logon e os processos associados a essa sessão.<br/>                                                            |
| [**\_ShareToDirectory Win32**](win32-sharetodirectory.md)   | Classe de associação<br/> Relaciona um recurso compartilhado no sistema de computador e o diretório no qual ele está mapeado.<br/>                                                                    |
| [**Compartilhamento do Win32 \_**](win32-share.md)                         | Classe de instância<br/> Representa um recurso compartilhado em um sistema de computador que executa o Windows.<br/>                                                                                              |



 

## <a name="start-menu"></a>Menu Iniciar

A subcategoria do menu iniciar agrupa as classes que representam grupos de programas.



| Classe                                                                                   | Descrição                                                                                                                                                              |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_LogicalProgramGroup Win32**](win32-logicalprogramgroup.md)                         | Classe de instância<br/> Representa um grupo de programas em um sistema de computador que executa o Windows.<br/>                                                                    |
| [**\_LogicalProgramGroupDirectory Win32**](win32-logicalprogramgroupdirectory.md)       | Classe de associação<br/> relaciona grupos de programas lógicos (agrupamentos no menu Iniciar) e os diretórios de arquivos nos quais eles são armazenados.<br/>                 |
| [**\_LogicalProgramGroupItem Win32**](win32-logicalprogramgroupitem.md)                 | Classe de instância<br/> Representa um elemento contido por uma instância de um do Win32, que não é outra instância de um do **Win32 \_** . **\_**<br/> |
| [**\_LogicalProgramGroupItemDataFile Win32**](win32-logicalprogramgroupitemdatafile.md) | Classe de associação<br/> relaciona os itens do grupo de programas da menu Iniciar e os arquivos nos quais eles estão armazenados.<br/>                                       |
| [**\_ProgramGroupContents Win32**](win32-programgroupcontents.md)                       | Classe de associação<br/> Relaciona uma ordem de grupo de programas e um grupo de programas individual ou item contido nele.<br/>                                           |
| [**\_ProgramGroupOrItem Win32**](win32-programgrouporitem.md)                           | Classe de instância<br/> Representa um agrupamento lógico de programas no menu **Iniciar** \| **programas** do usuário.<br/>                                               |



 

## <a name="storage"></a>Armazenamento

A subcategoria usuários agrupa as classes que representam informações de armazenamento.



| Classe                                                                   | Descrição                                                                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ShadowBy Win32**](/previous-versions/windows/desktop/vsswmi/win32-shadowby)                               | Classe de associação<br/> Representa a associação entre uma cópia de sombra e o provedor que cria a cópia de sombra.<br/>      |
| [**\_ShadowContext Win32**](/previous-versions/windows/desktop/vsswmi/win32-shadowcontext)                     | Classe de associação<br/> Especifica como uma cópia de sombra deve ser criada, consultada ou excluída.<br/>                                   |
| [**Cópia de sombra do Win32 \_**](/previous-versions/windows/desktop/legacy/aa394428(v=vs.85))                           | Classe de instância<br/> Representa uma cópia duplicada do volume original em um momento anterior.<br/>                                  |
| [**\_ShadowDiffVolumeSupport Win32**](/previous-versions/windows/desktop/vsswmi/win32-shadowdiffvolumesupport) | Classe de associação<br/> Representa uma associação entre um provedor de cópia de sombra e um volume de armazenamento.<br/>                       |
| [**\_ShadowFor Win32**](/previous-versions/windows/desktop/vsswmi/win32-shadowfor)                             | Classe de associação<br/> Representa uma associação entre uma cópia de sombra e o volume para o qual a cópia de sombra é criada.<br/> |
| [**\_Sombreamento do Win32**](/previous-versions/windows/desktop/vsswmi/win32-shadowon)                               | Classe de associação<br/> Representa uma associação entre uma cópia de sombra e onde os dados diferenciais são gravados.<br/>          |
| [**Win32 \_ ShadowProvider**](/previous-versions/windows/desktop/vsswmi/win32-shadowprovider)                   | Classe de associação<br/> Representa um componente que cria e representa cópias de sombra de volume.<br/>                             |
| [**Win32 \_ ShadowStorage**](/previous-versions/windows/desktop/legacy/aa394433(v=vs.85))                     | Classe de associação<br/> Representa uma associação entre uma cópia de sombra e onde os dados diferenciais são gravados.<br/>          |
| [**Win32 \_ ShadowVolumeSupport**](/previous-versions/windows/desktop/vsswmi/win32-shadowvolumesupport)         | Classe de associação<br/> Representa uma associação entre um provedor de cópia de sombra com um volume com suporte.<br/>                    |
| [**Win32 \_ Volume**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85))                                   | Classe de instância<br/> Representa uma área de armazenamento em um disco rígido.<br/>                                                           |
| [**VolumeUserQuota do Win32 \_**](/previous-versions/windows/desktop/vdswmi/win32-volumeuserquota)                 | Classe de associação<br/> Representa um volume para as configurações de cota por volume.<br/>                                                |



 

## <a name="users"></a>Usuários

A subcategoria Usuários agrupa classes que representam informações de conta de usuário, como detalhes de associação de grupo.



| Classe                                                                 | Descrição                                                                                                                                      |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Conta do \_ Win32**](win32-account.md)                               | Classe de instância<br/> Representa informações sobre contas de usuário e contas de grupo conhecidas para o sistema de computadores que executa Windows.<br/> |
| [**Grupo \_ Win32**](win32-group.md)                                   | Classe de instância<br/> Representa dados sobre uma conta de grupo.<br/>                                                                      |
| [**Win32 \_ GroupInDomain**](/previous-versions/windows/desktop/cimwin32a/win32-groupindomain)                   | Classe de associação<br/> Identifica as contas de grupo associadas a um Windows NT domínio.<br/>                                       |
| [**Win32 \_ GroupUser**](win32-groupuser.md)                           | Classe de associação<br/> Relaciona um grupo e uma conta que é membro desse grupo.<br/>                                           |
| [**\_LogonSession do Win32**](win32-logonsession.md)                     | Classe de instância<br/> Descreve a sessão de logon ou as sessões associadas a um usuário conectado ao Windows.<br/>                        |
| [**Logon \_ do Win32SessionMappedDisk**](/windows/desktop/CIMWin32Prov/win32-logonsessionmappeddisk) | Classe de instância<br/> Representa os discos lógicos mapeados associados à sessão.<br/>                                            |
| [**Win32 \_ NetworkLoginProfile**](win32-networkloginprofile.md)       | Classe de instância<br/> Representa as informações de logon de rede de um usuário específico em um sistema de computador executando Windows.<br/>           |
| [**Win32 \_ SystemAccount**](win32-systemaccount.md)                   | Classe de instância<br/> Representa uma conta do sistema.<br/>                                                                                |
| [**Win32 \_ UserAccount**](win32-useraccount.md)                       | Classe de instância<br/> Representa informações sobre uma conta de usuário em um sistema de computador executando Windows.<br/>                           |
| [**Win32 \_ UserInDomain**](/previous-versions/windows/desktop/cimwin32a/win32-userindomain)                     | Classe de associação<br/> Relaciona uma conta de usuário e um Windows NT domínio.<br/>                                                          |



 

## <a name="windows-event-log"></a>Log de eventos do Windows

As classes Windows de subcategoria do Log de Eventos que representam eventos, entradas de log de eventos, definições de configuração do log de eventos e assim por diante.



| Classe                                                         | Descrição                                                                                                                                                                   |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))         | Classe de instância<br/> Representa os dados armazenados em um arquivo Windows log de eventos.<br/>                                                                                      |
| [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)                 | Classe de instância<br/> Representa Windows eventos.<br/>                                                                                                               |
| [**Win32 \_ NTLogEventComputer**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventcomputer) | Classe de associação<br/> Relaciona instâncias de [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) e [**Win32 \_ ComputerSystem**](win32-computersystem.md).<br/>         |
| [**Win32 \_ NTLogEventLog**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventlog)           | Classe de associação<br/> Relaciona instâncias das [**classes Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) e [**Win32 \_ NTEventlogFile.**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))<br/> |
| [**Win32 \_ NTLogEventUser**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventuser)         | Classe de associação<br/> Relaciona instâncias de [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) e [**Win32 \_ UserAccount**](win32-useraccount.md).<br/>               |



 

## <a name="windows-product-activation"></a>Windows Ativação do produto

Windows A Ativação de Produto (WPA) é uma tecnologia antiespaco para reduzir a cópia casual de software.



| Classe                                                                                                               | Descrição                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ComputerSystemWindowsProductActivationSetting**](/previous-versions/windows/desktop/licwmiprov/win32-computersystemwindowsproductactivationsetting) | Classe de associação<br/> Relaciona instâncias do [**Win32 \_ ComputerSystem e**](win32-computersystem.md) [**Win32 \_ WindowsProductActivation**](/previous-versions/windows/desktop/legacy/aa394520(v=vs.85)).<br/> |
| [**Win32 \_ Proxy**](/previous-versions/windows/desktop/legacy/aa394389(v=vs.85))                                                                                 | Classe de instância<br/> Contém propriedades e métodos para consultar e configurar uma conexão com a Internet relacionada ao WPA.<br/>                                                                |
| [**Win32 \_ WindowsProductActivation**](/previous-versions/windows/desktop/legacy/aa394520(v=vs.85))                                           | Classe de instância<br/> Contém propriedades e métodos relacionados ao WPA.<br/>                                                                                                              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Win32 Classes](/previous-versions//aa394084(v=vs.85))
</dt> </dl>

 

