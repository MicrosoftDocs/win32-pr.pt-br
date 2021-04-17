---
description: Gravando um arquivo de mídia do Windows no DES
ms.assetid: 741ebcbc-62fb-4c7f-845f-a361f5b63f8c
title: Gravando um arquivo de mídia do Windows no DES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0626a3ef609dee87d90a6d3c2caa023e9ac9a29a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105761745"
---
# <a name="writing-a-windows-media-file-in-des"></a>Gravando um arquivo de mídia do Windows no DES

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Esta seção descreve como gravar um arquivo do Windows Media usando o des ( [serviços de edição do DirectShow](directshow-editing-services.md) ).

> [!IMPORTANT]
> Não use o mecanismo de processamento inteligente para gravar arquivos de mídia do Windows. Sempre use o mecanismo de processamento básico (CLSID \_ RenderEngine).

 

Para gravar um arquivo do Windows Media, faça o seguinte:

1.  Chame **SetSite** no mecanismo de processamento, com um ponteiro para o provedor de chave.
2.  Crie o front-end do grafo. (Consulte [renderizando um projeto](rendering-a-project.md).)
3.  Crie o filtro do [gravador ASF do WM](wm-asf-writer-filter.md) e adicione-o ao grafo.
4.  Use a interface [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) no filtro do gravador ASF do WM para definir o nome do arquivo.
5.  Configure o gravador ASF do WM para usar um perfil do Windows Media. Cada perfil tem um número predefinido de fluxos. Você deve escolher um perfil que corresponda aos grupos em seu projeto.

    A interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) contém alguns métodos diferentes para definir o perfil. Por exemplo, o método **ConfigureFilterUsingProfileGuid** especifica um perfil de sistema como um GUID. Ou, você pode usar os métodos de formato de mídia do Windows para obter um ponteiro **IWMProfile** e, em seguida, chamar [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile). Para obter mais informações, consulte [Configurando o gravador ASF](configuring-the-asf-writer.md).

6.  Conecte o front-end ao gravador ASF. O front-end do grafo contém um pino de saída para cada grupo. Supondo que você especificou um perfil compatível, o gravador ASF deve ter um conjunto correspondente de Pins de entrada. Conecte cada pino de saída ao PIN de entrada correspondente. A maneira mais fácil de fazer isso é usando o método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) . Primeiro, crie uma nova instância do [construtor do grafo de captura](capture-graph-builder.md) e inicialize-a com um ponteiro para o Gerenciador do grafo de filtro:

    ```C++
    ICaptureGraphBuilder2 *pBuild = 0;
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 0, CLSCTX_INPROC_SERVER,
        IID_ICaptureGraphBuilder2, (void**)&pBuild);
    pBuild->SetFiltergraph(pGraph); 
    ```

    

    Em seguida, recupere o pino de saída para cada grupo chamando o método [**IRenderEngine:: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) . Chame **RenderStream** para conectar o PIN ao gravador ASF:

    ```C++
    long cGroups = 0;
    hr = pTimeline->GetGroupCount(&cGroups);
    for (long i = 0; i < cGroups; i++)
    {
        IPin *pPin;
        hr = pRenderEngine->GetGroupOutputPin(i, &pPin);
        if (SUCCEEDED(hr))
        {
            hr = pBuild->RenderStream(0, 0, pPin, 0, pASF);
        }
        pPin->Release();
    }
    pBuild->Release
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Windows Media com os serviços de edição do DirectShow](using-windows-media-with-directshow-editing-services.md)
</dt> </dl>

 

 



