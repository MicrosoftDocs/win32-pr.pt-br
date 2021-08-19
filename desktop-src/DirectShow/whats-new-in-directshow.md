---
description: Novidades no DirectShow
ms.assetid: 675a34d4-7a33-4125-86af-cd4ed73ad430
title: Novidades no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd05d11931d7c23a078643724b99dfed84b65e3a7db3e4ed60df9cd2a3273f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071880"
---
# <a name="whats-new-in-directshow"></a>Novidades no DirectShow

## <a name="whats-new-for-directshow-in-windows-7"></a>Novidades do DirectShow no Windows 7

Novas interfaces:

-   [**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling)
-   [**IAMPluginControl**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol)

Filtros novos ou atualizados:

-   [**Decodificador de áudio Microsoft MPEG-1/DD/AAC**](microsoft-mpeg-1-dd-audio-decoder.md)
-   [**Decodificador de vídeo do Microsoft MPEG-2**](microsoft-mpeg-2-video-decoder.md)

Os algoritmos de "conexão inteligente" foram modificados para dar suporte a filtros preferenciais e bloqueados. Para obter detalhes, consulte [Intelligent Conexão](intelligent-connect.md).

Reprodução de DVD: novas opções para o [**método IDvdControl2::SetOption.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption)

## <a name="whats-new-for-directshow-in-windows-vista"></a>Novidades do DirectShow no Windows Vista

-   DirectShow agora faz parte do SDK do Windows. Os DirectShow, bibliotecas, exemplos e ferramentas não estão mais incluídos no SDK do DirectX.
-   A DXVA (Aceleração de Vídeo) 2.0 do DirectX contém muitas melhorias do DXVA 1.0.

    -   O pipeline de vídeo de hardware foi significativamente aprimorado.
    -   Componentes como decodificadores podem acessar o DXVA 2.0 diretamente sem se comunicar por meio do renderador de vídeo.
    -   O Gerenciador de Dispositivos Direct3D permite que os componentes compartilhem o mesmo dispositivo Direct3D.

    Para obter mais informações sobre o DXVA 2.0, consulte a documentação aceleração de vídeo [do DirectX 2.0,](../medfound/directx-video-acceleration-2-0.md) que faz parte [da documentação Microsoft Media Foundation](../medfound/microsoft-media-foundation-sdk.md) dados.

-   O [**EVR (Renderização**](enhanced-video-renderer-filter.md) de Vídeo Aprimorado) é um novo renderador de vídeo poderoso, que compartilha o mesmo modelo de plug-in que a Media Foundation versão do EVR. Para obter mais informações sobre o EVR, consulte a [documentação Microsoft Media Foundation](../medfound/microsoft-media-foundation-sdk.md) dados.
-   Suporte para Windows WDDM (Modelo de Driver de Exibição) do Vista. Esse recurso permite que os filtros aproveitem ao máximo as placas de vídeo com captura de vídeo integrada, a fim de reduzir cópias desnecessárias entre a memória do vídeo e a memória do sistema. Para obter mais informações, [consulte Using WDDM Capture in DirectShow](using-wddm-capture-in-directshow.md).
-   O decodificador de áudio MPEG-1 Camada II agora usa aritmética de ponto flutuante para melhorar a qualidade da decodificação.
-   Aprimoramentos de reprodução de DVD. Para obter detalhes, consulte [Aprimoramentos de](dvd-playback-enhancements-in-windows-vista.md)reprodução de DVD Windows Vista .
    -   Melhor suporte ao modo de truques: transições suaves entre taxas; faz a transição entre reprodução inversa e de avanço; suporte para reprodução de áudio durante o avanço rápido e o inverso.
    -   Cache aprimorado. Os aplicativos podem definir quantos dados o Navegador de DVD lê com antecedência. Definir um cache maior pode estender a vida útil da bateria e habilitar a reprodução silenciosa (após a unidade ficar inoclitada). Para obter mais informações, consulte [**SINALIZADOR DE OPÇÃO DE \_ \_ DVD**](/windows/win32/api/strmif/ne-strmif-dvd_option_flag).
-   Dispositivos de ponto de extremidade de áudio: os aplicativos podem associar o Filtro do [Renderador DirectSound](directsound-renderer-filter.md) a um dispositivo de ponto de extremidade de áudio específico. Os aplicativos podem usar a API dispositivo multimídia (MMDevice) para enumerar e selecionar o dispositivo de ponto de extremidade. Para obter mais informações, consulte a documentação da API de Áudio Principal Windows SDK.
-   Os seguintes filtros foram removidos do Windows Vista:
    -   [Filtro do filtro de filtro de ip do BDA](/previous-versions/windows/desktop/mstv/bda-ip-sink-filter)
    -   [Filtro de deframer BDA SLIP](/previous-versions/windows/desktop/mstv/bda-slip-deframer-filter)
    -   [Filtro de decodificador CC](cc-decoder-filter.md)
    -   [Filtro codec de VBI NABTS/FEC](/previous-versions/windows/desktop/mstv/nabts-fec-vbi-codec-filter)
    -   [Filtro de descompactador QT](qt-decompressor-filter.md)
    -   [Filtro do Analisador de Filme de QuickTime](quicktime-movie-parser-filter.md)
    -   [Filtro codec do WST](wst-codec-filter.md)
    -   [Filtro de decodificador WST](wst-decoder-filter.md)
-   O código de proxy/stub para muitas das interfaces DirectShow foi movido de quartz.dll para proppage.dll. Esse código foi removido do quartz.dll porque não foi destinado ao uso por aplicativos. No entanto, é útil para depuração, pois permite que um aplicativo de teste se conecte remotamente a um DirectShow de filtro em outro processo. Para usar esse recurso no Windows Vista, você deve primeiro registrar proppage.dll. Essa DLL está disponível no diretório Windows ferramentas do SDK. (Para obter mais informações, [consulte Carregando um Graph de um processo externo](loading-a-graph-from-an-external-process.md).)

 

 
