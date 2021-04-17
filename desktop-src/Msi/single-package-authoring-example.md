---
description: O PUASample.msi de exemplo é um exemplo de um pacote de Windows Installer 5,0 de uso duplo que é capaz de ser instalado no contexto de instalação por usuário ou por computador no Windows Server 2008 R2 e no Windows 7.
ms.assetid: be018e8a-ca5f-4135-a019-970ec4173f23
title: Exemplo de criação de pacote único
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0ed56b8d7aaf8793416ba3ecab24c1f2a48ffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749779"
---
# <a name="single-package-authoring-example"></a>Exemplo de criação de pacote único

O PUASample.msi de exemplo é um exemplo de um pacote de Windows Installer 5,0 de uso duplo que é capaz de ser instalado no [contexto de instalação](installation-context.md) por usuário ou por computador no windows Server 2008 R2 e no Windows 7. Este pacote de exemplo segue as diretrizes de desenvolvimento descritas em [criação de pacote único](single-package-authoring.md).

## <a name="obtaining-a-copy-of-the-sample"></a>Obtendo uma cópia do exemplo

Uma cópia deste exemplo e um Windows Installer editor de tabela de banco de dados, Orca.exe, estão nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). O editor de exemplo e tabela é fornecido com o kit de desenvolvimento de software do Windows para Windows Server 2008 R2 e Windows 7 como os arquivos de instalação do Windows Installer PUASample1.msi e Orca.msi.

## <a name="system-requirements"></a>Requisitos do Sistema

O editor de banco de dados, [Orca.exe](orca-exe.md), requer o windows Server 2008 R2 e versões anteriores e o Windows 7 e versões anteriores. O pacote de uso duplo, PUASample1.msi, pode ser instalado no [contexto de instalação](installation-context.md) por computador ou por usuário no windows Server 2008 R2 e no Windows 7. PUASample1.msi pode ser instalado somente no contexto por máquina no Windows Server 2008 e versões anteriores e no Windows Vista e versões anteriores. Você pode instalar o editor de banco de dados para examinar o conteúdo de PUASample1.msi sem instalar o exemplo. Para instalar os pacotes de exemplo ou editor, verifique se a política [DisableMSI](disablemsi.md) não está definida como um valor que bloqueia as instalações de aplicativos.

## <a name="identifying-a-dual-purpose-package"></a>Identificando um pacote de Dual-Purpose

Os pacotes de uso duplo devem inicializar o valor da propriedade [**MSIINSTALLPERUSER**](msiinstallperuser.md) como 1. Isso identifica o pacote como sendo capaz de ser instalado no contexto por computador ou por usuário no Windows Server 2008 R2 e no Windows 7. Defina a propriedade **MSIINSTALLPERUSER** no pacote somente se ele tiver sido escrito seguindo as diretrizes de desenvolvimento descritas em [criação de pacote único](single-package-authoring.md) e se você pretende fornecer aos usuários a opção de instalar o pacote no contexto por usuário ou por máquina. Um pacote de uso duplo também deve inicializar o valor da propriedade [**AllUsers**](allusers.md) como 2. Isso especifica por usuário como o contexto de instalação padrão para o aplicativo. Se o valor da propriedade **AllUsers** for qualquer valor diferente de 2, Windows Installer ignorará a propriedade **MSIINSTALLPERUSER** .

Use um editor de banco de dados Windows Installer, como [Orca.exe](orca-exe.md), para examinar o conteúdo de PUASample1.msi. A tabela de [Propriedades](property-table.md) no pacote de exemplo contém as duas entradas a seguir.

[Propriedade](property-table.md) Tabela (parcial)

| Propriedade          | Valor |
|-------------------|-------|
| ALLUSERS          | 2     |
| MSIINSTALLPERUSER | 1     |



 

## <a name="custom-dialog-box-for-installation-context"></a>Caixa de diálogo personalizada para contexto de instalação

A [interface do usuário](user-interface.md) do pacote de exemplo inclui um exemplo de uma caixa de diálogo personalizada, VerifyReadyDialog, que permite aos usuários selecionar o contexto de instalação por usuário ou por máquina no momento da instalação. A tabela de [diálogo](dialog-table.md) contém um registro que descreve a caixa de diálogo VerifyReadyDialog. O valor inserido no campo atributos é 39 porque essa caixa de diálogo usa os [bits de estilo de caixa de diálogo](dialog-style-bits.md)msidbDialogAttributesVisible (1), msidbDialogAttributesModal (2), msidbDialogAttributesMinimize (4) e msidbDialogAttributesTrackDiskSpace (32). A barra de título da caixa de diálogo exibe um título fornecido pelo valor da propriedade [**ProductName**](productname.md) .

[Caixa de diálogo](dialog-table.md) Tabela (parcial) 

| caixa de diálogo            | HCentering | VCentering | Largura | Altura | Atributos | Título           | Controlar \_ primeiro | Padrão de controle \_ | \_Cancelar controle |
|-------------------|------------|------------|-------|--------|------------|-----------------|----------------|------------------|-----------------|
| VerifyReadyDialog | 50         | 50         | 480   | 280    | 39         | \[ProductName\] | InstallPerUser | Avançar             | Cancelar          |



 

A tabela de [controle](control-table.md) contém entradas para os [controles](controls.md) exibidos pela caixa de diálogo VerifyReadyDialog. A caixa de diálogo exibe controles de [pressão](pushbutton-control.md) e um controle de [texto](text-control.md) . Todos os controles usam os [atributos de controle](control-attributes.md)msidbControlAttributesEnabled (2) e msidbControlAttributesVisible (1). O controle InstallPerMachine também usa o atributo de controle [ElevationShield](elevationshield-attribute.md) , msidbControlAttributesElevationShield (8388608.) Esse atributo de controle adiciona o ícone de elevação do UAC ( [*controle de conta de usuário*](u-gly.md) ) (ícone de escudo) ao controle InstallPerMachine e informa ao usuário que as credenciais do UAC são necessárias para instalar o aplicativo no contexto por máquina. O valor no campo de texto da tabela de controle é o texto e o estilo de texto exibidos pelo controle. Consulte a descrição do campo de texto no tópico da tabela de controle para obter mais informações sobre como adicionar texto a um controle usando estilos predefinidos.

[Controle](control-table.md) do Tabela (parcial)

| caixa de diálogo\_          | Control           | Tipo       | Atributo | Texto                                                   | \_Próximo controle     |
|-------------------|-------------------|------------|-----------|--------------------------------------------------------|-------------------|
| VerifyReadyDialog | Cancelar            | Botão | 3         | { \\ Tahoma10} &cancelar                                    | Avançar              |
| VerifyReadyDialog | Anterior          | Botão | 3         | { \\ Tahoma10} <<&anterior                          | Cancelar            |
| VerifyReadyDialog | Avançar              | Botão | 3         | { \\ Tahoma10} &próximo >>                             | InstallPerUser    |
| VerifyReadyDialog | Text2             | Texto       | 3         | Você está pronto para concluir a instalação suspensa? |                   |
| VerifyReadyDialog | InstallPerUser    | Botão | 3         | { \\ Tahoma10} instalar somente para o &me                       | InstallPerMachine |
| VerifyReadyDialog | InstallPerMachine | Botão | 8388611   | { \\ Tahoma10} instalar para &todos                      | Anterior          |
| VerifyReadyDialog | Cancelar            | Botão | 3         | { \\ Tahoma10} &cancelar                                    | Avançar              |



 

A tabela [ControlEvent,](controlevent-table.md) especifica o [ControlEvents](control-events.md), ou as ações, que o instalador executa quando o usuário interage com um controle. Quando um usuário ativa o botão de pressão InstallPerUser, a interface do usuário exibe uma caixa de diálogo OutOfDisk se a propriedade [**OutOfDiskSpace**](outofdiskspace.md) for 1, define o valor da propriedade [**MSIINSTALLPERUSER**](msiinstallperuser.md) como 1, define o valor da propriedade [**AllUsers**](allusers.md) como 2, define a propriedade [**MSIFASTINSTALL**](msifastinstall.md) como 1 e retorna. Como a propriedade **MSIFASTINSTALL** está definida, nenhum ponto de restauração do sistema é gerado para a instalação. Quando um usuário ativa o botão de pressão InstallPerMachine, a interface do usuário exibe uma caixa de diálogo OutOfDisk se a propriedade **OutOfDiskSpace** for 1, define o valor da propriedade **AllUsers** como 1 e retorna.

[ControlEvent,](controlevent-table.md) Tabela (parcial) 

| caixa de diálogo\_          | controle\_         | Evento                 | Argumento  | Condição                 | Ordem |
|-------------------|-------------------|-----------------------|-----------|---------------------------|-------|
| VerifyReadyDialog | InstallPerUser    | SpawnDialog           | OutOfDisk | OutOfDiskSpace = 1        | 1     |
| VerifyReadyDialog | InstallPerUser    | EndDialog             | Retorno    | OutOfDiskSpace <> 1 | 5     |
| VerifyReadyDialog | InstallPerUser    | \[MSIINSTALLPERUSER\] | 1         | 1                         | 2     |
| VerifyReadyDialog | InstallPerUser    | \[ALLUSERS\]          | 2         | 1                         | 3     |
| VerifyReadyDialog | InstallPerMachine | SpawnDialog           | OutOfDisk | OutOfDiskSpace = 1        | 1     |
| VerifyReadyDialog | InstallPerMachine | EndDialog             | Retorno    | OutOfDiskSpace <> 1 | 3     |
| VerifyReadyDialog | InstallPerMachine | \[ALLUSERS\]          | 1         | 1                         | 2     |
| VerifyReadyDialog | InstallPerUser    | \[MSIFASTINSTALL\]    | 1         | 1                         | 4     |



 

O controle InstallPerUser deve ser removido da interface do usuário de qualquer instalação usando uma versão Windows Installer anterior à Windows Installer Windows Installer 5,0. A tabela [ControlCondition](controlcondition-table.md) no pacote de exemplo contém quatro entradas que desabilitam e ocultam o controle InstallPerUser se a versão atual for menor que Windows Installer 5,0. A tabela usa o valor da propriedade [**VersionMsi**](versionmsi.md) e a [sintaxe de instrução condicional](conditional-statement-syntax.md) para definir essa condição. A ação especificada no campo ação será executada somente se a instrução no campo condição for verdadeira.

[ControlCondition](controlcondition-table.md) Tabela (parcial)

| caixa de diálogo\_          | controle\_      | Ação  | Condição               |
|-------------------|----------------|---------|-------------------------|
| VerifyReadyDialog | InstallPerUser | Habilitar  | VersionMsi >= "5, 0" |
| VerifyReadyDialog | InstallPerUser | Desabilitar | VersionMsi < "5, 0"  |
| VerifyReadyDialog | InstallPerUser | Mostrar    | VersionMsi >= "5, 0" |
| VerifyReadyDialog | InstallPerUser | Ocultar    | VersionMsi < "5, 0"  |



 

## <a name="specifying-directory-structure"></a>Especificando a estrutura do diretório

Use o editor de banco de dados para examinar a tabela de PUASample1.msi de [diretórios](directory-table.md) . O registro da tabela de diretórios que tem uma cadeia de caracteres vazia em seu \_ campo pai do diretório representa o diretório raiz das árvores de diretórios de origem e de destino. Se a propriedade [**TARGETDIR**](targetdir.md) for indefinida, o instalador definirá seu valor no momento da instalação para o valor da propriedade [**ROOTDRIVE**](rootdrive.md) . Se a propriedade [**SourceDir**](sourcedir.md) for indefinida, o instalador definirá seu valor como o local do diretório que contém o pacote de Windows Installer (arquivo. msi). Os nomes de diretório são especificados usando o \| formato curto longo.

[Do diretório](directory-table.md) Tabela (parcial)

| Diretório          | Pai do diretório \_  | DefaultDir               |
|--------------------|--------------------|--------------------------|
| TARGETDIR          |                    | SourceDir                |
| ProgramFilesFolder | TARGETDIR          | .                        |
| ProgramMenuFolder  | TARGETDIR          | .                        |
| INSTALLLOCATION    | Myvendor           | Sample1 \| msdn – PUASample1 |
| Myvendor           | ProgramFilesFolder | MSFT \| Microsoft          |



 

Na origem, essa tabela de [diretório](directory-table.md) é resolvida para os seguintes caminhos de diretório.

<dl> \[\] \\ Sample1 do MSFT SourceDir \\  
\[SourceDir\]  
</dl>

No destino, a tabela de [diretório](directory-table.md) é resolvida para os caminhos na tabela a seguir. O instalador define os valores das propriedades [**ProgramFilesFolder**](programfilesfolder.md) e [**ProgramMenuFolder**](programmenufolder.md) para locais que dependem do contexto de [instalação](installation-context.md) e se o sistema é as versões de 32 bits ou 64 bits do Windows Server 2008 R2 e do Windows 7. Os caminhos para as pastas de destino dependem se o usuário seleciona uma instalação por usuário ou por computador.

| Contexto de instalação | Sistema                                                                              | Caminhos de exemplo                                                                                                                    |
|----------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Per-Machine          | Windows Server 2008 R2 e Windows 7<br/> versão de 32 bits<br/>           | % ProgramFiles% \\ MSFT \\ Sample1<br/> \\ \\ \\ Programas de menu Iniciar do% ALLUSERSPROFILE% do Microsoft Windows \\<br/>                  |
| Per-Machine          | Windows Server 2008 R2 e Windows 7<br/> versão de 64 bits<br/>           | % ProgramFiles (x86)% \\ MSFT \\ Sample1<br/> \\ \\ \\ Programas de menu Iniciar do% ALLUSERSPROFILE% do Microsoft Windows \\<br/>             |
| Per-User             | Windows Server 2008 R2 e Windows 7<br/> versão de 32 bits ou 64 bits<br/> | % USERPROFILE% \\ AppData \\ \\ programas locais \\ MSFT \\ Sample1<br/> \\ \\ \\ Programas de menu Iniciar do% AppData% Microsoft Windows \\<br/> |



 

Os aplicativos por usuário devem ser armazenados em subpastas na pasta programas especificada pelo valor da propriedade [**ProgramFilesFolder**](programfilesfolder.md) . Normalmente, o caminho para o aplicativo usa o seguinte formulário.

% LocalAppData% \\ programas \\ *ISV nome* \\ *AppName*.

Os dados de configuração por usuário devem ser armazenados na pasta programas especificada pelo valor da propriedade [**ProgramMenuFolder**](programmenufolder.md) . Normalmente, essa pasta está localizada no caminho a seguir.

\\ \\ \\ Programas de menu Iniciar do% AppData% Microsoft Windows \\

Se estiver instalando componentes [de pacote de Windows Installer de 32 bits](32-bit-windows-installer-packages.md) , use a propriedade [**ProgramFilesFolder**](programfilesfolder.md) e [**CommonFilesFolder**](commonfilesfolder.md) na tabela de [diretórios](directory-table.md) . Se estiver instalando componentes de [pacote de Windows Installer de 64 bits](64-bit-windows-installer-packages.md) , use as propriedades [**ProgramFiles64Folder**](programfiles64folder.md) e [**CommonFiles64Folder**](commonfiles64folder.md) . Se seu aplicativo contiver versões de 32 bits e de 64 bits do mesmo componente, com o mesmo nome, verifique se essas versões são salvas em diretórios diferentes ou forneça nomes diferentes.

A tabela de [diretórios](directory-table.md) a seguir fornece um exemplo de um layout de diretório compatível com um pacote que inclui componentes de 32 bits e 64 bits e inclui alguns componentes que são compartilhados entre aplicativos.

| Diretório            | Pai do diretório \_    | DefaultDir                        |
|----------------------|----------------------|-----------------------------------|
| TARGETDIR            |                      | SourceDir                         |
| ProgramFilesFolder   | TARGETDIR            | .:P rog32                          |
| ProgramFiles64Folder | TARGETDIR            | .:P rog64                          |
| CommonFilesFolder    | TARGETDIR            | .:Share32                         |
| CommonFiles64Folder  | TARGETDIR            | .:Share64                         |
| ProgramMenuFolder    | TARGETDIR            | .: Sample1 \| msdn-PUASample1        |
| INSTALLLOCATION      | Myvendor             | Sample1 \| msdn – PUASample1          |
| INSTALLLOCATIONX64   | Vendorx64            | Sample1 \| msdn – PUASample1          |
| SHAREDLOCATION       | ShVendor             | Sample1 \| msdn – PUASample1          |
| SHAREDLOCATIONX64    | ShVendorx64          | Sample1 \| msdn – PUASample1          |
| Myvendor             | ProgramFilesFolder   | MSFT \| Microsoft                   |
| Vendorx64            | ProgramFiles64Folder | MSFT \| Microsoft                   |
| ShVendor             | CommonFilesFolder    | MSFT \| Microsoft                   |
| ShVendorx64          | CommonFiles64Folder  | MSFT \| Microsoft                   |
| Shrx86               | SHAREDLOCATION       | \|componentes de x32 de 32 bits            |
| Shrx64               | SHAREDLOCATIONX64    | \|componentes de 64 bits x64            |
| Binx86               | INSTALLLOCATION      | \|componentes de x32 de 32 bits            |
| Binx64               | INSTALLLOCATIONX64   | \|componentes de 64 bits x64            |
| App32                | Binx86               | \|componentes de 32 bits não compartilhados de MyApp |
| App64                | Binx64               | \|componentes de 64 bits não compartilhados de MyApp |
| Share32              | Shrx86               | \|componentes compartilhados de 32 bits compartilhados  |
| Share64              | Shrx64               | \|componentes compartilhados de 64 bits compartilhados  |



 

Na origem, essa tabela de [diretório](directory-table.md) é resolvida para os seguintes caminhos de diretório.

<dl> \[SourceDir \] Prog32 \\ MSFT \\ Sample1 \\ x32 \\ MyApp  
\[\]Arquivos comuns de Share32 de SourceDir \\ \\ MSFT \\ Sample1 \\ x32 \\ compartilhado  
\[SourceDir \] Prog64 \\ MSFT \\ Sample1 \\ x64 \\ MyApp  
\[\]Arquivos comuns de Share64 de SourceDir \\ \\ MSFT \\ Sample1 \\ x64 \\ compartilhado  
\[Sample1 de SourceDir \]  
</dl>

No destino, essa tabela de [diretório](directory-table.md) é resolvida para os seguintes caminhos de diretório. Os caminhos de destino dependem do [contexto](installation-context.md) e do sistema de instalação.

| Contexto de instalação | Sistema                                                                              | Caminhos de exemplo                                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Per-Machine          | Windows Server 2008 R2 e Windows 7<br/> versão de 32 bits<br/>           | % ProgramFiles% \\ MSFT \\ Sample1 \\ x32 \\ MyApp<br/> % ProgramFiles% \\ Arquivos comuns \\ MSFT \\ Sample1 \\ x32 \\ compartilhado<br/> % ProgramFiles (x86)% \\ MSFT \\ Sample1 \\ x64 \\ MyApp<br/> % ProgramFiles (x86)% \\ Arquivos comuns \\ MSFT \\ Sample1 \\ x64 \\ compartilhado<br/> % ProgramData de \\ \\ programas do \\ menu Iniciar do Microsoft Windows \\ \\ Sample1<br/>               |
| Per-Machine          | Windows Server 2008 R2 e Windows 7<br/> versão de 64 bits<br/>           | % ProgramFiles (x86)% \\ MSFT \\ Sample1 \\ x32 \\ MyApp<br/> % ProgramFiles (x86)% \\ Arquivos comuns \\ MSFT \\ Sample1 \\ x32 \\ compartilhado<br/> % ProgramFiles% \\ MSFT \\ Sample1 \\ x64 \\ MyApp<br/> % ProgramFiles% \\ Arquivos comuns \\ MSFT \\ Sample1 \\ x64 \\ compartilhado<br/> % ProgramData de \\ \\ programas do \\ menu Iniciar do Microsoft Windows \\ \\ Sample1<br/>               |
| Per-User             | Windows Server 2008 R2 e Windows 7<br/> versão de 32 bits ou 64 bits<br/> | % LOCALAPPDATA% \\ Programs \\ MSFT \\ Sample1 \\ x32 \\ MyApp<br/> % LOCALAPPDATA% \\ Programs \\ Common \\ MSFT \\ Sample1 \\ x32 \\ compartilhado<br/> % LOCALAPPDATA% \\ Programs \\ MSFT \\ Sample1 \\ x64 \\ MyApp<br/> % LOCALAPPDATA% \\ Programs \\ Common \\ MSFT \\ Sample1 \\ x64 \\ compartilhado<br/> % APPDATA% \\ \\ programas de \\ menu Iniciar do Microsoft Windows \\ \\ Sample1<br/> |



 

## <a name="application-registration"></a>registro de Aplicativo

O PUASample.msi adiciona uma subchave à chave do registro de caminhos de aplicativo para o aplicativo e executa registros que permitem que as informações do aplicativo sejam salvas no registro sob essa chave. Para obter mais informações sobre os caminhos de aplicativo e o registro de aplicativos, consulte o [PerceivedTypes, o SystemFileAssociations e o registro de aplicativos](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)) na seção [extensibilidade do Shell](https://msdn.microsoft.com/library/bb762762.aspx) do [Guia do desenvolvedor do Shell](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85)). No momento da instalação, o usuário toma a decisão de instalar o aplicativo no contexto de instalação por usuário ou por computador. No momento em que o pacote de uso duplo é criado, o desenvolvedor do pacote não pode saber se os registros devem ser executados no \_ computador local hKey \_ ou HKEY \_ Current \_ User Keys.

O desenvolvedor do pacote define o identificador de arquivo para o arquivo executável do aplicativo no campo arquivo da tabela de [arquivos](file-table.md) .

Do [arquivo](file-table.md) Tabela (parcial) 

| Arquivo      | Componente\_      | FileName                     | FileSize | Versão | Idioma | Atributos | Sequência |
|-----------|------------------|------------------------------|----------|---------|----------|------------|----------|
| MyAppfile | ProductComponent | PUASAMP1.EXE\|PUASample1.exe | 81920    |         |          | 0          | 1        |



 

Os valores a serem salvos no registro podem ser especificados no campo valor da tabela [do registro](registry-table.md) como uma cadeia de caracteres [formatada](formatted.md) . Use o identificador de arquivo definido no campo arquivo da tabela de [arquivos](file-table.md) e a \[ \#  \] Convenção FileKey do tipo formatado, para especificar o valor padrão para a chave do registro de caminhos do aplicativo. A ação de [instalação](install-action.md) de nível superior executa as ações na tabela [InstallExecuteSequence](installexecutesequence-table.md) . Depois que as ações [CostInitialize](costinitialize-action.md), [filecost](filecost-action.md)e [InstallFinalize](installfinalize-action.md) nessa tabela forem concluídas, a Windows Installer substituirá a subcadeia de caracteres \[ \# MyApp formatada \] na tabela do registro pelo caminho completo do arquivo de aplicativo.

O exemplo define uma propriedade personalizada, RegRoot, para conter o local da chave raiz e usa uma ação personalizada para redefinir o valor da propriedade se o usuário escolher uma instalação por máquina. Use a propriedade personalizada, RegRoot, em qualquer valor de cadeia de caracteres formatado que referencie o local raiz. Na tabela de [Propriedades](property-table.md) , o pacote de PUASample.msi define a propriedade personalizada e define o valor de REGROOT como HKCU. Isso inicializa o valor da propriedade para o contexto de instalação por usuário, o contexto padrão recomendado para pacotes de uso duplo.

[Propriedade](property-table.md) Tabela (parcial)

| Propriedade | Valor |
|----------|-------|
| RegRoot  | HKCU  |



 

Na tabela [CustomAction](customaction-table.md) , o pacote define uma ação personalizada chamada Set \_ RegRoot \_ HKLM. O valor no campo tipo identifica isso como uma ação personalizada do [tipo de ação personalizada 51](custom-action-type-51.md) padrão. O significado dos campos de origem e de destino na tabela CustomAction depende do tipo de ação personalizada. Para obter mais informações sobre os tipos padrão de ações personalizadas, consulte [tipos de ação personalizadas](summary-list-of-all-custom-action-types.md). O campo de origem para a \_ \_ ação personalizada Set RegRoot HKLM especifica que o valor da propriedade RegRoot. Se o instalador executar a \_ \_ ação personalizada Set RegRoot HKLM, isso redefinirá o valor da propriedade REGROOT como HKLM.

[CustomAction](customaction-table.md) Tabela (parcial)

| Ação             | Tipo | Fonte      | Destino |
|--------------------|------|-------------|--------|
| Definir \_ RegRoot \_ HKLM | 51   | \[RegRoot\] | HKLM   |



 

A ação de [instalação](install-action.md) de nível superior executa as ações na tabela [InstallExecuteSequence](installexecutesequence-table.md) , na sequência especificada no campo sequência dessa tabela. O valor criado no campo sequência para a \_ ação personalizada Set RegRoot \_ HKLM (1501) especifica que essa ação personalizada seja executada após a ação [InstallInitialize](installinitialize-action.md) (1500) e antes da ação [ProcessComponents](processcomponents-action.md) (1600.) Essa sequência garante que o registro para a \_ \_ ação personalizada Set RegRoot HKLM seja avaliado no momento da instalação. Para obter mais informações sobre a sequência recomendada de ações na tabela InstallExecuteSequence, consulte o tópico [sugerido InstallExecuteSequence](suggested-installexecutesequence.md) . A [sintaxe da instrução condicional](conditional-statement-syntax.md) criada no campo condição especifica que a ação Set \_ RegRoot \_ HKLM será executada somente se o valor da propriedade [**AllUsers**](allusers.md) for avaliado como 1 no momento da instalação. Um valor de propriedade **AllUsers** de 1 especifica uma instalação por máquina.

[InstallExecuteSequence](installexecutesequence-table.md) Tabela (parcial)

| Ação             | Condição  | Sequência |
|--------------------|------------|----------|
| Definir \_ RegRoot \_ HKLM | ALLUSERS = 1 | 1501     |



 

Os registros a seguir na tabela de [registro](registry-table.md) executam os registros se o componente ProductComponent estiver instalado. O valor-1 no campo raiz é necessário para executar o registro em HKEY \_ local \_ Machine para uma instalação por usuário e em hKey \_ Current \_ User para uma instalação por usuário. O registro com uma cadeia de caracteres vazia no campo do registro adiciona uma subchave para o aplicativo na chave do registro AppPaths e define o valor "(padrão)" como o caminho completo do arquivo executável do aplicativo. O registro MyAppPathAlias mapeia o arquivo executável para um alias de aplicativo e permite que o aplicativo seja iniciado se o usuário digitar o alias "puapct" em um prompt de linha de comando. O registro MyAppPathRegistration mapeia o nome do arquivo executável para o caminho completo do arquivo.



| Registro              | Root | Chave                                                                     | Nome | Valor                                                                            | Componente        |
|-----------------------|------|-------------------------------------------------------------------------|------|----------------------------------------------------------------------------------|------------------|
|                       | -1   | Software \\ Microsoft \\ MyAppPathRegistrationLocation                      |      | \[\] \\ Caminhos de aplicativo RegRoot software \\ Microsoft \\ Windows \\ CurrentVersion \\ \\PUAPCT.exe | ProductComponent |
| MyAppPathAlias        | -1   | \\Caminhos de aplicativo do software Microsoft \\ Windows \\ CurrentVersion \\ \\PUAPCT.exe     |      | \[\#MyAppfile\]                                                                  | ProductComponent |
| MyAppPathRegistration | -1   | \\Caminhos de aplicativo do software Microsoft \\ Windows \\ CurrentVersion \\ \\PUASample1.exe |      | \[\#MyAppfile\]                                                                  | ProductComponent |



 

## <a name="autoplay-cancel-registration"></a>Cancelar o registro de reprodução automática

O PUASample.msi executa registros que permitem ao usuário do aplicativo impedir que a [reprodução automática de hardware](/previous-versions/windows/desktop/legacy/cc144210(v=vs.85)) seja iniciada para os dispositivos selecionados. Para obter informações sobre como registrar um manipulador para cancelar a reprodução automática em resposta a um evento, consulte o tópico [preparando o hardware e o software para uso com a reprodução automática](/previous-versions//cc144208(v=vs.85)) na seção [extensibilidade do Shell](https://msdn.microsoft.com/library/bb762762.aspx) do [Guia do desenvolvedor do Shell](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85)). O registro a seguir registra o manipulador especificado no campo nome quando o componente ProductComponent é instalado. O valor-1 no campo raiz é necessário para especificar o Windows Installer que o registro deve ser redirecionado para um local que depende do contexto de instalação.

[Registro do](registry-table.md) Tabela 

| Registro                     | Root | Chave                                                                                             | Nome                                 | Valor | Componente        |
|------------------------------|------|-------------------------------------------------------------------------------------------------|--------------------------------------|-------|------------------|
| MyAutoplayCancelRegistration | -1   | SOFTWARE \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ AutoplayHandlers \\ CancelAutoplay \\ CLSID | 66A32FE6-229D-427b-A608-D273F40C034C |       | ProductComponent |



 

## <a name="preview-handler-registration"></a>Registro do Gerenciador de visualização

O PUASample.msi executa registros que são necessários para instalar um [Gerenciador de visualização](../shell/preview-handlers.md) que habilita uma visualização somente leitura de arquivos. pua sem iniciar o aplicativo. Para obter informações sobre como registrar gerenciadores de visualização, consulte o tópico [Registrando manipuladores de visualização](../shell/how-to-register-a-preview-handler.md) na seção [extensibilidade do Shell](https://msdn.microsoft.com/library/bb762762.aspx) do [Guia do desenvolvedor do Shell](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85)). Os registros a seguir na tabela de [registro](registry-table.md) registram o manipulador quando o componente ProductComponent é instalado. O valor-1 no campo raiz é necessário para especificar o Windows Installer que o registro deve ser redirecionado para um local que depende do contexto de instalação.

[Registro do](registry-table.md) Tabela

| Registro                       | Root | Chave                                                                              | Nome                                   | Valor                                        | Componente        |
|--------------------------------|------|----------------------------------------------------------------------------------|----------------------------------------|----------------------------------------------|------------------|
| MyPreviewHandlerRegistration1  | -1   | Classes de software \\ \\ . pua                                                          |                                        | puafile                                      | ProductComponent |
| MyPreviewHandlerRegistration2  | -1   | Software \\ Microsoft \\ Windows \\ CurrentVersion \\ PreviewHandlers                    | {1531d583-8375-4d3f-b5fb-d23bbd169f22} | Gerenciador de visualização de teste do Microsoft Windows PUA   | ProductComponent |
| MyPreviewHandlerRegistration3  | -1   | Classes de software \\ \\ puafile \\ shellex \\ {8895b1c6-b41f-4c1c-a562-0d564250836f}      |                                        | {1531d583-8375-4d3f-b5fb-d23bbd169f22}       | ProductComponent |
| MyPreviewHandlerRegistration4  | -1   | CLSID de classes de software \\ \\ \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 |                                        | Per-User o Gerenciador de visualização de exemplo 1 aplicativo | ProductComponent |
| MyPreviewHandlerRegistration5  | -1   | CLSID de classes de software \\ \\ \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 | AppID                                  | {6d2b5079-2f0b-48dd-ab7f-97cec514d30b}       | ProductComponent |
| MyPreviewHandlerRegistration6  | -1   | CLSID de classes de software \\ \\ \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 | DisplayName                            | @shell32,-38242                              | ProductComponent |
| MyPreviewHandlerRegistration7  | -1   | CLSID de classes de software \\ \\ \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 | ícone                                   | notepad.exe, 2                                | ProductComponent |
| MyPreviewHandlerRegistration8  | -1   | CLSID de classes de software \\ \\ \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22} \\ InprocServer32 | ThreadingModel                         | Sta                                    | ProductComponent |
| MyPreviewHandlerRegistration9  | -1   | CLSID de classes de software \\ \\ \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22} \\ InprocServer32 |                                        | \#%% SystemRoot% \\ system32 \\shell32.dll       | ProductComponent |
| MyPreviewHandlerRegistration10 | -1   | CLSID de classes de software \\ \\ \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22} \\ InprocServer32 | ProgID                                 | puafile                                      | ProductComponent |



 

 

 
