---
description: Sobre o filtro de leitor ASF do WM
ms.assetid: e698c0da-88b2-497a-8a25-9d3b76c85a7d
title: Sobre o filtro de leitor ASF do WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350e6597aa6aa66193af37a30ed54c37139d5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825937"
---
# <a name="about-the-wm-asf-reader-filter"></a>Sobre o filtro de leitor ASF do WM

A reprodução de arquivos ASF é tratada pelo filtro de [leitor ASF do WM](wm-asf-reader-filter.md) . Quando o leitor ASF do WM lê um arquivo, ele cria automaticamente um PIN de saída para cada fluxo, incluindo fluxos da Web, fluxos de comando de script e qualquer outro tipo de fluxo arbitrário. No caso de vários arquivos de taxa de bits, os Pins são criados somente para os fluxos selecionados no momento. Para reproduzir um arquivo ASF com o filtro de leitor ASF do WM, chame [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) ou [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).

O leitor ASF do WM dá suporte à interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) do DirectShow, que permite que os aplicativos executem a busca temporal dentro do arquivo. No entanto, a reprodução em velocidades diferentes de 1,0 (conforme especificado em [**IMediaSeeking:: SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)) não é suportada.

O filtro de leitor ASF do WM também expõe várias interfaces SDK do Windows Media Format, conforme descrito na tabela a seguir. Essas interfaces estão documentadas na documentação do Windows Media Format SDK.



| Interface                                             | Quão expostos                                 | Comentários                                                                                                                       |
|-------------------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | Por meio de **IServiceProvider** no filtro. | Fornecido para aplicativos que precisam reproduzir conteúdo protegido por DRM (Rights Management digital).                             |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface** no filtro.           | Fornecido para que os aplicativos possam ler atributos de arquivo e conteúdo, bem como informações de marcador e script e metadados.     |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface** no filtro.           | Parcialmente implementado no filtro para que os aplicativos possam acessar os métodos informativos no objeto do WM Reader.         |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface** no filtro.           | Parcialmente implementado no filtro para que os aplicativos possam acessar os métodos informativos no formato do objeto leitor SDK. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Lendo arquivos ASF no DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



