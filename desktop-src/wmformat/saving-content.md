---
title: Salvar conteúdo
description: Salvar conteúdo
ms.assetid: 22f4e580-43a4-48b5-8eb3-90e1346a1093
keywords:
- SDK do Windows Media Format, salvando conteúdo
- SDK do Windows Media Format, streaming de cache rápido
- ASF (Advanced Systems Format), salvando conteúdo
- ASF (formato de sistemas avançados), salvando conteúdo
- ASF (Advanced Systems Format), streaming de cache rápido
- ASF (formato de sistemas avançados), streaming de cache rápido
- fluxos, salvando conteúdo
- Streaming de cache rápido, salvando conteúdo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6c215a81accef29f8943ed52ca24264f785d94
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103640294"
---
# <a name="saving-content"></a><span data-ttu-id="3364a-111">Salvar conteúdo</span><span class="sxs-lookup"><span data-stu-id="3364a-111">Saving Content</span></span>

<span data-ttu-id="3364a-112">Ao usar esse SDK, um aplicativo pode salvar o conteúdo baixado ou transmitido no computador local do usuário, chamando o método [**IWMReaderAdvanced2:: SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) no objeto Reader.</span><span class="sxs-lookup"><span data-stu-id="3364a-112">By using this SDK, an application can save downloaded or streamed content to the user's local computer, by calling the [**IWMReaderAdvanced2::SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) method on the reader object.</span></span> <span data-ttu-id="3364a-113">Para conteúdo transmitido, o servidor deve usar o streaming de cache rápido, que é descrito na seção [habilitando o streaming de cache rápido do cliente](enabling-fast-cache-streaming-from-the-client.md).</span><span class="sxs-lookup"><span data-stu-id="3364a-113">For streamed content, the server must be using Fast Cache streaming, which is described in the section [Enabling Fast Cache Streaming from the Client](enabling-fast-cache-streaming-from-the-client.md).</span></span> <span data-ttu-id="3364a-114">Para conteúdo transmitido, o método **SaveFileAs** cria um arquivo ASX que aponta para um arquivo ASF que contém o conteúdo salvo.</span><span class="sxs-lookup"><span data-stu-id="3364a-114">For streamed content, the **SaveFileAs** method creates an ASX file that points to an ASF file containing the saved content.</span></span> <span data-ttu-id="3364a-115">Se o objeto leitor estiver transmitindo uma lista de reprodução no servidor, cada entrada será salva como um arquivo ASF separado e o arquivo ASX apontará para cada um dos arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="3364a-115">If the reader object is streaming a server-side playlist, each entry is saved as a separate ASF file, and the ASX file points to each of the ASF files.</span></span> <span data-ttu-id="3364a-116">Para conteúdo baixado, o método **SaveFileAs** simplesmente cria um arquivo asf.</span><span class="sxs-lookup"><span data-stu-id="3364a-116">For downloaded content, the **SaveFileAs** method simply creates an ASF file.</span></span>

<span data-ttu-id="3364a-117">Para salvar o conteúdo em um arquivo local, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3364a-117">To save content to a local file, do the following:</span></span>

1.  <span data-ttu-id="3364a-118">Chame [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) com a URL.</span><span class="sxs-lookup"><span data-stu-id="3364a-118">Call [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) with the URL.</span></span> <span data-ttu-id="3364a-119">**Open** é uma chamada assíncrona e retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="3364a-119">**Open** is an asynchronous call, and returns immediately.</span></span> <span data-ttu-id="3364a-120">Aguarde a conclusão da operação, conforme descrito em [para criar um leitor e abrir um arquivo](to-create-a-reader-and-open-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="3364a-120">Wait for the operation to complete, as described in [To Create a Reader and Open a File](to-create-a-reader-and-open-a-file.md).</span></span>
2.  <span data-ttu-id="3364a-121">Consulte o objeto de leitor para a interface [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) .</span><span class="sxs-lookup"><span data-stu-id="3364a-121">Query the reader object for the [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) interface.</span></span>
3.  <span data-ttu-id="3364a-122">Verifique se o conteúdo pode ser salvo chamando o método [**IWMReaderAdvanced4:: CanSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cansavefileas) .</span><span class="sxs-lookup"><span data-stu-id="3364a-122">Check whether the content can be saved by calling the [**IWMReaderAdvanced4::CanSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cansavefileas) method.</span></span> <span data-ttu-id="3364a-123">Se o método retornar false, o conteúdo não poderá ser salvo localmente.</span><span class="sxs-lookup"><span data-stu-id="3364a-123">If the method returns False, the content cannot be saved locally.</span></span> <span data-ttu-id="3364a-124">Caso contrário, vá para a etapa 4.</span><span class="sxs-lookup"><span data-stu-id="3364a-124">Otherwise, proceed to step 4.</span></span>
4.  <span data-ttu-id="3364a-125">Chame o método [**IWMReaderAdvanced4:: IsUsingFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-isusingfastcache) para determinar se o servidor está usando o streaming de cache rápido.</span><span class="sxs-lookup"><span data-stu-id="3364a-125">Call the [**IWMReaderAdvanced4::IsUsingFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-isusingfastcache) method to determine whether the server is using Fast Cache streaming.</span></span>
5.  <span data-ttu-id="3364a-126">Chame o [**IWMReaderAdvanced2:: SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) com um nome de arquivo para o arquivo local.</span><span class="sxs-lookup"><span data-stu-id="3364a-126">Call the [**IWMReaderAdvanced2::SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) with a file name for the local file.</span></span> <span data-ttu-id="3364a-127">Se o método **IsUsingFastCache** retornou true, dê ao nome do arquivo uma extensão. asx.</span><span class="sxs-lookup"><span data-stu-id="3364a-127">If the **IsUsingFastCache** method returned True, give the file name an .asx extension.</span></span> <span data-ttu-id="3364a-128">Caso contrário, dê ao nome do arquivo uma extensão. ASF,. WMA ou. wmv.</span><span class="sxs-lookup"><span data-stu-id="3364a-128">Otherwise, give the file name an .asf, .wma, or .wmv extension.</span></span>

<span data-ttu-id="3364a-129">O aplicativo pode cancelar a operação de salvamento enquanto está em andamento, chamando o método [**IWMReaderAdvanced4:: CancelSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cancelsavefileas) .</span><span class="sxs-lookup"><span data-stu-id="3364a-129">The application can cancel the save operation while it is in progress, by calling the [**IWMReaderAdvanced4::CancelSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cancelsavefileas) method.</span></span>

<span data-ttu-id="3364a-130">O conteúdo salvo pode ser protegido com DRM, portanto, talvez não seja possível reproduzir o arquivo em outro computador.</span><span class="sxs-lookup"><span data-stu-id="3364a-130">The saved content might be protected with DRM, so it may not be possible to play the file on another computer.</span></span> <span data-ttu-id="3364a-131">Para obter mais informações sobre a proteção de conteúdo, consulte [recursos de Rights Management digital](digital-rights-management-features.md).</span><span class="sxs-lookup"><span data-stu-id="3364a-131">For more information on content protection, see [Digital Rights Management Features](digital-rights-management-features.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3364a-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3364a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3364a-133">**Interface IWMReader**</span><span class="sxs-lookup"><span data-stu-id="3364a-133">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="3364a-134">**Interface IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="3364a-134">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




