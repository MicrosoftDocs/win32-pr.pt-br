---
description: Depois de iniciar a visualização de um fluxo de vídeo, chame o método IWiaVideo::TakePicture da interface IWiaVideo para capturar uma imagem still do vídeo de streaming.
ms.assetid: 2b8c465b-0dbf-4741-a701-200862cc3de3
title: Capturando uma imagem ainda de um fluxo de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af98dc313ddde7f2da160515ab53d31357a6d9cc96e1737ed01767b40fb0e7c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814276"
---
# <a name="capturing-a-still-image-from-a-video-stream"></a>Capturando uma imagem ainda de um fluxo de vídeo

Depois de iniciar a visualização de um fluxo de vídeo, chame o método [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) da interface [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) para capturar uma imagem still do vídeo de streaming. Para obter instruções sobre como obter um ponteiro **IWiaVideo** e começar a visualizar o vídeo de streaming, consulte [Visualizando o vídeo](-wia-previewing-video.md).

Quando o [**método IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) retorna, o parâmetro *pbstrNewImageFilename* contém o caminho completo e o nome do arquivo de imagem resultante. O arquivo está no formato JPEG. O diretório no qual o arquivo é criado é especificado pelo valor da propriedade [**IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) da interface [**IWiaVideo.**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo)

> [!Note]  
> Windows A WIA (Aquisição de Imagem) não dá suporte a dispositivos de vídeo Windows Server 2003, Windows Vista ou posterior. Para essas versões do Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) para adquirir imagens do vídeo.

 

 

 
