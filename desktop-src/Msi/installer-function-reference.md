---
description: Para habilitar Windows Instalador em seu aplicativo, você deve usar as funções do instalador. As tabelas neste tópico identificam as funções por categoria.
ms.assetid: 05a16915-6b47-4d51-b62a-5a4d92b87e50
title: Referência de função do instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ab6a77bd3aa02be85f0d2a3cb11a864861535360f5741c6566f77e9fc1aa11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630541"
---
# <a name="installer-function-reference"></a>Referência de função do instalador

Para habilitar Windows Instalador em seu aplicativo, você deve usar as funções do instalador. As tabelas neste tópico identificam as funções por categoria.

## <a name="user-interface-and-logging-functions"></a>Interface do Usuário e funções de registro em log



| Nome                                                     | Descrição                                                                           |
|----------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)             | Habilita a interface do usuário interna do instalador.                                 |
| [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)             | Habilita um manipulador de interface do usuário externo que recebe mensagens em um formato de cadeia de caracteres. |
| [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord) | Habilita um manipulador de interface do usuário externo que recebe mensagens em um formato de registro. |
| [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)                     | Define o modo de log para todas as instalações no processo de chamada.                       |



 

## <a name="handle-management-functions"></a>Manipular funções de gerenciamento



| Nome                                             | Descrição                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle)         | Fecha um alça de instalação aberta.                           |
| [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) | Fecha todos os alças de instalação abertos. Não use para limpeza. |



 

## <a name="installation-and-configuration-functions"></a>Funções de instalação e configuração



| Nome                                                                     | Descrição                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta)                       | Anuncia um produto.                                                                                                                                                                                                        |
| [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)                   | Anuncia um produto.                                                                                                                                                                                                        |
| [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)                         | Copia um arquivo de script de anúncio em locais especificados.                                                                                                                                                                    |
| [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)                           | Instala ou remove um aplicativo ou pacote de aplicativos.                                                                                                                                                                     |
| [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)                       | Instala ou remove um aplicativo ou pacote de aplicativos.                                                                                                                                                                     |
| [**MsiConfigureProductEx**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)                   | Instala ou remove um aplicativo ou pacote de aplicativos. Uma linha de comando do produto pode ser especificada.                                                                                                                            |
| [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)                       | Reinstala ou repara uma instalação.                                                                                                                                                                                       |
| [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)                       | Configura o estado instalado de um recurso.                                                                                                                                                                                 |
| [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)                       | Valida ou repara recursos.                                                                                                                                                                                               |
| [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)         | Instala componentes ausentes.                                                                                                                                                                                                 |
| [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)                   | Instala arquivos ausentes.                                                                                                                                                                                                      |
| [**MsiNotifySidChange**](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)                         | Notifica e atualiza as informações internas Windows instalador com alterações nos SIDs do usuário. Disponível a partir do Windows 3.1.                                                                                   |
| [**MsiProcessAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiprocessadvertisescripta)           | Processa um arquivo de script de anúncio em locais especificados.                                                                                                                                                                 |
| [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)                 | Adiciona ou reordena as fontes de um patch ou produto em um contexto especificado.                                                                                                                                                   |
| [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)             | Adiciona ou reordena as fontes de um patch ou produto em um contexto especificado. Cria uma lista de origem para um patch que não existe em um contexto especificado. Disponível no Windows Installer 3.0.                                |
| [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)             | Remove uma fonte existente para um produto ou patch em um contexto especificado. Disponível no Windows Installer 3.0.                                                                                                               |
| [**MsiSourceListClearAll**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearalla)                   | Remove todas as fontes existentes de um tipo de origem específico para uma instância de produto especificada.                                                                                                                                 |
| [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)               | Remove todas as fontes existentes de um tipo de origem específico para uma instância de produto especificada. Disponível no Windows Installer 3.0.                                                                                            |
| [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)     | Remove o registro da fonte atual do produto ou patch, que é registrado como a propriedade "LastUsedSource". Essa função não afeta a lista de origem registrada.                                      |
| [**MsiSourceListForceResolutionEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa) | Remove o registro da fonte atual do produto ou patch, que é registrado como a propriedade "LastUsedSource". Essa função não afeta a lista de origem registrada. Disponível no Windows Installer 3.0. |
| [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)                     | Recupera informações sobre a lista de origem de um produto ou patch em um contexto específico.                                                                                                                                    |
| [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)                     | Define a origem usada mais recentemente para um produto ou patch em um contexto especificado. Disponível no Windows Installer 3.0.                                                                                                       |
| [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)       | Enumera a lista de discos registrados para a fonte de mídia para um patch ou produto. Disponível no Windows Installer 3.0.                                                                                                    |
| [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)           | Adiciona ou atualiza um disco da fonte de mídia de um produto ou patch registrado. Disponível no Windows Installer 3.0.                                                                                                            |
| [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)      | Remove um disco registrado existente na fonte de mídia de um produto ou patch em um contexto específico. Disponível no Windows Installer 3.0.                                                                                |
| [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)             | Enumera as fontes na lista de origem de um patch ou produto especificado. Disponível no Windows Installer 3.0.                                                                                                              |



 

## <a name="component-specific-functions"></a>Component-Specific funções



| Nome                                                                     | Descrição                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)                         | Instala e retorna o caminho completo do componente para um assembly.                                                                                                                                                                 |
| [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)                       | Instala e retorna o caminho completo do componente de um componente.                                                                                                                                                                  |
| [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)     | Instala e retorna o caminho completo do componente de um componente qualificado.                                                                                                                                                        |
| [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa) | Instala e retorna o caminho completo do componente de um componente qualificado que é publicado por um produto.                                                                                                                         |
| [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)                       | Retorna o caminho completo ou a chave do registro para um componente instalado.                                                                                                                                                              |
| [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)                   | Retorna o caminho completo ou a chave do registro para um componente instalado nas contas de usuário e no contexto de instalação. **[Windows Installer 4,5 e anteriores](not-supported-in-windows-installer-4-5.md):** Sem suporte.<br/> |
| [**MsiLocateComponent**](/windows/desktop/api/Msi/nf-msi-msilocatecomponenta)                         | Retorna o caminho completo para um componente instalado sem um código de produto.                                                                                                                                                       |
| [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)                 | Retorna o estado instalado de um componente. Pode consultar componentes de uma instância de um produto instalado em contas de usuário que não sejam o usuário atual. disponível no Windows Installer 3,0 ou posterior.                        |



 

## <a name="application-only-functions"></a>Funções de Application-Only



| Nome                                             | Descrição                                                            |
|--------------------------------------------------|------------------------------------------------------------------------|
| [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) | Armazena informações do usuário de um assistente de instalação.                   |
| [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea)           | Incrementa a contagem de uso de um recurso e indica o estado da instalação. |
| [**MsiUseFeatureEx**](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)       | Incrementa a contagem de uso de um recurso e indica o estado da instalação. |
| [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea)   | Retorna o código do produto usando o código do componente.                         |



 

## <a name="system-status-functions"></a>Funções de status do sistema



| Nome                                                             | Descrição                                                                                                                                                                                                                       |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)                       | Enumera os produtos anunciados.                                                                                                                                                                                                   |
| [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)                   | Enumera todas as instâncias de produtos anunciados ou instalados em um contexto especificado. disponível no Windows Installer 3,0 ou posterior.                                                                                    |
| [**MsiEnumRelatedProducts**](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)         | Enumera os produtos atualmente instalados que têm um código de atualização especificado.                                                                                                                                                          |
| [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)                       | Enumera recursos publicados.                                                                                                                                                                                                    |
| [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)                   | Enumera os componentes instalados.                                                                                                                                                                                              |
| [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)               | Enumera os componentes instalados nas contas de usuário e no contexto de instalação. **[Windows Installer 4,5 e anteriores](not-supported-in-windows-installer-4-5.md):** Sem suporte.<br/>                                 |
| [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)                         | Enumera os clientes de um componente instalado.                                                                                                                                                                                 |
| [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)                     | Enumera os clientes de um componente instalado nas contas de usuário e no contexto de instalação. **[Windows Installer 4,5 e anteriores](not-supported-in-windows-installer-4-5.md):** Sem suporte.<br/>                    |
| [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) | Enumera os qualificadores anunciados para um componente.                                                                                                                                                                             |
| [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)             | Retorna o estado instalado de um recurso.                                                                                                                                                                                         |
| [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)         | Retorna o estado instalado para um recurso do produto. Pode consultar recursos de uma instância de um produto instalado em contas de usuário que não sejam o usuário atual. disponível no Windows Installer 3,0 ou posterior.                        |
| [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)             | Retorna o estado instalado de um aplicativo ou pacote de aplicativos.                                                                                                                                                              |
| [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)                 | Retorna as métricas de uso para um recurso.                                                                                                                                                                                              |
| [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)                   | Retorna informações do produto para produtos publicados e instalados.                                                                                                                                                                 |
| [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)               | Retorna informações do produto para produtos anunciados e instalados. Pode recuperar informações em uma instância de um produto instalado em uma conta de usuário que não seja o usuário atual. disponível no Windows Installer 3,0 ou posterior. |
| [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)                         | Retorna informações de usuário registradas para um produto instalado.                                                                                                                                                                     |



 

## <a name="product-query-functions"></a>Funções de consulta de produto



| Nome                                                               | Descrição                                                                            |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta)                           | Abre um produto a ser usado com as funções que acessam o banco de dados.                    |
| [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)                           | Abre um pacote para usar com as funções que acessam o banco de dados.                    |
| [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa)                       | Abre um pacote para usar com as funções que acessam o banco de dados.                    |
| [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)               | Verifica se o produto está instalado com privilégios elevados.                      |
| [**MsiGetProductInfoFromScript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) | Retorna informações do produto de um arquivo de script do instalador.                              |
| [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)             | Recupera as propriedades no banco de dados do produto.                                          |
| [**MsiGetShortcutTarget**](/windows/desktop/api/Msi/nf-msi-msigetshortcuttargeta)               | Examina um atalho e retorna seu produto, o nome do recurso e o componente, se disponível. |
| [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)                     | Retorna informações descritivas de um recurso.                                         |
| [**MsiVerifyPackage**](/windows/desktop/api/Msi/nf-msi-msiverifypackagea)                       | Verifica se um arquivo especificado é um pacote de instalação.                             |



 

## <a name="patching-functions"></a>Funções de aplicação de patch



| Nome                                                                   | Descrição                                                                                                                                                        |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)                                 | Invoca uma instalação e aplica um pacote de patch.                                                                                                               |
| [**MsiEnumPatches**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)                    | Retorna o GUID de cada patch que é aplicado a um produto e uma lista de transformações de cada patch que se aplicam ao produto.                                  |
| [**MsiGetPatchInfo**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoa)                             | Retorna informações sobre um patch.                                                                                                                                 |
| [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)                           | Desinstala um patch de um produto. Disponível no Windows Installer 3.0.                                                                                             |
| [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)         | Determina a melhor sequência de aplicativos para um conjunto de patches e produto. Disponível no Windows Installer 3.0.                                                     |
| [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)             | Aplica um ou mais patches aos produtos. Disponível no Windows Installer 3.0.                                                                                       |
| [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)                           | Enumera todos os patches aplicados a um produto em um contexto específico ou em todos os contextos. Disponível no Windows Installer 3.0.                                   |
| [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista)                     | Quando é fornecida uma lista de arquivos .msp, essa função recupera a lista de arquivos que podem ser atualizados pelos patches para o targe. Disponível no Windows 4.0. |
| [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)                         | Consulta informações sobre a aplicação de um patch especificado a um produto especificado. Disponível no Windows Installer 3.0.                                     |
| [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)               | Extrai informações de um patch. Disponível no Windows Installer 3.0.                                                                                             |
| [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) | Determina o melhor conjunto de patches necessários para atualizar um produto ou conjunto de produtos. Disponível no Windows Installer 3.0.                                            |



 

## <a name="file-query-functions"></a>Funções de consulta de arquivo



| Nome                                                                     | Descrição                                                                                                 |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)                                 | Leva o caminho para um arquivo e retorna um hash de 128 bits desse arquivo.                                           |
| [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa) | Leva o caminho para um arquivo que foi assinado digitalmente e retorna o certificado e o hash do signante do arquivo. |
| [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona)                           | Retorna a cadeia de caracteres de versão e a cadeia de caracteres de idioma.                                                             |



 

## <a name="transaction-management-functions"></a>Funções de gerenciamento de transações



| Nome                                               | Descrição                                                                                                                                                                                         |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona) | Inicia o processamento de transação de uma instalação de vários pacotes e retorna um identificador para a transação. Essa função está disponível a partir do Windows Installer 4.5.                    |
| [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)   | Solicita que o Windows instalador faça do processo atual o proprietário da transação que instala uma instalação de vários pacotes. Essa função está disponível a partir do Windows Installer 4.5. |
| [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction)     | Confirma ou resimente todas as instalações que pertencem à transação. Essa função está disponível a partir do Windows Installer 4.5.                                                          |



 

## <a name="database-functions"></a>Funções de banco de dados

Além das funções do Windows Installer identificadas nas tabelas anteriores, você pode manipular informações no banco de dados de instalação usando as funções de acesso ao banco de dados descritas na seção Funções de Banco [de](database-functions.md) Dados.

## <a name="installer-structures"></a>Estruturas do instalador

Além disso, algumas informações no banco de dados de instalação são tratadas usando as estruturas descritas na [seção Estruturas do](installer-structures.md) Instalador.

 

 




