---
title: Acessando metadados e atributos no aplicativo
description: Obtendo e configurando metadados e atributos no aplicativo
ms.assetid: 308a722d-1c65-41eb-a0e2-21171eb410d5
keywords:
- Gerenciador de Dispositivos de mídia do Windows, metadados
- Gerenciador de Dispositivos, metadados
- Guia de programação, metadados
- aplicativos de área de trabalho, metadados
- Criando aplicativos de Gerenciador de Dispositivos de mídia do Windows, metadados
- metadata
- Gerenciador de Dispositivos de mídia do Windows, atributos
- Gerenciador de Dispositivos, atributos
- Guia de programação, atributos
- aplicativos de área de trabalho, atributos
- Criando aplicativos do Windows Media Gerenciador de Dispositivos, atributos
- Atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a78dbb31ebcc5ec99b1db3503b386b09b5a3c05
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/27/2019
ms.locfileid: "104293630"
---
# <a name="accessing-metadata-and-attributes-in-the-app"></a><span data-ttu-id="6066a-115">Acessando metadados e atributos no aplicativo</span><span class="sxs-lookup"><span data-stu-id="6066a-115">Accessing metadata and attributes in the app</span></span>

<span data-ttu-id="6066a-116">Uma discussão geral de metadados e atributos está disponível para [obter e definir metadados e atributos](getting-and-setting-metadata-and-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="6066a-116">A general discussion of metadata and attributes is available in [Getting and Setting Metadata and Attributes](getting-and-setting-metadata-and-attributes.md).</span></span> <span data-ttu-id="6066a-117">Esta seção aborda chamadas de método de aplicativo específicas para recuperar ou definir valores.</span><span class="sxs-lookup"><span data-stu-id="6066a-117">This section covers specific application method calls to retrieve or set values.</span></span>

<span data-ttu-id="6066a-118">Os aplicativos podem recuperar atributos ou metadados sobre um armazenamento específico chamando [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes), [**IWMDMStorage2:: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2), [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) ou [**IWMDMStorage4:: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span><span class="sxs-lookup"><span data-stu-id="6066a-118">Applications can retrieve attributes or metadata about a specific storage by calling [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes), [**IWMDMStorage2::GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2), [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) or [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span></span> <span data-ttu-id="6066a-119">**GetMetadata** recupera uma coleção completa de todos os metadados associados a um armazenamento, e o aplicativo pode enumerar por todos os valores ou solicitar valores específicos da coleção.</span><span class="sxs-lookup"><span data-stu-id="6066a-119">**GetMetadata** retrieves a full collection of all the metadata associated with a storage, and the application can then enumerate through all values or request specific values from the collection.</span></span> <span data-ttu-id="6066a-120">**GetSpecifiedMetadata** cria um objeto de metadados em nome do chamador.</span><span class="sxs-lookup"><span data-stu-id="6066a-120">**GetSpecifiedMetadata** creates a metadata object on behalf of the caller.</span></span> <span data-ttu-id="6066a-121">O chamador pode solicitar um subconjunto dos dados disponíveis preenchendo o parâmetro *ppwszPropNames* com uma matriz das cadeias de caracteres de propriedades do Windows Media Gerenciador de dispositivos desejadas e a contagem dessa matriz.</span><span class="sxs-lookup"><span data-stu-id="6066a-121">The caller may request a subset of the available data by filling in the *ppwszPropNames* parameter with an array of the desired Windows Media Device Manager property strings, and the count of that array.</span></span> <span data-ttu-id="6066a-122">O objeto de metadados retornado será preenchido com as propriedades que poderiam ser recuperadas.</span><span class="sxs-lookup"><span data-stu-id="6066a-122">The returned metadata object will be filled with those properties that could be retrieved.</span></span> <span data-ttu-id="6066a-123">As propriedades que não puderam ser recuperadas estarão ausentes.</span><span class="sxs-lookup"><span data-stu-id="6066a-123">Those properties that couldn't be retrieved will be absent.</span></span> <span data-ttu-id="6066a-124">Os metadados são retornados em uma base de melhor esforço.</span><span class="sxs-lookup"><span data-stu-id="6066a-124">Metadata is returned on a best-effort basis.</span></span>

<span data-ttu-id="6066a-125">Um dispositivo pode definir atributos ou metadados em um armazenamento chamando [**IWMDMStorage:: SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes), [**IWMDMStorage2:: SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)ou [**IWMDMStorage3:: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span><span class="sxs-lookup"><span data-stu-id="6066a-125">A device can set attributes or metadata on a storage by calling [**IWMDMStorage::SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes), [**IWMDMStorage2::SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2), or [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span></span> <span data-ttu-id="6066a-126">Observe que não há nenhuma garantia de que os valores definidos serão persistidos, pois eles podem ser armazenados em um repositório de arquivos externo não persistente, os valores podem não ter suporte ou o dispositivo pode não dar suporte às propriedades como graváveis.</span><span class="sxs-lookup"><span data-stu-id="6066a-126">Note that there is no guarantee that any values set will persist, because they may be stored in a non-persistent external file store, the values may not be supported, or, the device may not support the properties as writeable.</span></span>

<span data-ttu-id="6066a-127">Você também pode obter ou definir metadados sobre um dispositivo chamando [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) ou [**IWMDMDevice3:: SetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty).</span><span class="sxs-lookup"><span data-stu-id="6066a-127">You can also get or set metadata about a device by calling [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) or [**IWMDMDevice3::SetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty).</span></span> <span data-ttu-id="6066a-128">Há uma tabela separada de constantes de metadados de dispositivo listadas no final das [constantes de metadados](metadata-constants.md).</span><span class="sxs-lookup"><span data-stu-id="6066a-128">There is a separate table of device metadata constants listed at the end of [Metadata Constants](metadata-constants.md).</span></span>

<span data-ttu-id="6066a-129">Exemplos de como usar esses métodos são fornecidos na documentação de referência de cada método.</span><span class="sxs-lookup"><span data-stu-id="6066a-129">Examples of using these methods are given in each method's reference documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6066a-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6066a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6066a-131">**Criando um aplicativo de Gerenciador de Dispositivos de mídia do Windows**</span><span class="sxs-lookup"><span data-stu-id="6066a-131">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[<span data-ttu-id="6066a-132">**Obtendo e configurando metadados e atributos**</span><span class="sxs-lookup"><span data-stu-id="6066a-132">**Getting and Setting Metadata and Attributes**</span></span>](getting-and-setting-metadata-and-attributes.md)
</dt> </dl>

 

 




