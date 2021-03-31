---
title: Referência de captura de vídeo
description: Referência de captura de vídeo
ms.assetid: 5356c575-2a59-4459-b4eb-76967deb6877
keywords:
- Video for Windows (VFW), referência de captura de vídeo
- VFW (vídeo para Windows), referência de captura de vídeo
- AVICap, referência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cef19834e244f6070a1d8bb3383dcac017e4d161
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005116"
---
# <a name="video-capture-reference"></a>Referência de captura de vídeo

Esta seção descreve as funções, estruturas, mensagens e macros associadas à classe de janela AVICap. Esses elementos são agrupados da seguinte maneira.

## <a name="basic-capture-operations"></a>Operações básicas de captura

-   [**capCreateCaptureWindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa)
-   [**\_abortar Cap do WM \_**](wm-cap-abort.md)
-   [**conexão do driver do WM \_ Cap \_ \_**](wm-cap-driver-connect.md)
-   [**\_sequência de Cap do WM \_**](wm-cap-sequence.md)
-   [**\_parada da Cap do WM \_**](wm-cap-stop.md)

## <a name="capture-windows"></a>Capturar janelas

-   [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus)
-   [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona)
-   [**conexão do driver do WM \_ Cap \_ \_**](wm-cap-driver-connect.md)
-   [**desconexão do driver do WM \_ Cap \_ \_**](wm-cap-driver-disconnect.md)
-   [**STATUS da obtenção do WM \_ Cap \_ \_**](wm-cap-get-status.md)

## <a name="capture-drivers"></a>Drivers de captura

-   [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)
-   [**Driver do WM \_ Cap \_ \_ obter \_ Caps**](wm-cap-driver-get-caps.md)
-   [**\_nome de \_ obtenção do driver \_ \_ do WM Cap**](wm-cap-driver-get-name.md)
-   [**\_ \_ \_ versão get do driver \_ do WM Cap**](wm-cap-driver-get-version.md)
-   [**introdução do WM \_ Cap \_ \_ AUDIOFORMAT**](wm-cap-get-audioformat.md)
-   [**introdução do WM \_ Cap \_ \_ VIDEOFORMAT**](wm-cap-get-videoformat.md)
-   [**WM \_ Cap \_ set \_ AUDIOFORMAT**](wm-cap-set-audioformat.md)
-   [**WM \_ Cap \_ set \_ VIDEOFORMAT**](wm-cap-set-videoformat.md)

## <a name="capture-driver-preview-and-overlay-modes"></a>Capturar os modos de visualização e sobreposição do driver

-   [**sobreposição de conjunto de Cap do WM \_ \_ \_**](wm-cap-set-overlay.md)
-   [**\_visualização do \_ conjunto de Cap do WM \_**](wm-cap-set-preview.md)
-   [**WM \_ Cap \_ set \_ PREVIEWRATE**](wm-cap-set-previewrate.md)
-   [**\_escala de \_ conjunto de Cap do WM \_**](wm-cap-set-scale.md)
-   [**\_ \_ rolagem do conjunto de Cap do WM \_**](wm-cap-set-scroll.md)

## <a name="capture-driver-video-dialog-boxes"></a>Caixas de diálogo de vídeo do driver de captura

-   [**WM \_ Cap \_ DLG \_ VIDEOCOMPRESSION**](wm-cap-dlg-videocompression.md)
-   [**WM \_ Cap \_ DLG \_ VIDEODISPLAY**](wm-cap-dlg-videodisplay.md)
-   [**WM \_ Cap \_ DLG \_ VIDEOFORMAT**](wm-cap-dlg-videoformat.md)
-   [**visualização do WM \_ Cap de \_ DLG \_**](wm-cap-dlg-videosource.md)

## <a name="audio-format"></a>Formato de áudio

-   [**introdução do WM \_ Cap \_ \_ AUDIOFORMAT**](wm-cap-get-audioformat.md)
-   [**WM \_ Cap \_ set \_ AUDIOFORMAT**](wm-cap-set-audioformat.md)

## <a name="video-capture-settings"></a>Configurações de captura de vídeo

-   [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [**\_configuração da \_ \_ sequência get \_ do WM Cap**](wm-cap-get-sequence-setup.md)
-   [**configuração da sequência do WM \_ Cap \_ set \_ \_**](wm-cap-set-sequence-setup.md)

## <a name="capture-file-and-buffers"></a>Arquivos de captura e buffers

-   [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [**\_ \_ alocar arquivo do WM Cap \_**](wm-cap-file-allocate.md)
-   [**arquivo \_ de \_ \_ captura de \_ obter \_ arquivo do WM Cap**](wm-cap-file-get-capture-file.md)
-   [**\_ \_ salvar arquivo do WM Cap \_**](wm-cap-file-saveas.md)
-   [**\_arquivo de \_ captura do conjunto de arquivos \_ \_ do WM Cap \_**](wm-cap-file-set-capture-file.md)

## <a name="directly-using-capture-data"></a>Usando dados de captura diretamente

-   [**Cadeia de extremidade do WM \_ \_ \_ nofile**](wm-cap-sequence-nofile.md)

## <a name="capture-from-mci-device"></a>Capturar do dispositivo MCI

-   [**WM \_ Cap \_ set \_ MCI \_ Device**](wm-cap-set-mci-device.md)

## <a name="manual-frame-capture"></a>Captura de quadro manual

-   [**\_ \_ quadro único do WM Cap \_**](wm-cap-single-frame.md)
-   [**\_fechamento de \_ \_ quadro único \_ do WM Cap**](wm-cap-single-frame-close.md)
-   [**\_quadro único do WM Cap \_ \_ \_ aberto**](wm-cap-single-frame-open.md)

## <a name="still-image-capture"></a>Captura de Still-Image

-   [**\_cópia de \_ edição da Cap do WM \_**](wm-cap-edit-copy.md)
-   [**SAVEDIB do arquivo do WM \_ Cap \_ \_**](wm-cap-file-savedib.md)
-   [**\_quadro de \_ captura da Cap do WM \_**](wm-cap-grab-frame.md)
-   [**quadro de captura da Cap do WM \_ \_ \_ \_ nostop**](wm-cap-grab-frame-nostop.md)

## <a name="advanced-capture-options"></a>Opções avançadas de captura

-   [**\_INFOCHUNK do \_ conjunto de arquivos \_ \_ do WM Cap**](wm-cap-file-set-infochunk.md)
-   [**o \_ WM \_ Cap \_ Obtém \_ dados do usuário**](wm-cap-get-user-data.md)
-   [**WM \_ Cap \_ definir \_ dados do usuário \_**](wm-cap-set-user-data.md)

## <a name="working-with-palettes"></a>Trabalhando com paletas

-   [**\_cópia de \_ edição da Cap do WM \_**](wm-cap-edit-copy.md)
-   [**\_criação de \_ AutoCriar do WM Cap PAL \_**](wm-cap-pal-autocreate.md)
-   [**WM \_ Cap \_ PAL \_ MANUALCREATE**](wm-cap-pal-manualcreate.md)
-   [**\_PAL Cap do WM \_ \_ aberto**](wm-cap-pal-open.md)
-   [**\_colar da \_ PAL da Cap do WM \_**](wm-cap-pal-paste.md)
-   [**\_salvar proteção \_ PAL do WM \_**](wm-cap-pal-save.md)

## <a name="yielding-to-other-applications"></a>Respondendo a outros aplicativos

-   [**\_configuração da \_ \_ sequência get \_ do WM Cap**](wm-cap-get-sequence-setup.md)
-   [**o \_ \_ retorno de \_ chamada de Set Cap do WM \_**](wm-cap-set-callback-yield.md)
-   [**configuração da sequência do WM \_ Cap \_ set \_ \_**](wm-cap-set-sequence-setup.md)

## <a name="avicap-callback-functions"></a>Funções de retorno de chamada AVICap

-   [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback)
-   [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka)
-   [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka)
-   [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback)
-   [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback)
-   [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback)
-   [**WM \_ Cap \_ set \_ callback \_ CAPCONTROL**](wm-cap-set-callback-capcontrol.md)
-   [**\_erro de \_ retorno de \_ chamada de Set Cap \_ do WM**](wm-cap-set-callback-error.md)
-   [**\_quadro de \_ retorno de \_ chamada Set \_ Cap do WM**](wm-cap-set-callback-frame.md)
-   [**WM \_ Cap \_ definir \_ status de retorno de chamada \_**](wm-cap-set-callback-status.md)
-   [**WM \_ Cap \_ set \_ callback \_ VIDEOSTREAM**](wm-cap-set-callback-videostream.md)
-   [**\_WAVESTREAM de \_ retorno de \_ chamada de Set Cap \_ do WM**](wm-cap-set-callback-wavestream.md)
-   [**o \_ \_ retorno de \_ chamada de Set Cap do WM \_**](wm-cap-set-callback-yield.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 




