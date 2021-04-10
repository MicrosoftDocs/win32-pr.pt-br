---
title: Lendo arquivos ASF no DirectShow (SDK do Windows Media Format 11)
description: Lendo arquivos ASF no DirectShow
ms.assetid: eec2c91f-1762-4798-91d0-d68ec2160d6a
keywords:
- SDK do Windows Media Format, DirectShow
- SDK do Windows Media Format, lendo arquivos ASF
- SDK do Windows Media Format, filtro de leitor ASF do WM
- SDK do Windows Media Format, interface IMediaSeeking
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), lendo arquivos
- ASF (formato de sistemas avançados), lendo arquivos
- ASF (Advanced Systems Format), filtro de leitor ASF do WM
- ASF (formato de sistemas avançados), filtro de leitor ASF do WM
- Formato de sistema avançado (ASF), interface IMediaSeeking
- ASF (formato de sistemas avançados), interface IMediaSeeking
- DirectShow, lendo arquivos ASF
- Filtro de leitor ASF do DirectShow, WM
- DirectShow, interface IMediaSeeking
- Filtro de leitor ASF do WM
- IMediaSeeking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1ddf7ba34444f4a3b46f4413958bd26ba4bafc8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104294713"
---
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="1c033-120">Lendo arquivos ASF no DirectShow (SDK do Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="1c033-120">Reading ASF Files in DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="1c033-121">A reprodução de arquivos ASF é tratada pelo filtro de [leitor ASF do WM](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="1c033-121">Playback of ASF files is handled by the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="1c033-122">Quando o leitor ASF do WM lê um arquivo, ele cria automaticamente um PIN de saída para cada fluxo, incluindo fluxos da Web, fluxos de comando de script e qualquer outro tipo de fluxo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="1c033-122">When the WM ASF Reader reads a file, it automatically creates an output pin for each stream, including Web streams, script command streams, and any other type of arbitrary stream.</span></span> <span data-ttu-id="1c033-123">No caso de vários arquivos de taxa de bits, os Pins são criados somente para os fluxos selecionados no momento.</span><span class="sxs-lookup"><span data-stu-id="1c033-123">In the case of multiple bit rate files, pins are created only for the currently selected streams.</span></span>

<span data-ttu-id="1c033-124">O leitor ASF do WM dá suporte à interface **IMediaSeeking** do DirectShow, que permite que os aplicativos executem a busca temporal dentro do arquivo.</span><span class="sxs-lookup"><span data-stu-id="1c033-124">The WM ASF Reader supports the DirectShow **IMediaSeeking** interface, which enables applications to perform temporal seeking within the file.</span></span> <span data-ttu-id="1c033-125">No entanto, a reprodução em velocidades diferentes de 1,0 (conforme especificado em **IMediaSeeking:: SetRate**) não é suportada.</span><span class="sxs-lookup"><span data-stu-id="1c033-125">However, playback at speeds other than 1.0 (as specified in **IMediaSeeking::SetRate**) is not supported.</span></span>

<span data-ttu-id="1c033-126">O filtro também expõe várias interfaces do Windows Media Format SDK, conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1c033-126">The filter also exposes several Windows Media Format SDK interfaces as described in the following table.</span></span>



| <span data-ttu-id="1c033-127">Interface</span><span class="sxs-lookup"><span data-stu-id="1c033-127">Interface</span></span>                                        | <span data-ttu-id="1c033-128">Quão expostos</span><span class="sxs-lookup"><span data-stu-id="1c033-128">How exposed</span></span>                            | <span data-ttu-id="1c033-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c033-129">Comments</span></span>                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c033-130">**IWMDRMReader**</span><span class="sxs-lookup"><span data-stu-id="1c033-130">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | <span data-ttu-id="1c033-131">Por meio de **IServiceProvider** no filtro</span><span class="sxs-lookup"><span data-stu-id="1c033-131">Through **IServiceProvider** on filter</span></span> | <span data-ttu-id="1c033-132">Fornecido para aplicativos que precisam executar conteúdo protegido por DRM (Rights Management digital).</span><span class="sxs-lookup"><span data-stu-id="1c033-132">Provided for applications that need to play content protected by Digital Rights Management (DRM).</span></span> <span data-ttu-id="1c033-133">Essa interface também pode ser usada para obter outras interfaces diretamente no objeto leitor.</span><span class="sxs-lookup"><span data-stu-id="1c033-133">This interface can also be used to obtain other interfaces on the Reader Object directly.</span></span> |
| [<span data-ttu-id="1c033-134">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="1c033-134">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="1c033-135">**QueryInterface** no filtro</span><span class="sxs-lookup"><span data-stu-id="1c033-135">**QueryInterface** on filter</span></span>           | <span data-ttu-id="1c033-136">Fornecido para que os aplicativos possam ler atributos de arquivo e conteúdo, bem como informações de marcador e script e metadados.</span><span class="sxs-lookup"><span data-stu-id="1c033-136">Provided so that applications can read file and content attributes, as well as marker and script information and metadata.</span></span>                                                                  |
| [<span data-ttu-id="1c033-137">**IWMReaderAdvanced**</span><span class="sxs-lookup"><span data-stu-id="1c033-137">**IWMReaderAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | <span data-ttu-id="1c033-138">**QueryInterface** no filtro</span><span class="sxs-lookup"><span data-stu-id="1c033-138">**QueryInterface** on filter</span></span>           | <span data-ttu-id="1c033-139">Parcialmente implementado no filtro para que os aplicativos possam acessar os métodos informativos no objeto do WM Reader.</span><span class="sxs-lookup"><span data-stu-id="1c033-139">Partially implemented on the filter so that applications can access the informational methods on the WM Reader object.</span></span>                                                                      |
| [<span data-ttu-id="1c033-140">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="1c033-140">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | <span data-ttu-id="1c033-141">**QueryInterface** no filtro</span><span class="sxs-lookup"><span data-stu-id="1c033-141">**QueryInterface** on filter</span></span>           | <span data-ttu-id="1c033-142">Parcialmente implementado no filtro para que os aplicativos possam acessar os métodos informativos no objeto leitor.</span><span class="sxs-lookup"><span data-stu-id="1c033-142">Partially implemented on the filter so that applications can access the informational methods on the Reader Object.</span></span>                                                                         |



 

<span data-ttu-id="1c033-143">O filtro de [leitor ASF do WM](wm-asf-reader-filter.md) foi disponibilizado primeiro no DirectShow 8,0.</span><span class="sxs-lookup"><span data-stu-id="1c033-143">The [WM ASF Reader](wm-asf-reader-filter.md) filter was first made available in DirectShow 8.0.</span></span> <span data-ttu-id="1c033-144">A versão do filtro que acompanha o DirectShow 8,1 e 9,0 dá suporte à versão 7. *x* do Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="1c033-144">The version of the filter that ships with DirectShow 8.1 and 9.0 supports version 7.*x* of the Windows Media Format SDK.</span></span> <span data-ttu-id="1c033-145">A versão mais recente do filtro, juntamente com os outros componentes do QASF, é fornecida com o e dá suporte ao SDK da série Windows Media Format 9 Series e às versões posteriores, e ele substitui o filtro no DirectX 9,0.</span><span class="sxs-lookup"><span data-stu-id="1c033-145">The most recent version of the filter, along with the other QASF components, ships with and supports the Windows Media Format 9 Series SDK, and later versions, and it supersedes the filter in DirectX 9.0.</span></span> <span data-ttu-id="1c033-146">Se você instalar o SDK do Windows Media Format depois de instalar o DirectX 8. *x* ou 9. *x* SDK, você substituirá a versão do DirectX do qasf.dll pela versão da série 9.</span><span class="sxs-lookup"><span data-stu-id="1c033-146">If you install the Windows Media Format SDK after installing the DirectX 8.*x* or 9.*x* SDK, you will overwrite the DirectX version of qasf.dll with the 9 Series version.</span></span> <span data-ttu-id="1c033-147">Isso não deve apresentar nenhum problema, exceto possivelmente em um cenário no qual resultará em um comportamento diferente no método DirectShow **IGraphBuilder:: RenderFile** .</span><span class="sxs-lookup"><span data-stu-id="1c033-147">This should not present any problems except possibly in one scenario where it will result in different behavior in the DirectShow **IGraphBuilder::RenderFile** method.</span></span> <span data-ttu-id="1c033-148">A versão do SDK do Windows Media Format 9 Series do leitor ASF do WM é o filtro de origem padrão para as extensões de nome de arquivo. ASF,. wmv e. WMA.</span><span class="sxs-lookup"><span data-stu-id="1c033-148">The Windows Media Format 9 Series SDK version of the WM ASF Reader is the default source filter for the .asf, .wmv, and .wma file name extensions.</span></span> <span data-ttu-id="1c033-149">Isso significa que o leitor ASF do WM é criado e adicionado automaticamente ao grafo de filtro pelo Gerenciador de gráficos de filtro em métodos como **IGraphBuilder:: RenderFile** ou **IGraphBuilder:: AddSourceFilter** quando um arquivo desse tipo é especificado.</span><span class="sxs-lookup"><span data-stu-id="1c033-149">This means that the WM ASF Reader is automatically created and added to the filter graph by the Filter Graph Manager in methods such as **IGraphBuilder::RenderFile** or **IGraphBuilder::AddSourceFilter** when a file of this type is specified.</span></span> <span data-ttu-id="1c033-150">No DirectX 9,0 e versões anteriores, e no Windows XP Service Pack 1 e versões anteriores, o método **RenderFile** usa o filtro de origem de mídia mais antigo do Windows.</span><span class="sxs-lookup"><span data-stu-id="1c033-150">In DirectX 9.0 and earlier, and Windows XP Service Pack 1 and earlier, the **RenderFile** method uses the older Windows Media Source Filter.</span></span> <span data-ttu-id="1c033-151">Esse comportamento foi mantido para garantir a compatibilidade com versões anteriores com aplicativos que usavam o Windows Media Player 6,4.</span><span class="sxs-lookup"><span data-stu-id="1c033-151">This behavior was maintained to ensure backward compatibility with applications that used the Windows Media Player 6.4.</span></span> <span data-ttu-id="1c033-152">Para obter mais informações sobre o filtro de origem de mídia do Windows herdado, consulte a documentação do SDK do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1c033-152">For more information about the legacy Windows Media Source Filter, see the DirectShow SDK Documentation.</span></span>

<span data-ttu-id="1c033-153">Para reproduzir um arquivo ASF com conteúdo baseado no Windows Media usando o leitor ASF do WM, as três etapas principais são criar uma instância do Gerenciador de gráfico de filtro, chamar **IGraphBuilder:: RenderFile** para criar o grafo e, em seguida, chamar **IMediaControl:: Run** para reproduzir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="1c033-153">To play an ASF file with Windows Media–based content using the WM ASF Reader, the three primary steps are to create an instance of the Filter Graph Manager, call **IGraphBuilder::RenderFile** to create the graph, and then call **IMediaControl::Run** to play the file.</span></span> <span data-ttu-id="1c033-154">O exemplo de código a seguir é um programa completo que reproduz um arquivo ASF usando o DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1c033-154">The following code example is a complete program that plays an ASF file using DirectShow.</span></span> <span data-ttu-id="1c033-155">Para executar este exemplo, você deve ter o SDK do DirectX instalado e seu ambiente de compilação deve ser configurado de acordo com as instruções no tópico de documentação do SDK do DirectShow "Configurando o ambiente de compilação".</span><span class="sxs-lookup"><span data-stu-id="1c033-155">To run this example, you must have the DirectX SDK installed and your build environment must be configured according to the instructions in the DirectShow SDK documentation topic "Setting Up the Build Environment."</span></span> <span data-ttu-id="1c033-156">Além disso, você deve especificar um arquivo em seu computador na chamada para **RenderFile**.</span><span class="sxs-lookup"><span data-stu-id="1c033-156">Also, you must specify a file on your computer in the call to **RenderFile**.</span></span>


```C++
#include <dshow.h>
#include <stdio.h>

void main(void)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEvent   *pEvent = NULL;

    // Initialize the COM library.
    HRESULT hr = CoInitialize(NULL);
    if (FAILED(hr))
    {
        printf("ERROR - Could not initialize COM library");
        return;
    }

    // Create the Filter Graph Manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file
    // on your system.
    hr = pGraph->RenderFile(L"test.wmv", NULL);
    if (SUCCEEDED(hr))
    {
        // Run the graph.
        hr = pControl->Run();
        if (SUCCEEDED(hr))
        {
            // Wait for completion.
            long evCode;
            pEvent->WaitForCompletion(INFINITE, &evCode);

            // Note: Do not use INFINITE in a real application, because it
            // can block indefinitely.
        }
    }
    pControl->Release();
    pEvent->Release();
    pGraph->Release();
    CoUninitialize();
}

```



<span data-ttu-id="1c033-157">Observe que o código do aplicativo para esse exemplo simples nunca faz referência especificamente ao leitor ASF do WM.</span><span class="sxs-lookup"><span data-stu-id="1c033-157">Note that the application code for this simple example never references the WM ASF Reader specifically.</span></span> <span data-ttu-id="1c033-158">Esse filtro é criado, conectado, executado e eventualmente liberado pelo Gerenciador de gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="1c033-158">That filter is created, connected, run, and eventually released by the Filter Graph Manager.</span></span> <span data-ttu-id="1c033-159">Em muitos cenários, no entanto, talvez você queira configurar o leitor ASF do WM antes de começar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="1c033-159">In many scenarios, however, you may want to configure the WM ASF Reader before beginning playback.</span></span>

 

 




