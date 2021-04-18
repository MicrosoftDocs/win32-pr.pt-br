---
description: Driver MSDV
ms.assetid: 146ca753-fe41-49d3-8b1c-077e10a28192
title: Driver MSDV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b7c1bda24980abe84a11613126476ccfe35380d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370065"
---
# <a name="msdv-driver"></a>Driver MSDV

MSDV é o driver Microsoft Windows Driver Model (WDM) para DV camcorders. O driver aparece como um filtro do DirectShow quando o dispositivo está conectado. Ele é enumerado em duas categorias de filtro:

-   CLSID \_ VideoInputDeviceCategory ("fontes de captura de vídeo")
-   \_KSCATEGORY \_ de renderização ("dispositivos de renderização de streaming WDM")

O nome amigável do filtro é `Microsoft DV Camera and VCR` ou um equivalente localizado. Em alguns dispositivos, a propriedade **Description** contém uma descrição do modelo específico, que pode ser usado em vez do nome amigável genérico. Para obter mais informações, consulte [selecionando um dispositivo de captura](selecting-a-capture-device.md).

MSDV tem dois Pins de saída. Um PIN fornece quadros de DV que contêm dados intercalados de áudio e vídeo. O outro PIN fornece quadros somente de vídeo sem áudio. MSDV não pode transmitir de ambos os Pins de uma vez, de modo que apenas um PIN de saída pode ser conectado por vez. Para obter mais informações sobre como capturar vídeo de um dispositivo DV, consulte [capturar DV para o arquivo](capture-dv-to-file.md).

![capturando dados de DV do dispositivo](images/dv-filters4.png)

A maioria das camcorders DV tem uma subunidade VTR (gravador de fita de vídeo), que pode transmitir dados de fita para o computador. Para o aplicativo, a captura de fita funciona da mesma forma que a captura de vídeo ao vivo. A única diferença é que o aplicativo deve controlar o transporte de fita externa — iniciar e parar a fita, retroceder e assim por diante. Para essa finalidade, o MSDV expõe as interfaces [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)e [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) . Para obter mais informações sobre como controlar um VTR, consulte [controlando uma camcorder DV](controlling-a-dv-camcorder.md).

Você também pode transmitir DV do computador para a camcorder. O vídeo pode ser exibido na tela de integração da camcorder ou gravado em fita. Para dar suporte a essa funcionalidade, MSDV tem um pino de entrada que pode receber um fluxo de DV intercalado. Quando o pino de entrada está conectado, MSDV atua como um filtro de renderizador em vez de um filtro de captura. MSDV não dá suporte a busca nesse modo. Para obter mais informações sobre como enviar DV para o dispositivo, consulte [transmitir DV de arquivo para fita](transmit-dv-from-file-to-tape.md).

![transmitindo dados de DV para o dispositivo](images/dv-filters5.png)

Observe que os Pins de entrada e de saída não podem ser conectados ao mesmo tempo, porque o dispositivo não pode transmitir em ambas as direções ao mesmo tempo.

Em muitas camcorders, alternar entre o modo de VTR e o modo de câmera faz com que o dispositivo seja desligado. Portanto, o DirectShow pode perder o dispositivo quando o usuário alternar entre os modos. Para obter informações sobre eventos de remoção de dispositivo, consulte [notificação de remoção de dispositivo](device-removal-notification.md).

## <a name="remarks"></a>Comentários

Para obter informações sobre quais formatos de DV são suportados pelo driver MSDV, consulte [**subtipos de vídeo DV**](dv-video-subtypes.md).

Algumas dicas sobre a criação de gráficos de filtro com o MSDV:

-   Você não pode usar [**IGraphBuilder:: render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) para processar um pino de saída em MSDV. (O Gerenciador do grafo de filtro tenta conectar o pino de saída ao pino de entrada do MSDV, que falha.) Em vez disso, use [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) ou [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).
-   Quando um grafo de filtro contém MSDV, MSDV deve fornecer o relógio de referência para o grafo. A partir do DirectX 8,0, o Gerenciador de gráfico de filtro escolherá automaticamente MSDV como o relógio de referência. Com versões anteriores, você deve chamar o método [**IMediaFilter:: Setsincronizate**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) no Gerenciador do grafo de filtro. Para obter mais informações sobre relógios, consulte [tempo e relógios no DirectShow](time-and-clocks-in-directshow.md).
-   Dependendo do dispositivo, alguns métodos em **IAMExtDevice**, **IAMExtTransport** e **IAMTimeCodeReader** podem retornar códigos de erro do Windows em vez de valores **HRESULT** . Os códigos de erro possíveis incluem o seguinte.

    | Código do Erro              | Descrição                                                                                      |
    |-------------------------|--------------------------------------------------------------------------------------------------|
    | \_tempo limite do erro          | Um comando de dispositivo externo atingiu o tempo limite.                                                        |
    | Req. de erro \_ \_ não \_ ACCEP  | O dispositivo não aceitou este comando de dispositivo externo.                                          |
    | ERRO \_ sem \_ suporte   | O dispositivo não dá suporte a este comando de dispositivo externo.                                        |
    | solicitação de erro \_ \_ anulada | Um comando de dispositivo externo foi anulado. Possivelmente, o dispositivo foi removido ou uma redefinição de barramento ocorreu. |

    

     

### <a name="device-information"></a>Informações do dispositivo

No Windows Millennium Edition e no Windows XP, o moniker do dispositivo do filtro DV dá suporte a uma propriedade **Description** , além da propriedade **FriendlyName** . Essa propriedade retorna uma descrição do dispositivo, extraída do arquivo INF, que geralmente contém o nome da marca do dispositivo. No entanto, essa propriedade não tem suporte em todos os modelos de dispositivo.

Para obter mais informações sobre monikers de dispositivo, consulte [usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).

### <a name="clock-times"></a>Horas de relógio

O driver MSDV usa o relógio de barramento 1394 que está contido nos pacotes de dados 1394 para derivar o relógio. Ele usa esses valores para carimbar o tempo dos exemplos de mídia DV. Como esse relógio de origem não é o relógio do sistema do computador, os horários eventualmente serão descompassos do relógio do sistema do computador. Como observado acima, no entanto, por padrão, o Gerenciador do grafo de filtro selecionará MSDV como o relógio de referência do grafo.

A interface [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) relata a medida atual do driver dos quadros descartados; Esse valor pode não estar perfeitamente sincronizado com o número real de quadros descartados em um determinado momento. Se os quadros forem descartados, isso indica que o sistema não está balanceado (a produção de dados excede o consumo de dados). Por exemplo, o disco rígido do usuário pode não ser rápido o suficiente para dar suporte a taxas de captura de DV.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



