---
title: Obtendo e configurando metadados e atributos
description: Obtendo e configurando metadados e atributos
ms.assetid: 83534998-4e7d-49b6-a160-ef9a0ddea5db
keywords:
- Gerenciador de Dispositivos de mídia do Windows, atributos
- Gerenciador de Dispositivos, atributos
- aplicativos de área de trabalho, atributos
- provedores de serviços, atributos
- Guia de programação, atributos
- Atributos
- Gerenciador de Dispositivos de mídia do Windows, metadados
- Gerenciador de Dispositivos, metadados
- aplicativos de área de trabalho, metadados
- provedores de serviços, metadados
- Guia de programação, metadados
- metadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8697f62dac44f5aab4b08aa4f6c516ac35a17e4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822735"
---
# <a name="getting-and-setting-metadata-and-attributes"></a><span data-ttu-id="83cde-115">Obtendo e configurando metadados e atributos</span><span class="sxs-lookup"><span data-stu-id="83cde-115">Getting and Setting Metadata and Attributes</span></span>

<span data-ttu-id="83cde-116">Um aplicativo pode obter dois tipos de informações sobre um armazenamento ou dispositivo: atributos e metadados.</span><span class="sxs-lookup"><span data-stu-id="83cde-116">An application can get two kinds of information about a storage or device: attributes and metadata.</span></span> <span data-ttu-id="83cde-117">Atributos são valores Boolianos mais simples que geralmente descrevem informações do sistema de arquivos, como se um armazenamento tem objetos filho, se ele pode ser renomeado, lido ou excluído, e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="83cde-117">Attributes are simpler Boolean values that generally describe file system information, such as whether a storage has child objects, whether it can be renamed, read, or deleted, and so on.</span></span> <span data-ttu-id="83cde-118">Os atributos são recuperados como valores de sinalizadores chamando [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) ou [**IWMDMStorage2:: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2).</span><span class="sxs-lookup"><span data-stu-id="83cde-118">Attributes are retrieved as flags values by calling [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) or [**IWMDMStorage2::GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2).</span></span> <span data-ttu-id="83cde-119">Os atributos são definidos chamando [**IWMDMStorage3:: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span><span class="sxs-lookup"><span data-stu-id="83cde-119">Attributes are set by calling [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span></span>

<span data-ttu-id="83cde-120">Um aplicativo também pode solicitar dados mais complexos (numéricos, cadeias de caracteres ou outros tipos de dados) como *metadados*.</span><span class="sxs-lookup"><span data-stu-id="83cde-120">An application can also request more complex data (numeric, string, or other data types) as *metadata*.</span></span> <span data-ttu-id="83cde-121">Os valores de metadados são identificados por nomes de cadeia de caracteres exclusivos.</span><span class="sxs-lookup"><span data-stu-id="83cde-121">Metadata values are identified by unique string names.</span></span> <span data-ttu-id="83cde-122">O Windows Media Gerenciador de Dispositivos define uma lista de constantes de cadeia de caracteres que podem ser usadas para solicitar valores; esses valores definidos são listados em [constantes de metadados](metadata-constants.md).</span><span class="sxs-lookup"><span data-stu-id="83cde-122">Windows Media Device Manager defines a list of string constants that can be used to request values; these defined values are listed in [Metadata Constants](metadata-constants.md).</span></span> <span data-ttu-id="83cde-123">Um provedor de serviços pode definir suas próprias constantes, mas um aplicativo de chamada deve estar ciente dessas definições para solicitar ou definir esses valores de metadados personalizados.</span><span class="sxs-lookup"><span data-stu-id="83cde-123">A service provider can define its own constants, but a calling application must be aware of these definitions in order to request or set these custom metadata values.</span></span> <span data-ttu-id="83cde-124">O aplicativo solicita metadados chamando [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) ou [**IWMDMStorage4:: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span><span class="sxs-lookup"><span data-stu-id="83cde-124">The application requests metadata by calling [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) or [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span></span>

<span data-ttu-id="83cde-125">Um aspecto importante de obter e definir metadados e atributos é entender de onde vêm os valores recuperados.</span><span class="sxs-lookup"><span data-stu-id="83cde-125">An important aspect of getting and setting metadata and attributes is understanding where the retrieved values come from.</span></span> <span data-ttu-id="83cde-126">O provedor de serviços ou o dispositivo pode obter esses valores de vários locais diferentes, incluindo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="83cde-126">The service provider or the device can get these values from many different places, including the following:</span></span>

-   <span data-ttu-id="83cde-127">No cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="83cde-127">From the file header.</span></span> <span data-ttu-id="83cde-128">Por exemplo, em um arquivo ASF, a taxa de bits é armazenada no cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="83cde-128">For example, in an ASF file, the bit rate is stored in the file header.</span></span>
-   <span data-ttu-id="83cde-129">De valores definidos explicitamente pelo aplicativo ao chamar um método.</span><span class="sxs-lookup"><span data-stu-id="83cde-129">From values set explicitly by the application when calling a method.</span></span> <span data-ttu-id="83cde-130">Esses valores podem ser salvos em um repositório de metadados externo no provedor de serviços ou no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83cde-130">These values may be saved in an external metadata store in the service provider or the device.</span></span> <span data-ttu-id="83cde-131">Esse armazenamento pode ou não persistir quando o dispositivo se desconectar ou desligar.</span><span class="sxs-lookup"><span data-stu-id="83cde-131">This store may or may not persist when the device disconnects or turns off.</span></span> <span data-ttu-id="83cde-132">Por exemplo, a contagem de execuções e as classificações de estrelas do usuário normalmente são armazenadas em repositórios externos no computador ou dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83cde-132">For example, the play count and user star ratings are typically stored in external stores on the computer or device.</span></span>
-   <span data-ttu-id="83cde-133">Examinando as informações fornecidas pelo sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="83cde-133">By examining information provided by the file system.</span></span> <span data-ttu-id="83cde-134">Por exemplo, se um arquivo é somente leitura ou se uma pasta tem filhos.</span><span class="sxs-lookup"><span data-stu-id="83cde-134">For example, whether a file is read-only or whether a folder has children.</span></span>
-   <span data-ttu-id="83cde-135">Abrindo e analisando os dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="83cde-135">By opening and parsing the file data.</span></span>

<span data-ttu-id="83cde-136">É importante perceber que uma propriedade pode ser armazenada em mais de um local (dentro do cabeçalho do arquivo e também em um repositório local) e que pode ou não ser editável.</span><span class="sxs-lookup"><span data-stu-id="83cde-136">It is important to realize that a property might be stored in more than one location (within the file header and also in a local store), and that it may or may not be editable.</span></span> <span data-ttu-id="83cde-137">Por exemplo, alterar uma descrição de arquivo pode ou não ser persistente; Se o provedor de serviços armazenar a descrição localmente, ele não será mantido no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83cde-137">For example, changing a file description may or may not be persistent; if the service provider stores the description locally, it will not persist on the device.</span></span> <span data-ttu-id="83cde-138">Da mesma forma, se a descrição do arquivo for extraída do cabeçalho do arquivo, a modificação será persistente somente se o provedor ou o dispositivo de serviço abrir e modificar os dados do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="83cde-138">Similarly, if the file description is taken from the file header, modifying this will only be persistent if the service provider or device opens and modifies the header data.</span></span> <span data-ttu-id="83cde-139">A maioria dos aplicativos faz uma melhor tentativa alterando os valores desejados, mas não depende de nenhuma propriedade ser alterada de forma persistente.</span><span class="sxs-lookup"><span data-stu-id="83cde-139">Most applications make a best attempt by changing desired values, but do not depend on any properties to be persistently changed.</span></span>

<span data-ttu-id="83cde-140">Mais informações sobre como obter e definir valores são fornecidas nas seções apropriadas para desenvolvedores de aplicativos e desenvolvedores de provedores de serviços mais adiante na documentação.</span><span class="sxs-lookup"><span data-stu-id="83cde-140">More information on getting and setting values is given in the appropriate sections for application developers and service provider developers later in the documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83cde-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="83cde-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83cde-142">**Tarefas comuns a aplicativos e provedores de serviços**</span><span class="sxs-lookup"><span data-stu-id="83cde-142">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




