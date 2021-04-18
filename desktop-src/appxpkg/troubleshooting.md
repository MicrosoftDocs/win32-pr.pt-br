---
title: Solucionar problemas de empacotamento, implantação e consulta de aplicativos Windows
description: Use essas sugestões para solucionar problemas que você enfrenta ao empacotar, implantar ou consultar um pacote de aplicativo.
ms.assetid: 38E327C6-0345-4FA6-BCDB-5FA2FCD421FB
ms.topic: article
ms.date: 02/20/2020
manager: dcscontentpm
ms.custom:
- CI 111497
- CSSTroubleshooting
- contperf-fy21q2
ms.openlocfilehash: a2ee7c28e7de2d616bd01e9b5cae0de3c325caf4
ms.sourcegitcommit: 80198645ddacc3c12c72f3814b71ade0f415e705
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/25/2021
ms.locfileid: "105810806"
---
# <a name="troubleshooting-packaging-deployment-and-query-of-windows-apps"></a>Solucionar problemas de empacotamento, implantação e consulta de aplicativos Windows

Use essas sugestões para solucionar problemas que você enfrenta ao empacotar, implantar ou consultar um pacote de aplicativo do Windows (. msix/. AppX) como desenvolvedor.

> [!NOTE]
> Este artigo destina-se a desenvolvedores. Se você não for um desenvolvedor e estiver procurando ajuda com um erro de instalação de aplicativo do Windows, consulte [suporte do Windows](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10).

## <a name="get-diagnostic-information"></a>Obter informações de diagnóstico

Quando uma API falha, ela retorna um código de erro que descreve o problema. Se o código de erro não fornecer informações suficientes, você encontrará mais informações de diagnóstico nos logs de eventos detalhados.

Para acessar os logs de eventos de empacotamento e implantação usando **Visualizador de eventos**, siga estas etapas:

1. Execute uma das seguintes etapas:

    * Clique em **Iniciar** no menu Windows, digite **Visualizador de eventos** e **pressione Enter**.
    * Execute **eventvwr. msc**.

2. Na página esquerda, expanda **Visualizador de eventos (local)**  >  **logs de aplicativos e serviços**  >  **Microsoft**  >  **Windows**.
3. Verifique os logs disponíveis nessas categorias:

    * **AppxPackagingOM**  >  **Microsoft-Windows-AppxPackaging/operacional**
    * **AppXDeployment-servidor**  >  **Microsoft-Windows-AppXDeploymentServer/operacional**

Comece examinando os logs em **AppXDeployment-Server**. Se o erro foi causado por **0x80073CF0** ou **ERROR_INSTALL_OPEN_PACKAGE_FAILED**, detalhes adicionais podem estar presentes nos logs do **AppxpackagingOM** .

Você também pode usar o comando [Get-AppxLog](/powershell/module/appx/get-appxlog) no PowerShell para obter os primeiros eventos registrados. O exemplo a seguir exibe os logs associados à operação de implantação mais recente.

```PowerShell
Get-Appxlog
```

O exemplo a seguir exibe os logs associados à operação de implantação mais recente em uma tabela interativa em uma janela separada.

```PowerShell
Get-Appxlog | Out-GridView
```

## <a name="common-error-codes"></a>Códigos de erro comuns

Esta tabela lista alguns dos códigos de erro mais comuns. Se você precisar de ajuda adicional com um desses erros, ou se estiver encontrando um código de erro que não esteja nessa lista, consulte [Opções de ajuda adicionais](#get-additional-help).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Código do erro</th>
<th>Valor</th>
<th>Descrição e possíveis causas</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td><strong>E_FILENOTFOUND</strong></td>
<td>0x80070002</td>
<td>Arquivo ou caminho não encontrado. Isso pode ocorrer durante uma validação de typelib COM e requer que o caminho para o diretório realmente exista no pacote MSIX.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_BAD_FORMAT</strong></td>
<td>0x8007000B</td>
<td>O pacote não está formatado corretamente e deve ser recompilado ou assinado novamente.<br/> Você poderá receber esse erro se houver uma incompatibilidade entre o nome da entidade do certificado de autenticação e o nome do editor de AppxManifest.xml.<br/> Consulte <a href="how-to-sign-a-package-using-signtool.md">como assinar um pacote de aplicativo usando Signtool</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>E_INVALIDARG</strong></td>
<td>0x80070057</td>
<td>Um ou mais argumentos não são válidos. Se você verificar o log de eventos AppXDeployment-Server e vir o seguinte evento: "durante a instalação do pacote, o sistema não pôde registrar a extensão Windows. repositoryExtension devido ao seguinte erro: o parâmetro está incorreto". <br/> Você poderá receber esse erro se o DisplayName ou a descrição dos elementos do manifesto contiverem caracteres não permitidos pelo firewall do Windows; a saber |  e todos, devido ao que o Windows falha ao criar o perfil do AppContainer para o pacote. Remova esses caracteres do manifesto e tente instalar o pacote. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_OPEN_</strong><br/> <strong>PACKAGE_FAILED</strong><br/></td>
<td>0x80073CF0</td>
<td>Não foi possível abrir o pacote.<br/> Possíveis causas:<br/>
<ul>
<li>O pacote não está assinado.</li>
<li>O nome do editor não corresponde ao assunto do certificado de autenticação.</li>
<li>O prefixo file://está ausente ou o pacote não pôde ser encontrado no local especificado.</li>
</ul>
Para obter mais informações, verifique o log de eventos <strong>AppxPackagingOM</strong> .<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_PACKAGE_</strong><br/> <strong>NOT_FOUND</strong><br/></td>
<td>0x80073CF1</td>
<td>Não foi possível encontrar o pacote.<br/> Você pode receber esse erro ao remover um pacote que não está instalado para o usuário atual.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_INVALID_</strong><br/> <strong>AGRUPA</strong><br/></td>
<td>0x80073CF2</td>
<td>Os dados do pacote não são válidos.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_RESOLVE_</strong><br/> <strong>DEPENDENCY_FAILED</strong><br/></td>
<td>0x80073CF3</td>
<td>Falha na atualização do pacote, dependência ou validação de conflito.<br/> Possíveis causas:<br/>
<ul>
<li>O pacote de entrada está em conflito com um pacote instalado.</li>
<li>Uma dependência de pacote especificada não pode ser encontrada.</li>
<li>O pacote não dá suporte à arquitetura de processador correta.</li>
</ul>
Para obter mais informtion, verifique o log de eventos <strong>AppXDeployment-Server</strong> .<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_OUT_</strong><br/> <strong>OF_DISK_SPACE</strong><br/></td>
<td>0x80073CF4</td>
<td>Não há espaço em disco suficiente no computador. Libere algum espaço e tente novamente.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_NETWORK_</strong><br/> <strong>FAILURE</strong><br/></td>
<td>0x80073CF5</td>
<td>O pacote não pode ser baixado.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>REGISTRATION_FAILURE</strong><br/></td>
<td>0x80073CF6</td>
<td>O pacote não pode ser registrado.<br/> Para obter mais informações, verifique o log de eventos <strong>AppXDeployment-Server</strong> .<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>DEREGISTRATION_EFAILURE</strong><br/></td>
<td>0x80073CF7</td>
<td>Não é possível cancelar o registro do pacote.<br/> Você pode receber esse erro ao remover um pacote.<br/> Para obter mais informações, verifique o log de eventos <strong>AppXDeployment-Server</strong> .<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_CANCEL</strong></td>
<td>0x80073CF8</td>
<td>O usuário cancelou a solicitação de instalação.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_FAILED</strong></td>
<td>0x80073CF9</td>
<td>Falha na instalação do pacote. Contate o fornecedor do software.<br/> Para obter mais informações, verifique o log de eventos <strong>AppXDeployment-Server</strong> .<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_REMOVE_FAILED</strong></td>
<td>0x80073CFA</td>
<td>Falha na remoção do pacote.<br/> Você pode receber esse erro para falhas que ocorrem durante a desinstalação do pacote.<br/> Para obter mais informações, consulte <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>RemovePackageAsync</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_</strong><br/> <strong>ALREADY_EXISTS</strong><br/></td>
<td>0x80073CFB</td>
<td>O pacote fornecido já foi instalado e sua reinstalação está bloqueada. <br/> Você poderá receber esse erro se estiver instalando um pacote que não seja um bit idêntico ao pacote que já está instalado. Observe que a assinatura digital também faz parte do pacote. Portanto, se um pacote for recriado ou assinado, ele não será mais idêntico a bit que o pacote instalado anteriormente. Duas opções possíveis para corrigir esse erro são: (1) incrementar o número de versão do aplicativo e, em seguida, recompilar e desistir do pacote (2) remover o pacote antigo para cada usuário no sistema antes de instalar o novo pacote. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_NEEDS_REMEDIATION</strong></td>
<td>0x80073CFC</td>
<td>O aplicativo não pode ser iniciado. Tente reinstalar o aplicativo.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>PREREQUISITE_FAILED</strong><br/></td>
<td>0x80073CFD</td>
<td>Um pré-requisito de instalação especificado não pôde ser atendido.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_</strong><br/> <strong>REPOSITORY_CORRUPTED</strong><br/></td>
<td>0x80073CFE</td>
<td>O repositório do pacote está corrompido.<br/> Você poderá receber esse erro se a pasta referenciada por essa chave do registro não existir ou estiver corrompida: <br/> <strong>HKLM\Software\Microsoft\Windows</strong><br/> <strong>CurrentVersion\Appx\PackageRepositoryRoot</strong><br/> Para se recuperar desse Estado, atualize seu computador.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>POLICY_FAILURE</strong><br/></td>
<td>0x80073CFF</td>
<td>Para instalar esse aplicativo, você precisa de uma licença de desenvolvedor ou um sistema habilitado para Sideload. <br/> Você poderá receber esse erro se o pacote não atender a um dos seguintes requisitos:<br/>
<ul>
<li>O aplicativo é implantado usando F5 no Visual Studio em um computador com uma licença de desenvolvedor do Windows.</li>
<li>O pacote é assinado com uma assinatura da Microsoft e implantado como parte do Windows ou do Microsoft Store.</li>
<li>O pacote é assinado com uma assinatura confiável e instalado em um computador com uma licença de desenvolvedor, um computador ingressado no domínio com a política AllowAllTrustedApps habilitada ou um computador com uma licença de Sideload do Windows com a política AllowAllTrustedApps habilitada.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_UPDATING</strong></td>
<td>0x80073D00</td>
<td>O aplicativo não pode ser iniciado porque está sendo atualizado no momento.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_</strong><br/> <strong>BLOCKED_BY_POLICY</strong><br/></td>
<td>0x80073D01</td>
<td>A operação de implantação de pacote está bloqueada pela política. Entre em contato com o administrador do sistema.<br/> Possíveis causas:<br/>
<ul>
<li>A implantação de pacote é bloqueada pelas políticas de controle de aplicativo.</li>
<li>A implantação do pacote é bloqueada pela &quot; política permitir implantação em perfis especiais &quot; .</li>
</ul>
Um dos motivos possíveis é a necessidade de um perfil móvel. Para obter informações sobre como configurar perfis de usuário móvel em contas de usuário, consulte <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">implantar perfis de usuário de roaming</a>. Se não houver políticas configuradas no seu sistema e você ainda vir esse erro, talvez você esteja conectado com um perfil temporário. Faça logoff e logon novamente e tente a operação novamente.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGES_IN_USE</strong></td>
<td>0x80073D02</td>
<td>Não foi possível instalar o pacote porque os recursos que ele modifica estão em uso no momento.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_RECOVERY_</strong><br/> <strong>FILE_CORRUPT</strong><br/></td>
<td>0x80073D03</td>
<td>Não foi possível recuperar o pacote porque os dados necessários para a recuperação estão corrompidos.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INVALID_</strong><br/> <strong>STAGED_SIGNATURE</strong><br/></td>
<td>0x80073D04</td>
<td>A assinatura não é válida. Para se registrar no modo de desenvolvedor, AppxSignature. P7X e AppxBlockMap.xml devem ser válidos ou não devem estar presentes.<br/> Se você for um desenvolvedor usando F5 com o Visual Studio, verifique se o diretório do projeto criado não contém arquivos de mapa de assinatura ou de bloco de versões anteriores do pacote.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DELETING_EXISTING_</strong><br/> <strong>APPLICATIONDATA_STORE_FAILED</strong><br/></td>
<td>0x80073D05</td>
<td>Ocorreu um erro ao excluir os dados de aplicativo anteriormente existentes do pacote.<br/> Você pode obter esse erro se o <a href="/previous-versions/hh441475(v=vs.110)">simulador</a> estiver em execução. Feche o simulador. Você também pode obter esse erro se houver arquivos abertos nos dados do aplicativo (por exemplo, se você tiver um arquivo de log aberto em um editor de texto).<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>PACKAGE_DOWNGRADE</strong><br/></td>
<td>0x80073D06</td>
<td>Não foi possível instalar o pacote porque uma versão mais recente deste pacote já está instalada.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SYSTEM_</strong><br/> <strong>NEEDS_REMEDIATION</strong><br/></td>
<td>0x80073D07</td>
<td>Foi detectado um erro em um binário do sistema. Para corrigir o problema, tente atualizar o computador. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_APPX_INTEGRITY_</strong><br/> <strong>FAILURE_EXTERNAL</strong><br/></td>
<td>0x80073D08</td>
<td>Um binário não Windows corrompido foi detectado no sistema. <br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_RESILIENCY_</strong><br/> <strong>FILE_CORRUPT</strong><br/></td>
<td>0x80073D09</td>
<td>A operação não pôde ser retomada porque os dados necessários para a recuperação estão corrompidos. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_FIREWALL_</strong><br/> <strong>SERVICE_NOT_RUNNING</strong><br/></td>
<td>0x80073D0A</td>
<td>Não foi possível instalar o pacote porque o serviço de firewall do Windows não está em execução. Habilite o serviço de firewall do Windows e tente novamente.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_MOVE_FAILED</strong></td>
<td>0x80073D0B</td>
<td>Falha na operação de movimentação de pacote.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_VOLUME_</strong><br/> <strong>NOT_EMPTY</strong><br/></td>
<td>0x80073D0C</td>
<td>A operação de implantação falhou porque o volume não está vazio.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_VOLUME_</strong><br/> <strong>OFFLINE</strong><br/></td>
<td>0x80073D0D</td>
<td>A operação de implantação falhou porque o volume está offline. Para uma atualização de pacote, o volume refere-se ao volume instalado de todas as versões de pacote.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_VOLUME_</strong><br/> <strong>CORROMPIDO</strong><br/></td>
<td>0x80073D0E</td>
<td>A operação de implantação falhou porque o volume especificado está corrompido.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_NEEDS_REGISTRATION</strong><br/> <strong></strong><br/></td>
<td>0x80073D0F</td>
<td>A operação de implantação falhou porque o aplicativo especificado precisa ser registrado primeiro.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_WRONG_</strong><br/> <strong>PROCESSOR_ARCHITECTURE</strong><br/></td>
<td>0x80073D10</td>
<td>A operação de implantação falhou porque o pacote se destina à arquitetura de processador incorreta.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEV_SIDELOAD_</strong><br/> <strong>LIMIT_EXCEEDED</strong><br/></td>
<td>0x80073D11</td>
<td>Você atingiu o número máximo de pacotes Sideload do desenvolvedor permitidos neste dispositivo. Desinstale um pacote Sideload e tente novamente.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_OPTIONAL_</strong><br/> <strong>PACKAGE_REQUIRES_</strong><br/> <strong>MAIN_PACKAGE</strong><br/></td>
<td>0x80073D12</td>
<td>Um pacote do aplicativo principal é necessário para instalar esse pacote opcional. Primeiro, instale o pacote principal e tente novamente.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_NOT_</strong><br/> <strong>SUPPORTED_ON_FILESYSTEM</strong><br/></td>
<td>0x80073D13</td>
<td>Este tipo de pacote de aplicativo não tem suporte neste sistema de arquivos.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_MOVE_</strong><br/> <strong>BLOCKED_BY_STREAMING</strong><br/></td>
<td>0x80073D14</td>
<td>A operação de movimentação de pacote é bloqueada até que o aplicativo tenha terminado o streaming.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_OPTIONAL_</strong><br/> <strong>PACKAGE_APPLICATIONID_</strong><br/> <strong>NOT_UNIQUE</strong><br/></td>
<td>0x80073D15</td>
<td>Um pacote de aplicativo principal ou outro opcional tem a mesma ID de aplicativo que o pacote opcional. Altere a ID do aplicativo para o pacote opcional para evitar conflitos.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_STAGING_</strong><br/> <strong>ONHOLD</strong><br/></td>
<td>0x80073D16</td>
<td>Esta sessão de preparo foi mantida para permitir que outra operação de preparo seja priorizada.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_INVALID_</strong><br/> <strong>RELATED_SET_UPDATE</strong><br/></td>
<td>0x80073D17</td>
<td>Um conjunto relacionado não pode ser atualizado porque o conjunto atualizado é inválido. Todos os pacotes no conjunto relacionado devem ser atualizados ao mesmo tempo.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_OPTIONAL_</strong><br/> <strong>PACKAGE_REQUIRES_MAIN_</strong><br/> <strong>PACKAGE_FULLTRUST_CAPABILITY</strong><br/></td>
<td>0x80073D18</td>
<td>Um pacote opcional com um ponto de entrada FullTrust exige que o pacote principal tenha o recurso <strong>runFullTrust</strong> .<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_USER_LOG_OFF</strong><br/></td>
<td>0x80073D19</td>
<td>Ocorreu um erro porque um usuário foi desconectado.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PROVISION_OPTIONAL_</strong><br/> <strong>PACKAGE_REQUIRES_MAIN_</strong><br/> <strong>PACKAGE_PROVISIONED</strong><br/></td>
<td>0x80073D1A</td>
<td>Um provisionamento de pacote opcional requer que o pacote principal de dependência também seja provisionado.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGES_REPUTATION_</strong><br/> <strong>CHECK_FAILED</strong><br/></td>
<td>0x80073D1B</td>
<td>Os pacotes falharam na <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">verificação de reputação do SmartScreen</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGES_REPUTATION_</strong><br/> <strong>CHECK_TIMEDOUT</strong><br/></td>
<td>0x80073D1C</td>
<td>A operação de <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">verificação de reputação do SmartScreen</a> atingiu o tempo limite.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_OPTION_</strong><br/> <strong>NOT_SUPPORTED</strong><br/></td>
<td>0x80073D1D</td>
<td>Não há suporte para a opção de implantação atual.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_APPINSTALLER_</strong><br/> <strong>ACTIVATION_BLOCKED</strong><br/></td>
<td>0x80073D1E</td>
<td>A ativação está bloqueada devido às configurações de atualização. AppInstaller para este aplicativo.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_REGISTRATION_FROM_</strong><br/> <strong>REMOTE_DRIVE_NOT_SUPPORTED</strong><br/></td>
<td>0x80073D1F</td>
<td>Não há suporte para unidades remotas. Use <strong> \\ server\share</strong> para registrar um pacote remoto.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_APPX_RAW_</strong><br/> <strong>DATA_WRITE_FAILED</strong><br/></td>
<td>0x80073D20</td>
<td>Falha ao processar e gravar os dados de pacote baixados no disco.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_VOLUME_POLICY_PACKAGE</strong><br/></td>
<td>0x80073D21</td>
<td>A operação de implantação foi bloqueada devido a uma política da família por pacote restringindo implantações em um volume que não é do sistema. Por política, esse aplicativo deve ser instalado na unidade do sistema, mas não é definido como o padrão. Em configurações de armazenamento, torne a unidade do sistema o local padrão para salvar o novo conteúdo e repita a instalação.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_VOLUME_POLICY_MACHINE</strong><br/></td>
<td>0x80073D22</td>
<td>A operação de implantação foi bloqueada devido a uma política de todo o computador restringindo implantações em um volume que não é do sistema. Por política, esse aplicativo deve ser instalado na unidade do sistema, mas não é definido como o padrão. Em configurações de armazenamento, torne a unidade do sistema o local padrão para salvar o novo conteúdo e repita a instalação.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_PROFILE_POLICY</strong><br/></td>
<td>0x80073D23</td>
<td>A operação de implantação foi bloqueada porque a implantação de perfil especial não é permitida (perfis especiais são perfis de usuário em que as alterações são descartadas após o usuário sair). Tente fazer logon em uma conta que não seja um perfil especial. Você pode tentar fazer logoff e logon novamente na conta atual ou tentar fazer logon em uma conta diferente.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEPLOYMENT_FAILED_</strong><br/> <strong>CONFLICTING_MUTABLE_PACKAGE_</strong><br/> <strong>ACTIVE</strong><br/></td>
<td>0x80073D24</td>
<td>A operação de implantação falhou devido a um <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">diretório de pacote mutável</a>do pacote conflitante. Para instalar este pacote, remova o pacote existente com o diretório de pacote mutável conflitante.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SINGLETON_RESOURCE_</strong><br/> <strong>INSTALLED_IN_ACTIVE_USER</strong><br/></td>
<td>0x80073D25</td>
<td>A instalação do pacote falhou porque um recurso singleton foi especificado e outro usuário com esse pacote instalado está conectado. Verifique se todos os usuários ativos com o pacote instalado estão desconectados e tente novamente a instalação.<br/></td>
</tr>
<tr class="even">
<td>ERROR_DIFFERENT_VERSION_<strong></strong><br/> <strong>OF_PACKAGED_SERVICE_INSTALLED</strong><br/></td>
<td>0x80073D26</td>
<td>A instalação do pacote falhou porque uma versão diferente do serviço está instalada. Tente instalar uma versão mais recente do pacote.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SERVICE_EXISTS_</strong><br/> <strong>AS_NON_PACKAGED_SERVICE</strong><br/></td>
<td>0x80073D27</td>
<td>A instalação do pacote falhou porque existe uma versão do serviço fora de um pacote. msix/. Appx. Contate o fornecedor do software.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGED_SERVICE_</strong><br/> <strong>REQUIRES_ADMIN_PRIVILEGES</strong><br/></td>
<td>0x80073D28</td>
<td>A instalação do pacote falhou porque são necessários privilégios de administrador. Contate um administrador para instalar este pacote.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_REDIRECTION_TO_</strong><br/> <strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong><br/></td>
<td>0x80073D29</td>
<td>A implantação do pacote falhou porque a operação seria redirecionada para a conta padrão, quando o chamador disse que não fazer isso.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_LACKS_</strong><br/> <strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong><br/></td>
<td>0x80073D2A</td>
<td>A implantação do pacote falhou porque o pacote requer um recurso para direcionar nativamente esse host.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_UNSIGNED_PACKAGE_</strong><br/> <strong>INVALID_CONTENT</strong><br/></td>
<td>0x80073D2B</td>
<td>A implantação do pacote falhou porque seu conteúdo não é válido para um pacote não assinado.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_UNSIGNED_PACKAGE_</strong><br/> <strong>INVALID_PUBLISHER_NAMESPACE</strong><br/></td>
<td>0x80073D2C</td>
<td>A implantação do pacote falhou porque seu Publicador não está no namespace não assinado.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SIGNED_PACKAGE_</strong><br/> <strong>INVALID_PUBLISHER_NAMESPACE</strong><br/></td>
<td>0x80073D2D</td>
<td>A implantação do pacote falhou porque seu Publicador não está no namespace assinado.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_EXTERNAL_</strong><br/> <strong>LOCATION_NOT_ALLOWED</strong><br/></td>
<td>0x80073D2E</td>
<td>A implantação do pacote falhou porque seu Publicador não está no namespace assinado.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_FULLTRUST_</strong><br/> <strong>HOSTRUNTIME_REQUIRES_MAIN_</strong><br/> <strong>PACKAGE_FULLTRUST_CAPABILITY</strong><br/></td>
<td>0x80073D2F</td>
<td>Uma dependência de tempo de execução de host resolvendo para um pacote com conteúdo de confiança total requer que o pacote principal tenha o recurso <strong>runFullTrust</strong> .<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_PACKAGING_INTERNAL</strong></td>
<td>0x80080200</td>
<td>A API de empacotamento encontrou um erro interno.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INTERLEAVING_</strong><br/> <strong>NOT_ALLOWED</strong><br/></td>
<td>0x80080201</td>
<td>O pacote não é válido porque seu conteúdo é intercalado.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_RELATIONSHIPS_</strong><br/> <strong>NOT_ALLOWED</strong><br/></td>
<td>0x80080202</td>
<td>O pacote não é válido porque contém relações OPC.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_MISSING_</strong><br/> <strong>REQUIRED_FILE</strong><br/></td>
<td>0x80080203</td>
<td>O pacote não é válido porque está faltando um manifesto ou um mapa de bloco ou um arquivo de integridade de código está presente, mas um arquivo de assinatura está ausente.<br/> Verifique se o pacote não tem um ou mais desses arquivos necessários:<br/>
<ul>
<li>\AppxManifest.xml</li>
<li>\AppxBlockMap.xml</li>
</ul>
Se o pacote contiver \AppxMetadata\CodeIntegrity.cat, ele também deverá conter \AppxSignature.p7x.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_MANIFEST</strong></td>
<td>0x80080204</td>
<td>O arquivo de AppxManifest.xml do pacote não é válido.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_BLOCKMAP</strong></td>
<td>0x80080205</td>
<td>O arquivo de AppxBlockMap.xml do pacote não é válido.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_CORRUPT_CONTENT</strong></td>
<td>0x80080206</td>
<td>O conteúdo do pacote não pode ser lido porque está corrompido.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_BLOCK_</strong><br/> <strong>HASH_INVALID</strong><br/></td>
<td>0x80080207</td>
<td>O valor de hash calculado do bloco não corresponde ao valor de tem armazenado no mapa de bloco.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_REQUESTED_</strong><br/> <strong>RANGE_TOO_LARGE</strong><br/></td>
<td>0x80080208</td>
<td>O intervalo de bytes solicitado é de mais de 4 GB quando convertido em um intervalo de bytes de blocos.<br/></td>
</tr>
<tr class="even">
<td><strong>TRUST_E_NOSIGNATURE</strong></td>
<td>0x800B0100</td>
<td>Nenhuma assinatura está presente no assunto.<br/> Você poderá receber esse erro se o pacote não estiver assinado ou se a assinatura não for válida. O pacote deve ser assinado para ser implantado.<br/></td>
</tr>
<tr class="odd">
<td><strong>CERT_E_UNTRUSTEDROOT</strong></td>
<td>0x800B0109</td>
<td>Uma cadeia de certificados foi processada, mas terminada em um certificado raiz que não é confiável pelo provedor de confiança.<br/> Consulte <a href="/previous-versions/br230260(v=vs.110)">assinando um pacote</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>CERT_E_CHAINING</strong></td>
<td>0x800B010A</td>
<td>Não foi possível criar uma cadeia de certificados para uma autoridade de certificação raiz confiável.<br/> Consulte <a href="/previous-versions/br230260(v=vs.110)">assinando um pacote</a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong> <br/> <strong>SIP_CLIENT_DATA</strong> <br/></td>
<td>0x80080209</td>
<td>A estrutura de <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>usada para assinar o pacote não contém os dados necessários<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong> <br/> <strong>KEY_INFO</strong> <br/></td>
<td>0x8008020A</td>
<td>A estrutura de <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> usada para criptografar ou descriptografar o pacote contém dados inválidos.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>CONTENTGROUPMAP</strong><br/></td>
<td>0x8008020B</td>
<td>O mapa do grupo de conteúdo do pacote. msix/. Appx é inválido.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>APPINSTALLER</strong><br/></td>
<td>0x8008020C</td>
<td>O <a href="/windows/msix/app-installer/app-installer-root">arquivo. AppInstaller</a> do pacote é inválido.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_DELTA_BASELINE_</strong><br/> <strong>VERSION_MISMATCH</strong><br/></td>
<td>0x8008020D</td>
<td>A versão do pacote de linha de base no pacote Delta não corresponde à versão do pacote de linha de base a ser atualizada.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_DELTA_PACKAGE_</strong><br/> <strong>MISSING_FILE</strong><br/></td>
<td>0x8008020E</td>
<td>O pacote Delta não tem um arquivo do pacote atualizado.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>DELTA_PACKAGE</strong><br/></td>
<td>0x8008020F</td>
<td>O pacote delta é inválido.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_DELTA_APPENDED_</strong><br/> <strong>PACKAGE_NOT_ALLOWED</strong><br/></td>
<td>0x80080210</td>
<td>O pacote Delta anexado não é permitido para a operação atual.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>PACKAGING_LAYOUT</strong><br/></td>
<td>0x80080211</td>
<td>O arquivo de layout de empacotamento é inválido.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>PACKAGESIGNCONFIG</strong><br/></td>
<td>0x80080212</td>
<td>O arquivo packageSignConfig é inválido.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_RESOURCESPRI_</strong><br/> <strong>NOT_ALLOWED</strong><br/></td>
<td>0x80080213</td>
<td>O arquivo Resources. pri não é permitido quando não há elementos de recurso no manifesto do pacote.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_FILE_</strong><br/> <strong>COMPRESSION_MISMATCH</strong><br/></td>
<td>0x80080214</td>
<td>O estado de compactação do arquivo na linha de base e no pacote atualizado não corresponde.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>PAYLOAD_PACKAGE_EXTENSION</strong><br/></td>
<td>0x80080215</td>
<td>Extensões não. Appx não são permitidas para pacotes de carga destinados a plataformas mais antigas.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong><br/></td>
<td>0x80080216</td>
<td>O arquivo encryptionExclusionFileList é inválido.<br/></td>
</tr>
</tbody>
</table>

## <a name="applications-dont-start-and-their-names-are-dimmed"></a>Os aplicativos não são iniciados e seus nomes ficam esmaecidos

Em um computador baseado no Windows 10, você não pode iniciar alguns aplicativos e os nomes dos aplicativos aparecem esmaecidos.

![Alguns nomes de aplicativos aparecem esmaecidos no menu iniciar](./images/app-names-dimmed.png)

Ao tentar abrir um aplicativo selecionando o nome esmaecido, você poderá receber uma das seguintes mensagens de erro:

> Há um problema com o \<*application name*> . Contate o administrador do sistema para reparar ou reinstalá-lo  
> Erro: este aplicativo não pode ser aberto

Além disso, as entradas de evento a seguir são registradas no log "Microsoft-Windows-TWinUI/Operational" em **Applications and Services\Microsoft\Windows\Apps**:

> Nome do log: Microsoft-Windows-TWinUI/Operational  
> Fonte: Microsoft-Windows-imersiva-Shell  
> Data: *Data* de <>  
> ID do evento: 5960  
> Categoria da tarefa: (5960)  
> Nível: erro  
> Palavras-chave:  
> Descrição:  
> Ativação do aplicativo Microsoft.BingNews_8wekyb3d8bbwe! AppexNews para o Windows. O contrato de inicialização foi bloqueado com o erro 0x80073CFC porque seu pacote está em estado: modificado.  

### <a name="cause"></a>Causa

Esse problema ocorre porque a entrada do registro para o valor de status do pacote correspondente do aplicativo foi modificada.

### <a name="resolution"></a>Resolução

> [!WARNING]
> Podem ocorrer problemas sérios se você modificar o Registro incorretamente, usando o Editor do Registro ou outro método. Esses problemas podem exigir que você reinstale o sistema operacional. A Microsoft não garante que esses problemas possam ser solucionados. Modifique o Registro por conta própria.

Para corrigir esse problema:

1. Inicie o editor do registro e localize a subchave **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** .
2. Para fazer backup dos dados da subchave, clique com o botão direito do mouse em **PackageList**, selecione **Exportar** e, em seguida, salve os dados como um arquivo do registro.
3. Para cada um dos aplicativos listados nas entradas de log da ID de evento 5960, siga estas etapas:  
   1. Localize a entrada **PackageStatus** .
   2. Defina o valor de **PackageStatus** como zero (**0**).
   > [!NOTE]  
   > Se não houver entradas para o aplicativo em **PackageList**, o problema terá alguma outra causa. No caso do evento de exemplo neste artigo, a subchave completa é **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**
4. Reinicie o computador.

## <a name="get-additional-help"></a>Obter ajuda técnica

Se precisar de ajuda adicional para resolver um problema que você está experimentando ao empacotar, implantar ou consultar um pacote de aplicativo do Windows (. msix/. AppX) como desenvolvedor, consulte esses recursos adicionais de suporte do desenvolvedor.

- O [Microsoft Q&a](/answers/topics/uwp.html?filter=all&sort=active) oferece respostas relevantes e oportunas aos problemas técnicos de uma comunidade de especialistas e engenheiros da Microsoft.
- Para assistência da Comunidade com perguntas de desenvolvimento, há nossos [fóruns](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required)e [StackOverflow](https://stackoverflow.com/questions).
- O site de [suporte do desenvolvedor do Windows](https://developer.microsoft.com/windows/support) explica outras opções de suporte.

## <a name="related-topics"></a>Tópicos relacionados

- [Como assinar um pacote de aplicativos usando o SignTool](how-to-sign-a-package-using-signtool.md)
- [Como solucionar problemas de erros de assinatura do pacote de aplicativo](how-to-troubleshoot-app-package-signature-errors.md)
