---
description: O Windows Installer tem as seguintes ações padrão.
ms.assetid: 219b5eb6-501f-4e30-b398-4ed5e0cdf2ab
title: Referência de ações padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5104c39639ff2bc7b504996467cf707eb52bb014
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165440"
---
# <a name="standard-actions-reference"></a>Referência de ações padrão

O Windows Installer tem as seguintes ações padrão.



| Nome da ação                                                     | Breve descrição da ação                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ADMIN](admin-action.md)                                       | Uma ação de nível superior usada para uma instalação administrativa.                                                                                                                   |
| [ANUNCI](advertise-action.md)                               | Uma ação de nível superior chamada para instalar ou remover componentes anunciados.                                                                                                         |
| [AllocateRegistrySpace](allocateregistryspace-action.md)       | Valida se o espaço livre especificado por [**AVAILABLEFREEREG**](availablefreereg.md) existe no registro.                                                               |
| [AppSearch](appsearch-action.md)                               | Pesquisa versões anteriores de produtos e determina que as atualizações estão instaladas.                                                                                        |
| [BindImage](bindimage-action.md)                               | Associa executáveis a DLLs importadas.                                                                                                                                           |
| [CCPSearch](ccpsearch-action.md)                               | O usa assinaturas de arquivo para validar que produtos qualificados estejam instalados em um sistema antes que uma instalação de atualização seja executada.                                              |
| [CostFinalize](costfinalize-action.md)                         | Encerra o processo de custos de instalação interna iniciado pela [ação CostInitialize](costinitialize-action.md).                                                               |
| [CostInitialize](costinitialize-action.md)                     | Inicia o processo de custos de instalação.                                                                                                                                      |
| [Createfolders](createfolders-action.md)                       | Cria pastas vazias para componentes.                                                                                                                                         |
| [Createatalhos](createshortcuts-action.md)                   | Cria atalhos.                                                                                                                                                            |
| [Excluirservices](deleteservices-action.md)                     | Remove serviços do sistema.                                                                                                                                                      |
| [DisableRollback](disablerollback-action.md)                   | Desabilita a reversão para o restante da instalação.                                                                                                                      |
| [DuplicateFiles](duplicatefiles-action.md)                     | Duplica os arquivos instalados pela ação InstallFiles.                                                                                                                        |
| [ExecuteAction](executeaction-action.md)                       | Verifica a propriedade [**ExecuteAction**](executeaction.md) para determinar qual ação de nível superior inicia a sequência de execução e executa essa ação.                          |
| [Custo de](filecost-action.md)                                 | Inicializa o cálculo de custo do disco com o instalador. O custo do disco não é finalizado até que a ação CostFinalize seja executada.                                                |
| [FindRelatedProducts](findrelatedproducts-action.md)           | Detecta a correspondência entre a [tabela de atualização](upgrade-table.md) e os produtos instalados.                                                                                 |
| [ForceReboot](forcereboot-action.md)                           | Usado na sequência de ação para solicitar ao usuário uma reinicialização do sistema durante a instalação.                                                                           |
| [PRÉ-instalação](install-action.md)                                   | Uma ação de nível superior chamada para instalar ou remover componentes.                                                                                                                    |
| [InstallAdminPackage](installadminpackage-action.md)           | Copia o banco de dados do instalador para o ponto de instalação administrativa.                                                                                                       |
| [InstallExecute](installexecute-action.md)                     | Executa um script que contém todas as operações na sequência de ação desde o início da instalação ou a última ação de InstallFinalize. Não encerra a transação.   |
| [InstallFiles](installfiles-action.md)                         | Copia arquivos da origem para o diretório de destino.                                                                                                                    |
| [InstallFinalize](installfinalize-action.md)                   | Executa um script que contém todas as operações na sequência de ação desde o início da instalação ou a última ação de InstallFinalize. Marca o final de uma transação. |
| [InstallInitialize](installinitialize-action.md)               | Marca o início de uma transação.                                                                                                                                         |
| [InstallSFPCatalogFile](installsfpcatalogfile-action.md)       | A ação InstallSFPCatalogFile instala os catálogos usados pela proteção de arquivo do Windows me para Windows.                                                                        |
| [InstallValidate](installvalidate-action.md)                   | Verifica se todos os volumes com custos atribuídos têm espaço suficiente para a instalação.                                                                                   |
| [IsolateComponents](isolatecomponents-action.md)               | Processa a [tabela IsolatedComponent](isolatedcomponent-table.md)                                                                                                          |
| [LaunchConditions](launchconditions-action.md)                 | Avalia um conjunto de instruções condicionais contidas na tabela LaunchCondition que devem ser avaliadas como true para que a instalação possa continuar.                          |
| [MigrateFeatureStates](migratefeaturestates-action.md)         | Migra os Estados de recursos atuais para a instalação pendente.                                                                                                                  |
| [MoveFile](movefiles-action.md)                               | Localiza arquivos existentes e move ou copia esses arquivos para um novo local.                                                                                                     |
| [MsiConfigureServices](msiconfigureservices-action.md)         | Configura um serviço para o sistema. **[Windows Installer 4,5 e anteriores](not-supported-in-windows-installer-4-5.md):** Sem suporte.<br/>                           |
| [Ação MsiPublishAssemblies](msipublishassemblies-action.md)  | Gerencia o anúncio de assemblies de Common Language Runtime e assemblies do Win32 que estão sendo instalados.                                                                |
| [MsiUnpublishAssemblies](msiunpublishassemblies-action.md)     | Gerencia o anúncio de assemblies de Common Language Runtime e assemblies do Win32 que estão sendo removidos.                                                                  |
| [InstallODBC](installodbc-action.md)                           | Instala os drivers ODBC, os tradutores e as fontes de dados.                                                                                                                     |
| [Instalarservices](installservices-action.md)                   | Registra um serviço com o sistema.                                                                                                                                          |
| [PatchFiles](patchfiles-action.md)                             | Consulta a tabela patch para determinar quais patches são aplicados a arquivos específicos e, em seguida, executa a aplicação de patches em byte dos arquivos.                                       |
| [ProcessComponents](processcomponents-action.md)               | Registra os componentes, seus caminhos de chave e os clientes de componentes.                                                                                                                 |
| [PublishComponents](publishcomponents-action.md)               | Anuncia os componentes especificados na tabela PublishComponent.                                                                                                            |
| [PublishFeatures](publishfeatures-action.md)                   | Grava o estado do recurso de cada recurso no registro do sistema                                                                                                             |
| [PublishProduct](publishproduct-action.md)                     | Publica informações do produto com o sistema.                                                                                                                                |
| [RegisterClassInfo](registerclassinfo-action.md)               | Gerencia o registro de informações de classe com com o sistema.                                                                                                            |
| [RegisterComPlus](registercomplus-action.md)                   | A ação RegisterComPlus registra aplicativos COM+.                                                                                                                       |
| [RegisterExtensionInfo](registerextensioninfo-action.md)       | Registra informações relacionadas à extensão com o sistema.                                                                                                                      |
| [RegisterFonts](registerfonts-action.md)                       | Registra as fontes instaladas com o sistema.                                                                                                                                    |
| [RegisterMIMEInfo](registermimeinfo-action.md)                 | Registra informações de MIME com o sistema.                                                                                                                                   |
| [RegisterProduct](registerproduct-action.md)                   | Registra as informações do produto com o instalador e armazena o banco de dados do instalador no computador local.                                                                     |
| [RegisterProgIdInfo](registerprogidinfo-action.md)             | Registra informações de ProgId OLE com o sistema.                                                                                                                             |
| [RegisterTypeLibraries](registertypelibraries-action.md)       | Registra bibliotecas de tipos com o sistema.                                                                                                                                     |
| [RegisterUser](registeruser-action.md)                         | Registra as informações do usuário para identificar o usuário de um produto.                                                                                                                 |
| [RemoveDuplicateFiles](removeduplicatefiles-action.md)         | Exclui os arquivos instalados pela ação DuplicateFiles.                                                                                                                         |
| [RemoveEnvironmentStrings](removeenvironmentstrings-action.md) | Modifica os valores de variáveis de ambiente.                                                                                                                                 |
| [RemoveExistingProducts](removeexistingproducts-action.md)     | Remove as versões instaladas de um produto.                                                                                                                                      |
| [Removes](removefiles-action.md)                           | Remove os arquivos instalados anteriormente pela ação InstallFiles.                                                                                                                |
| [RemoveFolders](removefolders-action.md)                       | Remove pastas vazias vinculadas a componentes definidos para serem removidas.                                                                                                                 |
| [RemoveIniValues](removeinivalues-action.md)                   | Exclui informações do arquivo. ini associadas a um componente especificado na tabela IniFile.                                                                                     |
| [RemoveODBC](removeodbc-action.md)                             | Remove fontes de dados ODBC, tradutores e drivers.                                                                                                                          |
| [RemoveRegistryValues](removeregistryvalues-action.md)         | Remove as chaves do registro de um aplicativo que foram criadas a partir da tabela do registro.                                                                                            |
| [RemoveShortcuts](removeshortcuts-action.md)                   | Gerencia a remoção de um atalho anunciado cujo recurso está selecionado para desinstalação.                                                                                   |
| [Resolver](resolvesource-action.md)                       | Determina o local de origem e define a propriedade [**SourceDir**](sourcedir.md) .                                                                                          |
| [RMCCPSearch](rmccpsearch-action.md)                           | O usa assinaturas de arquivo para validar que produtos qualificados estejam instalados em um sistema antes que uma instalação de atualização seja executada.                                              |
| [ScheduleReboot](schedulereboot-action.md)                     | Solicita ao usuário uma reinicialização do sistema no final da instalação.                                                                                                         |
| [SelfRegModules](selfregmodules-action.md)                     | Processa os módulos na tabela SelfReg e os registra se estiverem instalados.                                                                                              |
| [SelfUnregModules](selfunregmodules-action.md)                 | Cancela o registro dos módulos na tabela SelfReg que estão definidos para serem desinstalados.                                                                                                  |
| [SEQUENCE](sequence-action.md)                                 | Executa as ações em uma tabela especificada pela propriedade [**Sequence**](sequence.md) .                                                                                           |
| [Ação SetODBCFolders](setodbcfolders-action.md)              | Verifica o sistema em busca de drivers ODBC existentes e define o diretório de destino para novos drivers ODBC.                                                                                   |
| [Iniciarservices](startservices-action.md)                       | Inicia os serviços do sistema.                                                                                                                                                       |
| [Pararservices](stopservices-action.md)                         | Interrompe os serviços do sistema.                                                                                                                                                        |
| [UnpublishComponents](unpublishcomponents-action.md)           | Gerencia o desanúncio de componentes da tabela PublishComponent e remove informações sobre os componentes publicados.                                                 |
| [UnpublishFeatures](unpublishfeatures-action.md)               | Remove as informações de mapeamento de estado de seleção e componente de recurso do registro do sistema.                                                                               |
| [UnregisterClassInfo](unregisterclassinfo-action.md)           | Gerencia a remoção de classes COM do registro do sistema.                                                                                                                  |
| [UnregisterComPlus](unregistercomplus-action.md)               | A ação UnregisterComPlus remove aplicativos COM+ do registro.                                                                                                     |
| [UnregisterExtensionInfo](unregisterextensioninfo-action.md)   | Gerencia a remoção de informações relacionadas à extensão do sistema.                                                                                                         |
| [UnregisterFonts](unregisterfonts-action.md)                   | Remove informações de registro sobre as fontes instaladas do sistema.                                                                                                       |
| [UnregisterMIMEInfo](unregistermimeinfo-action.md)             | Cancela o registro de informações relacionadas a MIME do registro do sistema.                                                                                                                |
| [UnregisterProgIdInfo](unregisterprogidinfo-action.md)         | Gerencia o cancelamento de registro de informações de ProgId de OLE com o sistema.                                                                                                         |
| [UnregisterTypeLibraries](unregistertypelibraries-action.md)   | Cancela o registro de bibliotecas de tipos com o sistema.                                                                                                                                   |
| [ValidateProductID](validateproductid-action.md)               | Define a propriedade [**ProductID**](productid.md) como o identificador completo do produto.                                                                                                  |
| [WriteEnvironmentStrings](writeenvironmentstrings-action.md)   | Modifica os valores de variáveis de ambiente.                                                                                                                                 |
| [WriteIniValues](writeinivalues-action.md)                     | Grava informações do arquivo. ini.                                                                                                                                                 |
| [WriteRegistryValues](writeregistryvalues-action.md)           | Configura informações do registro.                                                                                                                                                 |



 

 

 




