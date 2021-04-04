---
title: Usando marcadores
description: Usando marcadores
ms.assetid: b801c985-4ec7-441e-9f8a-40c69b1299a9
keywords:
- Windows Media Format SDK, marcadores
- ASF (Advanced Systems Format), marcadores
- ASF (formato de sistemas avançados), marcadores
- ASF (Advanced Systems Format), buscando marcadores
- ASF (formato de sistemas avançados), buscando marcadores
- marcadores, sobre
- marcadores, adicionando
- marcadores, removendo
- marcadores, recuperando
- marcadores, buscando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44cc585b8c71e3bfbae85953650809ad031d36a2
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103640302"
---
# <a name="using-markers"></a><span data-ttu-id="f8b4d-113">Usando marcadores</span><span class="sxs-lookup"><span data-stu-id="f8b4d-113">Using Markers</span></span>

<span data-ttu-id="f8b4d-114">Um *marcador* é um ponto nomeado em um arquivo asf.</span><span class="sxs-lookup"><span data-stu-id="f8b4d-114">A *marker* is a named point within an ASF file.</span></span> <span data-ttu-id="f8b4d-115">Cada marcador consiste em um nome e uma hora associada, medido como um deslocamento do início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f8b4d-115">Each marker consists of a name and an associated time, measured as an offset from the start of the file.</span></span> <span data-ttu-id="f8b4d-116">Um aplicativo pode usar marcadores para atribuir nomes a vários pontos dentro do conteúdo, exibir esses nomes para o usuário e, em seguida, buscar as posições do marcador.</span><span class="sxs-lookup"><span data-stu-id="f8b4d-116">An application can use markers to assign names to various points within the content, display those names to the user, and then seek to the marker positions.</span></span> <span data-ttu-id="f8b4d-117">Um aplicativo pode adicionar ou remover marcadores de um arquivo ASF existente.</span><span class="sxs-lookup"><span data-stu-id="f8b4d-117">An application can add or remove markers from an existing ASF file.</span></span>

<span data-ttu-id="f8b4d-118">A interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) contém métodos para trabalhar com marcadores.</span><span class="sxs-lookup"><span data-stu-id="f8b4d-118">The [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface contains methods for working with markers.</span></span> <span data-ttu-id="f8b4d-119">O objeto editor de metadados dá suporte à adição e remoção de marcadores.</span><span class="sxs-lookup"><span data-stu-id="f8b4d-119">The metadata editor object supports adding and removing markers.</span></span> <span data-ttu-id="f8b4d-120">Os objetos gravador e leitor podem recuperar marcadores, mas não podem adicionar ou remover marcadores.</span><span class="sxs-lookup"><span data-stu-id="f8b4d-120">The writer and reader objects can retrieve markers but cannot add or remove markers.</span></span>

## <a name="adding-markers"></a><span data-ttu-id="f8b4d-121">Adicionando marcadores</span><span class="sxs-lookup"><span data-stu-id="f8b4d-121">Adding Markers</span></span>

<span data-ttu-id="f8b4d-122">Para adicionar um marcador, consulte o editor de metadados para a interface **IWMHeaderInfo** .</span><span class="sxs-lookup"><span data-stu-id="f8b4d-122">To add a marker, query the metadata editor for the **IWMHeaderInfo** interface.</span></span> <span data-ttu-id="f8b4d-123">Em seguida, chame o método [**IWMHeaderInfo:: Addmarkr**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker) , especificando o nome do marcador como uma cadeia de caracteres largos e a hora em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="f8b4d-123">Then call the [**IWMHeaderInfo::AddMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker) method, specifying the marker name as a wide-character string and the time in 100-nanosecond units.</span></span> <span data-ttu-id="f8b4d-124">A hora não deve exceder a duração do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f8b4d-124">The time must not exceed the file duration.</span></span> <span data-ttu-id="f8b4d-125">Dois marcadores podem ter a mesma hora.</span><span class="sxs-lookup"><span data-stu-id="f8b4d-125">Two markers can have the same time.</span></span>

<span data-ttu-id="f8b4d-126">O exemplo a seguir adiciona vários marcadores a um arquivo:</span><span class="sxs-lookup"><span data-stu-id="f8b4d-126">The following example adds several markers to a file:</span></span>


```C++
IWMMetadataEditor *pEdit = 0;
IWMHeaderInfo     *pInfo = 0;

// Create the metadata editor object.

WMCreateEditor(&pEdit);
pEdit->Open(L"C:\\example.wmv");
pEdit->QueryInterface(IID_IWMHeaderInfo, (void**)&pInfo);

// Add the markers. Note that we add the last ones first. Do this when possible
// for improved performance when writing the markers to the file.
hr = pInfo->AddMarker(L"End",  520000000);   // 52 sec.
hr = pInfo->AddMarker(L"Segue",  350000000); // 35 sec.
hr = pInfo->AddMarker(L"Intro",  15000000);  // 1.5 sec.

// Commit changes and clean up.

pEdit->Flush();
pEdit->Close(); 
pInfo->Release();
pEdit->Release();

```



## <a name="removing-markers"></a><span data-ttu-id="f8b4d-127">Removendo marcadores</span><span class="sxs-lookup"><span data-stu-id="f8b4d-127">Removing Markers</span></span>

<span data-ttu-id="f8b4d-128">Para remover um marcador, chame [**IWMHeaderInfo:: RemoveMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker), especificando o índice do marcador a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f8b4d-128">To remove a marker, call [**IWMHeaderInfo::RemoveMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker), specifying the index of the marker to remove.</span></span> <span data-ttu-id="f8b4d-129">Os marcadores são automaticamente classificados em ordem de tempo crescente, portanto, o índice 0 é sempre o primeiro marcador.</span><span class="sxs-lookup"><span data-stu-id="f8b4d-129">Markers are automatically sorted in increasing time order, so index 0 is always the first marker.</span></span> <span data-ttu-id="f8b4d-130">Observe que a chamada de **RemoveMarker** altera os números de índice dos marcadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f8b4d-130">Note that calling **RemoveMarker** changes the index numbers of any markers that follow.</span></span> <span data-ttu-id="f8b4d-131">O código a seguir, em que *pInfo* é um ponteiro para uma interface **IWMHeaderInfo** , remove todos os marcadores de um arquivo:</span><span class="sxs-lookup"><span data-stu-id="f8b4d-131">The following code, where *pInfo* is a pointer to an **IWMHeaderInfo** interface, removes all the markers from a file:</span></span>


```C++
WORD count = 0;
pInfo->GetMarkerCount(&count);
while (count--)
{
    pInfo->RemoveMarker(0);
}

```



## <a name="retrieving-markers"></a><span data-ttu-id="f8b4d-132">Recuperando marcadores</span><span class="sxs-lookup"><span data-stu-id="f8b4d-132">Retrieving Markers</span></span>

<span data-ttu-id="f8b4d-133">Para recuperar o nome e a hora de um marcador, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="f8b4d-133">To retrieve the name and time of a marker, perform the following steps:</span></span>

1.  <span data-ttu-id="f8b4d-134">Chame o método [**IWMHeaderInfo:: GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount) para determinar quantos marcadores o arquivo contém.</span><span class="sxs-lookup"><span data-stu-id="f8b4d-134">Call the [**IWMHeaderInfo::GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount) method to determine how many markers the file contains.</span></span>
2.  <span data-ttu-id="f8b4d-135">Recupere o tamanho da cadeia de caracteres necessária para conter o nome do marcador.</span><span class="sxs-lookup"><span data-stu-id="f8b4d-135">Retrieve the size of the string needed to contain the marker name.</span></span> <span data-ttu-id="f8b4d-136">Para fazer isso, chame o método [**IWMHeaderInfo:: Getmarcer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) .</span><span class="sxs-lookup"><span data-stu-id="f8b4d-136">To do so, call the [**IWMHeaderInfo::GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) method.</span></span> <span data-ttu-id="f8b4d-137">Especifique o índice do marcador a ser recuperado e **NULL** para o buffer da cadeia de caracteres (o parâmetro *pwszMarkerName* ).</span><span class="sxs-lookup"><span data-stu-id="f8b4d-137">Specify the index of the marker to retrieve, and **NULL** for the string buffer (the *pwszMarkerName* parameter).</span></span> <span data-ttu-id="f8b4d-138">O método retorna o comprimento da cadeia de caracteres, incluindo o caractere de terminação ' \\ 0 ', no parâmetro *pcchMarkerNameLen* .</span><span class="sxs-lookup"><span data-stu-id="f8b4d-138">The method returns the length of the string, including the terminating '\\0' character, in the *pcchMarkerNameLen* parameter.</span></span>
3.  <span data-ttu-id="f8b4d-139">Aloque uma cadeia de caracteres largos para receber o nome.</span><span class="sxs-lookup"><span data-stu-id="f8b4d-139">Allocate a wide-character string to receive the name.</span></span>
4.  <span data-ttu-id="f8b4d-140">Chame **Getmarcer** novamente, mas desta vez passe o endereço da cadeia de caracteres no parâmetro *pwszMarkerName* .</span><span class="sxs-lookup"><span data-stu-id="f8b4d-140">Call **GetMarker** again, but this time pass the address of the string in the *pwszMarkerName* parameter.</span></span> <span data-ttu-id="f8b4d-141">O método grava o nome do marcador na cadeia de caracteres e retorna a hora do marcador no parâmetro *pcnsMarkerTime* .</span><span class="sxs-lookup"><span data-stu-id="f8b4d-141">The method writes the marker name into the string, and returns the marker time in the *pcnsMarkerTime* parameter.</span></span>

<span data-ttu-id="f8b4d-142">O código a seguir percorre cada marcador em ordem e recupera o nome e a hora:</span><span class="sxs-lookup"><span data-stu-id="f8b4d-142">The following code loops through every marker in order and retrieves the name and time:</span></span>


```C++
WORD cMarkers = 0;
HRESULT hr = pInfo->GetMarkerCount(&cMarkers);

WCHAR *wszName = 0;
WORD  len = 0;
for (WORD iMarker = 0; iMarker < cMarkers; ++iMarker)
{
    QWORD rtTime = 0;
    WORD req_len = 0;
    hr = pInfo->GetMarker(iMarker, 0, &req_len, &rtTime);
    
    // Reallocate if necessary.
    if (len < req_len)
    {
        delete[] wszName;
        wszName = new WCHAR[req_len];
        len = req_len;
    }
    hr = pInfo->GetMarker(iMarker, wszName, &req_len, &rtTime);
    // Display the name...
}
delete[] wszName;

```



## <a name="seeking-to-a-marker"></a><span data-ttu-id="f8b4d-143">Buscando um marcador</span><span class="sxs-lookup"><span data-stu-id="f8b4d-143">Seeking to a Marker</span></span>

<span data-ttu-id="f8b4d-144">Para iniciar a reprodução de um local de marcador, chame o método [**IWMReaderAdvanced2:: StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker) do objeto Reader, especificando o índice do marcador.</span><span class="sxs-lookup"><span data-stu-id="f8b4d-144">To start playback from a marker location, call the reader object's [**IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker) method, specifying the index of the marker.</span></span> <span data-ttu-id="f8b4d-145">Os parâmetros restantes são idênticos aos do método [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) .</span><span class="sxs-lookup"><span data-stu-id="f8b4d-145">The remaining parameters are identical to those for the [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) method.</span></span> <span data-ttu-id="f8b4d-146">O exemplo a seguir consulta o leitor para a interface [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) e busca o primeiro marcador.</span><span class="sxs-lookup"><span data-stu-id="f8b4d-146">The following example queries the reader for the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface and seeks to the first marker.</span></span>


```C++
IWMReaderAdvanced2 *pReader2 = 0
WORD iMarkerIndex = 0;
hr = pReader->QueryInterface(IID_IWMReaderAdvanced2, (void**)&pReader2);
if (SUCCEEDED(hr))
{
    hr = pPlayer2->StartAtMarker(iMarkerIndex, 0, 1.0, 0);
    pPlayer2->Release();
}

```



## <a name="related-topics"></a><span data-ttu-id="f8b4d-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f8b4d-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8b4d-148">**Interface IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="f8b4d-148">**IWMHeaderInfo Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[<span data-ttu-id="f8b4d-149">**IWMReaderAdvanced2::StartAtMarker**</span><span class="sxs-lookup"><span data-stu-id="f8b4d-149">**IWMReaderAdvanced2::StartAtMarker**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker)
</dt> <dt>

[<span data-ttu-id="f8b4d-150">**Trabalhando com metadados**</span><span class="sxs-lookup"><span data-stu-id="f8b4d-150">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




