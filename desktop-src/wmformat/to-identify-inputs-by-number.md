---
title: Para identificar entradas por número
description: Para identificar entradas por número
ms.assetid: f468f74d-7eed-4819-957d-241903f44d2d
keywords:
- ASF (Advanced Systems Format), identificando entradas por número
- ASF (formato de sistemas avançados), identificando entradas por número
- perfis, identificando entradas por número
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0629776eaaff4252a690c0e31cd6002f5de42b31
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007101"
---
# <a name="to-identify-inputs-by-number"></a><span data-ttu-id="18b77-106">Para identificar entradas por número</span><span class="sxs-lookup"><span data-stu-id="18b77-106">To Identify Inputs By Number</span></span>

<span data-ttu-id="18b77-107">Cada exemplo que você passa para o gravador deve estar associado a um número de entrada.</span><span class="sxs-lookup"><span data-stu-id="18b77-107">Every sample you pass to the writer must be associated with an input number.</span></span> <span data-ttu-id="18b77-108">Cada número de entrada corresponde a um ou mais fluxos no perfil que o gravador está usando para gravar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="18b77-108">Each input number corresponds to one or more streams in the profile that the writer is using to write the file.</span></span> <span data-ttu-id="18b77-109">Em um perfil, as fontes de mídia são identificadas por um nome de conexão.</span><span class="sxs-lookup"><span data-stu-id="18b77-109">In a profile, media sources are identified by a connection name.</span></span> <span data-ttu-id="18b77-110">O gravador associa um número de entrada a cada nome de conexão quando você define o perfil para o gravador.</span><span class="sxs-lookup"><span data-stu-id="18b77-110">The writer associates an input number with each connection name when you set the profile for the writer.</span></span> <span data-ttu-id="18b77-111">Antes de poder passar amostras para o gravador, você deve determinar quais dados cada entrada está esperando.</span><span class="sxs-lookup"><span data-stu-id="18b77-111">Before you can pass samples to the writer, you must determine what data each input is expecting.</span></span> <span data-ttu-id="18b77-112">Você não pode pressupor que as entradas estarão na mesma ordem que os fluxos em um perfil, mesmo que esse geralmente seja o caso.</span><span class="sxs-lookup"><span data-stu-id="18b77-112">You cannot assume that the inputs will be in the same order as the streams in a profile, even if this is often the case.</span></span> <span data-ttu-id="18b77-113">Portanto, a única maneira confiável de corresponder entradas com fluxos é comparar o nome de conexão da entrada com o nome da conexão do fluxo.</span><span class="sxs-lookup"><span data-stu-id="18b77-113">Therefore, the only reliable way to match inputs with streams is to compare the connection name of the input with the connection name of the stream.</span></span>

<span data-ttu-id="18b77-114">Para identificar os nomes de conexão e os números de entrada correspondentes para um perfil carregado, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="18b77-114">To identify the connection names and corresponding input numbers for a loaded profile, perform the following steps:</span></span>

1.  <span data-ttu-id="18b77-115">Crie um objeto do gravador e defina um perfil a ser usado.</span><span class="sxs-lookup"><span data-stu-id="18b77-115">Create a writer object and set a profile to use.</span></span> <span data-ttu-id="18b77-116">Para obter mais informações sobre como configurar perfis no gravador, consulte [para usar perfis com o gravador](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="18b77-116">For more information about setting profiles in the writer, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span> <span data-ttu-id="18b77-117">Você deve saber os nomes de conexão usados para os fluxos no perfil.</span><span class="sxs-lookup"><span data-stu-id="18b77-117">You should know the connection names used for the streams in the profile.</span></span> <span data-ttu-id="18b77-118">Você pode obter o nome da conexão de dentro do perfil obtendo o objeto de configuração de fluxo para cada fluxo e chamando [**IWMStreamConfig:: GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname).</span><span class="sxs-lookup"><span data-stu-id="18b77-118">You can get the connection name from within the profile by getting the stream configuration object for each stream and calling [**IWMStreamConfig::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname).</span></span> <span data-ttu-id="18b77-119">Para obter mais informações sobre perfis e objetos de configuração de fluxo, consulte [trabalhando com perfis](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="18b77-119">For more information about profiles and stream configuration objects, see [Working with Profiles](working-with-profiles.md).</span></span>
2.  <span data-ttu-id="18b77-120">Recupere o número total de entradas chamando [**IWMWriter:: GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount).</span><span class="sxs-lookup"><span data-stu-id="18b77-120">Retrieve the total number of inputs by calling [**IWMWriter::GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount).</span></span>
3.  <span data-ttu-id="18b77-121">Execute o loop por todas as entradas, executando as etapas a seguir para cada uma.</span><span class="sxs-lookup"><span data-stu-id="18b77-121">Loop through all of the inputs, performing the following steps for each.</span></span>
    -   <span data-ttu-id="18b77-122">Recupere a interface [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) para a entrada chamando [**IWMWriter:: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span><span class="sxs-lookup"><span data-stu-id="18b77-122">Retrieve the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface for the input by calling [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span></span>
    -   <span data-ttu-id="18b77-123">Recupere o nome da conexão que corresponde ao número de entrada chamando [**IWMInputMediaProps:: GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname).</span><span class="sxs-lookup"><span data-stu-id="18b77-123">Retrieve the connection name that corresponds to the input number by calling [**IWMInputMediaProps::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname).</span></span> <span data-ttu-id="18b77-124">Depois de ter o nome da conexão, você sabe os fluxos associados aos números de entrada atribuídos pelo gravador.</span><span class="sxs-lookup"><span data-stu-id="18b77-124">After you have the connection name, you know the streams that are associated with the input numbers assigned by the writer.</span></span>

<span data-ttu-id="18b77-125">O código de exemplo a seguir exibe o nome da conexão para cada entrada.</span><span class="sxs-lookup"><span data-stu-id="18b77-125">The following example code displays the connection name for each input.</span></span> <span data-ttu-id="18b77-126">Para obter mais informações sobre como usar esse código, consulte [usando os exemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="18b77-126">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT GetNamesForInputs(IWMWriter* pWriter)
{
    DWORD    cInputs  = 0;
    HRESULT  hr       = S_OK;
    WCHAR*   pwszName = NULL;
    WORD     cchName  = 0;

    IWMInputMediaProps* pProps = NULL;

    // Get the total number of inputs for the file.
    hr = pWriter->GetInputCount(&cInputs);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all supported inputs.
    for (DWORD inputIndex = 0; inputIndex < cInputs; inputIndex++)
    {
        // Get the input properties for the input.
        hr = pWriter->GetInputProps(inputIndex, &pProps);  
        GOTO_EXIT_IF_FAILED(hr);

        // Get the size of the connection name.
        hr = pProps->GetConnectionName(0, &cchName);
        GOTO_EXIT_IF_FAILED(hr);

        if (cchName > 0)
        {
            // Allocate memory for the connection name.
            pwszName = new WCHAR[cchName];
            if (wszName == NULL)
            {
                hr = E_OUTOFMEMORY;
                goto Exit;
            }

            // Get the connection name.
            hr = pProps->GetConnectionName(pwszName, &cchName);
            GOTO_EXIT_IF_FAILED(hr);
            
            // Display the name.
            printf("Input # %d = %S\n", pwszName);
        } // end if

        // Clean up for next iteration.
        SAFE_ARRAY_DELETE(pwszName);
        SAFE_RELEASE(pProps);
    } // end for inputIndex

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_RELEASE(pProps);
    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="18b77-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="18b77-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18b77-128">**Interface IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="18b77-128">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="18b77-129">**Gravando arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="18b77-129">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




