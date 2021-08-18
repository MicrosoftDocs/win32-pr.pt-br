---
title: Glossário de empacotamento, implantação e consulta
description: fornece definições para termos relacionados ao empacotamento, implantação e consulta para aplicativos Windows.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 15E35DCF-C6C1-446A-B09B-6428F9C8A677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678a273b82806a724e50c7f29c512d19e1723283582abb3aa8b97f49f6293182
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130268"
---
# <a name="packaging-deployment-and-query-glossary"></a>Glossário de empacotamento, implantação e consulta

<dl> <dt>

<span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**ID do modelo de usuário do aplicativo**
</dt> <dd>

A ID do modelo de usuário do aplicativo identifica exclusivamente um aplicativo no sistema operacional para que o sistema operacional possa enviar notificações e assim por diante para o aplicativo.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**mapa de blocos**
</dt> <dd>

Define os índices e hashes criptográficos para blocos de código executável e dados que são armazenados nos arquivos de um pacote de aplicativo. Um arquivo de BlockMap.xml é necessário para cada pacote de aplicativo.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**pacote de dependência**
</dt> <dd>

Um pacote do qual outro pacote depende. A dependência é declarada no manifesto do pacote dependente e não no manifesto do pacote de dependência.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**pacote dependente**
</dt> <dd>

Um pacote que usa uma dependência em outro pacote. A dependência é declarada no manifesto do pacote dependente.

</dd> <dt>

<span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**arquivos de superfície**
</dt> <dd>

Arquivos em um pacote de aplicativo que não fazem parte do aplicativo a ser implantado. Esses arquivos fornecem metadados referentes ao pacote. Os arquivos de superfície padrão incluem o manifesto, o mapa de blocos, o mapa de fluxo e a assinatura digital. Os arquivos de superfície são criados como parte do processo de compilação do pacote. Além da especificação OPC, os \[ \_ tipos de conteúdo \].xml e arquivos cujos nomes correspondem ao \* \\ \_ padrão "rels \\ \* . rels" são arquivos de superfície.

</dd> <dt>

<span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**manifesto**
</dt> <dd>

Um arquivo XML que descreve o conteúdo e os metadados associados a um pacote, incluindo a ID do pacote. Um arquivo XML de manifesto é necessário para cada pacote de aplicativo.

</dd> <dt>

<span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**OPC**
</dt> <dd>

As Open Packaging Conventions (OPC) descreve uma tecnologia de arquivo de contêiner documentada nos padrões ISO/IEC 29500 e ECMA 376. Os pacotes de aplicativos são compatíveis com OPC.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**agrupa**
</dt> <dd>

A unidade de implantação, gerenciamento e software de serviço associada ao modelo de empacotamento de aplicativo. Um pacote contém os arquivos que constituem o aplicativo, juntamente com um arquivo de manifesto que descreve o software a ser Windows.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**nome da família de pacotes**
</dt> <dd>

Uma forma serializada da ID do pacote que representa exclusivamente a família de pacotes no computador. Ele é adequado para nomear objetos, como arquivos e pastas. O nome da família de pacotes é semelhante ao nome completo do pacote, mas inclui apenas o nome e o Publicador. Como ela exclui informações que mudam com a manutenção (versão, arquitetura e informações de recursos), ela é útil para referências independentes de versão para o pacote.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**nome completo do pacote**
</dt> <dd>

Uma forma serializada da ID do pacote que representa exclusivamente esta versão do pacote no computador. Ele é adequado para nomear objetos, como arquivos e pastas.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**ID do pacote**
</dt> <dd>

Um identificador global exclusivo para um pacote. Ele é composto de uma tupla de atributos para o pacote, incluindo nome, editor, arquitetura com suporte, informações de recursos e versão. Consulte nome completo do pacote e nome da família de pacotes para formulários serializados da ID do pacote.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**ID do aplicativo relativo do pacote**
</dt> <dd>

O atributo **ID** no elemento [**Application**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) no manifesto do pacote, que também é conhecido como PRAID. Essa cadeia de caracteres identifica exclusivamente um aplicativo em um pacote. Esse atributo é necessário para o elemento **Application** .

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**arquivos de carga**
</dt> <dd>

Os arquivos em um pacote de aplicativo que fazem parte do aplicativo a ser implantado. Esses arquivos são extraídos e colocados na pasta de instalação do usuário.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**ID do recurso**
</dt> <dd>

Uma parte opcional de uma ID de pacote que é usada para diferenciar os recursos no pacote. Por exemplo, uma ID de recurso pode ser usada para especificar o idioma ou a localidade.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**Diretório central ZIP**
</dt> <dd>

As sequências de bytes em um arquivo ZIP que armazenam metadados sobre o arquivo ZIP e seu conteúdo, incluindo nome, tamanho, configurações de compactação e local dentro do arquivo morto.

</dd> </dl>

 

 