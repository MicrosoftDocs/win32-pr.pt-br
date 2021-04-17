---
description: O que há de novo no DirectShow
ms.assetid: 675a34d4-7a33-4125-86af-cd4ed73ad430
title: O que há de novo no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74747349848a7b370cd4766113085c84d0c7a1d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754688"
---
# <a name="whats-new-in-directshow"></a>O que há de novo no DirectShow

## <a name="whats-new-for-directshow-in-windows-7"></a>O que há de novo no DirectShow no Windows 7

Novas interfaces:

-   [**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling)
-   [**IAMPluginControl**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol)

Filtros novos ou atualizados:

-   [**Decodificador de áudio do Microsoft MPEG-1/DD/AAC**](microsoft-mpeg-1-dd-audio-decoder.md)
-   [**Decodificador de vídeo do Microsoft MPEG-2**](microsoft-mpeg-2-video-decoder.md)

Os algoritmos "conexão inteligente" foram modificados para dar suporte a filtros preferenciais e bloqueados. Para obter detalhes, consulte [conexão inteligente](intelligent-connect.md).

Reprodução de DVD: novas opções para o método [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) .

## <a name="whats-new-for-directshow-in-windows-vista"></a>O que há de novo no DirectShow no Windows Vista

-   O DirectShow agora faz parte do SDK do Windows. Os cabeçalhos, as bibliotecas, as amostras e as ferramentas do DirectShow não são mais incluídas no SDK do DirectX.
-   A DXVA (DirectX Video Acceleration) 2,0 contém muitos aprimoramentos do DXVA 1,0.

    -   O pipeline de vídeo de hardware foi significativamente melhorado.
    -   Componentes como decodificadores podem acessar o DXVA 2,0 diretamente sem se comunicar por meio do processador de vídeo.
    -   O Direct3D Gerenciador de Dispositivos permite que os componentes compartilhem o mesmo dispositivo Direct3D.

    Para obter mais informações sobre o DXVA 2,0, consulte a documentação do [DirectX Video Acceleration 2,0](../medfound/directx-video-acceleration-2-0.md) , que faz parte da documentação do [Microsoft Media Foundation](../medfound/microsoft-media-foundation-sdk.md) .

-   O EVR ( [**processador de vídeo avançado**](enhanced-video-renderer-filter.md) ) é um novo processador de vídeo poderoso, que compartilha o mesmo modelo de plug-in que a versão Media Foundation do EVR. Para obter mais informações sobre o EVR, consulte a documentação do [Microsoft Media Foundation](../medfound/microsoft-media-foundation-sdk.md) .
-   Suporte para a captura do Windows Vista Display Driver Model (WDDM). Esse recurso permite que os filtros aproveitem ao máximo as placas de vídeo com a captura de vídeo integrada para reduzir as cópias desnecessárias entre a memória de vídeo e a memória do sistema. Para obter mais informações, consulte [usando a captura do WDDM no DirectShow](using-wddm-capture-in-directshow.md).
-   O decodificador de áudio MPEG-1 Layer II agora usa aritmética de ponto flutuante, para melhor qualidade de decodificação.
-   Aprimoramentos na reprodução de DVD. Para obter detalhes, consulte [aprimoramentos de reprodução de DVD no Windows Vista](dvd-playback-enhancements-in-windows-vista.md).
    -   Melhor suporte ao modo de vazar: transições suaves entre tarifas; transições entre a reprodução direta e inversa; suporte para reprodução de áudio durante avanço e reversão.
    -   Cache aprimorado. Os aplicativos podem definir a quantidade de dados que o navegador de DVD lê antecipadamente. Definir um cache maior pode estender a vida útil da bateria e habilitar a reprodução silenciosa (depois que a unidade for desativada). Para obter mais informações, [**consulte \_ \_ sinalizador de opção de DVD**](/windows/win32/api/strmif/ne-strmif-dvd_option_flag).
-   Dispositivos de ponto de extremidade de áudio: os aplicativos podem associar o [filtro de renderizador DirectSound](directsound-renderer-filter.md) a um dispositivo de ponto de extremidade de áudio específico. Os aplicativos podem usar a API do dispositivo de multimídia (MMDevice) para enumerar e selecionar o dispositivo de ponto de extremidade. Para obter mais informações, consulte a documentação da API de áudio principal no SDK do Windows.
-   Os seguintes filtros foram removidos do Windows Vista:
    -   [Filtro de coletor de IP BDA](/previous-versions/windows/desktop/mstv/bda-ip-sink-filter)
    -   [Filtro de desestruturação de guias BDA](/previous-versions/windows/desktop/mstv/bda-slip-deframer-filter)
    -   [Filtro de decodificador de CC](cc-decoder-filter.md)
    -   [Filtro de codec VBI NABTS/FEC](/previous-versions/windows/desktop/mstv/nabts-fec-vbi-codec-filter)
    -   [Filtro de descompactação de QT](qt-decompressor-filter.md)
    -   [Filtro do analisador de filmes QuickTime](quicktime-movie-parser-filter.md)
    -   [Filtro de codec de WST](wst-codec-filter.md)
    -   [Filtro de decodificador de WST](wst-decoder-filter.md)
-   O código de proxy/stub para muitas das interfaces do DirectShow foi movido de quartz.dll para proppage.dll. Esse código foi removido da quartz.dll porque ele não foi desenvolvido para uso por aplicativos. No entanto, ele é útil para depuração, pois permite que um aplicativo de teste se conecte remotamente a um grafo de filtro do DirectShow em outro processo. Para usar esse recurso no Windows Vista, primeiro você deve registrar proppage.dll. Essa DLL está disponível no diretório de ferramentas de SDK do Windows. (Para obter mais informações, consulte [carregando um grafo de um processo externo](loading-a-graph-from-an-external-process.md).)

 

 
