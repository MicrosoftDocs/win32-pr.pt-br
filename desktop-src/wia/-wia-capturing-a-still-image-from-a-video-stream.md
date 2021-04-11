---
description: 'Após iniciar a visualização de um fluxo de vídeo, chame o método IWiaVideo:: TakePicture da interface IWiaVideo para capturar uma imagem ainda do vídeo de streaming.'
ms.assetid: 2b8c465b-0dbf-4741-a701-200862cc3de3
title: Capturando uma imagem ainda de um fluxo de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be475405f4aa9719514a531a6af0105d7a786f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169544"
---
# <a name="capturing-a-still-image-from-a-video-stream"></a>Capturando uma imagem ainda de um fluxo de vídeo

Após iniciar a visualização de um fluxo de vídeo, chame o método [**IWiaVideo:: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) da interface [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) para capturar uma imagem ainda do vídeo de streaming. Para obter instruções sobre como obter um ponteiro **IWiaVideo** e iniciar a visualização de vídeo de streaming, consulte [visualizando vídeo](-wia-previewing-video.md).

Quando o método [**IWiaVideo:: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) retorna, o parâmetro *pbstrNewImageFilename* contém o caminho completo e o nome do arquivo de imagem resultante. O arquivo está em formato JPEG. O diretório no qual o arquivo é criado é especificado pelo valor da propriedade [**IWiaVideo:: ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) da interface [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) .

> [!Note]  
> A aquisição de imagens do Windows (WIA) não oferece suporte a dispositivos de vídeo no Windows Server 2003, Windows Vista ou posterior. Para essas versões do Windows, use o [DirectShow](/previous-versions//ms783323(v=vs.85)) para adquirir imagens do vídeo.

 

 

 
