---
description: A tabela de instalação é usada para instalar um serviço e tem as colunas a seguir.
ms.assetid: 81688d31-e560-4dd0-8d84-efb50206c76e
title: Tabela de desinstalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502583802a26c10bfd9572375149720c7c597f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754632"
---
# <a name="serviceinstall-table"></a>Tabela de desinstalação

A tabela de instalação é usada para instalar um serviço e tem as colunas a seguir.



| Coluna         | Tipo                               | Chave | Nullable |
|----------------|------------------------------------|-----|----------|
| Instalar o | [Identificador](identifier.md)       | S   | N        |
| Nome           | [Binário](formatted.md)         | N   | N        |
| DisplayName    | [Binário](formatted.md)         | N   | S        |
| ServiceType    | [DoubleInteger](doubleinteger.md) | N   | N        |
| StartType      | [DoubleInteger](doubleinteger.md) | N   | N        |
| ErrorControl   | [DoubleInteger](doubleinteger.md) | N   | N        |
| LoadOrderGroup | [Binário](formatted.md)         | N   | S        |
| Dependências   | [Binário](formatted.md)         | N   | S        |
| StartName      | [Binário](formatted.md)         | N   | S        |
| Senha       | [Binário](formatted.md)         | N   | S        |
| Argumentos      | [Binário](formatted.md)         | N   | S        |
| Componente\_    | [Identificador](identifier.md)       | N   | N        |
| Descrição    | [Binário](formatted.md)         | N   | S        |



 

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
| \_início automático do serviço \_   | 0x00000002 | Um serviço é iniciado durante a inicialização do sistema.                                                              |
| \_início da demanda de serviço \_ | 0x00000003 | Um serviço é iniciado quando o Gerenciador de controle de serviço chama a função [**StartService**](/windows/win32/api/winsvc/nf-winsvc-startservicea) . |
| SERVIÇO \_ desabilitado      | 0x00000004 | Especifica um serviço que não pode mais ser iniciado.                                                         |



 

O Windows Installer não pode usar as opções de início de inicialização do serviço e início do \_ \_ sistema de serviço \_ \_ .

</dd> <dt>

<span id="ErrorControl"></span><span id="errorcontrol"></span><span id="ERRORCONTROL"></span>ErrorControl
</dt> <dd>

Essa coluna especifica a ação realizada pelo programa de inicialização se o serviço não for iniciado durante a inicialização. Esses valores afetam os eventos StartService de controle dos serviços instalados. Um dos seguintes sinalizadores de controle de erro deve ser especificado nesta coluna.

Adicionar a constante **msidbServiceInstallErrorControlVital** (Value = 0x08000) aos sinalizadores na tabela a seguir especifica que a instalação geral deverá falhar se o serviço não puder ser instalado no sistema.



| Sinalizador de controle de erro       | Valor      | Ação do programa de inicialização                                                                                                                                                                       |
|--------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ignorar erro de serviço \_   | 0x00000000 | Registra o erro e continua com a operação de inicialização.                                                                                                                                       |
| erro de serviço \_ \_ normal   | 0x00000001 | Registra o erro, exibe uma caixa de mensagem e continua a operação de inicialização.                                                                                                                    |
| \_erro \_ crítico do serviço | 0x00000003 | Registra o erro se for possível e o sistema será reiniciado com a última configuração conhecida como boa. Se a última configuração válida estiver sendo iniciada, a operação de inicialização falhará. |



 

</dd> <dt>

<span id="LoadOrderGroup"></span><span id="loadordergroup"></span><span id="LOADORDERGROUP"></span>OrderGroup
</dt> <dd>

Esta coluna contém a cadeia de caracteres que nomeia o grupo de ordenação de carga do qual esse serviço é membro. Especifique uma cadeia de caracteres nula ou vazia se o serviço não pertencer a um grupo.

</dd> <dt>

<span id="Dependencies"></span><span id="dependencies"></span><span id="DEPENDENCIES"></span>Depend
</dt> <dd>

Esta coluna é uma lista de nomes de serviços ou grupos de ordenação de carga que o sistema deve iniciar antes desse serviço. Separe os nomes na lista por nulos. Se o serviço não tiver dependências, especifique NULL ou uma cadeia de caracteres vazia. Use a sintaxe \[ ~ \] para inserir um valor nulo. A dependência de um grupo significa que esse serviço pode ser executado se pelo menos um membro do grupo estiver em execução depois de uma tentativa de iniciar todos os membros do grupo.

Por exemplo, para exigir que o sistema inicie Service1 e Service2, antes de iniciar o serviço listado na coluna instalar, insira Service1 \[ ~ \] Service2 \[ ~ \] \[ ~ \] na coluna dependências. Os identificadores Service1 e Service2 devem ocorrer na chave primária da tabela ou ser o nome do serviço que já está instalado.

Você deve prefixar nomes de grupos com + para que eles possam ser diferenciados de um nome de serviço. Para exigir que o sistema inicie o Service1 e pelo menos um membro do grupo de pedidos myGroup antes de iniciar o serviço listado na coluna Service install, insira Service1 \[ ~ \] + myGroup \[ ~ \] \[ ~ \] .

</dd> <dt>

<span id="StartName"></span><span id="startname"></span><span id="STARTNAME"></span>StartName
</dt> <dd>

O serviço está conectado como o nome fornecido pela cadeia de caracteres nesta coluna. Se o tipo de serviço for serviço de \_ próprio processo do Win32, \_ \_ use um nome de conta no formato: DomainName \\ username. Se a conta pertencer ao domínio interno, será permitido especificar. \\ Usu. A conta LocalSystem deve ser usada se o tipo de serviço for serviço \_ de \_ compartilhamento do Win32 \_ ou \_ processo interativo do serviço \_ . A função [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) usará a conta LocalSystem se StartName for especificado como NULL e a maioria dos serviços, portanto, deixar essa coluna em branco.

</dd> <dt>

<span id="Password"></span><span id="password"></span><span id="PASSWORD"></span>La
</dt> <dd>

Essa cadeia de caracteres é a senha para o nome da conta especificada na coluna StartName. Observe que o usuário deve ter permissões para fazer logon como um serviço. O serviço não terá senha se StartName for nulo ou uma cadeia de caracteres vazia. O StartName do LocalSystem é nulo e, portanto, a senha dessa instância é nula, portanto, a maioria dos serviços deixa essa coluna em branco.

Observe que, depois de excluir um serviço que foi instalado com um nome de usuário e senha, o instalador não pode reverter o serviço sem primeiro usar uma ação personalizada para obter a senha. O instalador pode adquirir todas as informações necessárias sobre o serviço, exceto a senha, que é armazenada em uma parte protegida do sistema. A ação personalizada adquire a senha solicitando o usuário, lendo uma propriedade do banco de dados ou lendo um arquivo. A ação personalizada deve então chamar [**ChangeServiceConfig**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga)para fornecer a senha, antes de reinstalar o serviço.

Windows Installer não grava o valor inserido no campo de senha no arquivo de log.

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumentos
</dt> <dd>

Esta coluna contém quaisquer argumentos de linha de comando ou propriedades necessárias para executar o serviço.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa para a coluna um da [tabela de componentes](component-table.md). Observe que para instalar esse serviço usando a tabela InstallService, o caminho Keypara esse componente deve ser o arquivo executável para o serviço.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição
</dt> <dd>

Esta coluna contém uma descrição localizável para o serviço que está sendo configurado. Se essa coluna for deixada em branco, o instalador usará a descrição existente do serviço, se houver. Para obter mais informações, consulte \_ a descrição do serviço no kit de desenvolvimento de software (SDK) do Microsoft Windows. Para apagar uma descrição existente, insira " \[ ~ \] " nesta coluna. Isso resulta em uma descrição em branco para um serviço novo ou existente.

</dd> </dl>

## <a name="remarks"></a>Comentários

A ação [installservices](installservices-action.md) em [*tabelas de sequência*](s-gly.md) processa as informações nesta tabela. Para obter informações sobre como usar *tabelas de sequência*, consulte [usando uma tabela de sequência](using-a-sequence-table.md).

Esta tabela tem a maioria dos parâmetros para a função [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) do Win32.

Embora seja possível usar a interface do usuário para especificar que um serviço seja instalado como execução da origem, o instalador não dá suporte a esse tipo de instalação. Os serviços executados com o nível de privilégio do sistema local devem ser instalados para serem executados do disco rígido local. Evite instalar serviços que representam os privilégios de um usuário específico, pois isso pode gravar dados de segurança em um log ou no registro do sistema. Isso pode potencialmente criar um problema de segurança, um conflito de senha ou a perda de dados de configuração quando o sistema é reiniciado.

Para excluir um serviço durante uma desinstalação, deve haver um registro correspondente para o serviço na [tabela de UserControl](servicecontrol-table.md) e o sinalizador **msidbServiceControlEventUninstallDelete** deve aparecer na coluna de evento. O instalador não exclui um serviço na tabela de instalação durante a desinstalação sem essa entrada na tabela de UserControl.

Para obter informações sobre como proteger um serviço, consulte a [tabela MsiLockPermissionsEx](msilockpermissionsex-table.md).

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

 

 
