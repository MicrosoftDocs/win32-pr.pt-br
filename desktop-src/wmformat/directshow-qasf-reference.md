---
title: Referência do QASF do DirectShow
description: Referência do QASF do DirectShow
ms.assetid: 66f483b5-3886-48b4-bc43-7c3517abd20d
keywords:
- SDK do Windows Media Format, QASF
- SDK do Windows Media Format, DirectShow
- DirectShow, referência de QASF
- Filtros QASF, referência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c509030f676b83a84f67590a242aea623656a514
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366333"
---
# <a name="directshow-qasf-reference"></a>Referência do QASF do DirectShow

Esta seção contém referências de programação para os seguintes filtros, interfaces e enumerações do QASF do DirectShow. A documentação do SDK do DirectShow contém materiais de referência e de guia de programação para interfaces genéricas adicionais expostas por esses filtros, como **IBaseFilter** e **IPin**, e para versões anteriores dos componentes do QASF.

Para obter uma explicação do nome do QASF, consulte [sobre o DirectShow](about-directshow.md).

Os filtros a seguir estão incluídos nos componentes do QASF do DirectShow.



| Filtrar                                           | Descrição                                                      |
|--------------------------------------------------|------------------------------------------------------------------|
| [Filtro de leitor ASF do WM](wm-asf-reader-filter.md) | Lê e analisa arquivos ASF locais ou remotos.                      |
| [Filtro de gravador ASF do WM](wm-asf-writer-filter.md) | Cria arquivos ASF a partir de fluxos de entrada compactados ou não compactados. |



 

As interfaces a seguir são definidas para uso com os componentes do QASF do DirectShow.



| Interface                                                  | Descrição                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)                 | Fornece um método que permite que os aplicativos se registrem para retornos de chamada dos Pins de entrada do [gravador ASF do WM](wm-asf-writer-filter.md) ou dos Pins de saída do filtro de [leitor ASF do WM](wm-asf-reader-filter.md) . Usado na indexação e ao adicionar extensões de unidade de dados. |
| [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) | Implementado por aplicativos e chamados pelos filtros. Os aplicativos usam o método One nessa interface para obter informações sobre exemplos individuais no fluxo. Usado na indexação e ao adicionar extensões de unidade de dados.                                                 |
| [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))               | Implementado no gravador ASF do WM. Usado por aplicativos para especificar perfis e parâmetros de indexação para o arquivo.                                                                                                                                                              |
| [**IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))             | Fornece funções de configuração adicionais no gravador ASF do WM.                                                                                                                                                                                                             |



 

A enumeração, a estrutura e os eventos a seguir são definidos para uso com os componentes do QASF do DirectShow.



| Enumeração                                                               | Descrição                                                                                                                                                                       |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_\_parâmetro am ASFWRITERCONFIG \_](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) | Define os parâmetros de configuração de filtro usados nos métodos [**IConfigAsfWriter2:: GetParam**](iconfigasfwriter2-getparam.md) e [**SetParam**](iconfigasfwriter2-setparam.md) . |



 



| Estrutura                                         | Descrição                                                                                                                                           |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_dados de \_ evento am WMT \_**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) | Contém informações referentes a um evento de [**\_ status WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) e o código de status associado retornado pelo Windows Media Format SDK. |



 



| Evento                                           | Descrição                                                                                                     |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [\_evento de WMT do EC \_](ec-wmt-event.md)              | Evento encaminhado do SDK do Windows Media Format.                                                              |
| [evento de índice do EC \_ WMT \_ \_](ec-wmt-index-event.md) | Enviado quando um aplicativo usa o [gravador ASF do WM](wm-asf-writer-filter.md) para indexar arquivos de vídeo do Windows Media. |



 

 

 