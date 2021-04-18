---
title: Gravar playlists que contêm arquivos seguros
description: Gravar playlists que contêm arquivos seguros
ms.assetid: 0d9415a1-a154-4fe4-af4c-cce4cb05ade5
keywords:
- Windows Media Format SDK, gravando listas de reprodução com arquivos seguros
- SDK do Windows Media Format, playlists com arquivos seguros
- ASF (Advanced Systems Format), gravando listas de reprodução com arquivos seguros
- ASF (formato de sistemas avançados), gravando listas de reprodução com arquivos seguros
- Formato de sistema avançado (ASF), listas de reprodução com arquivos seguros
- ASF (formato de sistemas avançados), listas de reprodução com arquivos seguros
- DRM (gerenciamento de direitos digitais), gravando listas de reprodução com arquivos seguros
- DRM (gerenciamento de direitos digitais), gravação de listas de reprodução com arquivos seguros
- DRM (gerenciamento de direitos digitais), listas de reprodução com arquivos seguros
- DRM (gerenciamento de direitos digitais), listas de reprodução com arquivos seguros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214c1dbd4ee08f90b3e5e8aa6186508af5044f29
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "105787679"
---
# <a name="burning-playlists-that-contain-secure-files"></a><span data-ttu-id="0fd2e-113">Gravar playlists que contêm arquivos seguros</span><span class="sxs-lookup"><span data-stu-id="0fd2e-113">Burning Playlists That Contain Secure Files</span></span>

<span data-ttu-id="0fd2e-114">As licenças criadas usando os objetos do SDK do Windows Media Rights Manager 10 podem especificar o direito de copiar um arquivo para um CD como parte de uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-114">Licenses created by using the objects of the Windows Media Rights Manager 10 SDK can specify the right to copy a file to compact disc as part of a playlist.</span></span> <span data-ttu-id="0fd2e-115">Esse recurso, chamado de gravação de playlist, requer que você verifique as licenças de todos os arquivos na lista de reprodução antes de começar a copiar os dados.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-115">This feature, called playlist burning, requires that you verify the licenses of all of the files in the playlist before starting to copy data.</span></span> <span data-ttu-id="0fd2e-116">O Windows Media Format SDK fornece a interface [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) para executar a verificação de arquivos para você.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-116">The Windows Media Format SDK provides the [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) interface to perform file verification for you.</span></span>

<span data-ttu-id="0fd2e-117">Para implementar a gravação da lista de reprodução, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="0fd2e-117">To implement playlist burning, perform the following steps:</span></span>

1.  <span data-ttu-id="0fd2e-118">Crie uma instância do objeto leitor ou o objeto leitor síncrono.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-118">Create an instance of the reader object, or the synchronous reader object.</span></span> <span data-ttu-id="0fd2e-119">Para obter mais informações, consulte [lendo arquivos ASF](reading-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="0fd2e-119">For more information, see [Reading ASF Files](reading-asf-files.md).</span></span>
2.  <span data-ttu-id="0fd2e-120">Chame o método **QueryInterface** da interface do leitor ([**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) ou [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)) para obter um ponteiro para a interface [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) .</span><span class="sxs-lookup"><span data-stu-id="0fd2e-120">Call the **QueryInterface** method of the reader interface ([**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) or [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)) to obtain a pointer to the [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) interface.</span></span>
3.  <span data-ttu-id="0fd2e-121">Copie os nomes de arquivo da lista de reprodução em uma matriz de cadeias de caracteres largos.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-121">Copy the file names from the playlist into an array of wide-character strings.</span></span> <span data-ttu-id="0fd2e-122">Os nomes de arquivo na matriz devem estar na mesma ordem em que aparecem na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-122">The file names in the array must be in the same order as they appear in the playlist.</span></span>
4.  <span data-ttu-id="0fd2e-123">Chame o método [**IWMReaderPlaylistBurn:: InitPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) , passando um ponteiro para a matriz criada na etapa 3, para inicializar a verificação de licença para os arquivos.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-123">Call the [**IWMReaderPlaylistBurn::InitPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) method, passing in a pointer to the array created in step 3, to initialize the license verification for the files.</span></span>
5.  <span data-ttu-id="0fd2e-124">Quando a verificação de licença é concluída, o objeto leitor envia uma \_ \_ mensagem de \_ gravação de WMT init para a implementação do método de retorno de chamada [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) .</span><span class="sxs-lookup"><span data-stu-id="0fd2e-124">When the license verification is completed, the reader object sends a WMT\_INIT\_PLAYLIST\_BURN message to your implementation of the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method.</span></span> <span data-ttu-id="0fd2e-125">Quando o retorno de chamada receber essa mensagem, chame o método [**IWMReaderPlaylistBurn:: GetInitResults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) para obter os resultados da verificação de licença.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-125">When your callback receives this message, call the [**IWMReaderPlaylistBurn::GetInitResults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) method to get the results of the license check.</span></span> <span data-ttu-id="0fd2e-126">Esse método usa uma matriz de variáveis **HRESULT** que correspondem aos nomes de arquivo na matriz passada para **InitPlaylistBurn**.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-126">This method takes an array of **HRESULT** variables that correspond to the file names in the array passed to **InitPlaylistBurn**.</span></span> <span data-ttu-id="0fd2e-127">Se todos os valores na matriz de resultados forem iguais a S \_ OK, você poderá continuar.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-127">If all of the values in the result array are equal to S\_OK, you can continue.</span></span> <span data-ttu-id="0fd2e-128">Se qualquer resultado for um código de erro, a lista de reprodução não deverá ser copiada.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-128">If any result is an error code, the playlist must not be copied.</span></span>
6.  <span data-ttu-id="0fd2e-129">Usando a mesma instância do leitor, abra e Leia cada arquivo.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-129">Using the same instance of the reader, open and read each file.</span></span> <span data-ttu-id="0fd2e-130">Você deve abrir os arquivos na ordem em que os nomes de arquivo exibidos na matriz de nome de arquivo passado para **InitPlaylistBurn**.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-130">You must open the files in the order in which the file names appeared in the file name array passed to **InitPlaylistBurn**.</span></span>
7.  <span data-ttu-id="0fd2e-131">Quando você copiou todos os arquivos na lista de reprodução, chame o [**IWMReaderPlaylistBurn:: EndPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) para concluir o processo de gravação da playlist e libere os recursos usados pelo leitor.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-131">When you have copied all of the files in the playlist, call the [**IWMReaderPlaylistBurn::EndPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) to complete the playlist burn process and free the resources used by the reader.</span></span>

> [!Note]  
> <span data-ttu-id="0fd2e-132">O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="0fd2e-132">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0fd2e-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0fd2e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fd2e-134">**Habilitando o suporte a DRM**</span><span class="sxs-lookup"><span data-stu-id="0fd2e-134">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




