---
description: Usando fluxos de multimídia em aplicativos
ms.assetid: 73cfe89b-df46-445a-92c7-2f7323672441
title: Usando fluxos de multimídia em aplicativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30dab204bc7b0bddbdc293708daecbe0558e8f9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930155"
---
# <a name="using-multimedia-streams-in-applications"></a>Usando fluxos de multimídia em aplicativos

> [!Note]  
> Essas APIs são preteridas. Os aplicativos devem usar o filtro de [**apoio de exemplo**](sample-grabber-filter.md) ou implementar um filtro personalizado para obter dados de um grafo de filtro do DirectShow.

 

As interfaces de streaming de multimídia simplificam bastante o processo de manipulação de dados de multimídia removendo a dependência de características específicas da fonte de hardware ou software e fornecendo suporte para todos os formatos de mídia do Microsoft DirectX®. Os fluxos abstraim os dados para um nível muito alto; os aplicativos podem até mesmo mover dados de um fluxo para outro sem saber nada sobre o formato dos dados.

Execute as etapas a seguir para criar um fluxo de multimídia.

1.  Crie o fluxo de multimídia. O método de criação e inicialização do fluxo é específico da arquitetura. O DirectShow dá suporte à interface [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) , que é usada para inicializar o fluxo. Outras implementações de servidor em processo de [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) serão criadas e inicializadas usando mecanismos diferentes.
2.  Depois que o objeto de fluxo de multimídia for inicializado, o aplicativo usará **QueryInterface** para recuperar a interface **IMultiMediaStream** do objeto. Use essa interface para determinar as propriedades do fluxo e enumerar os fluxos em si. Você pode recuperar um fluxo específico chamando o método [**IMultiMediaStream:: GetMediaStream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) com uma ID de finalidade específica. MSPID \_ PrimaryVideo e MSPID \_ PrimaryAudio, que representam os fluxos de áudio e vídeo primários, são as IDs de finalidade usadas com mais frequência.
3.  Chame **IUnknown:: QueryInterface** para uma interface específica para o tipo de mídia do fluxo. Se você quiser renderizar um fluxo de vídeo, por exemplo, recupere sua interface [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) . As interfaces específicas de mídia definem métodos adicionais necessários para aproveitar ao máximo os recursos de um formato.
4.  Crie um ou mais exemplos dos dados de fluxo. Cada fluxo de mídia dá suporte ao método [**IMediaStream:: CreateSharedSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample) para a criação de exemplo. O exemplo resultante dá suporte à interface [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) , que fornece controle sobre a amostra e suas características. Normalmente, o fluxo de mídia dá suporte a um método específico de formato de criação de exemplo que é mais potente do que os métodos **IStreamSample** mencionados anteriormente. **IDirectDrawMediaStream**, por exemplo, pode criar amostras anexadas a uma superfície do DirectDraw e ao retângulo de recorte desejados. Em algumas situações, no entanto, você deve lidar com os dados sem saber mais sobre seu formato de dados. Se você quiser transmitir dados independentemente de seu formato, use o método **IMediaStream:: CreateSharedSample** para criar os exemplos de dados.
5.  Depois de criar todos os exemplos de fluxo desejados, inicie o fluxo chamando o método [**IMultiMediaStream:: SetState**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-setstate) e passe o sinalizador de execução streamstate \_ como seu parâmetro.
6.  Chame [**IStreamSample:: Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) para atualizar o exemplo de fluxo. Quando o método **IStreamSample:: Update** é encerrado, você pode acessar os dados do exemplo. Se você quiser que um gatilho seja um evento ou uma chamada de função específica quando a atualização retornar, passe os ponteiros apropriados para o método **IStreamSample:: Update** .

Para obter mais informações sobre as interfaces de streaming de multimídia, consulte [Multimedia streaming](multimedia-streaming.md).

 

 



