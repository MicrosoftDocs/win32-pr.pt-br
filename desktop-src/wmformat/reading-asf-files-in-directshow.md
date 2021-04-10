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
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a>Lendo arquivos ASF no DirectShow (SDK do Windows Media Format 11)

A reprodução de arquivos ASF é tratada pelo filtro de [leitor ASF do WM](wm-asf-reader-filter.md) . Quando o leitor ASF do WM lê um arquivo, ele cria automaticamente um PIN de saída para cada fluxo, incluindo fluxos da Web, fluxos de comando de script e qualquer outro tipo de fluxo arbitrário. No caso de vários arquivos de taxa de bits, os Pins são criados somente para os fluxos selecionados no momento.

O leitor ASF do WM dá suporte à interface **IMediaSeeking** do DirectShow, que permite que os aplicativos executem a busca temporal dentro do arquivo. No entanto, a reprodução em velocidades diferentes de 1,0 (conforme especificado em **IMediaSeeking:: SetRate**) não é suportada.

O filtro também expõe várias interfaces do Windows Media Format SDK, conforme descrito na tabela a seguir.



| Interface                                        | Quão expostos                            | Comentários                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | Por meio de **IServiceProvider** no filtro | Fornecido para aplicativos que precisam executar conteúdo protegido por DRM (Rights Management digital). Essa interface também pode ser usada para obter outras interfaces diretamente no objeto leitor. |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface** no filtro           | Fornecido para que os aplicativos possam ler atributos de arquivo e conteúdo, bem como informações de marcador e script e metadados.                                                                  |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface** no filtro           | Parcialmente implementado no filtro para que os aplicativos possam acessar os métodos informativos no objeto do WM Reader.                                                                      |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface** no filtro           | Parcialmente implementado no filtro para que os aplicativos possam acessar os métodos informativos no objeto leitor.                                                                         |



 

O filtro de [leitor ASF do WM](wm-asf-reader-filter.md) foi disponibilizado primeiro no DirectShow 8,0. A versão do filtro que acompanha o DirectShow 8,1 e 9,0 dá suporte à versão 7. *x* do Windows Media Format SDK. A versão mais recente do filtro, juntamente com os outros componentes do QASF, é fornecida com o e dá suporte ao SDK da série Windows Media Format 9 Series e às versões posteriores, e ele substitui o filtro no DirectX 9,0. Se você instalar o SDK do Windows Media Format depois de instalar o DirectX 8. *x* ou 9. *x* SDK, você substituirá a versão do DirectX do qasf.dll pela versão da série 9. Isso não deve apresentar nenhum problema, exceto possivelmente em um cenário no qual resultará em um comportamento diferente no método DirectShow **IGraphBuilder:: RenderFile** . A versão do SDK do Windows Media Format 9 Series do leitor ASF do WM é o filtro de origem padrão para as extensões de nome de arquivo. ASF,. wmv e. WMA. Isso significa que o leitor ASF do WM é criado e adicionado automaticamente ao grafo de filtro pelo Gerenciador de gráficos de filtro em métodos como **IGraphBuilder:: RenderFile** ou **IGraphBuilder:: AddSourceFilter** quando um arquivo desse tipo é especificado. No DirectX 9,0 e versões anteriores, e no Windows XP Service Pack 1 e versões anteriores, o método **RenderFile** usa o filtro de origem de mídia mais antigo do Windows. Esse comportamento foi mantido para garantir a compatibilidade com versões anteriores com aplicativos que usavam o Windows Media Player 6,4. Para obter mais informações sobre o filtro de origem de mídia do Windows herdado, consulte a documentação do SDK do DirectShow.

Para reproduzir um arquivo ASF com conteúdo baseado no Windows Media usando o leitor ASF do WM, as três etapas principais são criar uma instância do Gerenciador de gráfico de filtro, chamar **IGraphBuilder:: RenderFile** para criar o grafo e, em seguida, chamar **IMediaControl:: Run** para reproduzir o arquivo. O exemplo de código a seguir é um programa completo que reproduz um arquivo ASF usando o DirectShow. Para executar este exemplo, você deve ter o SDK do DirectX instalado e seu ambiente de compilação deve ser configurado de acordo com as instruções no tópico de documentação do SDK do DirectShow "Configurando o ambiente de compilação". Além disso, você deve especificar um arquivo em seu computador na chamada para **RenderFile**.


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



Observe que o código do aplicativo para esse exemplo simples nunca faz referência especificamente ao leitor ASF do WM. Esse filtro é criado, conectado, executado e eventualmente liberado pelo Gerenciador de gráfico de filtro. Em muitos cenários, no entanto, talvez você queira configurar o leitor ASF do WM antes de começar a reprodução.

 

 




