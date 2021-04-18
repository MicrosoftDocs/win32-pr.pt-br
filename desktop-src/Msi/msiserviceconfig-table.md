---
description: A tabela MsiServiceConfig configura um serviço que está instalado ou sendo instalado pelo pacote atual.
ms.assetid: 0d9fd005-9326-4a18-8496-35b5d1927f47
title: Tabela MsiServiceConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357b6787e56d52a893dd1a118a3e2fcbc13379e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780509"
---
# <a name="msiserviceconfig-table"></a>Tabela MsiServiceConfig

A tabela MsiServiceConfig configura um serviço que está instalado ou sendo instalado pelo pacote atual.

**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte. Esta tabela está disponível a partir do Windows Installer 5,0.

A tabela MsiServiceConfig tem as colunas a seguir.



| Coluna           | Tipo                         | Chave | Nullable |
|------------------|------------------------------|-----|----------|
| MsiServiceConfig | [Identificador](identifier.md) | S   | N        |
| Nome             | [Binário](formatted.md)   | N   | N        |
| Evento            | [Inteiro](integer.md)       | N   | N        |
| ConfigType       | [Inteiro](integer.md)       | N   | N        |
| Argumento         | [Binário](formatted.md)   | N   | S        |
| Componente\_      | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="MsiServiceConfig"></span><span id="msiserviceconfig"></span><span id="MSISERVICECONFIG"></span>MsiServiceConfig
</dt> <dd>

Esta é a chave primária desta tabela.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes
</dt> <dd>

Esta coluna contém o nome de um serviço que faz parte deste pacote ou que já está instalado.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Circunstância
</dt> <dd>

Esta coluna especifica quando alterar a configuração do serviço. Os valores a seguir podem ser combinados para representar várias operações. Quaisquer valores incluídos a não ser ignorados.



| Constante                                         | Descrição                                              |
|--------------------------------------------------|----------------------------------------------------------|
| **msidbServiceConfigEventInstall** 1<br/>   | Executa a ação durante a instalação do componente.   |
| **msidbServiceConfigEventUninstall** 2<br/> | Executa a ação durante a desinstalação do componente. |
| **msidbServiceConfigEventReinstall** 4<br/> | Executa a ação durante a reinstalação do componente. |



 

</dd> <dt>

<span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>ConfigType
</dt> <dd>

O valor nesse campo, combinado com o valor no campo argumentos, especifica a alteração a ser feita na configuração do serviço. A alteração especificada entrará em vigor na próxima vez em que o sistema for iniciado.



| Config                                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Serviço \_ do \_ \_ \_ Início automático atrasado de configuração** 3<br/>       | Configure o atraso de tempo de um [serviço de início automático](../services/automatically-starting-services.md). <br/> Insira 1 no campo argumento para iniciar o serviço após outros serviços de início automático mais um atraso de tempo. <br/> Insira 0 no campo argumento para desativar o atraso do serviço de início automático.<br/> Aplica-se somente aos serviços ou serviços de início automático instalados por este pacote com o **\_ \_ início automático do serviço** no campo StartType da tabela do serviço de [instalação](serviceinstall-table.md).<br/>                                                                         |
| **Serviço \_ do CONFIGURAR \_ \_ \_ informações de privilégios necessários** 6<br/> | Altere a lista de privilégios exigida pelo serviço.<br/> Insira uma lista de privilégios solicitados no campo argumento. O valor da cadeia de caracteres [formatada](formatted.md) no campo argumento lista as [**constantes de privilégio**](../secauthz/privilege-constants.md) para os privilégios solicitados. Você pode usar a \[ ~ \] sintaxe da cadeia de caracteres [formatada](formatted.md) para inserir um caractere nulo. Separe as constantes de privilégio na lista por \[ ~ \] .<br/>                                                                                                                              |
| **Serviço \_ do \_Informações de \_ SID \_ do serviço de configuração** 5<br/>         | Adicione um tipo de SID de serviço ao token de processo que contém este serviço.<br/> Insira no campo de argumento um tipo de SID de serviço válido para a estrutura de [**\_ \_ informações de Sid de serviço**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) : tipo de Sid de serviço **\_ \_ \_ nenhum** (0x00), **tipo de Sid de serviço \_ \_ \_ restrito** (0x03) ou **tipo de Sid de serviço \_ \_ \_ irrestrito** (0x01). <br/>                                                                                                                                                                                                                                              |
| **Serviço \_ do CONFIGURAR \_ \_ informações de pré-desligamento** 7<br/>          | Configure o período de tempo que o SCM ( [Gerenciador de controle de serviço](../services/service-control-manager.md) ) espera antes de prosseguir com outras operações de desligamento. O SCM espera por esse período de tempo depois de enviar a notificação de **\_ \_ pré-desligamento de controle de serviço** para o serviço. <br/> Insira o comprimento do intervalo de tempo, em milissegundos, no campo argumento. Deixe o campo de argumento vazio para redefinir o tempo de espera para o padrão de 3 minutos. <br/>                                                                                                                               |
| **Serviço \_ do \_Sinalizador de \_ ações \_ de falha de configuração** 4<br/>     | Configure quando executar as ações de falha para este serviço. Essa configuração será ignorada se o serviço não tiver nenhuma ação de falha configurada.<br/> Digite 0 para executar as ações somente se o serviço for encerrado sem que o serviço de relatório seja **\_ interrompido**.<br/> Digite 1 para executar as ações se o serviço encerrar o serviço de relatório **\_ interrompido** e o membro **dwWin32ExitCode** da estrutura de [**\_ status do serviço**](/windows/win32/api/winsvc/ns-winsvc-service_status) não for um **\_ êxito de erro**. As ações de falha configuradas também serão executadas se o serviço for encerrado sem que o serviço de relatório seja **\_ interrompido**.<br/> |



 

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argumento
</dt> <dd>

O valor nesse campo, combinado com o valor no campo Configtype, especifique a alteração a ser feita na configuração do serviço. A alteração especificada entrará em vigor na próxima vez em que o sistema for iniciado.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa para a coluna componente da [tabela de componentes](component-table.md).

</dd> </dl>

## <a name="validation"></a>Validação

<dl>

[ICE102](ice-102.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 
