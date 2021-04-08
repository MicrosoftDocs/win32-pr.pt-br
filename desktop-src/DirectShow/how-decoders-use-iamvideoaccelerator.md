---
description: Como os decodificadores usam o IAMVideoAccelerator
ms.assetid: 0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d
title: Como os decodificadores usam o IAMVideoAccelerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436768b3561a999f6708ef4f6438b816e0ad303b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919696"
---
# <a name="how-decoders-use-iamvideoaccelerator"></a>Como os decodificadores usam o IAMVideoAccelerator

A interface [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) permite operações genéricas de aceleração de vídeo, incluindo o DirectX Video ACCELERATION (VA). Para a aceleração não-DirectX VA, o decodificador e o driver de vídeo devem aderir a um protocolo comum.

Esta seção descreve a ordem geral das operações que qualquer decodificador deve seguir ao usar essa interface. Mais informações específicas para decodificadores baseados em DirectX VA podem ser encontradas em [mapeando aceleração de vídeo DirectX para IAMVideoAccelerator](mapping-directx-video-acceleration-to-iamvideoaccelerator.md).

> [!Note]  
> Essa interface está disponível no Windows 2000 e posterior.

 

A interface [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) é exposta no pino de entrada do [mixer de sobreposição](overlay-mixer-filter.md) ou do processador de mixagem de vídeo (VMR). A interface [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) é exposta no pino de saída do decodificador. A sequência de eventos para conectar os Pins de filtro é a seguinte:

1.  O Gerenciador do grafo de filtro chama [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) no pino de saída do filtro de decodificador. Um [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) é um parâmetro opcional.
    -   [**Am \_ O \_ tipo de mídia**](/windows/win32/api/strmif/ns-strmif-am_media_type) é uma estrutura de dados que descreve um tipo de mídia. Ele contém um GUID de majortype (que, em nosso caso, deve ser \_ vídeo de MediaType), um GUID de subtipo (que, em nosso caso, deve ser um GUID de acelerador de vídeo) e uma variedade de outras coisas. Uma dessas coisas é um GUID de tipo de formato que contém informações sobre a mídia, incluindo, em nosso caso, a largura e a altura de uma imagem de vídeo descompactada, provavelmente em uma estrutura [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader), [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo)ou [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .
    -   A estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , se presente, instrui o decodificador a operar usando o tipo de mídia especificado, que pode ser "totalmente especificado" ou "parcialmente especificado". Se "totalmente especificado", o decodificador normalmente simplesmente tentaria operar com esse tipo de mídia. Se "parcialmente especificado", ele tentará encontrar um modo de operação compatível "totalmente especificado" que pode ser usado para se conectar de maneira consistente com o tipo de mídia "parcialmente especificado".
    -   A maneira comum de tentar encontrar um tipo de mídia "totalmente especificado" a ser usado para uma conexão é simplesmente executar uma lista de todos os tipos de mídia "totalmente especificados" que o PIN de saída suporta, que é compatível com o tipo de mídia "parcialmente especificado" e tentar se conectar a cada um deles até que tenha êxito. O processo normalmente seria semelhante se nenhum tipo de \_ mídia am \_ estiver contido na chamada [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) , mas com o PIN de saída que precisa verificar todos os seus tipos de mídia.
2.  Se o decodificador quiser verificar se um [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) específico (incluindo um GUID de acelerador de vídeo) tem suporte no pino de entrada downstream, ele poderá chamar o [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) (com o GUID do acelerador de vídeo como o subtipo do **\_ \_ tipo de mídia am**) ou simplesmente tentar se conectar a esse PIN, conforme descrito no item 5 abaixo.
3.  Se o decodificador não souber qual GUID de vídeo é compatível com o PIN de entrada downstream e não quiser propor apenas algum GUID de acelerador de vídeo candidato específico chamando o [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept)do pino de entrada downstream, o decodificador poderá chamar [**IAMVideoAccelerator:: GetVideoAcceleratorGUIDs**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getvideoacceleratorguids) para obter uma lista dos GUIDs do acelerador de vídeo com suporte do PIN.
4.  Para alguns GUIDs de acelerador de vídeo específicos, o decodificador pode chamar o [**IAMVideoAccelerator:: GetUncompFormatsSupported**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getuncompformatssupported) do pino de entrada downstream para obter uma lista dos formatos de pixel **DDPIXELFORMAT** que podem ser usados para renderizar um GUID de acelerador de vídeo específico. A lista retornada deve ser considerada em ordem de preferência decrescente (ou seja, com o formato mais preferencial listado primeiro).
5.  O decodificador chama o [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection)do pino de entrada downstream, passando-o para um [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) com o GUID do acelerador de vídeo apropriado como o subtipo do tipo de mídia. Isso configura a conexão para a operação, incluindo a criação das superfícies de saída não compactadas (que são alocadas usando a largura e a altura encontradas no **\_ \_ tipo de mídia am** e o número de superfícies a serem alocadas por uma chamada descrita abaixo e quaisquer outras informações que o acelerador de vídeo tenha disponível e que você queira usar para essa finalidade — como o próprio Media Accelerator GUID). Se o pino de entrada downstream rejeitar o GUID do acelerador de vídeo ou algum outro aspecto da conexão, isso poderá fazer com que **IPin:: ReceiveConnection** falhe. Se **IPin:: ReceiveConnection** falhar, isso será indicado em um **HRESULT** retornado e o decodificador poderá tentar fazer a chamada novamente, por exemplo, com um novo GUID de acelerador de vídeo na estrutura do **\_ \_ tipo de mídia am** .
    -   [!Note]  
        > Essa é outra maneira (e a maneira mais definitiva) para o decodificador determinar o que é suportado pelo PIN de entrada downstream, simplesmente chamando [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) e tentando se conectar e, em seguida, verificando se a tentativa de conexão foi bem-sucedida.

         

    -   Durante o [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection), o renderizador chama o [**IAMVideoAcceleratorNotify:: GetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo)do decodificador, passando-o para o GUID do acelerador de vídeo e uma estrutura de [**AMVAUncompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompbufferinfo) , a fim de descobrir quantas superfícies descompactadas alocar. O decodificador preenche e retorna a estrutura, que contém o número mínimo e máximo de superfícies a serem alocadas do tipo específico e uma estrutura **DDPIXELFORMAT** que descreve o formato de pixel das superfícies a serem alocadas.
    -   [!Note]  
        > Na verdade, nada é passado para o decodificador na chamada para [**IAMVideoAcceleratorNotify:: GetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo) diferente do GUID do acelerador de vídeo.

         

6.  O renderizador chama o [**IAMVideoAcceleratorNotify:: SetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-setuncompsurfacesinfo)do decodificador, passando para o decodificador o número real de superfícies não compactadas que foram alocadas.
7.  O renderizador chama o [**IAMVideoAcceleratorNotify:: GetCreateVideoAcceleratorData**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata) do decodificador para obter todos os dados necessários para inicializar o acelerador de vídeo.
8.  O decodificador chama [**IAMVideoAccelerator:: GetCompBufferInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo), passando a ele um GUID de acelerador de vídeo, uma estrutura [**AMVAUncompDataInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompdatainfo) e o número de tipos de buffer compactados, para retornar um conjunto de estruturas de dados [**AMVACompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) , um correspondente a cada tipo de buffer de dados compactado usado pelo GUID do acelerador de vídeo.
    -   A estrutura [**AMVAUncompDataInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompdatainfo) contém a largura e a altura dos dados não compactados decodificados (em pixels) e o DDPIXELFORMAT da imagem não compactada.
    -   As estruturas de dados [**AMVACompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) retornavam cada uma delas:
        -   O número de buffers compactados necessários do tipo específico.
        -   A largura e a altura da superfície a ser criada (campos que podem ou não ter nenhum significado real).
            > [!Note]  
            > A operação de alocação de superfície do DirectDraw para os buffers compactados não fornece atualmente a largura ou a altura dessas superfícies para ser maior ou igual a 2 ^ 15, embora a chamada de alocação de superfície não possa overtly falhar se esse limite for violado. Portanto, o driver pode estruturar suas solicitações de memória de buffer compactado para evitar esses tamanhos extremos. Por exemplo, em vez de solicitar um buffer com width = "1" e Height = "65536", o driver deve solicitar um buffer de Width = "1024" e Height = "64".

             

        -   O número total de bytes a serem usados pela superfície.
        -   Uma estrutura do tipo **DDSCAPS2** definindo um objeto DirectDrawSurface, descrevendo os recursos para criar superfícies para armazenar dados compactados.
        -   Um DDPIXELFORMAT, que descreve o formato de pixel usado para criar superfícies para armazenar dados compactados (um campo que pode ou não ter qualquer significado real).

> [!Note]  
> As chamadas do renderizador para alguns dos métodos de interface [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) de decodificador podem (e normalmente) ocorrem dentro da chamada do decodificador para [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection)do renderizador. Especificamente, isso se aplica ao seguinte:
>
> -   [**IAMVideoAcceleratorNotify:: GetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo),
> -   [**IAMVideoAcceleratorNotify:: SetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-setuncompsurfacesinfo)e
> -   [**IAMVideoAcceleratorNotify:: GetCreateVideoAcceleratorData**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata).

 

> [!Note]  
> Para dar suporte a alterações de formato dinâmico, o decodificador também pode chamar [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) e outros métodos por acima enquanto os filtros estão conectados e em execução. Esse recurso é fornecido para dar suporte a alterações de formato dinâmico (embora não esteja no H. 263, o anexo P, Sense-como todos os conjuntos de dados são iniciados novamente do zero e todas as informações de imagem de referência são, portanto, perdidas).

 

Veja a seguir uma descrição do uso do [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) durante a operação após a inicialização:

1.  Para cada superfície descompactada, o decodificador chama [**IAMVideoAccelerator:: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) para iniciar o processamento para criar a imagem de saída. Quando ele faz isso, o decodificador envia uma estrutura [**AMVABeginFrameInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabeginframeinfo) .
    -   A estrutura [**AMVABeginFrameInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabeginframeinfo) contém um índice para um buffer de destino, um ponteiro para alguns dados para enviar downstream e um ponteiro para um local onde o acelerador pode colocar alguns dados para o decodificador ler.
    -   Observação 1: o acelerador não recebe realmente o índice de buffer de destino, pois ele é convertido pelo renderizador antes de passar pelo downstream.
    -   Observação 2: [**IAMVideoAccelerator:: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) pode ser chamado mais de uma vez entre as chamadas para [**IAMVideoAccelerator:: endframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe).
    -   Observação 3: não há nenhuma suposição na operação de interface que [**IAMVideoAccelerator:: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) e [**IAMVideoAccelerator:: endframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) precisa ser chamada para o processamento de cada imagem individual no fragmentado.

        O que [**IAMVideoAccelerator:: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) faz, no que diz respeito à interface, é criar uma associação dentro do renderizador entre um índice e uma superfície não compactada. Ele também fornece um meio para chamar uma função específica em um driver de dispositivo (com suporte de um meio de passar dados arbitrários entre o decodificador e o driver de dispositivo).

        (No entanto, na operação DirectX VA, há um requisito descrito abaixo que [**IAMVideoAccelerator:: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) e [**IAMVideoAccelerator:: endframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) precisam ser chamados para o processamento de cada imagem individual na fragmentado.)

2.  Para enviar dados descompactados para o acelerador, o decodificador chama:
    -   [**IAMVideoAccelerator:: QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) para determinar se um buffer é seguro para leitura ou gravação.
    -   [**IAMVideoAccelerator:: GetBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer) para bloquear e obter acesso a um buffer especificado (se ele não tiver chamado anteriormente para obter esse acesso). **GetBuffer** também pode ser usado para obter uma cópia do conteúdo da última imagem de saída não compactada para a qual [**IAMVideoAccelerator:: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) foi chamado, fornecendo [**IAMVideoAccelerator:: endframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) não foi chamado para esse índice de buffer de destino. Se a DDI retornar um status de renderização de DDERR \_ WASSTILLDRAWING para o buffer solicitado, um loop de suspensão será operado no **GetBuffer** até que essa condição seja apagada. Para chamar **GetBuffer**, o decodificador precisará de algumas informações de uma estrutura de dados do [**AMVACompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) que é obtida chamando [**IAMVideoAccelerator:: GetCompBufferInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo).
    -   [**IAMVideoAccelerator:: execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) para indicar que os dados em um conjunto de buffers compactados, conforme indicado em uma matriz de estruturas de dados [**AMVABUFFERINFO**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabufferinfo) devem ser processados. Um código de função dwFunction é passado para o driver nesta chamada. Um ponteiro lpPrivateInputData também é passado para alguns dados para enviar downstream, e um ponteiro lpPrivateOutputData é passado para um local onde o processo downstream pode colocar alguns dados para que o decodificador seja lido.
    -   [**IAMVideoAccelerator:: ReleaseBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-releasebuffer) para indicar que o decodificador concluiu o uso de um buffer especificado para o momento e não precisa mais de acesso bloqueado ao buffer. (Se o decodificador quiser continuar a usar o buffer, ele poderá simplesmente não chamar **IAMVideoAccelerator:: ReleaseBuffer** por enquanto, evitando a necessidade de chamar [**IAMVideoAccelerator:: GetBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer) até que realmente pretenda não usar mais o buffer.) O decodificador não deve gravar no buffer após a [**execução**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) ser chamada até que [**QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) indique que o buffer é seguro para gravação.
3.  Para concluir o processamento de saída para um buffer de destino, o decodificador chama [**IAMVideoAccelerator:: endframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe). Ele pode passar alguns dados arbitrários downstream com essa chamada, e isso é essencialmente tudo o que acontece como resultado dessa chamada. Ele não envia um índice de buffer de destino nessa chamada, portanto, não pode indicar ao acelerador precisamente qual buffer de destino é concluído, a menos que essa indicação esteja contida nos dados arbitrários que são passados.
4.  Para exibir um quadro, o decodificador chama [**IAMVideoAccelerator::D isplayframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) com o índice do quadro a ser exibido e uma estrutura [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) que contém carimbos de data e hora de início e parada e sinalizadores relevantes, como **dwTypeSpecificFlags** na estrutura de [**\_ \_ Propriedades SAMPLE2 am**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) e **dwInterlaceFlags** na estrutura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . O decodificador deve verificar se todas as operações de descompactação que afetam o conteúdo do quadro foram concluídas antes de chamar **DisplayFrame**.
5.  Por fim, o decodificador deve, após a conclusão de todo o processamento, indicar a conclusão de todos os quadros de saída de início restantes chamando [**IAMVideoAccelerator:: endframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) e liberar todos os seus buffers bloqueados chamando [**IAMVideoAccelerator:: ReleaseBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-releasebuffer) para cada buffer não liberado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interfaces e especificações do decodificador](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



