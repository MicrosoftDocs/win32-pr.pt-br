---
description: Um objeto de instalador deve ser criado inicialmente para carregar o suporte de automação que é necessário para que o COM acesse as funções do instalador. Esse objeto fornece wrappers para criar os objetos de nível superior e acessar seus métodos.
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
ms.openlocfilehash: 4afddcce55a739ad322be10c736a6e9119f5c9eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748774"
---
# <a name="installer-object"></a>Objeto do instalador

Um objeto de **instalador** deve ser criado inicialmente para carregar o suporte de automação que é necessário para que o com Acesse as funções do instalador. Esse objeto fornece wrappers para criar os objetos de nível superior e acessar seus métodos.

Você pode criar o objeto do **instalador** do ProgID "WindowsInstaller. Installer".

## <a name="members"></a>Membros

O objeto do **instalador** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto do **instalador** tem esses métodos.



| Método                                                                   | Descrição                                                                                                                                                                                     |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Addsource**](installer-addsource.md)                                 | Adiciona uma origem à lista de fontes de rede válidas na SourceList.<br/>                                                                                                                |
| [**AdvertiseProduct**](installer-advertiseproduct.md)                   | Anuncia um pacote de instalação.<br/>                                                                                                                                                  |
| [**AdvertiseScript**](installer-advertisescript.md)                     | Anuncia um pacote de instalação. <br/>                                                                                                                                                 |
| [**ApplyMultiplePatches**](installer-applymultiplepatches.md)           | Aplica um ou mais patches aos produtos qualificados para receber o patch. Define a propriedade [**patch**](patch.md) para o caminho dos pacotes de patch fornecidos.<br/>                          |
| [**ApplyPatch**](installer-applypatch.md)                               | Invoca uma instalação e define a propriedade [**patch**](patch.md) para o caminho do pacote de patches para cada produto listado pelo pacote de patch como qualificado para receber o patch.<br/> |
| [**ClearSourceList**](installer-clearsourcelist.md)                     | Remove todas as fontes de rede da SourceList.<br/>                                                                                                                                     |
| [**CollectUserInfo**](installer-collectuserinfo.md)                     | Invoca uma sequência do assistente de interface do usuário que coleta e armazena informações do usuário e o código do produto.<br/>                                                                        |
| [**ConfigureFeature**](installer-configurefeature.md)                   | Configura o estado instalado de um recurso do produto.<br/>                                                                                                                                 |
| [**ConfigureProduct**](installer-configureproduct.md)                   | Instala ou desinstala um produto.<br/>                                                                                                                                                    |
| [**CreateAdvertiseScript**](installer-createadvertisescript.md)         | Gera um script de anúncio.<br/>                                                                                                                                                       |
| [**CreateRecord**](installer-createrecord.md)                           | Retorna um novo objeto de [**registro**](record-object.md) com o número de campos solicitado.<br/>                                                                                            |
| [**EnableLog**](installer-enablelog.md)                                 | Habilita o registro em log do tipo de mensagem selecionado para todas as sessões de instalação subsequentes no espaço de processo atual.<br/>                                                                  |
| [**ExtractPatchXMLData**](installer-extractpatchxmldata.md)             | Extrai informações de um patch como uma cadeia de caracteres XML.<br/>                                                                                                                                  |
| [**FileHash**](installer-filehash.md)                                   | Usa o caminho para um arquivo e retorna um hash de 128 bits desse arquivo.<br/>                                                                                                                    |
| [**FileSignatureInfo**](installer-filesignatureinfo.md)                 | Usa o caminho para um arquivo e retorna um **SafeArray** de bytes que representa o hash ou o certificado codificado.<br/>                                                                   |
| [**Tamanho**](installer-filesize.md)                                   | Retorna o tamanho do arquivo especificado.<br/>                                                                                                                                              |
| [**FileVersion**](installer-fileversion.md)                             | Retorna a cadeia de caracteres de versão ou de linguagem do caminho especificado.<br/>                                                                                                                 |
| [**ForceSourceListResolution**](installer-forcesourcelistresolution.md) | Força o instalador a Pesquisar a lista de origem para uma fonte de produto válida na próxima vez que uma fonte for necessária.<br/>                                                                        |
| [**InstallProduct**](installer-installproduct.md)                       | Abre um pacote do instalador e Inicializa uma sessão de instalação.<br/>                                                                                                                  |
| [**LastErrorRecord**](installer-lasterrorrecord.md)                     | Retorna um objeto de [**registro**](record-object.md) que contém parâmetros de erro para o erro mais recente da função que produziu o registro de erro.<br/>                          |
| [**OpenDatabase**](installer-opendatabase.md)                           | Abre um banco de dados existente ou cria um novo.<br/>                                                                                                                                     |
| [**OpenPackage**](installer-openpackage.md)                             | Abre um pacote do instalador para uso com funções que acessam o banco de dados do produto e o mecanismo de instalação.<br/>                                                                               |
| [**OpenProduct**](installer-openproduct.md)                             | Abre um pacote do instalador para um produto instalado usando o código do produto.<br/>                                                                                                          |
| [**ProvideAssembly**](installer-provideassembly.md)                     | Retorna o caminho instalado de um assembly.<br/>                                                                                                                                           |
| [**ProvideComponent**](installer-providecomponent.md)                   | Retorna o caminho completo do componente e executa qualquer instalação necessária.<br/>                                                                                                             |
| [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) | Retorna o caminho completo do componente e executa qualquer instalação necessária.<br/>                                                                                                             |
| [**Registrovalue**](installer-registryvalue.md)                         | Lê informações sobre uma chave de valor especificada do registro.<br/>                                                                                                                           |
| [**ReinstallFeature**](installer-reinstallfeature.md)                   | Reinstala recursos ou corrige problemas com os recursos instalados.<br/>                                                                                                                    |
| [**ReinstallProduct**](installer-reinstallproduct.md)                   | Reinstala um produto ou corrige problemas de instalação em um produto instalado.<br/>                                                                                                      |
| [**RemovePatches**](installer-removepatches.md)                         | Remove um ou mais patches para produtos qualificados para receber o patch. <br/>                                                                                                              |
| [**UseFeature**](installer-usefeature.md)                               | Incrementa a contagem de uso de um recurso específico e retorna o estado de instalação para esse recurso.<br/>                                                                             |



 

### <a name="properties"></a>Propriedades

O objeto do **instalador** tem essas propriedades.



| Propriedade                                                                    | Tipo de acesso           | Descrição                                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClientsEx**](installer-components.md)<br/>                        |                       | Retorna um objeto [**recordlist**](recordlist-object.md) que lista os produtos que usam um componente instalado especificado.<br/> **[Windows Installer 4,5 e anteriores](not-supported-in-windows-installer-4-5.md):** Sem suporte.<br/>       |
| [**ComponentClients**](installer-componentclients.md)<br/>           |                       | Retorna um objeto [**StringList**](stringlist-object.md) que enumera o conjunto de clientes de um componente especificado.<br/>                                                                                                                           |
| [**ComponentPath**](installer-componentpath.md)<br/>                 |                       | Retorna o caminho completo para um componente instalado.<br/>                                                                                                                                                                                            |
| [**ComponentPathEx**](installer-componentpathex.md)<br/>             |                       | Retorna um objeto [**recordlist**](recordlist-object.md) que fornece o caminho completo de um componente instalado especificado. <br/> **[Windows Installer 4,5 e anteriores](not-supported-in-windows-installer-4-5.md):** Sem suporte.<br/>       |
| [**ComponentQualifiers**](installer-componentqualifiers.md)<br/>     |                       | Retorna um objeto [**StringList**](stringlist-object.md) que enumera o conjunto de qualificadores registrados para o componente especificado.<br/>                                                                                                          |
| [**Componentes**](installer-components.md)<br/>                       |                       | Retorna um objeto [**StringList**](stringlist-object.md) que enumera o conjunto de componentes instalados para todos os produtos.<br/>                                                                                                                      |
| [**ComponentsEx**](installer-componentsex.md)<br/>                   |                       | Retorna um objeto [**recordlist**](recordlist-object.md) que lista os componentes instalados.<br/> **[Windows Installer 4,5 e anteriores](not-supported-in-windows-installer-4-5.md):** Sem suporte.<br/>                                    |
| [**Ambiente**](installer-environment.md)<br/>                     | Leitura/gravação<br/> | O valor da cadeia de caracteres para uma variável de ambiente do processo atual.<br/>                                                                                                                                                                        |
| [**FeatureParent**](installer-featureparent.md)<br/>                 |                       | Especifica o recurso pai de um recurso.<br/>                                                                                                                                                                                                  |
| [**Recursos**](installer-features.md)<br/>                           |                       | Retorna um objeto [**StringList**](stringlist-object.md) que enumera o conjunto de recursos publicados para o produto especificado.<br/>                                                                                                               |
| [**Recurso**](installer-featurestate.md)<br/>                   |                       | Retorna o estado instalado de um recurso.<br/>                                                                                                                                                                                                   |
| [**FeatureUsageCount**](installer-featureusagecount.md)<br/>         |                       | Retorna o número de vezes que o recurso foi usado.<br/>                                                                                                                                                                                 |
| [**FeatureUsageDate**](installer-featureusagedate.md)<br/>           |                       | Retorna a data em que o recurso especificado foi usado pela última vez.<br/>                                                                                                                                                                                  |
| [**FileAttributes**](installer-fileattributes.md)<br/>               |                       | Retorna um número que representa os atributos de arquivo combinados para o caminho designado para um arquivo ou pasta.<br/>                                                                                                                                  |
| [**Atualizados**](installer-patches.md)<br/>                             |                       | Retorna um objeto [**StringList**](stringlist-object.md) que contém todos os patches aplicados ao produto.<br/>                                                                                                                              |
| [**PatchesEx**](installer-patchesex.md)<br/>                         |                       | Enumera uma coleção de objetos [**patch**](patch-object.md) .<br/>                                                                                                                                                                           |
| [**PatchFiles**](installer-patchfiles.md)<br/>                       |                       | Retorna um objeto [**StringList**](stringlist-object.md) que contém uma lista de arquivos que podem ser atualizados pela lista de patches fornecida.<br/>                                                                                                 |
| [**PatchInfo**](installer-patchinfo.md)<br/>                         |                       | Retorna informações sobre um patch.<br/>                                                                                                                                                                                                          |
| [**PatchTransforms**](installer-patchtransforms.md)<br/>             |                       | Retorna a lista delimitada por ponto e vírgula de transformações que estão no pacote de patch especificado e aplicadas ao produto especificado.<br/>                                                                                                            |
| [**ProductElevated**](installer-productelevated.md)<br/>             |                       | Retornará true se o produto for gerenciado ou falso se o produto não for gerenciado.<br/>                                                                                                                                                              |
| [**ProductInfo**](installer-productinfo.md)<br/>                     |                       | Retorna o valor do atributo especificado para um produto instalado ou publicado.<br/>                                                                                                                                                         |
| [**ProductInfoFromScript**](installer-productinfofromscript.md)<br/> |                       | Retorna o valor do atributo especificado que é armazenado em um script de anúncio.<br/>                                                                                                                                                         |
| [**Produtos**](installer-products.md)<br/>                           |                       | Retorna um objeto [**StringList**](stringlist-object.md) que enumera o conjunto de todos os produtos instalados ou anunciados para o usuário e a máquina atuais. <br/>                                                                                     |
| [**ProductsEx**](installer-productsex.md)<br/>                       |                       | Enumera uma coleção de objetos [**Product**](product-object.md) .<br/>                                                                                                                                                                       |
| [**ProductState**](installer-productstate-property.md)<br/>          |                       | Retorna as informações de estado de instalação de um produto.<br/>                                                                                                                                                                                        |
| [**QualifierDescription**](installer-qualifierdescription.md)<br/>   |                       | Retorna uma cadeia de texto que descreve o componente qualificado.<br/>                                                                                                                                                                               |
| [**RelatedProducts**](installer-relatedproducts.md)<br/>             |                       | Retorna um objeto [**StringList**](stringlist-object.md) que enumera o conjunto de todos os produtos instalados ou anunciados para o usuário atual e computador com uma propriedade [**UpgradeCode**](upgradecode.md) especificada em sua tabela de propriedades.<br/> |
| [**ShortcutTarget**](installer-shortcuttarget.md)<br/>               |                       | Examina um atalho e retorna seu produto, o nome do recurso e o componente, se disponível.<br/>                                                                                                                                                       |
| [**SummaryInformation**](installer-summaryinformation.md)<br/>       |                       | Retorna um objeto [**SummaryInfo**](summaryinfo-object.md) que pode ser usado para examinar, atualizar e adicionar propriedades ao fluxo de informações de Resumo de um pacote ou de uma transformação.<br/>                                                              |
| [**UILevel**](installer-uilevel.md)<br/>                             | Leitura/gravação<br/> | Indica o tipo de interface do usuário a ser usado ao abrir e processar pacotes subsequentes no espaço de processo atual.<br/>                                                                                                           |
| [**Versão**](installer-version.md)<br/>                             |                       | Retorna a representação da cadeia de caracteres da versão atual do Windows Installer.<br/>                                                                                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando a interface de automação](using-the-automation-interface.md)
</dt> <dt>

[Exemplos de script de Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




