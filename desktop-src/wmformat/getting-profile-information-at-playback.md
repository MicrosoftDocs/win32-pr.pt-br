---
title: Obtendo informações de perfil na reprodução
description: Obtendo informações de perfil na reprodução
ms.assetid: 4ea6c063-fd53-4b5e-ac01-9e2790322ace
keywords:
- SDK do Windows Media Format, perfis
- ASF (Advanced Systems Format), perfis
- ASF (formato de sistemas avançados), perfis
- ASF (Advanced Systems Format), exclusão mútua
- ASF (formato de sistemas avançados), exclusão mútua
- ASF (Advanced Systems Format), compartilhamento de largura de banda
- ASF (formato de sistemas avançados), compartilhamento de largura de banda
- fluxos, obtendo informações de perfil na reprodução
- perfis, obtendo informações em reprodução
- exclusão mútua, obtendo informações de perfil na reprodução
- compartilhamento de largura de banda, obtendo informações de perfil em reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5c7083f7bf9e986e8a23ba2c78dfe4404942a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104084362"
---
# <a name="getting-profile-information-at-playback"></a><span data-ttu-id="54aa2-114">Obtendo informações de perfil na reprodução</span><span class="sxs-lookup"><span data-stu-id="54aa2-114">Getting Profile Information at Playback</span></span>

<span data-ttu-id="54aa2-115">As informações do perfil usado para criar um arquivo são armazenadas na seção de cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="54aa2-115">Information from the profile used to create a file is stored in the header section of the file.</span></span> <span data-ttu-id="54aa2-116">Ambos os objetos de leitura podem acessar as informações de perfil do cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="54aa2-116">Both reader objects can access the profile information from the file header.</span></span> <span data-ttu-id="54aa2-117">Há várias razões pelas quais você pode querer acessar dados de perfil do leitor.</span><span class="sxs-lookup"><span data-stu-id="54aa2-117">There are several reasons why you might want to access profile data from the reader.</span></span> <span data-ttu-id="54aa2-118">Normalmente, você precisará recuperar informações sobre fluxos, objetos de exclusão mútua e objetos de compartilhamento de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="54aa2-118">Most commonly, you will need to retrieve information about streams, mutual exclusion objects, and bandwidth sharing objects.</span></span>

<span data-ttu-id="54aa2-119">O objeto leitor assíncrono e o objeto leitor síncrono podem ser consultados para a interface [**IWMProfile**](iwmprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="54aa2-119">Both the asynchronous reader object and the synchronous reader object can be queried for the [**IWMProfile**](iwmprofile.md) interface.</span></span> <span data-ttu-id="54aa2-120">Nenhuma alteração feita nas informações do perfil pode afetar o arquivo no leitor.</span><span class="sxs-lookup"><span data-stu-id="54aa2-120">No changes made to the profile information can have any affect on the file in the reader.</span></span> <span data-ttu-id="54aa2-121">Para obter mais informações sobre como acessar informações de perfil, consulte [trabalhando com perfis](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="54aa2-121">For more information about accessing profile information, see [Working with Profiles](working-with-profiles.md).</span></span>

## <a name="stream-information"></a><span data-ttu-id="54aa2-122">Informações de fluxo</span><span class="sxs-lookup"><span data-stu-id="54aa2-122">Stream Information</span></span>

<span data-ttu-id="54aa2-123">Às vezes, é importante saber como um fluxo é configurado.</span><span class="sxs-lookup"><span data-stu-id="54aa2-123">It is sometimes important to know how a stream is configured.</span></span> <span data-ttu-id="54aa2-124">Ao recuperar propriedades de mídia de qualquer um dos objetos de leitor, você obtém as propriedades das saídas.</span><span class="sxs-lookup"><span data-stu-id="54aa2-124">When you retrieve media properties from the either of the reader objects, you get the properties of the outputs.</span></span> <span data-ttu-id="54aa2-125">As propriedades de saída descrevem como os dados descompactados de um fluxo serão entregues pelo leitor, e não como o fluxo é configurado no arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="54aa2-125">Output properties describe how the uncompressed data from a stream is going to be delivered by the reader, not how the stream is configured within the ASF file.</span></span>

<span data-ttu-id="54aa2-126">Ao receber amostras de fluxo não compactado de um objeto de leitor, você deve usar as informações de perfil para identificar o formato dos dados compactados.</span><span class="sxs-lookup"><span data-stu-id="54aa2-126">When receiving uncompressed stream samples from either reader object, you must use the profile information to identify the format of the compressed data.</span></span> <span data-ttu-id="54aa2-127">Isso é particularmente importante se você pretende gravar o fluxo compactado em outro arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="54aa2-127">This is particularly important if you are going to write the compressed stream to another ASF file.</span></span>

<span data-ttu-id="54aa2-128">Você também precisa acessar as informações de fluxo ao usar a recompactação inteligente para transcodificar um fluxo de áudio para uma taxa de bits inferior.</span><span class="sxs-lookup"><span data-stu-id="54aa2-128">You also need to access stream information when using smart recompression to transcode an audio stream to a lower bit rate.</span></span>

<span data-ttu-id="54aa2-129">Talvez você queira determinar se um fluxo foi gravado usando a codificação de taxa de bits variável (VBR).</span><span class="sxs-lookup"><span data-stu-id="54aa2-129">You may want to determine whether a stream was written using variable bit rate (VBR) encoding.</span></span> <span data-ttu-id="54aa2-130">Você não pode acessar nenhuma informação de VBR da interface **IWMProfile** de um objeto de leitor.</span><span class="sxs-lookup"><span data-stu-id="54aa2-130">You cannot access any VBR information from the **IWMProfile** interface of either reader object.</span></span> <span data-ttu-id="54aa2-131">Isso ocorre porque as informações de VBR não são armazenadas no arquivo após a codificação.</span><span class="sxs-lookup"><span data-stu-id="54aa2-131">This is because the VBR information is not stored in the file after encoding.</span></span> <span data-ttu-id="54aa2-132">Você pode determinar se um fluxo foi criado usando a codificação de VBR, obtendo um ponteiro para a interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) do objeto leitor e chamando [**IWMHeaderInfo:: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span><span class="sxs-lookup"><span data-stu-id="54aa2-132">You can determine whether a stream was created using VBR encoding by obtaining a pointer to the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface of the reader object and calling [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span></span> <span data-ttu-id="54aa2-133">Você deve especificar o número do fluxo e passar g \_ wszIsVBR como o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="54aa2-133">You must specify the stream number and pass g\_wszIsVBR as the attribute name.</span></span>

## <a name="mutual-exclusion-information"></a><span data-ttu-id="54aa2-134">Informações de exclusão mútua</span><span class="sxs-lookup"><span data-stu-id="54aa2-134">Mutual Exclusion Information</span></span>

<span data-ttu-id="54aa2-135">Se você quiser criar um aplicativo de leitura que usa a exclusão mútua, você desejará acessar as informações sobre todos os objetos de exclusão mútua incluídos no perfil.</span><span class="sxs-lookup"><span data-stu-id="54aa2-135">If you want to create a reading application that uses mutual exclusion, you will want to access the information about any mutual exclusion objects included in the profile.</span></span> <span data-ttu-id="54aa2-136">Para todos os tipos de exclusão mútua, exceto a taxa de bits, o aplicativo de leitura é responsável por qualquer alternância de fluxo que seja necessária.</span><span class="sxs-lookup"><span data-stu-id="54aa2-136">For all mutual exclusion types except bit rate, the reading application is responsible for any stream switching that is required.</span></span> <span data-ttu-id="54aa2-137">Para alternar fluxos, você precisa saber quais fluxos são.</span><span class="sxs-lookup"><span data-stu-id="54aa2-137">To switch streams, you need to know which streams are which.</span></span>

## <a name="bandwidth-sharing-information"></a><span data-ttu-id="54aa2-138">Informações de compartilhamento de largura de banda</span><span class="sxs-lookup"><span data-stu-id="54aa2-138">Bandwidth Sharing Information</span></span>

<span data-ttu-id="54aa2-139">Os objetos de compartilhamento de largura de banda que são incluídos em um perfil são incluídos apenas para fins informativos.</span><span class="sxs-lookup"><span data-stu-id="54aa2-139">Bandwidth sharing objects that are included in a profile are included only for informational purposes.</span></span> <span data-ttu-id="54aa2-140">Nem o objeto Writer nem qualquer um dos objetos de leitor executa nenhuma ação como resultado de dados de compartilhamento de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="54aa2-140">Neither the writer object nor either of the reader objects takes any action as a result of bandwidth sharing data.</span></span> <span data-ttu-id="54aa2-141">Se você quiser usar o compartilhamento de largura de banda em seu aplicativo de leitura, deverá acessar as informações de compartilhamento de largura de banda dos dados de perfil.</span><span class="sxs-lookup"><span data-stu-id="54aa2-141">If you want to use bandwidth sharing in your reading application, you must access the bandwidth sharing information from the profile data.</span></span>

> [!Note]  
> <span data-ttu-id="54aa2-142">Nem todas as informações do perfil usado para criar um arquivo estão presentes no cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="54aa2-142">Not all of the information from the profile used to create a file is present in the file header.</span></span> <span data-ttu-id="54aa2-143">Como regra geral, os dados que são usados somente no momento da codificação não são persistidos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="54aa2-143">As a general rule, data that is used only at the time of encoding is not persisted in the file.</span></span> <span data-ttu-id="54aa2-144">Isso inclui configurações de entrada que foram definidas usando o método [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) , bem como propriedades definidas usando o método [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="54aa2-144">This includes input settings that were set using the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) method, as well as properties set using the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="54aa2-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="54aa2-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54aa2-146">**Interface IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="54aa2-146">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="54aa2-147">**Lendo arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="54aa2-147">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




