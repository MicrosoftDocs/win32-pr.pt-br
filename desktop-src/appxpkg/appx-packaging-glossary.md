---
title: Glossário de empacotamento, implantação e consulta
description: Fornece definições para termos relacionados ao empacotamento, implantação e consulta para aplicativos do Windows.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 15E35DCF-C6C1-446A-B09B-6428F9C8A677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a2112b593e2d2a5aaf4f06525160e2d799bad1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104365832"
---
# <a name="packaging-deployment-and-query-glossary"></a><span data-ttu-id="d4151-103">Glossário de empacotamento, implantação e consulta</span><span class="sxs-lookup"><span data-stu-id="d4151-103">Packaging, deployment, and query glossary</span></span>

<dl> <dt>

<span data-ttu-id="d4151-104"><span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**ID do modelo de usuário do aplicativo**</span><span class="sxs-lookup"><span data-stu-id="d4151-104"><span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**application user model ID**</span></span>
</dt> <dd>

<span data-ttu-id="d4151-105">A ID do modelo de usuário do aplicativo identifica exclusivamente um aplicativo no sistema operacional para que o sistema operacional possa enviar notificações e assim por diante para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d4151-105">The application user model ID uniquely identifies an app on the operating system so the operating system can send notifications and so on to the app.</span></span>

</dd> <dt>

<span data-ttu-id="d4151-106"><span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**mapa de blocos**</span><span class="sxs-lookup"><span data-stu-id="d4151-106"><span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**block map**</span></span>
</dt> <dd>

<span data-ttu-id="d4151-107">Define os índices e hashes criptográficos para blocos de código executável e dados que são armazenados nos arquivos de um pacote de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d4151-107">Defines the indices and cryptographic hashes for blocks of executable code and data that are stored in the files of an app package.</span></span> <span data-ttu-id="d4151-108">Um arquivo de BlockMap.xml é necessário para cada pacote de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d4151-108">A BlockMap.xml file is required for every app package.</span></span>

</dd> <dt>

<span data-ttu-id="d4151-109"><span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**pacote de dependência**</span><span class="sxs-lookup"><span data-stu-id="d4151-109"><span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**dependency package**</span></span>
</dt> <dd>

<span data-ttu-id="d4151-110">Um pacote do qual outro pacote depende.</span><span class="sxs-lookup"><span data-stu-id="d4151-110">A package on which another package depends.</span></span> <span data-ttu-id="d4151-111">A dependência é declarada no manifesto do pacote dependente e não no manifesto do pacote de dependência.</span><span class="sxs-lookup"><span data-stu-id="d4151-111">The dependency is declared in the dependent package's manifest and not in the dependency package's manifest.</span></span>

</dd> <dt>

<span data-ttu-id="d4151-112"><span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**pacote dependente**</span><span class="sxs-lookup"><span data-stu-id="d4151-112"><span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**dependent package**</span></span>
</dt> <dd>

<span data-ttu-id="d4151-113">Um pacote que usa uma dependência em outro pacote.</span><span class="sxs-lookup"><span data-stu-id="d4151-113">A package that takes a dependency on another package.</span></span> <span data-ttu-id="d4151-114">A dependência é declarada no manifesto do pacote dependente.</span><span class="sxs-lookup"><span data-stu-id="d4151-114">The dependency is declared in the dependent package's manifest.</span></span>

</dd> <dt>

<span data-ttu-id="d4151-115"><span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**arquivos de superfície**</span><span class="sxs-lookup"><span data-stu-id="d4151-115"><span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**footprint files**</span></span>
</dt> <dd>

<span data-ttu-id="d4151-116">Arquivos em um pacote de aplicativo que não fazem parte do aplicativo a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="d4151-116">Files within an app package that are not part of the app to be deployed.</span></span> <span data-ttu-id="d4151-117">Esses arquivos fornecem metadados referentes ao pacote.</span><span class="sxs-lookup"><span data-stu-id="d4151-117">These files provide metadata pertaining to the package.</span></span> <span data-ttu-id="d4151-118">Os arquivos de superfície padrão incluem o manifesto, o mapa de blocos, o mapa de fluxo e a assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="d4151-118">Standard footprint files include the manifest, block map, stream map, and digital signature.</span></span> <span data-ttu-id="d4151-119">Os arquivos de superfície são criados como parte do processo de compilação do pacote.</span><span class="sxs-lookup"><span data-stu-id="d4151-119">Footprint files are created as part of the package build process.</span></span> <span data-ttu-id="d4151-120">Além da especificação OPC, \[ Content \_ Types \] . xml e arquivos cujos nomes correspondem ao \* \\ \_ padrão "rels \\ \* . rels" são os arquivos de superfície.</span><span class="sxs-lookup"><span data-stu-id="d4151-120">In addition per the OPC specification, \[Content\_Types\].xml and files whose names match the "\*\\\_rels\\\*.rels" pattern are footprint files.</span></span>

</dd> <dt>

<span data-ttu-id="d4151-121"><span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**manifesto**</span><span class="sxs-lookup"><span data-stu-id="d4151-121"><span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**manifest**</span></span>
</dt> <dd>

<span data-ttu-id="d4151-122">Um arquivo XML que descreve o conteúdo e os metadados associados a um pacote, incluindo a ID do pacote.</span><span class="sxs-lookup"><span data-stu-id="d4151-122">An XML file that describes the contents and metadata associated with a package including the package ID.</span></span> <span data-ttu-id="d4151-123">Um arquivo XML de manifesto é necessário para cada pacote de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d4151-123">A manifest XML file is required for every app package.</span></span>

</dd> <dt>

<span data-ttu-id="d4151-124"><span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**OPC**</span><span class="sxs-lookup"><span data-stu-id="d4151-124"><span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**OPC**</span></span>
</dt> <dd>

<span data-ttu-id="d4151-125">As Open Packaging Conventions (OPC) descreve uma tecnologia de arquivo de contêiner documentada nos padrões ISO/IEC 29500 e ECMA 376.</span><span class="sxs-lookup"><span data-stu-id="d4151-125">Open Packaging Conventions (OPC) describes a container-file technology that is documented in the ISO/IEC 29500 and ECMA 376 standards.</span></span> <span data-ttu-id="d4151-126">Os pacotes de aplicativos são compatíveis com OPC.</span><span class="sxs-lookup"><span data-stu-id="d4151-126">App packages are OPC-compliant.</span></span>

</dd> <dt>

<span data-ttu-id="d4151-127"><span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**agrupa**</span><span class="sxs-lookup"><span data-stu-id="d4151-127"><span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**package**</span></span>
</dt> <dd>

<span data-ttu-id="d4151-128">A unidade de implantação, gerenciamento e software de serviço associada ao modelo de empacotamento de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d4151-128">The unit of deployment, management, and servicing software associated with the app packaging model.</span></span> <span data-ttu-id="d4151-129">Um pacote contém os arquivos que constituem o aplicativo, juntamente com um arquivo de manifesto que descreve o software para o Windows.</span><span class="sxs-lookup"><span data-stu-id="d4151-129">A package contains the files that constitute the app, along with a manifest file that describes the software to Windows.</span></span>

</dd> <dt>

<span data-ttu-id="d4151-130"><span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**nome da família de pacotes**</span><span class="sxs-lookup"><span data-stu-id="d4151-130"><span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**package family name**</span></span>
</dt> <dd>

<span data-ttu-id="d4151-131">Uma forma serializada da ID do pacote que representa exclusivamente a família de pacotes no computador.</span><span class="sxs-lookup"><span data-stu-id="d4151-131">A serialized form of the package ID that uniquely represents the package family on the computer.</span></span> <span data-ttu-id="d4151-132">Ele é adequado para nomear objetos, como arquivos e pastas.</span><span class="sxs-lookup"><span data-stu-id="d4151-132">It is suitable for naming objects such as files and folders.</span></span> <span data-ttu-id="d4151-133">O nome da família de pacotes é semelhante ao nome completo do pacote, mas inclui apenas o nome e o Publicador.</span><span class="sxs-lookup"><span data-stu-id="d4151-133">The package family name is similar to the package full name, but includes only the name and publisher.</span></span> <span data-ttu-id="d4151-134">Como ela exclui informações que mudam com a manutenção (versão, arquitetura e informações de recursos), ela é útil para referências independentes de versão para o pacote.</span><span class="sxs-lookup"><span data-stu-id="d4151-134">Because it excludes info that changes with servicing (version, architecture, and resource info), it is useful for version-independent references to the package.</span></span>

</dd> <dt>

<span data-ttu-id="d4151-135"><span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**nome completo do pacote**</span><span class="sxs-lookup"><span data-stu-id="d4151-135"><span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**package full name**</span></span>
</dt> <dd>

<span data-ttu-id="d4151-136">Uma forma serializada da ID do pacote que representa exclusivamente esta versão do pacote no computador.</span><span class="sxs-lookup"><span data-stu-id="d4151-136">A serialized form of the package ID that uniquely represents this version of the package on the computer.</span></span> <span data-ttu-id="d4151-137">Ele é adequado para nomear objetos, como arquivos e pastas.</span><span class="sxs-lookup"><span data-stu-id="d4151-137">It is suitable for naming objects such as files and folders.</span></span>

</dd> <dt>

<span data-ttu-id="d4151-138"><span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**ID do pacote**</span><span class="sxs-lookup"><span data-stu-id="d4151-138"><span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**package ID**</span></span>
</dt> <dd>

<span data-ttu-id="d4151-139">Um identificador global exclusivo para um pacote.</span><span class="sxs-lookup"><span data-stu-id="d4151-139">A globally unique identifier for a package.</span></span> <span data-ttu-id="d4151-140">Ele é composto de uma tupla de atributos para o pacote, incluindo nome, editor, arquitetura com suporte, informações de recursos e versão.</span><span class="sxs-lookup"><span data-stu-id="d4151-140">It is composed of a tuple of attributes for the package including name, publisher, supported architecture, resource info, and version.</span></span> <span data-ttu-id="d4151-141">Consulte nome completo do pacote e nome da família de pacotes para formulários serializados da ID do pacote.</span><span class="sxs-lookup"><span data-stu-id="d4151-141">See package full name and package family name for serialized forms of the package ID.</span></span>

</dd> <dt>

<span data-ttu-id="d4151-142"><span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**ID do aplicativo relativo do pacote**</span><span class="sxs-lookup"><span data-stu-id="d4151-142"><span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**package relative application ID**</span></span>
</dt> <dd>

<span data-ttu-id="d4151-143">O atributo **ID** no elemento [**Application**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) no manifesto do pacote, que também é conhecido como PRAID.</span><span class="sxs-lookup"><span data-stu-id="d4151-143">The **Id** attribute on the [**Application**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) element within the package manifest, which is also known as PRAID.</span></span> <span data-ttu-id="d4151-144">Essa cadeia de caracteres identifica exclusivamente um aplicativo em um pacote.</span><span class="sxs-lookup"><span data-stu-id="d4151-144">This string uniquely identifies an app within a package.</span></span> <span data-ttu-id="d4151-145">Esse atributo é necessário para o elemento **Application** .</span><span class="sxs-lookup"><span data-stu-id="d4151-145">This attribute is required for the **Application** element.</span></span>

</dd> <dt>

<span data-ttu-id="d4151-146"><span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**arquivos de carga**</span><span class="sxs-lookup"><span data-stu-id="d4151-146"><span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**payload files**</span></span>
</dt> <dd>

<span data-ttu-id="d4151-147">Os arquivos em um pacote de aplicativo que fazem parte do aplicativo a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="d4151-147">The files within an app package that are part of the app to be deployed.</span></span> <span data-ttu-id="d4151-148">Esses arquivos são extraídos e colocados na pasta de instalação do usuário.</span><span class="sxs-lookup"><span data-stu-id="d4151-148">These files are extracted and placed in the user's installation folder.</span></span>

</dd> <dt>

<span data-ttu-id="d4151-149"><span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**ID do recurso**</span><span class="sxs-lookup"><span data-stu-id="d4151-149"><span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**resource ID**</span></span>
</dt> <dd>

<span data-ttu-id="d4151-150">Uma parte opcional de uma ID de pacote que é usada para diferenciar os recursos no pacote.</span><span class="sxs-lookup"><span data-stu-id="d4151-150">An optional part of a package ID that is used to differentiate the resources in the package.</span></span> <span data-ttu-id="d4151-151">Por exemplo, uma ID de recurso pode ser usada para especificar o idioma ou a localidade.</span><span class="sxs-lookup"><span data-stu-id="d4151-151">For example, a resource ID can be used to specify the language or locale.</span></span>

</dd> <dt>

<span data-ttu-id="d4151-152"><span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**Diretório central ZIP**</span><span class="sxs-lookup"><span data-stu-id="d4151-152"><span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**ZIP central directory**</span></span>
</dt> <dd>

<span data-ttu-id="d4151-153">As sequências de bytes em um arquivo ZIP que armazenam metadados sobre o arquivo ZIP e seu conteúdo, incluindo nome, tamanho, configurações de compactação e local dentro do arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="d4151-153">The byte sequences in a ZIP file that store metadata about the ZIP archive and its contents including name, size, compression settings, and location within the archive.</span></span>

</dd> </dl>

 

 