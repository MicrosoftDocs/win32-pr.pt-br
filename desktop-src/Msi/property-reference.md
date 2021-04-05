---
description: 'Esta seção lista as propriedades definidas por Windows Installer:'
ms.assetid: c91119b9-59d5-4a33-91cd-d3ba63659d12
title: Referência de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2ae30800d3c718549ecc887e3438d743881f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662150"
---
# <a name="property-reference"></a>Referência de propriedade

Esta seção lista as propriedades definidas por Windows Installer:

-   [Propriedades de local do componente](#component-location-properties)
-   [Propriedades de configuração](#configuration-properties)
-   [Propriedades de data, hora](#date-time-properties)
-   [Propriedades de opções de instalação de recurso](#feature-installation-options-properties)
-   [Propriedades de hardware](#hardware-properties)
-   [Propriedades de status da instalação](#installation-status-properties)
-   [Propriedades do sistema operacional](#operating-system-properties)
-   [Propriedades de informações do produto](#product-information-properties)
-   [Propriedades de atualização de informações de resumo](#summary-information-update-properties)
-   [Propriedades da pasta do sistema](#system-folder-properties)
-   [Propriedades de informações do usuário](#user-information-properties)

Propriedades adicionais podem ser especificadas por dados criados ou ações personalizadas. Propriedades com nomes que não contêm letras minúsculas são propriedades públicas e podem ser especificadas na linha de comando.

Para obter informações sobre os valores da chave de registro de **desinstalação** que são fornecidos pelas propriedades do instalador, consulte [desinstalar chave do registro](uninstall-registry-key.md).

## <a name="component-location-properties"></a>Propriedades de local do componente

A lista a seguir fornece links para mais informações sobre as propriedades de local do componente.



| Propriedade                                                            | Descrição                                                                                                                                                                                                        |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OriginalDatabase**](originaldatabase.md)<br/>             | O instalador define essa propriedade como o banco de dados iniciado de, o banco de dados na origem ou o banco de dados armazenado em cache.<br/>                                                                                     |
| [**ParentOriginalDatabase**](parentoriginaldatabase.md)<br/> | O instalador define essa propriedade para instalações executadas por uma ação de [instalação simultânea](concurrent-installations.md) .<br/>                                                                             |
| [**SourceDir**](sourcedir.md)<br/>                           | Diretório raiz que contém os arquivos de origem.<br/>                                                                                                                                                          |
| [**TARGETDIR**](targetdir.md)<br/>                           | Especifica o diretório de destino raiz para a instalação. Durante uma [instalação administrativa](administrative-installation.md) , essa propriedade é o local para copiar o pacote de instalação.<br/> |



 

## <a name="configuration-properties"></a>Configuration Properties

A lista a seguir fornece links para mais informações sobre outras propriedades configuráveis.



| Propriedade                                                                                | Descrição                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACTION**](action.md)<br/>                                                     | Ação inicial chamada depois que o instalador é inicializado.<br/>                                                                                                                                                                                                                                                                                                                          |
| [**ALLUSERS**](allusers.md)<br/>                                                 | Determina onde as informações de configuração são armazenadas.<br/>                                                                                                                                                                                                                                                                                                                              |
| [**ARPAUTHORIZEDCDFPREFIX**](arpauthorizedcdfprefix.md)<br/>                     | URL do canal de atualização para um aplicativo.<br/>                                                                                                                                                                                                                                                                                                                                      |
| [**ARPCOMMENTS**](arpcomments.md)<br/>                                           | Fornece comentários para **Adicionar ou remover programas** no **painel de controle**.<br/>                                                                                                                                                                                                                                                                                                         |
| [**ARPCONTACT**](arpcontact.md)<br/>                                             | Fornece contato para **Adicionar ou remover programas** no **painel de controle**.<br/>                                                                                                                                                                                                                                                                                                          |
| [**ARPINSTALLLOCATION**](arpinstalllocation.md)<br/>                             | Caminho totalmente qualificado para a pasta principal de um aplicativo.<br/>                                                                                                                                                                                                                                                                                                                      |
| [**ARPNOMODIFY**](arpnomodify.md)<br/>                                           | Desabilita a funcionalidade que modifica um produto.<br/>                                                                                                                                                                                                                                                                                                                                    |
| [**ARPNOREMOVE**](arpnoremove.md)<br/>                                           | Desabilita a funcionalidade que remove um produto.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**ARPNOREPAIR**](arpnorepair.md)<br/>                                           | Desabilita o botão **reparar** no assistente de programas.<br/>                                                                                                                                                                                                                                                                                                                             |
| [**ARPPRODUCTICON**](arpproducticon.md)<br/>                                     | Especifica o ícone primário para o pacote de instalação.<br/>                                                                                                                                                                                                                                                                                                                           |
| [**ARPREADME**](arpreadme.md)<br/>                                               | Fornece um **Leiame** para **Adicionar ou remover programas** no **painel de controle**.<br/>                                                                                                                                                                                                                                                                                                     |
| [**ARPSIZE**](arpsize.md)<br/>                                                   | Tamanho estimado de um aplicativo em kilobytes.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**ARPSYSTEMCOMPONENT**](arpsystemcomponent.md)<br/>                             | Impede a exibição de um aplicativo na lista **Adicionar ou remover programas** .<br/>                                                                                                                                                                                                                                                                                                         |
| [**ARPURLINFOABOUT**](arpurlinfoabout.md)<br/>                                   | URL para a home page de um aplicativo.<br/>                                                                                                                                                                                                                                                                                                                                           |
| [**ARPURLUPDATEINFO**](arpurlupdateinfo.md)<br/>                                 | URL para informações de atualização do aplicativo.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**AVAILABLEFREEREG**](availablefreereg.md)<br/>                                 | Espaço do registro (em kilobytes) que um aplicativo requer. Usado pela [ação AllocateRegistrySpace](allocateregistryspace-action.md).<br/>                                                                                                                                                                                                                                              |
| [**\_unidade CCP**](ccp-drive.md)<br/>                                              | O caminho raiz para produtos qualificados para o CCP.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**DefaultUIFont**](defaultuifont.md)<br/>                                       | Estilo de fonte padrão usado para controles.<br/>                                                                                                                                                                                                                                                                                                                                              |
| [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md)<br/>                         | Defina para desabilitar a geração de atalhos específicos que dão suporte à [instalação sob demanda](installation-on-demand.md).<br/>                                                                                                                                                                                                                                                            |
| [**DISABLEMEDIA**](-disablemedia.md)<br/>                                        | Impede que o instalador Registre fontes de mídia, como um CD-ROMs, como fontes válidas para o produto.<br/>                                                                                                                                                                                                                                                                        |
| [**DISABLEROLLBACK**](-disablerollback.md)<br/>                                  | Desabilita a reversão da configuração atual.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**EXECUTEACTION**](executeaction.md)<br/>                                       | Ação de nível superior que ExecuteAction inicia.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**EXECUTEmode**](executemode.md)<br/>                                           | Modo de execução que o instalador executa.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**FASTOEM**](fastoem.md)<br/>                                                   | Melhora o desempenho da instalação em cenários específicos de OEM.<br/>                                                                                                                                                                                                                                                                                                                    |
| [**INSTALLLEVEL**](installlevel.md)<br/>                                         | Nível inicial em que os recursos são instalados.<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**LIMITUI**](limitui.md)<br/>                                                   | Nível de interface do usuário limitado como básico.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**LOGACTION**](logaction.md)<br/>                                               | Lista de nomes de ação a serem registrados.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**MEDIAPACKAGEPATH**](mediapackagepath.md)<br/>                                 | Essa propriedade deve ser definida como o caminho relativo se o pacote de instalação não estiver localizado na raiz do CD-ROM.<br/>                                                                                                                                                                                                                                                               |
| [**MSIARPSETTINGSIDENTIFIER**](msiarpsettingsidentifier.md)<br/>                 | Essa propriedade opcional contém uma lista delimitada por ponto e vírgula dos locais do registro onde o aplicativo armazena as configurações e preferências de um usuário. Disponível com Windows Installer 4,0.<br/>                                                                                                                                                                                        |
| [**MSIDISABLEEEUI**](msidisableeeui.md)<br/>                                     | Desabilite a interface do usuário inserida para a instalação.<br/> **[Windows Installer 4,0 e anteriores](not-supported-in-windows-installer-4-0.md):** Sem suporte.<br/>                                                                                                                                                                                                           |
| [**MSIFASTINSTALL**](msifastinstall.md)<br/>                                     | Reduza o tempo necessário para instalar um pacote de Windows Installer grande.<br/> **[Windows Installer 4,5 e anteriores](not-supported-in-windows-installer-4-5.md):** Sem suporte.<br/>                                                                                                                                                                                              |
| [**MSIINSTALLPERUSER**](msiinstallperuser.md)<br/>                               | Solicita que o Windows Installer instale o pacote somente para o usuário atual.<br/> **[Windows Installer 4,5 e anteriores](not-supported-in-windows-installer-4-5.md):** Sem suporte.<br/>                                                                                                                                                                                  |
| [**MSINODISABLEMEDIA**](msinodisablemedia.md)<br/>                               | Defina essa propriedade para impedir que o instalador defina a propriedade [**DISABLEMEDIA**](-disablemedia.md) .<br/>                                                                                                                                                                                                                                                                        |
| [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)<br/>   | Defina essa propriedade como 1 (uma) na linha de comando ou na [tabela de propriedades](property-table.md) para aplicar as regras de componente de atualização durante [pequenas atualizações](small-updates.md) [e pequenas atualizações de](minor-upgrades.md) um produto específico. Disponível a partir do Windows Installer 3,0.<br/>                                                                                     |
| [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md)<br/> | Quando essa propriedade tiver sido definida como 1, o instalador poderá cancelar o registro e desinstalar componentes redundantes para evitar deixar por trás dos componentes órfãos no computador.<br/> **[Windows Installer 4,0 e anteriores](not-supported-in-windows-installer-4-0.md):** Sem suporte.<br/>                                                                                                  |
| [**PRIMARYFOLDER**](primaryfolder.md)<br/>                                       | Permite que o autor designe uma pasta principal para uma instalação. Usado para determinar os valores para as propriedades [**PrimaryVolumePath**](primaryvolumepath.md), [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md), [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md)e [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) .<br/> |
| [**Privilégio**](privileged.md)<br/>                                             | Executa uma instalação com privilégios elevados.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md)<br/>                             | Ação se não houver espaço em disco suficiente para a instalação.<br/>                                                                                                                                                                                                                                                                                                                   |
| [**Inicialize**](reboot.md)<br/>                                                     | Força ou suprime uma reinicialização.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| [**REBOOTPROMPT**](rebootprompt.md)<br/>                                         | Suprime a exibição de prompts para reinicializações para o usuário. Todas as reinicializações necessárias ocorrem automaticamente.<br/>                                                                                                                                                                                                                                                                     |
| [**ROOTDRIVE**](rootdrive.md)<br/>                                               | Unidade padrão para uma instalação.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**SEQUENCE**](sequence.md)<br/>                                                 | Uma tabela que tem o esquema de tabela de sequência.<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**SHORTFILENAMES**](shortfilenames.md)<br/>                                     | Faz com que nomes de arquivo curtos sejam usados.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**TRANSFORMAÇÕES**](transforms.md)<br/>                                             | Lista de transformações a serem aplicadas a um banco de dados.<br/>                                                                                                                                                                                                                                                                                                                                    |
| [**TRANSFORMSATSOURCE**](transformsatsource.md)<br/>                             | Informa o instalador de que as transformações de um produto residem na origem.<br/>                                                                                                                                                                                                                                                                                                      |
| [**TRANSFORMSSECURE**](transformssecure.md)<br/>                                 | Definir a propriedade [**TRANSFORMSECURE**](transformssecure.md) como 1 (uma) informa ao instalador que as transformações devem ser armazenadas em cache localmente no computador do usuário em um local em que o usuário não tem acesso de gravação.<br/>                                                                                                                                                           |
| [**MsiLogFileLocation**](msilogfilelocation.md)<br/>                             | O instalador define o valor dessa propriedade como o caminho completo do arquivo de log, quando o log foi habilitado. Essa propriedade está disponível a partir do Windows Installer 4,0.<br/>                                                                                                                                                                                                     |
| [**MsiLogging**](msilogging.md)<br/>                                             | Define o modo de log padrão para o pacote de Windows Installer. Essa propriedade está disponível a partir do Windows Installer 4,0.<br/>                                                                                                                                                                                                                                                   |
| [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md)<br/>                 | Defina essa propriedade como 1 para solicitar que o instalador Use informações reais do usuário ao definir a propriedade [**AdminUser**](adminuser.md) . Essa propriedade está disponível a partir do Windows Installer 4,0.<br/>                                                                                                                                                                         |



 

## <a name="date-time-properties"></a>Propriedades de data, hora

As propriedades de [**Data**](date.md) e [**hora**](time.md) são propriedades dinâmicas que o instalador define quando os dados são extraídos.



| Propriedade                        | Descrição                  |
|---------------------------------|------------------------------|
| [**Data**](date.md)<br/> | A data atual.<br/> |
| [**Momento**](time.md)<br/> | A hora atual.<br/> |



 

## <a name="feature-installation-options-properties"></a>Propriedades de opções de instalação de recurso

A lista a seguir fornece links para mais informações sobre as propriedades de opções de instalação de recursos.



| Propriedade                                                                | Descrição                                                                                                                                                                       |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ADDDEFAULT**](adddefault.md)<br/>                             | Lista de recursos a serem instalados na configuração padrão.<br/>                                                                                                         |
| [**ADDLOCAL**](addlocal.md)<br/>                                 | Lista de recursos a serem instalados localmente.<br/>                                                                                                                              |
| [**Addsource**](addsource.md)<br/>                               | Lista de recursos a serem executados da origem.<br/>                                                                                                                                |
| [**ANUNCI**](advertise.md)<br/>                               | Lista de recursos a serem anunciados.<br/>                                                                                                                                     |
| [**COMPADDDEFAULT**](compadddefault.md)<br/>                     | Lista de componentes a serem instalados na configuração padrão.<br/>                                                                                                       |
| [**COMPADDLOCAL**](compaddlocal.md)<br/>                         | Lista de IDs de componentes a serem instalados localmente.<br/>                                                                                                                         |
| [**COMPADDSOURCE**](compaddsource.md)<br/>                       | Lista de IDs de componentes a serem executados da mídia de origem.<br/>                                                                                                                        |
| [**FILEADDDEFAULT**](fileadddefault.md)<br/>                     | Lista de chaves de arquivo para os arquivos a serem instalados na configuração padrão.<br/>                                                                                              |
| [**FILEADDLOCAL**](fileaddlocal.md)<br/>                         | Lista de chaves de arquivo para os arquivos a serem executados localmente.<br/>                                                                                                                         |
| [**FILEADDSOURCE**](fileaddsource.md)<br/>                       | Lista de chaves de arquivo a serem executadas na mídia de origem.<br/>                                                                                                                     |
| [**MSIDISABLELUAPATCHING**](msidisableluapatching.md)<br/>       | Definir essa propriedade impede a aplicação de patches de LUA (usuário menos privilegiado) de um aplicativo.<br/>                                                                                 |
| [**MsiPatchRemovalList**](msipatchremovallist.md)<br/>           | Lista de patches a serem removidos durante a instalação.<br/>                                                                                                                 |
| [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)<br/> | Especifica se o pacote usa o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) ou a funcionalidade [FilesInUse](filesinuse-dialog.md) .<br/>                                          |
| [**MSIDISABLERMRESTART**](msidisablermrestart.md)<br/>           | Especifica como os aplicativos ou serviços que estão usando atualmente arquivos afetados por uma atualização devem ser desligados e reiniciados para habilitar a instalação da atualização.<br/> |
| [**MSIRMSHUTDOWN**](msirmshutdown.md)<br/>                       | Especifica como os aplicativos ou serviços que estão usando atualmente arquivos afetados por uma atualização devem ser desligados para habilitar a instalação da atualização.<br/>               |
| [**MSIPATCHREMOVE**](msipatchremove.md)<br/>                     | Definir essa propriedade Remove patches.<br/>                                                                                                                                 |
| [**DISTRIBUÍDO**](patch.md)<br/>                                       | A definição dessa propriedade aplica um patch.<br/>                                                                                                                                 |
| [**Install**](reinstall.md)<br/>                               | Lista de recursos a serem reinstalados.<br/>                                                                                                                                    |
| [**REINSTALLMODE**](reinstallmode.md)<br/>                       | Uma cadeia de caracteres que contém letras que especificam o tipo de reinstalação a ser executado.<br/>                                                                                          |
| [**EXCLU**](remove.md)<br/>                                     | Lista de recursos a serem removidos.<br/>                                                                                                                                        |



 

## <a name="hardware-properties"></a>Propriedades de hardware

A lista a seguir identifica as propriedades de hardware que o Windows Installer define na inicialização.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propriedade</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="alpha.md"><strong>Alpha</strong></a><br/></td>
<td>O nível numérico do processador quando executado em um processador Alpha.<br/>
<blockquote>
[!Note]<br />
Esta propriedade é obsoleta, a plataforma alfa não tem suporte pelo Windows Installer.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="borderside.md"><strong>BorderSide</strong></a><br/></td>
<td>A largura das bordas da janela, em pixels.<br/></td>
</tr>
<tr class="odd">
<td><a href="bordertop.md"><strong>BorderTop</strong></a><br/></td>
<td>A altura das bordas da janela, em pixels.<br/></td>
</tr>
<tr class="even">
<td><a href="captionheight.md"><strong>CaptionHeight</strong></a><br/></td>
<td>A altura da área de legenda normal, em pixels.<br/></td>
</tr>
<tr class="odd">
<td><a href="colorbits.md"><strong>ColorBits</strong></a><br/></td>
<td>O número de bits de cor adjacentes para cada pixel.<br/></td>
</tr>
<tr class="even">
<td><a href="intel.md"><strong>Processador</strong></a><br/></td>
<td>O nível numérico do processador quando executado em um processador Intel.<br/></td>
</tr>
<tr class="odd">
<td><a href="intel64.md"><strong>Intel64</strong></a><br/></td>
<td>O nível numérico do processador quando executado em um processador Itanium.<br/></td>
</tr>
<tr class="even">
<td><a href="msix64.md"><strong>Msix64</strong></a><br/></td>
<td>O nível numérico do processador quando executado em um processador x64.<br/></td>
</tr>
<tr class="odd">
<td><a href="physicalmemory.md"><strong>PhysicalMemory</strong></a><br/></td>
<td>O tamanho da RAM instalada, em megabytes.<br/></td>
</tr>
<tr class="even">
<td><a href="screenx.md"><strong>ScreenX</strong></a><br/></td>
<td>A largura da tela, em pixels.<br/></td>
</tr>
<tr class="odd">
<td><a href="screeny.md"><strong>Tela</strong></a><br/></td>
<td>A altura da tela, em pixels.<br/></td>
</tr>
<tr class="even">
<td><a href="textheight.md"><strong>TextHeight</strong></a><br/></td>
<td>A altura dos caracteres, em unidades lógicas.<br/></td>
</tr>
<tr class="odd">
<td><a href="virtualmemory.md"><strong>VirtualMemory</strong></a><br/></td>
<td>A quantidade de espaço de arquivo de paginação disponível, em megabytes.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="installation-status-properties"></a>Propriedades de status da instalação

A lista a seguir fornece links para mais informações sobre as propriedades de status que são atualizadas pelo instalador durante a instalação.



| Propriedade                                                                      | Descrição                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AFTERREBOOT**](afterreboot.md)<br/>                                 | Indica que a instalação atual segue uma reinicialização que a [ação ForceReboot](forcereboot-action.md) invoca.<br/>                                                                                                                                                |
| [**CostingComplete**](costingcomplete.md)<br/>                         | Indica se o custo do espaço em disco foi concluído.<br/>                                                                                                                                                                                                             |
| [**Instalado**](installed.md)<br/>                                     | Indica que um produto já está instalado.<br/>                                                                                                                                                                                                                |
| [**MSICHECKCRCS**](msicheckcrcs.md)<br/>                               | O instalador fará um CRC nos arquivos somente se a propriedade [**MSICHECKCRCS**](msicheckcrcs.md) estiver definida.<br/>                                                                                                                                                           |
| [**MsiRestartManagerSessionKey**](msirestartmanagersessionkey.md)<br/> | O instalador define essa propriedade como a chave de sessão para a sessão do [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) .<br/>                                                                                                                                                         |
| [**MsiRunningElevated**](msirunningelevated-.md)<br/>                  | O instalador define o valor dessa propriedade como 1 quando o instalador está sendo executado com privilégios [*elevados*](e-gly.md) .<br/>                                                                                                                   |
| [**MsiSystemRebootPending**](msisystemrebootpending.md)<br/>           | O instalador definirá essa propriedade como 1 se uma reinicialização do sistema operacional estiver pendente no momento.<br/>                                                                                                                                                              |
| [**MsiUIHideCancel**](msiuihidecancel.md)<br/>                         | O instalador define [**MsiUIHideCancel**](msiuihidecancel.md) como 1 quando o nível de instalação interno inclui **INSTALLUILEVEL \_ HIDECANCEL**.<br/>                                                                                                                   |
| [**MsiUIProgressOnly**](msiuiprogressonly.md)<br/>                     | O instalador define [**MsiUIProgressOnly**](msiuiprogressonly.md) como 1 quando o nível de instalação interno inclui **INSTALLUILEVEL \_ PROGRESSONLY**.<br/>                                                                                                             |
| [**MsiUISourceResOnly**](msiuisourceresonly.md)<br/>                   | [**MsiUISourceResOnly**](msiuisourceresonly.md) para 1 (um) quando o nível de instalação interno inclui **INSTALLUILEVEL \_ SOURCERESONLY**.<br/>                                                                                                                       |
| [**Nocompanyname**](nocompanyname.md)<br/>                             | Suprime a configuração automática da propriedade [**CompanyName**](companyname.md) .<br/>                                                                                                                                                                          |
| [**NOUSERNAME**](nousername.md)<br/>                                   | Suprime a configuração automática da propriedade [**username**](username.md) .<br/>                                                                                                                                                                                |
| [**OutOfDiskSpace**](outofdiskspace.md)<br/>                           | Espaço em disco insuficiente para acomodar a instalação.<br/>                                                                                                                                                                                                      |
| [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)<br/>                   | Espaço em disco insuficiente com reversão desativada.<br/>                                                                                                                                                                                                             |
| [**Pré-selecionados**](preselected.md)<br/>                                 | Os recursos já estão selecionados.<br/>                                                                                                                                                                                                                                |
| [**PrimaryVolumePath**](primaryvolumepath.md)<br/>                     | O instalador define o valor dessa propriedade como o caminho do volume que a propriedade [**PRIMARYFOLDER**](primaryfolder.md) designa.<br/>                                                                                                                  |
| [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md)<br/> | O instalador define o valor dessa propriedade como uma cadeia de caracteres que representa o número total de bytes disponíveis no volume que a propriedade [**PrimaryVolumePath**](primaryvolumepath.md) faz referência.<br/>                                                      |
| [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md)<br/> | O instalador define o valor dessa propriedade como uma cadeia de caracteres que representa o número total de bytes restantes no volume que a propriedade [**PrimaryVolumePath**](primaryvolumepath.md) faz referência se todos os recursos selecionados no momento estiverem instalados.<br/> |
| [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md)<br/>   | O instalador define o valor dessa propriedade como uma cadeia de caracteres que representa o número total de bytes exigidos por todos os recursos atualmente selecionados no volume ao qual a propriedade [**PrimaryVolumePath**](primaryvolumepath.md) faz referência.<br/>                    |
| [**ProductLanguage**](productlanguage.md)<br/>                         | Identificador de idioma numérico (LANGid) para o banco de dados. NECESSÁRIA<br/>                                                                                                                                                                                             |
| [**ReplacedInUseFiles**](replacedinusefiles.md)<br/>                   | Defina se o instalador é instalado em um arquivo que está sendo mantido em uso.<br/>                                                                                                                                                                                          |
| [**Volte**](resume.md)<br/>                                           | Instalação retomada.<br/>                                                                                                                                                                                                                                         |
| [**RollbackDisabled**](rollbackdisabled.md)<br/>                       | O instalador define essa propriedade quando a reversão está desabilitada.<br/>                                                                                                                                                                                                   |
| [**UILevel**](uilevel.md)<br/>                                         | Indica o nível da interface do usuário.<br/>                                                                                                                                                                                                                           |
| [**UpdateStarted**](updatestarted.md)<br/>                             | Defina quando as alterações no sistema começaram para esta instalação.<br/>                                                                                                                                                                                              |
| [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md)<br/>               | Definido pelo instalador quando uma atualização remove um aplicativo.<br/>                                                                                                                                                                                                  |
| [**VersionMsi**](versionmsi.md)<br/>                                   | O instalador define essa propriedade para a versão do Windows Installer que é executada durante a instalação.<br/>                                                                                                                                                     |



 

## <a name="operating-system-properties"></a>Propriedades do sistema operacional

A lista a seguir fornece links para mais informações sobre as propriedades do sistema operacional que o instalador define na inicialização.



| Nome da Propriedade                                                                             | Breve descrição                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdminUser**](adminuser.md)<br/>                                                 | Definido no Windows 2000 se o usuário tiver privilégios de administrador.<br/>                                                                                                                                                                                                                        |
| [**ComputerName**](computername.md)<br/>                                           | Nome do computador do sistema atual.<br/>                                                                                                                                                                                                                                                 |
| [**MsiNetAssemblySupport**](msinetassemblysupport.md)<br/>                         | Em sistemas que dão suporte a assemblies de Common Language Runtime, o instalador define o valor dessa propriedade como a versão de arquivo do fusion.dll. O instalador não definirá essa propriedade se o sistema operacional não oferecer suporte a assemblies Common Language Runtime.<br/>                   |
| [**MsiNTProductType**](msintproducttype.md)<br/>                                   | Indica o tipo de produto do Windows.<br/>                                                                                                                                                                                                                                                  |
| [**MsiNTSuiteBackOffice**](msintsuitebackoffice.md)<br/>                           | No Windows 2000 e sistemas operacionais posteriores, o instalador definirá essa propriedade como 1 (uma) somente se os componentes do Microsoft BackOffice estiverem instalados.<br/>                                                                                                                                      |
| [**MsiNTSuiteDataCenter**](msintsuitedatacenter.md)<br/>                           | No Windows 2000 e sistemas operacionais posteriores, o instalador definirá essa propriedade como 1 (uma) somente se o Windows 2000 Datacenter Server estiver instalado.<br/>                                                                                                                                        |
| [**MsiNTSuiteEnterprise**](msintsuiteenterprise.md)<br/>                           | No Windows 2000 e sistemas operacionais posteriores, o instalador definirá essa propriedade como 1 (uma) somente se o Windows 2000 Advanced Server estiver instalado.<br/>                                                                                                                                          |
| [**MsiNTSuitePersonal**](msintsuitepersonal.md)<br/>                               | No Windows XP e sistemas operacionais posteriores, o instalador definirá essa propriedade como 1 (uma) somente se o sistema operacional for Home (não profissional).<br/>                                                                                                                                      |
| [**MsiNTSuiteSmallBusiness**](msintsuitesmallbusiness.md)<br/>                     | No Windows 2000 e sistemas operacionais posteriores, o instalador definirá essa propriedade como 1 (uma) somente se o Microsoft Small Business Server estiver instalado.<br/>                                                                                                                                       |
| [**MsiNTSuiteSmallBusinessRestricted**](msintsuitesmallbusinessrestricted.md)<br/> | No Windows 2000 e sistemas operacionais posteriores, o instalador definirá essa propriedade como 1 (uma) somente se o Microsoft Small Business Server estiver instalado com a licença de cliente restritiva.<br/>                                                                                                   |
| [**MsiNTSuiteWebServer**](msintsuitewebserver.md)<br/>                             | No Windows 2000 e sistemas operacionais posteriores, o instalador define a propriedade [**MsiNTSuiteWebServer**](msintsuitewebserver.md) como 1 (uma) se a edição da Web do Windows Server 2003 estiver instalada. Disponível somente com a versão 2003 do Windows Server do Windows Installer.<br/> |
| [**MsiTabletPC**](msitabletpc.md)<br/>                                             | O instalador definirá essa propriedade como um valor diferente de zero se o sistema operacional atual for o Windows XP Tablet PC Edition.<br/>                                                                                                                                                                 |
| [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md)<br/>                     | Em sistemas que dão suporte a assemblies do Win32, o instalador define o valor dessa propriedade como a versão do arquivo de sxs.dll. O instalador não definirá essa propriedade se o sistema operacional não oferecer suporte a assemblies Win32.<br/>                                                          |
| [**OLEAdvtSupport**](oleadvtsupport.md)<br/>                                       | Defina se o OLE dá suporte à Windows Installer.<br/>                                                                                                                                                                                                                                           |
| [**RedirectedDllSupport**](redirecteddllsupport.md)<br/>                           | O instalador definirá a propriedade [**RedirectedDllSupport**](redirecteddllsupport.md) se o sistema que estiver executando a instalação oferecer suporte a [componentes isolados](isolated-components.md).<br/>                                                                                              |
| [**RemoteAdminTS**](remoteadmints.md)<br/>                                         | O instalador define a propriedade [**RemoteAdminTS**](remoteadmints.md) quando o sistema é um servidor de administração remota que executa o serviço de função Terminal Server.<br/>                                                                                                                   |
| [**ServicePackLevel**](servicepacklevel.md)<br/>                                   | O número de versão do sistema operacional service pack.<br/>                                                                                                                                                                                                                             |
| [**ServicePackLevelMinor**](servicepacklevelminor.md)<br/>                         | O número de versão secundária do sistema operacional service pack.<br/>                                                                                                                                                                                                                       |
| [**SharedWindows**](sharedwindows.md)<br/>                                         | Defina quando o sistema está operando como janelas compartilhadas.<br/>                                                                                                                                                                                                                                  |
| [**ShellAdvtSupport**](shelladvtsupport.md)<br/>                                   | Defina se o Shell dá suporte ao anúncio de recursos.<br/>                                                                                                                                                                                                                                       |
| [**SystemLanguageID**](systemlanguageid.md)<br/>                                   | Identificador de idioma padrão do sistema.<br/>                                                                                                                                                                                                                                          |
| [**TerminalServer**](terminalserver.md)<br/>                                       | Defina quando o sistema é um servidor que executa o serviço de função Terminal Server.<br/>                                                                                                                                                                                                            |
| [**TTCSupport**](ttcsupport.md)<br/>                                               | Indica se o sistema operacional dá suporte ao uso de arquivos. TTC (conjuntos de fontes True Type).<br/>                                                                                                                                                                                            |
| [**Version9X**](version9x.md)<br/>                                                 | Número de versão do sistema operacional Windows.<br/>                                                                                                                                                                                                                                     |
| [**VersionDatabase**](versiondatabase.md)<br/>                                     | Versão de banco de dados numérica da instalação atual.<br/>                                                                                                                                                                                                                                |
| [**VersionNT**](versionnt.md)<br/>                                                 | Número de versão do sistema operacional.<br/>                                                                                                                                                                                                                                             |
| [**VersionNT64**](versionnt64.md)<br/>                                             | Número de versão do sistema operacional se o sistema estiver sendo executado em um computador de 64 bits.<br/>                                                                                                                                                                                               |
| [**Build do Windows**](windowsbuild.md)<br/>                                          | Número de Build do sistema operacional.<br/>                                                                                                                                                                                                                                                |



 

## <a name="product-information-properties"></a>Propriedades de informações do produto

A lista a seguir fornece links para mais informações sobre as propriedades específicas do produto especificadas na [tabela de propriedades](property-table.md).



| Nome da Propriedade                                                  | Breve descrição                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**ARPHELPLINK**](arphelplink.md)<br/>                  | Endereço de Internet ou URL para suporte técnico.<br/>                                                                                 |
| [**ARPHELPTELEPHONE**](arphelptelephone.md)<br/>        | Números de telefone de suporte técnico.<br/>                                                                                               |
| [**DiskPrompt**](diskprompt.md)<br/>                    | Cadeia de caracteres exibida por uma caixa de mensagem que solicita um disco.<br/>                                                                     |
| [**IsAdminPackage**](isadminpackage.md)<br/>            | Defina como 1 (um) se a instalação atual estiver sendo executada a partir de um pacote criado por meio de uma instalação administrativa.<br/>           |
| [**LeftUnit**](leftunit.md)<br/>                        | Coloca as unidades à esquerda do número.<br/>                                                                                        |
| [**Manufacturer**](manufacturer.md)<br/>                | Nome do fabricante do aplicativo. (Obrigatória)<br/>                                                                               |
| [**MediaSourceDir**](mediasourcedir.md)<br/>            | O instalador define essa propriedade como 1 (uma) quando a instalação usa uma fonte de mídia, como um CD-ROM.<br/>                       |
| [**MSIINSTANCEGUID**](msiinstanceguid.md)<br/>          | A presença dessa propriedade indica que um código de produto que altera a transformação está registrado para o produto.<br/>                   |
| [**MSINEWINSTANCE**](msinewinstance.md)<br/>            | Essa propriedade indica a instalação de uma nova instância de um produto com transformações de instância.<br/>                              |
| [**ParentProductCode**](parentoriginaldatabase.md)<br/> | O instalador define essa propriedade para instalações que uma ação de [instalação simultânea](concurrent-installations.md) executa.<br/> |
| [**PIDTemplate**](pidtemplate.md)<br/>                  | Cadeia de caracteres usada como modelo para a propriedade [**PIDKEY**](pidkey.md) .<br/>                                                           |
| [**ProductCode**](productcode.md)<br/>                  | Um identificador exclusivo para uma versão de produto específica. (Obrigatória)<br/>                                                                 |
| [**ProductName**](productname.md)<br/>                  | Nome legível por humanos de um aplicativo. (Obrigatória)<br/>                                                                              |
| [**ProductState**](productstate.md)<br/>                | Defina como o estado instalado de um produto.<br/>                                                                                       |
| [**ProductVersion**](productversion.md)<br/>            | Formato da cadeia de caracteres da versão do produto como um valor numérico. (Obrigatória)<br/>                                                            |
| [**UpgradeCode**](upgradecode.md)<br/>                  | Um GUID que representa um conjunto de produtos relacionado.<br/>                                                                              |



 

## <a name="summary-information-update-properties"></a>Propriedades de atualização de informações de resumo

As propriedades a seguir são definidas apenas por transformações em arquivos. msp que são usadas para atualizar o fluxo de informações de Resumo de uma imagem administrativa.



| Propriedade                                                              | Descrição                                                                                                                  |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**PATCHNEWPACKAGECODE**](patchnewpackagecode.md)<br/>         | O valor dessa propriedade é gravado na propriedade [**Resumo do número de revisão**](revision-number-summary.md) .<br/> |
| [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)<br/> | O valor dessa propriedade é gravado na propriedade [**Resumo dos comentários**](comments-summary.md) .<br/>               |
| [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md)<br/>   | O valor dessa propriedade é gravado na propriedade de [**Resumo da entidade**](subject-summary.md) .<br/>                 |



 

## <a name="system-folder-properties"></a>Propriedades da pasta do sistema

A lista a seguir fornece links para mais informações sobre pastas do sistema que o instalador define na instalação.



| Propriedade                                                        | Descrição                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**AdminToolsFolder**](admintoolsfolder.md)<br/>         | O caminho completo para o diretório que contém ferramentas administrativas.<br/>         |
| [**AppDataFolder**](appdatafolder.md)<br/>               | O caminho completo para a pasta de **roaming** do usuário atual.<br/>              |
| [**CommonAppDataFolder**](commonappdatafolder.md)<br/>   | O caminho completo para os dados do aplicativo para todos os usuários.<br/>                           |
| [**CommonFiles64Folder**](commonfiles64folder.md)<br/>   | O caminho completo para a pasta predefinida **Arquivos comuns de 64 bits** .<br/>            |
| [**CommonFilesFolder**](commonfilesfolder.md)<br/>       | O caminho completo para a pasta **Arquivos comuns** do usuário atual.<br/>         |
| [**DesktopFolder**](desktopfolder.md)<br/>               | O caminho completo para a pasta **da área de trabalho** .<br/>                                   |
| [**FavoritesFolder**](favoritesfolder.md)<br/>           | O caminho completo para a pasta **favoritos** do usuário atual.<br/>            |
| [**FontsFolder**](fontsfolder.md)<br/>                   | O caminho completo para a pasta **fontes** .<br/>                                     |
| [**LocalAppDataFolder**](localappdatafolder.md)<br/>     | O caminho completo para a pasta que contém aplicativos locais (não móveis).<br/> |
| [**MyPicturesFolder**](mypicturesfolder.md)<br/>         | O caminho completo para a pasta **imagens** .<br/>                                  |
| [**NetHoodFolder**](nethoodfolder.md)<br/>               | O caminho completo para a pasta **netbastidor** .<br/>                                   |
| [**PersonalFolder**](personalfolder.md)<br/>             | O caminho completo para a pasta **documentos** do usuário atual.<br/>            |
| [**PrintHoodFolder**](printhoodfolder.md)<br/>           | O caminho completo para a pasta de **enbastidor** .<br/>                                 |
| [**ProgramFiles64Folder**](programfiles64folder.md)<br/> | O caminho completo para a pasta predefinida **arquivos de programas de 64 bits** .<br/>           |
| [**ProgramFilesFolder**](programfilesfolder.md)<br/>     | O caminho completo para a pasta predefinida **arquivos de programas de 32 bits** .<br/>           |
| [**ProgramMenuFolder**](programmenufolder.md)<br/>       | O caminho completo para a pasta de **menu do programa** .<br/>                              |
| [**RecentFolder**](recentfolder.md)<br/>                 | O caminho completo para a pasta **recente** .<br/>                                    |
| [**SendToFolder**](sendtofolder.md)<br/>                 | O caminho completo para a pasta **SendTo** do usuário atual.<br/>               |
| [**StartMenuFolder**](startmenufolder.md)<br/>           | O caminho completo para a pasta do **menu iniciar** .<br/>                                |
| [**StartupFolder**](startupfolder.md)<br/>               | O caminho completo para a pasta de **inicialização** .<br/>                                   |
| [**System16Folder**](system16folder.md)<br/>             | O caminho completo para a pasta para DLLs de sistema de 16 bits.<br/>                            |
| [**System64Folder**](system64folder.md)<br/>             | O caminho completo para a pasta **System64** predefinida.<br/>                       |
| [**SystemFolder**](systemfolder.md)<br/>                 | O caminho completo para a pasta do **sistema** para o usuário atual.<br/>               |
| [**TempFolder**](tempfolder.md)<br/>                     | O caminho completo para a pasta **Temp** .<br/>                                      |
| [**TemplateFolder**](templatefolder.md)<br/>             | O caminho completo para a pasta de **modelo** do usuário atual.<br/>             |
| [**WindowsFolder**](windowsfolder.md)<br/>               | O caminho completo para a pasta do **Windows** .<br/>                                   |
| [**WindowsVolume**](windowsvolume.md)<br/>               | O volume da pasta do **Windows** .<br/>                                      |



 

## <a name="user-information-properties"></a>Propriedades de informações do usuário

A lista a seguir fornece links para mais informações sobre as informações fornecidas pelo usuário.



| Propriedade                                                      | Descrição                                                                             |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**Adminproperties**](adminproperties.md)<br/>         | Lista de propriedades que são definidas durante uma instalação de administração.<br/>       |
| [**COMPANYNAME**](companyname.md)<br/>                 | Nome da organização do usuário que está executando a instalação.<br/>            |
| [**LogonUser**](logonuser.md)<br/>                     | Nome de usuário para o usuário que está conectado no momento.<br/>                           |
| [**MsiHiddenProperties**](msihiddenproperties.md)<br/> | Lista de propriedades que são impedidas de serem gravadas no log.<br/>       |
| [**PIDKEY**](pidkey.md)<br/>                           | Parte da ID do produto que o usuário insere.<br/>                                 |
| [**ProductID**](productid.md)<br/>                     | A ID completa do produto após uma validação bem-sucedida.<br/>                               |
| [**Userlanguageid**](userlanguageid.md)<br/>           | Identificador de idioma padrão do usuário atual.<br/>                             |
| [**USU**](username.md)<br/>                       | Usuário que está executando a instalação.<br/>                                     |
| [**Propriedade UserID**](usersid.md)<br/>                | Definido pelo instalador de acordo com o SID (identificador de segurança) do usuário.<br/> |



 

 

 
