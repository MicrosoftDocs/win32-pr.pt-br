---
description: MSDV Driver
ms.assetid: 146ca753-fe41-49d3-8b1c-077e10a28192
title: MSDV Driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5377471f61944c60f57720df6bc64482681d64515f54c853d78cfa405842ff15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748608"
---
# <a name="msdv-driver"></a>MSDV Driver

MSDV é o driver WDM (Microsoft Windows Driver Model) para gravações DV. O driver aparece como um DirectShow quando o dispositivo está conectado. Ele é enumerado em duas categorias de filtro:

-   CLSID \_ VideoInputDeviceCategory ("Fontes de Captura de Vídeo")
-   RENDERIZAÇÃO \_ AM KSCATEGORY \_ ("WDM Streaming Rendering Devices")

O nome amigável do filtro é `Microsoft DV Camera and VCR` ou um equivalente localizado. Em alguns dispositivos, a **propriedade Description** contém uma descrição do modelo específico, que pode ser usado em vez do nome amigável genérico. Para obter mais informações, consulte [Selecionando um dispositivo de captura](selecting-a-capture-device.md).

O MSDV tem dois pinos de saída. Um pino fornece quadros DV que contêm dados intercalados de áudio e vídeo. O outro pino fornece quadros somente vídeo sem áudio. O MSDV não pode transmitir de ambos os pinos ao mesmo tempo, portanto, apenas um pino de saída pode ser conectado por vez. Para obter mais informações sobre como capturar vídeo de um dispositivo DV, consulte [Capturar DV para arquivo](capture-dv-to-file.md).

![capturando dados dv do dispositivo](images/dv-filters4.png)

A maioria das câmeras dv tem uma subunidade de gravador de fita de vídeo (VTR), que pode transmitir dados da fita para o computador. Para o aplicativo, a captura de fita funciona da mesma forma que a captura de vídeo ao vivo. A única diferença é que o aplicativo deve controlar o transporte de fita externo – iniciar e parar a fita, retroceder e assim por diante. Para essa finalidade, o MSDV expõe as interfaces [**IAMExtDevice,**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice) [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)e [**IAMTimecodeReader.**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) Para obter mais informações sobre como controlar um VTR, consulte [Controlando uma dv camcorder](controlling-a-dv-camcorder.md).

Você também pode transmitir DV do computador para a câmera. O vídeo pode ser exibido na tela de integração da câmera ou gravado em fita. Para dar suporte a essa funcionalidade, o MSDV tem um pino de entrada que pode receber um fluxo DV intercalado. Quando o pino de entrada está conectado, o MSDV atua como um filtro de renderização em vez de um filtro de captura. O MSDV não dá suporte à busca nesse modo. Para obter mais informações sobre como enviar DV para o dispositivo, consulte [Transmitir DV de arquivo para fita.](transmit-dv-from-file-to-tape.md)

![transmitindo dados dv para o dispositivo](images/dv-filters5.png)

Observe que os pinos de entrada e saída não podem ser conectados ao mesmo tempo, porque o dispositivo não pode transmitir em ambas as direções ao mesmo tempo.

Em muitas câmeras, alternar entre o modo VTR e o modo de câmera faz com que o dispositivo seja desligado. Portanto, DirectShow pode perder o dispositivo quando o usuário alterna os modos. Para obter informações sobre eventos de remoção de dispositivo, consulte [Notificação de remoção de dispositivo](device-removal-notification.md).

## <a name="remarks"></a>Comentários

Para obter informações sobre quais formatos DV são suportados pelo driver MSDV, consulte [**Subtipos de vídeo DV**](dv-video-subtypes.md).

Algumas dicas sobre como criar grafos de filtro com MSDV:

-   Não é possível usar [**IGraphBuilder::Render para**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) renderizar um pino de saída no MSDV. (O Gerenciador Graph filtro tenta conectar o pino de saída ao pino de entrada do MSDV, o que falha.) Em vez disso, [**use IGraphBuilder::Conexão**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) [**ou ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).
-   Quando um grafo de filtro contém MSDV, o MSDV deve fornecer o relógio de referência para o grafo. A partir do DirectX 8.0, o Gerenciador Graph Filtro escolherá automaticamente o MSDV como o relógio de referência. Com versões anteriores, você deve chamar o método [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) no Gerenciador Graph Filtro. Para obter mais informações sobre relógios, consulte [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).
-   Dependendo do dispositivo, alguns métodos em **IAMExtDevice,** **IAMExtTransport** e **IAMTimeCodeReader** podem retornar códigos de erro Windows em vez de valores **HRESULT.** Os códigos de erro possíveis incluem o seguinte.

    | Código do Erro              | Descrição                                                                                      |
    |-------------------------|--------------------------------------------------------------------------------------------------|
    | TEMPO \_ DE TEMPO DE ERRO          | Um comando de dispositivo externo passou do tempo.                                                        |
    | ERROR \_ REQ \_ NOT \_ ACCEP  | O dispositivo não aceitou esse comando de dispositivo externo.                                          |
    | ERRO \_ SEM \_ SUPORTE   | O dispositivo não dá suporte a esse comando de dispositivo externo.                                        |
    | SOLICITAÇÃO \_ DE \_ ERRO ANULADA | Um comando de dispositivo externo foi anulado. Possivelmente, o dispositivo foi removido ou ocorreu uma redefinição de barramento. |

    

     

### <a name="device-information"></a>Informações do dispositivo

No Windows Edition e Windows XP, o moniker do dispositivo do filtro DV dá suporte a uma propriedade **Description** além da **propriedade FriendlyName.** Essa propriedade retorna uma descrição do dispositivo, retirada do arquivo INF, que geralmente contém o nome da marca do dispositivo. No entanto, essa propriedade não tem suporte para todos os modelos de dispositivo.

Para obter mais informações sobre monikers de dispositivo, consulte [Usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).

### <a name="clock-times"></a>Horas do Relógio

O driver MSDV usa o relógio do barramento 1394 contido nos pacotes de dados 1394 para derivar o relógio. Ele usa esses valores para carimbo de data/hora dos exemplos de mídia DV. Como esse relógio de origem não é o relógio do sistema do computador, os tempos acabarão se desgarrapando do relógio do sistema do computador. No entanto, conforme mencionado acima, por padrão, o Gerenciador Graph Filtro selecionará MSDV como o relógio de referência do grafo.

A interface [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) relata a medida atual do driver de quadros descartados; Esse valor pode não ser perfeitamente sincronizado com o número real de quadros descartados em um determinado momento. Se os quadros são descartados, indica que o sistema não está balanceado (a produção de dados excede o consumo de dados). Por exemplo, o disco rígido do usuário pode não ser rápido o suficiente para dar suporte a taxas de captura dv.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



