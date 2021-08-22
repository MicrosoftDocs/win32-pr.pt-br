---
description: Um objeto Installer deve ser criado inicialmente para carregar o suporte de automação necessário para que o COM acesse as funções do instalador. Esse objeto fornece wrappers para criar os objetos de nível superior e acessar seus métodos.
ms.assetid: fefc3e39-073e-4869-86b7-27d20a3b337b
title: Objeto do instalador
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7c0900f381a4d5887816a9e581d22eeb5ecb4a2b680d14aecc88646bf4ec72ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327976"
---
# <a name="installer-object"></a>Objeto do instalador

Um **objeto Installer** deve ser criado inicialmente para carregar o suporte de automação necessário para que o COM acesse as funções do instalador. Esse objeto fornece wrappers para criar os objetos de nível superior e acessar seus métodos.

Você pode criar o **objeto Installer** do ProgId "WindowsInstaller.Installer".

## <a name="members"></a>Membros

O **objeto Installer** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto Installer** tem esses métodos.



| Método                                                                   | Descrição                                                                                                                                                                                     |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddSource**](installer-addsource.md)                                 | Adiciona uma origem à lista de fontes de rede válidas na lista de origem.<br/>                                                                                                                |
| [**AdvertiseProduct**](installer-advertiseproduct.md)                   | Anuncia um pacote de instalação.<br/>                                                                                                                                                  |
| [**AdvertiseScript**](installer-advertisescript.md)                     | Anuncia um pacote de instalação. <br/>                                                                                                                                                 |
| [**ApplyMultiplePatches**](installer-applymultiplepatches.md)           | Aplica um ou mais patches aos produtos qualificados para receber o patch. Define a [**propriedade PATCH**](patch.md) como o caminho dos pacotes de patch fornecidos.<br/>                          |
| [**ApplyPatch**](installer-applypatch.md)                               | Invoca uma instalação e define a [**propriedade PATCH**](patch.md) como o caminho do pacote de patch para cada produto listado pelo pacote de patch como qualificado para receber o patch.<br/> |
| [**ClearSourceList**](installer-clearsourcelist.md)                     | Remove todas as fontes de rede da lista de origem.<br/>                                                                                                                                     |
| [**CollectUserInfo**](installer-collectuserinfo.md)                     | Invoca uma sequência de assistente de interface do usuário que coleta e armazena informações do usuário e o código do produto.<br/>                                                                        |
| [**ConfigureFeature**](installer-configurefeature.md)                   | Configura o estado instalado de um recurso de produto.<br/>                                                                                                                                 |
| [**ConfigureProduct**](installer-configureproduct.md)                   | Instala ou desinstala um produto.<br/>                                                                                                                                                    |
| [**CreateAdvertiseScript**](installer-createadvertisescript.md)         | Gera um script de anúncio.<br/>                                                                                                                                                       |
| [**CreateRecord**](installer-createrecord.md)                           | Retorna um novo [**objeto**](record-object.md) Record com o número solicitado de campos.<br/>                                                                                            |
| [**EnableLog**](installer-enablelog.md)                                 | Habilita o registro em log do tipo de mensagem selecionado para todas as sessões de instalação subsequentes no espaço de processo atual.<br/>                                                                  |
| [**ExtractPatchXMLData**](installer-extractpatchxmldata.md)             | Extrai informações de um patch como uma cadeia de caracteres XML.<br/>                                                                                                                                  |
| [**FileHash**](installer-filehash.md)                                   | Leva o caminho para um arquivo e retorna um hash de 128 bits desse arquivo.<br/>                                                                                                                    |
| [**FileSignatureInfo**](installer-filesignatureinfo.md)                 | Leva o caminho para um arquivo e retorna **um SAFEARRAY** de bytes que representa o hash ou o certificado codificado.<br/>                                                                   |
| [**FileSize**](installer-filesize.md)                                   | Retorna o tamanho do arquivo especificado.<br/>                                                                                                                                              |
| [**Fileversion**](installer-fileversion.md)                             | Retorna a cadeia de caracteres de versão ou a cadeia de caracteres de idioma do caminho especificado.<br/>                                                                                                                 |
| [**ForceSourceListResolution**](installer-forcesourcelistresolution.md) | Força o instalador a pesquisar na lista de origem uma fonte de produto válida na próxima vez que uma origem for necessária.<br/>                                                                        |
| [**InstallProduct**](installer-installproduct.md)                       | Abre um pacote do instalador e inicializa uma sessão de instalação.<br/>                                                                                                                  |
| [**LastErrorRecord**](installer-lasterrorrecord.md)                     | Retorna um [**objeto Record**](record-object.md) que contém parâmetros de erro para o erro mais recente da função que produziu o registro de erro.<br/>                          |
| [**OpenDatabase**](installer-opendatabase.md)                           | Abre um banco de dados existente ou cria um novo.<br/>                                                                                                                                     |
| [**OpenPackage**](installer-openpackage.md)                             | Abre um pacote do instalador para uso com funções que acessam o banco de dados do produto e o mecanismo de instalação.<br/>                                                                               |
| [**OpenProduct**](installer-openproduct.md)                             | Abre um pacote do instalador para um produto instalado usando o código do produto.<br/>                                                                                                          |
| [**Provideassembly**](installer-provideassembly.md)                     | Retorna o caminho instalado de um assembly.<br/>                                                                                                                                           |
| [**ProvideComponent**](installer-providecomponent.md)                   | Retorna o caminho completo do componente e executa qualquer instalação necessária.<br/>                                                                                                             |
| [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) | Retorna o caminho completo do componente e executa qualquer instalação necessária.<br/>                                                                                                             |
| [**RegistryValue**](installer-registryvalue.md)                         | Lê informações sobre uma chave de valor do Registro especificada.<br/>                                                                                                                           |
| [**ReinstalarFeature**](installer-reinstallfeature.md)                   | Reinstala recursos ou corrige problemas com recursos instalados.<br/>                                                                                                                    |
| [**ReinstalarProduto**](installer-reinstallproduct.md)                   | Reinstala um produto ou corrige problemas de instalação em um produto instalado.<br/>                                                                                                      |
| [**RemovePatches**](installer-removepatches.md)                         | Remove um ou mais patches para produtos qualificados para receber o patch. <br/>                                                                                                              |
| [**UseFeature**](installer-usefeature.md)                               | Incrementa a contagem de uso para um recurso específico e retorna o estado de instalação para esse recurso.<br/>                                                                             |



 

### <a name="properties"></a>Propriedades

O **objeto Installer** tem essas propriedades.



| Propriedade                                                                    | Tipo de acesso           | Description                                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClientsEx**](installer-components.md)<br/>                        |                       | Retorna um [**objeto RecordList**](recordlist-object.md) que lista os produtos que usam um componente instalado especificado.<br/> **[Windows Instalador 4.5 e versões anteriores:](not-supported-in-windows-installer-4-5.md)** Sem suporte.<br/>       |
| [**ComponentClients**](installer-componentclients.md)<br/>           |                       | Retorna um [**objeto StringList**](stringlist-object.md) enumerando o conjunto de clientes de um componente especificado.<br/>                                                                                                                           |
| [**ComponentPath**](installer-componentpath.md)<br/>                 |                       | Retorna o caminho completo para um componente instalado.<br/>                                                                                                                                                                                            |
| [**ComponentPathEx**](installer-componentpathex.md)<br/>             |                       | Retorna um [**objeto RecordList**](recordlist-object.md) que fornece o caminho completo de um componente instalado especificado. <br/> **[Windows Instalador 4.5 e versões anteriores:](not-supported-in-windows-installer-4-5.md)** Sem suporte.<br/>       |
| [**ComponentQualifiers**](installer-componentqualifiers.md)<br/>     |                       | Retorna um [**objeto StringList**](stringlist-object.md) enumerando o conjunto de qualificadores registrados para o componente especificado.<br/>                                                                                                          |
| [**Componentes**](installer-components.md)<br/>                       |                       | Retorna um [**objeto StringList**](stringlist-object.md) enumerando o conjunto de componentes instalados para todos os produtos.<br/>                                                                                                                      |
| [**ComponentsEx**](installer-componentsex.md)<br/>                   |                       | Retorna um [**objeto RecordList**](recordlist-object.md) que lista os componentes instalados.<br/> **[Windows Instalador 4.5 e versões anteriores:](not-supported-in-windows-installer-4-5.md)** Sem suporte.<br/>                                    |
| [**Ambiente**](installer-environment.md)<br/>                     | Leitura/gravação<br/> | O valor da cadeia de caracteres para uma variável de ambiente do processo atual.<br/>                                                                                                                                                                        |
| [**FeatureParent**](installer-featureparent.md)<br/>                 |                       | Especifica o recurso pai de um recurso.<br/>                                                                                                                                                                                                  |
| [**Recursos**](installer-features.md)<br/>                           |                       | Retorna um [**objeto StringList**](stringlist-object.md) enumerando o conjunto de recursos publicados para o produto especificado.<br/>                                                                                                               |
| [**FeatureState**](installer-featurestate.md)<br/>                   |                       | Retorna o estado instalado de um recurso.<br/>                                                                                                                                                                                                   |
| [**FeatureUsageCount**](installer-featureusagecount.md)<br/>         |                       | Retorna o número de vezes que o recurso foi usado.<br/>                                                                                                                                                                                 |
| [**FeatureUsageDate**](installer-featureusagedate.md)<br/>           |                       | Retorna a data em que o recurso especificado foi usado pela última vez.<br/>                                                                                                                                                                                  |
| [**Fileattributes**](installer-fileattributes.md)<br/>               |                       | Retorna um número que representa os atributos de arquivo combinados para o caminho designado para um arquivo ou pasta.<br/>                                                                                                                                  |
| [**Patches**](installer-patches.md)<br/>                             |                       | Retorna um [**objeto StringList**](stringlist-object.md) que contém todos os patches aplicados ao produto.<br/>                                                                                                                              |
| [**PatchesEx**](installer-patchesex.md)<br/>                         |                       | Enumera uma coleção de objetos [**Patch.**](patch-object.md)<br/>                                                                                                                                                                           |
| [**PatchFiles**](installer-patchfiles.md)<br/>                       |                       | Retorna um [**objeto StringList**](stringlist-object.md) que contém uma lista de arquivos que podem ser atualizados pela lista de patches fornecida.<br/>                                                                                                 |
| [**PatchInfo**](installer-patchinfo.md)<br/>                         |                       | Retorna informações sobre um patch.<br/>                                                                                                                                                                                                          |
| [**PatchTransforms**](installer-patchtransforms.md)<br/>             |                       | Retorna a lista delimitada por ponto e vírgula de transformaçãos que estão no pacote de patch especificado e aplicadas ao produto especificado.<br/>                                                                                                            |
| [**ProductElevated**](installer-productelevated.md)<br/>             |                       | Retornará True se o produto for gerenciado ou False se o produto não for gerenciado.<br/>                                                                                                                                                              |
| [**Productinfo**](installer-productinfo.md)<br/>                     |                       | Retorna o valor do atributo especificado para um produto instalado ou publicado.<br/>                                                                                                                                                         |
| [**ProductInfoFromScript**](installer-productinfofromscript.md)<br/> |                       | Retorna o valor do atributo especificado armazenado em um script de anúncio.<br/>                                                                                                                                                         |
| [**Produtos**](installer-products.md)<br/>                           |                       | Retorna um [**objeto StringList**](stringlist-object.md) enumerando o conjunto de todos os produtos instalados ou anunciados para o usuário e o computador atual. <br/>                                                                                     |
| [**ProductsEx**](installer-productsex.md)<br/>                       |                       | Enumera uma coleção de [**objetos Product.**](product-object.md)<br/>                                                                                                                                                                       |
| [**ProductState**](installer-productstate-property.md)<br/>          |                       | Retorna as informações de estado de instalação de um produto.<br/>                                                                                                                                                                                        |
| [**QualifierDescription**](installer-qualifierdescription.md)<br/>   |                       | Retorna uma cadeia de caracteres de texto que descreve o componente qualificado.<br/>                                                                                                                                                                               |
| [**Relatedproducts**](installer-relatedproducts.md)<br/>             |                       | Retorna um [**objeto StringList**](stringlist-object.md) enumerando o conjunto de todos os produtos instalados ou anunciados para o usuário atual e o computador com uma propriedade [**UpgradeCode especificada**](upgradecode.md) em sua tabela de propriedades.<br/> |
| [**ShortcutTarget**](installer-shortcuttarget.md)<br/>               |                       | Examina um atalho e retorna seu produto, nome do recurso e componente, se disponível.<br/>                                                                                                                                                       |
| [**SummaryInformation**](installer-summaryinformation.md)<br/>       |                       | Retorna um [**objeto SummaryInfo**](summaryinfo-object.md) que pode ser usado para examinar, atualizar e adicionar propriedades ao fluxo de informações resumidas de um pacote ou transformação.<br/>                                                              |
| [**UILevel**](installer-uilevel.md)<br/>                             | Leitura/gravação<br/> | Indica o tipo de interface do usuário a ser usado ao abrir e processar pacotes subsequentes dentro do espaço de processo atual.<br/>                                                                                                           |
| [**Versão**](installer-version.md)<br/>                             |                       | Retorna a representação de cadeia de caracteres da versão atual do Windows Installer.<br/>                                                                                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | O IInstaller IID é definido como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando a interface de automação](using-the-automation-interface.md)
</dt> <dt>

[Windows Exemplos de script do instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




