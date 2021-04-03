---
title: Trabalhando com dados de vídeo compactados em um fluxo
description: Trabalhando com dados de vídeo compactados em um fluxo
ms.assetid: b701e072-f162-438f-b607-aea7491a02f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0587ee6c12a93eb014368642ba1605f546129e0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007442"
---
# <a name="working-with-compressed-video-data-in-a-stream"></a>Trabalhando com dados de vídeo compactados em um fluxo

O AVIFile fornece várias maneiras de acessar fluxos de vídeo compactados.

Se você quiser exibir um ou mais quadros de um fluxo de vídeo compactado, poderá recuperar os quadros usando a função [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) e encaminhar os dados do quadro compactado para o DrawDib Functions para exibi-los. As funções DrawDib podem exibir imagens de várias profundidades de imagem e pontilhar automaticamente imagens para exibições que não podem lidar com certos tipos de bitmaps independentes de dispositivo (DIBs). Essas funções funcionam com imagens compactadas e descompactadas. Para obter mais informações sobre as funções do DrawDib, consulte [funções do DrawDib](drawdib-functions.md).

O AVIFile fornece funções para descompactar um único quadro de vídeo. Para alocar recursos, use a função [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) . Essa função cria um buffer para os dados descompactados.

Você pode descompactar um único quadro de vídeo usando a função [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) . Essa função descompacta o quadro e recupera um quadro completo de dados de imagem, retornando o endereço do DIB na estrutura [BITMAPINFOHEADER](/previous-versions//ms532290(v=vs.85)) . Seu aplicativo pode exibir o DIB usando funções de desenho padrão ou usando as funções DrawDib.

Se seu aplicativo fizer chamadas sucessivas para **AVIStreamGetFrame**, a função substituirá seu buffer por cada quadro recuperado.

Quando você terminar de usar o **AVIStreamGetFrame** e o DIB descompactado estiver em seu buffer, poderá liberar os recursos alocados usando a função [**AVIStreamGetFrameClose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose) .

Para obter mais informações sobre como descompactar imagens, consulte [Gerenciador de compactação de vídeo](video-compression-manager.md).

 

 