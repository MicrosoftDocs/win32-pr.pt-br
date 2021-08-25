---
description: Sobre o filtro de leitor ASF do WM
ms.assetid: e698c0da-88b2-497a-8a25-9d3b76c85a7d
title: Sobre o filtro de leitor ASF do WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b71d0b25070c446ebff88f18785df7b55ba7bbcc7b1bcaa1dcf21995185252ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873696"
---
# <a name="about-the-wm-asf-reader-filter"></a>Sobre o filtro de leitor ASF do WM

A reprodução de arquivos ASF é manipulada pelo filtro [Leitor do WM ASF.](wm-asf-reader-filter.md) Quando o Leitor do WM ASF lê um arquivo, ele cria automaticamente um pino de saída para cada fluxo, incluindo fluxos da Web, fluxos de comando de script e qualquer outro tipo de fluxo arbitrário. No caso de vários arquivos de taxa de bits, os pinos são criados somente para os fluxos selecionados no momento. Para reproduzir um arquivo ASF com o filtro leitor do WM ASF, chame [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) ou [**IGraphBuilder::AddSourceFilter.**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter)

O Leitor do WM ASF dá suporte à interface [**DirectShow IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) que permite que os aplicativos executem a busca temporal dentro do arquivo. No entanto, não há suporte para a reprodução em velocidades que não 1.0 (conforme especificado em [**IMediaSeeking::SetRate).**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)

O filtro Leitor do WM ASF também expõe várias interfaces Windows SDK de Formato de Mídia, conforme descrito na tabela a seguir. Essas interfaces estão documentadas na documentação do SDK Windows Formato de Mídia.



| Interface                                             | Como exposto                                 | Comentários                                                                                                                       |
|-------------------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | Por **meio de IServiceProvider** no filtro. | Fornecido para aplicativos que precisam reproduzir conteúdo protegido por DRM (Rights Management Digital)..                             |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface** no filtro.           | Fornecido para que os aplicativos possam ler atributos de arquivo e conteúdo, bem como informações de marcador e script e metadados.     |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface** no filtro.           | Parcialmente implementado no filtro para que os aplicativos possam acessar os métodos informacionais no objeto Leitor de WM.         |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface** no filtro.           | Parcialmente implementado no filtro para que os aplicativos possam acessar os métodos informacionais no Objeto de Leitor do SDK de Formato. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Lendo arquivos ASF no DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



