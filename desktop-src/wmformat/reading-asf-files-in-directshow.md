---
title: Lendo arquivos ASF no DirectShow (SDK Windows Media Format 11)
description: A reprodução de arquivos ASF é manipulada pelo filtro Leitor do WM ASF. Saiba mais sobre como ler arquivos ASF no DirectShow no SDK Windows Media Format 11.
ms.assetid: eec2c91f-1762-4798-91d0-d68ec2160d6a
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, lendo arquivos ASF
- Windows Media Format SDK, filtro leitor do WM ASF
- Windows Media Format SDK, interface IMediaSeeking
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), lendo arquivos
- ASF (Formato de Sistemas Avançados), lendo arquivos
- AsF (Advanced Systems Format), wm asf reader filter
- ASF (Formato de Sistemas Avançados),Filtro de Leitor do WM ASF
- AsF (Advanced Systems Format), interface IMediaSeeking
- ASF (formato de sistemas avançados), interface IMediaSeeking
- DirectShow, lendo arquivos ASF
- DirectShow, filtro leitor do WM ASF
- DirectShow, interface IMediaSeeking
- Filtro leitor do WM ASF
- Imediaseeking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aaab64798011eb21edbe43f49438db99d0bae6b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404319"
---
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="909e9-121">Lendo arquivos ASF no DirectShow (SDK Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="909e9-121">Reading ASF Files in DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="909e9-122">A reprodução de arquivos ASF é manipulada pelo filtro [Leitor do WM ASF.](wm-asf-reader-filter.md)</span><span class="sxs-lookup"><span data-stu-id="909e9-122">Playback of ASF files is handled by the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="909e9-123">Quando o Leitor do WM ASF lê um arquivo, ele cria automaticamente um pino de saída para cada fluxo, incluindo fluxos da Web, fluxos de comando de script e qualquer outro tipo de fluxo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="909e9-123">When the WM ASF Reader reads a file, it automatically creates an output pin for each stream, including Web streams, script command streams, and any other type of arbitrary stream.</span></span> <span data-ttu-id="909e9-124">No caso de vários arquivos de taxa de bits, os pinos são criados somente para os fluxos selecionados no momento.</span><span class="sxs-lookup"><span data-stu-id="909e9-124">In the case of multiple bit rate files, pins are created only for the currently selected streams.</span></span>

<span data-ttu-id="909e9-125">O Leitor do WM ASF dá suporte à interface **DirectShow IMediaSeeking,** que permite que os aplicativos executem a busca temporal dentro do arquivo.</span><span class="sxs-lookup"><span data-stu-id="909e9-125">The WM ASF Reader supports the DirectShow **IMediaSeeking** interface, which enables applications to perform temporal seeking within the file.</span></span> <span data-ttu-id="909e9-126">No entanto, não há suporte para a reprodução em velocidades que não 1.0 (conforme especificado em **IMediaSeeking::SetRate).**</span><span class="sxs-lookup"><span data-stu-id="909e9-126">However, playback at speeds other than 1.0 (as specified in **IMediaSeeking::SetRate**) is not supported.</span></span>

<span data-ttu-id="909e9-127">O filtro também expõe várias interfaces Windows Media Format SDK, conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="909e9-127">The filter also exposes several Windows Media Format SDK interfaces as described in the following table.</span></span>



| <span data-ttu-id="909e9-128">Interface</span><span class="sxs-lookup"><span data-stu-id="909e9-128">Interface</span></span>                                        | <span data-ttu-id="909e9-129">Como exposto</span><span class="sxs-lookup"><span data-stu-id="909e9-129">How exposed</span></span>                            | <span data-ttu-id="909e9-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="909e9-130">Comments</span></span>                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="909e9-131">**IWMDRMReader**</span><span class="sxs-lookup"><span data-stu-id="909e9-131">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | <span data-ttu-id="909e9-132">Por **meio de IServiceProvider** no filtro</span><span class="sxs-lookup"><span data-stu-id="909e9-132">Through **IServiceProvider** on filter</span></span> | <span data-ttu-id="909e9-133">Fornecido para aplicativos que precisam reproduzir conteúdo protegido por DRM (Rights Management Digital).</span><span class="sxs-lookup"><span data-stu-id="909e9-133">Provided for applications that need to play content protected by Digital Rights Management (DRM).</span></span> <span data-ttu-id="909e9-134">Essa interface também pode ser usada para obter outras interfaces diretamente no Objeto de Leitor.</span><span class="sxs-lookup"><span data-stu-id="909e9-134">This interface can also be used to obtain other interfaces on the Reader Object directly.</span></span> |
| [<span data-ttu-id="909e9-135">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="909e9-135">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="909e9-136">**QueryInterface** no filtro</span><span class="sxs-lookup"><span data-stu-id="909e9-136">**QueryInterface** on filter</span></span>           | <span data-ttu-id="909e9-137">Fornecido para que os aplicativos possam ler atributos de arquivo e conteúdo, bem como informações de marcador e script e metadados.</span><span class="sxs-lookup"><span data-stu-id="909e9-137">Provided so that applications can read file and content attributes, as well as marker and script information and metadata.</span></span>                                                                  |
| [<span data-ttu-id="909e9-138">**IWMReaderAdvanced**</span><span class="sxs-lookup"><span data-stu-id="909e9-138">**IWMReaderAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | <span data-ttu-id="909e9-139">**QueryInterface** no filtro</span><span class="sxs-lookup"><span data-stu-id="909e9-139">**QueryInterface** on filter</span></span>           | <span data-ttu-id="909e9-140">Parcialmente implementado no filtro para que os aplicativos possam acessar os métodos informacionais no objeto Leitor de WM.</span><span class="sxs-lookup"><span data-stu-id="909e9-140">Partially implemented on the filter so that applications can access the informational methods on the WM Reader object.</span></span>                                                                      |
| [<span data-ttu-id="909e9-141">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="909e9-141">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | <span data-ttu-id="909e9-142">**QueryInterface** no filtro</span><span class="sxs-lookup"><span data-stu-id="909e9-142">**QueryInterface** on filter</span></span>           | <span data-ttu-id="909e9-143">Parcialmente implementado no filtro para que os aplicativos possam acessar os métodos informacionais no Objeto de Leitor.</span><span class="sxs-lookup"><span data-stu-id="909e9-143">Partially implemented on the filter so that applications can access the informational methods on the Reader Object.</span></span>                                                                         |



 

<span data-ttu-id="909e9-144">O [filtro Leitor do WM ASF](wm-asf-reader-filter.md) foi disponibilizado pela primeira vez no DirectShow 8.0.</span><span class="sxs-lookup"><span data-stu-id="909e9-144">The [WM ASF Reader](wm-asf-reader-filter.md) filter was first made available in DirectShow 8.0.</span></span> <span data-ttu-id="909e9-145">A versão do filtro que acompanha o DirectShow 8.1 e 9.0 dá suporte à versão 7. *x* do SDK Windows Media Format dados.</span><span class="sxs-lookup"><span data-stu-id="909e9-145">The version of the filter that ships with DirectShow 8.1 and 9.0 supports version 7.*x* of the Windows Media Format SDK.</span></span> <span data-ttu-id="909e9-146">A versão mais recente do filtro, juntamente com os outros componentes qaSF, acompanha e dá suporte ao SDK do Windows Media Format Série 9 e versões posteriores, e ele é substituído pelo filtro no DirectX 9.0.</span><span class="sxs-lookup"><span data-stu-id="909e9-146">The most recent version of the filter, along with the other QASF components, ships with and supports the Windows Media Format 9 Series SDK, and later versions, and it supersedes the filter in DirectX 9.0.</span></span> <span data-ttu-id="909e9-147">Se você instalar o SDK Windows Media Format depois de instalar o DirectX 8. *x* ou 9. *X* SDK, você substituirá a versão directX do qasf.dll pela versão da série 9.</span><span class="sxs-lookup"><span data-stu-id="909e9-147">If you install the Windows Media Format SDK after installing the DirectX 8.*x* or 9.*x* SDK, you will overwrite the DirectX version of qasf.dll with the 9 Series version.</span></span> <span data-ttu-id="909e9-148">Isso não deve apresentar nenhum problema, exceto possivelmente em um cenário em que resultará em um comportamento diferente no método DirectShow **IGraphBuilder::RenderFile.**</span><span class="sxs-lookup"><span data-stu-id="909e9-148">This should not present any problems except possibly in one scenario where it will result in different behavior in the DirectShow **IGraphBuilder::RenderFile** method.</span></span> <span data-ttu-id="909e9-149">A Windows Media Format do SDK da Série 9 do WM ASF Reader é o filtro de origem padrão para as extensões de nome de arquivo .asf, .wmv e .wma.</span><span class="sxs-lookup"><span data-stu-id="909e9-149">The Windows Media Format 9 Series SDK version of the WM ASF Reader is the default source filter for the .asf, .wmv, and .wma file name extensions.</span></span> <span data-ttu-id="909e9-150">Isso significa que o Leitor do WM ASF é criado e adicionado automaticamente ao grafo de filtro pelo Gerenciador de Grafo de Filtro em métodos como **IGraphBuilder::RenderFile** ou **IGraphBuilder::AddSourceFilter** quando um arquivo desse tipo é especificado.</span><span class="sxs-lookup"><span data-stu-id="909e9-150">This means that the WM ASF Reader is automatically created and added to the filter graph by the Filter Graph Manager in methods such as **IGraphBuilder::RenderFile** or **IGraphBuilder::AddSourceFilter** when a file of this type is specified.</span></span> <span data-ttu-id="909e9-151">No DirectX 9.0 e anteriores e no Windows XP Service Pack 1 e anterior, o **método RenderFile** usa o Filtro de Fonte de Mídia do Windows mais antigo.</span><span class="sxs-lookup"><span data-stu-id="909e9-151">In DirectX 9.0 and earlier, and Windows XP Service Pack 1 and earlier, the **RenderFile** method uses the older Windows Media Source Filter.</span></span> <span data-ttu-id="909e9-152">Esse comportamento foi mantido para garantir a compatibilidade com aplicativos que usaram o Windows Media Player 6.4.</span><span class="sxs-lookup"><span data-stu-id="909e9-152">This behavior was maintained to ensure backward compatibility with applications that used the Windows Media Player 6.4.</span></span> <span data-ttu-id="909e9-153">Para obter mais informações sobre o Filtro de Fonte de Mídia do Windows herdado, consulte a Documentação do SDK do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="909e9-153">For more information about the legacy Windows Media Source Filter, see the DirectShow SDK Documentation.</span></span>

<span data-ttu-id="909e9-154">Para reproduzir um arquivo ASF com conteúdo baseado em Mídia do Windows usando o Leitor do WM ASF, as três etapas principais são criar uma instância do Gerenciador de Grafo de Filtro, chamar **IGraphBuilder::RenderFile** para criar o grafo e, em seguida, **chamar IMediaControl::Run** para reproduzir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="909e9-154">To play an ASF file with Windows Media–based content using the WM ASF Reader, the three primary steps are to create an instance of the Filter Graph Manager, call **IGraphBuilder::RenderFile** to create the graph, and then call **IMediaControl::Run** to play the file.</span></span> <span data-ttu-id="909e9-155">O exemplo de código a seguir é um programa completo que reproduz um arquivo ASF usando o DirectShow.</span><span class="sxs-lookup"><span data-stu-id="909e9-155">The following code example is a complete program that plays an ASF file using DirectShow.</span></span> <span data-ttu-id="909e9-156">Para executar este exemplo, você deve ter o SDK do DirectX instalado e seu ambiente de build deve ser configurado de acordo com as instruções no tópico de documentação do SDK do DirectShow "Configurando o ambiente de build".</span><span class="sxs-lookup"><span data-stu-id="909e9-156">To run this example, you must have the DirectX SDK installed and your build environment must be configured according to the instructions in the DirectShow SDK documentation topic "Setting Up the Build Environment."</span></span> <span data-ttu-id="909e9-157">Além disso, você deve especificar um arquivo em seu computador na chamada para **RenderFile**.</span><span class="sxs-lookup"><span data-stu-id="909e9-157">Also, you must specify a file on your computer in the call to **RenderFile**.</span></span>


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



<span data-ttu-id="909e9-158">Observe que o código do aplicativo para este exemplo simples nunca faz referência ao Leitor de ASF WM especificamente.</span><span class="sxs-lookup"><span data-stu-id="909e9-158">Note that the application code for this simple example never references the WM ASF Reader specifically.</span></span> <span data-ttu-id="909e9-159">Esse filtro é criado, conectado, executado e, eventualmente, liberado pelo Gerenciador de Grafo de Filtro.</span><span class="sxs-lookup"><span data-stu-id="909e9-159">That filter is created, connected, run, and eventually released by the Filter Graph Manager.</span></span> <span data-ttu-id="909e9-160">No entanto, em muitos cenários, talvez você queira configurar o Leitor do WM ASF antes de iniciar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="909e9-160">In many scenarios, however, you may want to configure the WM ASF Reader before beginning playback.</span></span>

 

 




