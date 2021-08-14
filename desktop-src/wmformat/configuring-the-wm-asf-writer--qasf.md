---
title: Configurando o gravador ASF do WM (QASF)
description: Configurando o gravador ASF do WM (QASF)
ms.assetid: 0f49ed5a-c228-456a-9551-8d277adccd0e
keywords:
- Windows SDK do formato de mídia, configurando o gravador ASF do WM (QASF)
- Windows SDK do formato de mídia, DirectShow
- Windows SDK do formato de mídia, gravador ASF do WM
- Windows SDK do formato de mídia, QASF
- ASF (Advanced Systems Format), configurando o gravador ASF do WM (QASF)
- ASF (formato de sistemas avançados), configurando o gravador ASF do WM (QASF)
- ASF (Advanced Systems Format), gravador ASF do WM
- ASF (formato de sistemas avançados), gravador ASF do WM
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), QASF
- ASF (formato de sistemas avançados), QASF
- DirectShow, configurando o gravador ASF do WM (QASF)
- DirectShow, gravador ASF do WM
- DirectShow, QASF
- Gravador ASF do WM, configurando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba4559fc1780bdb9a9b398471cc842e2f3cf46f9c84a483229b01b3b6fa4a1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199172"
---
# <a name="configuring-the-wm-asf-writer-qasf"></a>Configurando o gravador ASF do WM (QASF)

Quando o filtro do [gravador ASF do WM](wm-asf-writer-filter.md) é criado, ele é configurado automaticamente com o \_ perfil WMProfile V80 \_ 256Video como padrão. como esse perfil usa os codecs Windows mídia de áudio e Windows vídeo de mídia 8, é recomendável que você crie um perfil personalizado que usa os codecs da série 9 da mídia do Windows e, em seguida, passe o ponteiro [**IWMProfile**](iwmprofile.md) para o filtro usando o método [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) . O filtro deve ser adicionado ao grafo antes que o filtro possa ser configurado e deve ser configurado antes que possa ser conectado a filtros upstream. o filtro usa o perfil para determinar que tipo de Windows arquivo de formato de mídia gravar, quantos pins de entrada configurar e quais tipos de mídia os pins podem aceitar.

O filtro permite que os perfis sejam redefinidos enquanto seus PINs de entrada estão conectados, desde que o novo perfil não exija nenhum pino de entrada adicional. Por exemplo, se você alterar o perfil de um perfil somente de áudio de uma entrada para um perfil de áudio e vídeo de duas entradas, apenas o PIN de áudio será reconnectedAll os dados de entrada deverão ser carimbados por hora e todos os Pins de entrada deverão ser conectados antes que o filtro possa ser executado ou pausado. Isso significa que, se você configurar o filtro com um perfil que tenha um fluxo de áudio e um fluxo de vídeo, o filtro criará um áudio e um pino de entrada de vídeo, e ambos os Pins deverão ser conectados antes que o filtro possa ser executado.

Adicionando extensões de unidade de dados

Você pode configurar um fluxo de perfil para extensões de unidade de dados, como códigos de tempo SMPTE, antes ou depois que o filtro está conectado, desde que você siga esta ordem de operações:

1.  Adicione uma ou mais extensões de unidade de dados ao fluxo usando [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).
2.  Chame [**WMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) para atualizar o perfil.
3.  Chame [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) com o objeto de perfil atualizado.
4.  Localize o PIN de entrada de vídeo e chame o método [**IAMWMBufferPass:: setnotify**](iamwmbufferpass-setnotify.md) para registrar sua interface [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) definida pelo aplicativo.

Quando o grafo for executado, o método [**IAMWMBufferPassCallback:: Notify**](iamwmbufferpasscallback-notify.md) será chamado para cada quadro e você poderá obter e definir propriedades no exemplo usando seus métodos de interface [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) .

> [!Note]  
> Em alguns cenários com uso intensivo de processador, como o telecineon inverso, o gravador ASF do WM pode exigir mais buffers de saída do que alguns filtros downstream podem dar suporte. O codificador DV, por exemplo, não aceitará mais de um buffer para seu pino de saída e o mesmo será verdadeiro para o descompactador AVI em determinadas condições. Se você encontrar problemas ao tentar se conectar a esses filtros, ou possivelmente ao executar o grafo, pode ser necessário gravar um filtro intermediário que aceite qualquer número de buffers em seu pino de saída.

 

 

 