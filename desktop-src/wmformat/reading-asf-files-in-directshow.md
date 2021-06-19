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
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a>Lendo arquivos ASF no DirectShow (SDK Windows Media Format 11)

A reprodução de arquivos ASF é manipulada pelo filtro [Leitor do WM ASF.](wm-asf-reader-filter.md) Quando o Leitor do WM ASF lê um arquivo, ele cria automaticamente um pino de saída para cada fluxo, incluindo fluxos da Web, fluxos de comando de script e qualquer outro tipo de fluxo arbitrário. No caso de vários arquivos de taxa de bits, os pinos são criados somente para os fluxos selecionados no momento.

O Leitor do WM ASF dá suporte à interface **DirectShow IMediaSeeking,** que permite que os aplicativos executem a busca temporal dentro do arquivo. No entanto, não há suporte para a reprodução em velocidades que não 1.0 (conforme especificado em **IMediaSeeking::SetRate).**

O filtro também expõe várias interfaces Windows Media Format SDK, conforme descrito na tabela a seguir.



| Interface                                        | Como exposto                            | Comentários                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | Por **meio de IServiceProvider** no filtro | Fornecido para aplicativos que precisam reproduzir conteúdo protegido por DRM (Rights Management Digital). Essa interface também pode ser usada para obter outras interfaces diretamente no Objeto de Leitor. |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface** no filtro           | Fornecido para que os aplicativos possam ler atributos de arquivo e conteúdo, bem como informações de marcador e script e metadados.                                                                  |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface** no filtro           | Parcialmente implementado no filtro para que os aplicativos possam acessar os métodos informacionais no objeto Leitor de WM.                                                                      |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface** no filtro           | Parcialmente implementado no filtro para que os aplicativos possam acessar os métodos informacionais no Objeto de Leitor.                                                                         |



 

O [filtro Leitor do WM ASF](wm-asf-reader-filter.md) foi disponibilizado pela primeira vez no DirectShow 8.0. A versão do filtro que acompanha o DirectShow 8.1 e 9.0 dá suporte à versão 7. *x* do SDK Windows Media Format dados. A versão mais recente do filtro, juntamente com os outros componentes qaSF, acompanha e dá suporte ao SDK do Windows Media Format Série 9 e versões posteriores, e ele é substituído pelo filtro no DirectX 9.0. Se você instalar o SDK Windows Media Format depois de instalar o DirectX 8. *x* ou 9. *X* SDK, você substituirá a versão directX do qasf.dll pela versão da série 9. Isso não deve apresentar nenhum problema, exceto possivelmente em um cenário em que resultará em um comportamento diferente no método DirectShow **IGraphBuilder::RenderFile.** A Windows Media Format do SDK da Série 9 do WM ASF Reader é o filtro de origem padrão para as extensões de nome de arquivo .asf, .wmv e .wma. Isso significa que o Leitor do WM ASF é criado e adicionado automaticamente ao grafo de filtro pelo Gerenciador de Grafo de Filtro em métodos como **IGraphBuilder::RenderFile** ou **IGraphBuilder::AddSourceFilter** quando um arquivo desse tipo é especificado. No DirectX 9.0 e anteriores e no Windows XP Service Pack 1 e anterior, o **método RenderFile** usa o Filtro de Fonte de Mídia do Windows mais antigo. Esse comportamento foi mantido para garantir a compatibilidade com aplicativos que usaram o Windows Media Player 6.4. Para obter mais informações sobre o Filtro de Fonte de Mídia do Windows herdado, consulte a Documentação do SDK do DirectShow.

Para reproduzir um arquivo ASF com conteúdo baseado em Mídia do Windows usando o Leitor do WM ASF, as três etapas principais são criar uma instância do Gerenciador de Grafo de Filtro, chamar **IGraphBuilder::RenderFile** para criar o grafo e, em seguida, **chamar IMediaControl::Run** para reproduzir o arquivo. O exemplo de código a seguir é um programa completo que reproduz um arquivo ASF usando o DirectShow. Para executar este exemplo, você deve ter o SDK do DirectX instalado e seu ambiente de build deve ser configurado de acordo com as instruções no tópico de documentação do SDK do DirectShow "Configurando o ambiente de build". Além disso, você deve especificar um arquivo em seu computador na chamada para **RenderFile**.


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



Observe que o código do aplicativo para este exemplo simples nunca faz referência ao Leitor de ASF WM especificamente. Esse filtro é criado, conectado, executado e, eventualmente, liberado pelo Gerenciador de Grafo de Filtro. No entanto, em muitos cenários, talvez você queira configurar o Leitor do WM ASF antes de iniciar a reprodução.

 

 




