---
description: A tabela de instalação é usada para instalar um serviço e tem as colunas a seguir.
ms.assetid: 81688d31-e560-4dd0-8d84-efb50206c76e
title: Tabela de desinstalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3850b957df4dd0af662354c14f82717e4b86ad597f151c6a45bb8dc1bebea5af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039956"
---
# <a name="serviceinstall-table"></a>Tabela de desinstalação

A tabela de instalação é usada para instalar um serviço e tem as colunas a seguir.



| Coluna         | Tipo                               | Chave | Nullable |
|----------------|------------------------------------|-----|----------|
| Instalar o | [Identificador](identifier.md)       | Y   | N        |
| Nome           | [Binário](formatted.md)         | N   | N        |
| DisplayName    | [Binário](formatted.md)         | N   | Y        |
| ServiceType    | [DoubleInteger](doubleinteger.md) | N   | N        |
| StartType      | [DoubleInteger](doubleinteger.md) | N   | N        |
| ErrorControl   | [DoubleInteger](doubleinteger.md) | N   | N        |
| LoadOrderGroup | [Binário](formatted.md)         | N   | Y        |
| Dependências   | [Binário](formatted.md)         | N   | Y        |
| StartName      | [Binário](formatted.md)         | N   | Y        |
| Senha       | [Binário](formatted.md)         | N   | Y        |
| Argumentos      | [Binário](formatted.md)         | N   | Y        |
| Componente\_    | [Identificador](identifier.md)       | N   | N        |
| Descrição    | [Binário](formatted.md)         | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="ServiceInstall"></span><span id="serviceinstall"></span><span id="SERVICEINSTALL"></span>Instalar o
</dt> <dd>

Esta é a chave primária para a tabela.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes
</dt> <dd>

Essa coluna é a cadeia de caracteres que fornece o nome do serviço a ser instalado. A cadeia de caracteres tem um comprimento máximo de 256 caracteres. O banco de dados do Gerenciador de controle de serviço preserva o caso dos caracteres no nome do serviço, mas as comparações de nomes de serviço não diferenciam maiúsculas de minúsculas. Barra (/) e barra invertida ( \\ ) são caracteres de nome de serviço inválidos.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>DisplayName
</dt> <dd>

Essa coluna é a cadeia de caracteres localizável que os programas da interface do usuário usam para identificar o serviço. A cadeia de caracteres tem um comprimento máximo de 256 caracteres. O Gerenciador de controle de serviço preserva o caso do nome de exibição, mas as comparações de nome de exibição não diferenciam maiúsculas de minúsculas.

</dd> <dt>

<span id="ServiceType"></span><span id="servicetype"></span><span id="SERVICETYPE"></span>ServiceType
</dt> <dd>

Esta coluna é um conjunto de sinalizadores de bits que especificam o tipo de serviço. Um dos seguintes tipos de serviço deve ser especificado nesta coluna.



| Tipo de serviço                | Valor      | Descrição                                                                                                                                                                                                                  |
|--------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ Processo próprio do serviço do Win32 \_   | 0x00000010 | Um serviço Microsoft Win32 que executa seu próprio processo.                                                                                                                                                                         |
| \_Processo de \_ compartilhamento \_ Win32 do serviço | 0x00000020 | Um serviço Win32 que compartilha um processo.                                                                                                                                                                                       |
| \_processo interativo de serviço \_  | 0x00000100 | Um serviço Win32 que interage com a área de trabalho. Esse valor não pode ser usado sozinha e deve ser adicionado a um dos dois tipos anteriores. A coluna StartName deve ser definida como LocalSystem ou NULL ao usar esse sinalizador.<br/> |



 

Não há suporte para os tipos de serviço a seguir.



| Tipo de serviço               | Valor      | Descrição                   |
|-------------------------------|------------|-------------------------------|
| \_Driver de kernel de serviço \_       | 0x00000001 | Um serviço de driver.             |
| \_Driver do \_ sistema de arquivos de serviço \_ | 0x00000002 | Um serviço de driver do sistema de arquivos. |



 

</dd> <dt>

<span id="StartType"></span><span id="starttype"></span><span id="STARTTYPE"></span>StartType
</dt> <dd>

Esta coluna é um conjunto de sinalizadores de bits que especificam quando iniciar o serviço. Um dos seguintes tipos de início de serviço deve ser especificado nesta coluna.



| Tipo de início do serviço  | Valor      | Descrição                                                                                                |
|------------------------|------------|------------------------------------------------------------------------------------------------------------|
| INÍCIO \_ AUTOMÁTICO DO \_ SERVIÇO   | 0x00000002 | Um serviço é inicializado durante a inicialização do sistema.                                                              |
| INÍCIO \_ DA DEMANDA DE \_ SERVIÇO | 0x00000003 | Um serviço é iniciar quando o gerenciador de controle de serviço chama a [**função StartService.**](/windows/win32/api/winsvc/nf-winsvc-startservicea) |
| SERVIÇO \_ DESABILITADO      | 0x00000004 | Especifica um serviço que não pode mais ser iniciado.                                                         |



 

O Windows instalador não pode usar as opções INICIAR INICIALIZAÇÃO DO SERVIÇO e \_ \_ \_ INICIALIZAÇÃO DO \_ SISTEMA DE SERVIÇO.

</dd> <dt>

<span id="ErrorControl"></span><span id="errorcontrol"></span><span id="ERRORCONTROL"></span>ErrorControl
</dt> <dd>

Essa coluna especifica a ação tomada pelo programa de inicialização se o serviço não for inicializado durante a inicialização. Esses valores afetam os eventos ServiceControl StartService para serviços instalados. Um dos sinalizadores de controle de erro a seguir deve ser especificado nesta coluna.

Adicionar a constante **msidbServiceInstallErrorControlVital** (valor = 0x08000) aos sinalizadores na tabela a seguir especifica que a instalação geral deverá falhar se o serviço não puder ser instalado no sistema.



| Sinalizador de controle de erro       | Valor      | Ação do programa de inicialização                                                                                                                                                                       |
|--------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERRO \_ DE \_ SERVIÇO IGNORAR   | 0x00000000 | Registra o erro em logs e continua com a operação de inicialização.                                                                                                                                       |
| ERRO \_ DE \_ SERVIÇO NORMAL   | 0x00000001 | Registra o erro em logs, exibe uma caixa de mensagem e continua a operação de inicialização.                                                                                                                    |
| ERRO \_ DE \_ SERVIÇO CRÍTICO | 0x00000003 | Registra o erro se for possível e o sistema é reiniciado com a última configuração conhecida como boa. Se a última configuração conhecida estiver sendo iniciada, a operação de inicialização falhará. |



 

</dd> <dt>

<span id="LoadOrderGroup"></span><span id="loadordergroup"></span><span id="LOADORDERGROUP"></span>LoadOrderGroup
</dt> <dd>

Essa coluna contém a cadeia de caracteres que nomeia o grupo de ordenação de carga do qual esse serviço é membro. Especifique nulo ou uma cadeia de caracteres vazia se o serviço não pertencer a um grupo.

</dd> <dt>

<span id="Dependencies"></span><span id="dependencies"></span><span id="DEPENDENCIES"></span>Dependências
</dt> <dd>

Esta coluna é uma lista de nomes de serviços ou grupos de pedidos de carga que o sistema deve iniciar antes desse serviço. Separe os nomes na lista por Nulos. Se o serviço não tiver dependências, especifique Null ou uma cadeia de caracteres vazia. Use a sintaxe \[ ~ \] para inserir um Null. A dependência em um grupo significa que esse serviço poderá ser executado se pelo menos um membro do grupo estiver em execução após uma tentativa de iniciar todos os membros do grupo.

Por exemplo, para exigir que o sistema inicie service1 e service2, antes de iniciar o serviço listado na coluna ServiceInstall, insira service1 service2 na \[ ~ \] \[ ~ \] \[ ~ \] coluna Dependências. Os identificadores service1 e service2 devem ocorrer na chave primária da tabela ou ser o nome do serviço que já está instalado.

Você deve prefixar nomes de grupo com + para que eles possam ser diferenciados de um nome de serviço. Para exigir que o sistema inicie o service1 e pelo menos um membro do grupo de ordenação MyGroup antes de iniciar o serviço listado na coluna ServiceInstall, insira service1 \[ ~ \] +MyGroup \[ ~ \] \[ ~ \] .

</dd> <dt>

<span id="StartName"></span><span id="startname"></span><span id="STARTNAME"></span>Startname
</dt> <dd>

O serviço é conectado como o nome dado pela cadeia de caracteres nesta coluna. Se o tipo de serviço for SERVICE WIN32 OWN PROCESS, use um nome \_ de conta no \_ \_ formato: \\ DomainName UserName. Se a conta pertencer ao domínio integrado, ela poderá especificar . \\ Username. A conta LocalSystem deverá ser usada se o tipo de serviço for SERVICE \_ WIN32 \_ SHARE PROCESS ou SERVICE INTERACTIVE \_ \_ \_ PROCESS. A [**função CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) usará a conta LocalSystem se StartName for especificado como nulo e a maioria dos serviços deixar essa coluna em branco.

</dd> <dt>

<span id="Password"></span><span id="password"></span><span id="PASSWORD"></span>Senha
</dt> <dd>

Essa cadeia de caracteres é a senha para o nome da conta especificado na coluna StartName. Observe que o usuário deve ter permissões para fazer logoff como um serviço. O serviço não terá senha se StartName for nulo ou uma cadeia de caracteres vazia. O Startname de LocalSystem é nulo e, portanto, a senha nesta instância é nula, portanto, a maioria dos serviços deixa essa coluna em branco.

Observe que, depois de excluir um serviço que foi instalado com um nome de usuário e senha, o instalador não pode reverter o serviço sem primeiro usar uma ação personalizada para obter a senha. O instalador pode adquirir todas as informações necessárias sobre o serviço, exceto a senha, que é armazenada em uma parte protegida do sistema. A ação personalizada adquire a senha solicitando ao usuário, lendo uma propriedade do banco de dados ou lendo um arquivo. Em seguida, a ação personalizada deve [**chamar ChangeServiceConfig**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga)para fornecer a senha, antes de reinstalar o serviço.

Windows O instalador não escreve o valor inserido no campo Senha no arquivo de log.

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumentos
</dt> <dd>

Essa coluna contém quaisquer argumentos de linha de comando ou propriedades necessárias para executar o serviço.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa para a coluna um da [Tabela de Componentes](component-table.md). Observe que, para instalar esse serviço usando a tabela InstallService, o KeyPath para esse componente deve ser o arquivo executável para o serviço.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrição
</dt> <dd>

Essa coluna contém uma descrição localizável para o serviço que está sendo configurado. Se essa coluna for deixada em branco, o instalador usará a descrição existente do serviço, se houver. Para obter mais informações, consulte SERVICE \_ DESCRIPTION no Microsoft Windows Software Development Kit (SDK). Para apagar uma descrição existente, insira " \[ ~ \] " nesta coluna. Isso resulta em uma descrição em branco para um serviço novo ou existente.

</dd> </dl>

## <a name="remarks"></a>Comentários

A [ação InstallServices](installservices-action.md) em [*tabelas de sequência*](s-gly.md) processa as informações nesta tabela. Para obter informações sobre como usar *tabelas de sequência,* [consulte Usando uma tabela de sequência](using-a-sequence-table.md).

Esta tabela tem a maioria dos parâmetros para a função Win32 [**CreateService.**](/windows/win32/api/winsvc/nf-winsvc-createservicea)

Embora seja possível usar a interface do usuário para especificar que um serviço seja instalado como run-from-source, o instalador não dá suporte a esse tipo de instalação. Os serviços executados com o nível de privilégio do sistema local devem ser instalados para serem executados no disco rígido local. Evite instalar serviços que representem os privilégios de um usuário específico porque isso pode gravar dados de segurança em um log ou no registro do sistema. Isso pode criar um problema de segurança, um conflito de senha ou a perda de dados de configuração quando o sistema é reiniciado.

Para excluir um serviço durante uma desinstalação, deve haver um registro correspondente para o serviço na tabela [ServiceControl](servicecontrol-table.md) e o sinalizador **msidbServiceControlEventUninstallDelete** deve aparecer na coluna Evento. O instalador não exclui um serviço na tabela ServiceInstall durante a desinstalação sem essa entrada na tabela ServiceControl.

Para obter informações sobre como proteger um serviço, consulte a [Tabela MsiLockPermissionsEx](msilockpermissionsex-table.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE66](ice66.md)  
[ICE69](ice69.md)  
</dl>

 

 
