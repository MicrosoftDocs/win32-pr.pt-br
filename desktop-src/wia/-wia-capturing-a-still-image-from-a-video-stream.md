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
# <a name="capturing-a-still-image-from-a-video-stream"></a><span data-ttu-id="fda5b-103">Capturando uma imagem ainda de um fluxo de vídeo</span><span class="sxs-lookup"><span data-stu-id="fda5b-103">Capturing a Still Image from a Video Stream</span></span>

<span data-ttu-id="fda5b-104">Após iniciar a visualização de um fluxo de vídeo, chame o método [**IWiaVideo:: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) da interface [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) para capturar uma imagem ainda do vídeo de streaming.</span><span class="sxs-lookup"><span data-stu-id="fda5b-104">After beginning preview of a video stream, call the [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) method of the [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) interface to capture a still image from the streaming video.</span></span> <span data-ttu-id="fda5b-105">Para obter instruções sobre como obter um ponteiro **IWiaVideo** e iniciar a visualização de vídeo de streaming, consulte [visualizando vídeo](-wia-previewing-video.md).</span><span class="sxs-lookup"><span data-stu-id="fda5b-105">For instructions on how to get an **IWiaVideo** pointer and begin previewing streaming video, see [Previewing Video](-wia-previewing-video.md).</span></span>

<span data-ttu-id="fda5b-106">Quando o método [**IWiaVideo:: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) retorna, o parâmetro *pbstrNewImageFilename* contém o caminho completo e o nome do arquivo de imagem resultante.</span><span class="sxs-lookup"><span data-stu-id="fda5b-106">When the [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) method returns, the *pbstrNewImageFilename* parameter contains the full path and filename of the resulting image file.</span></span> <span data-ttu-id="fda5b-107">O arquivo está em formato JPEG.</span><span class="sxs-lookup"><span data-stu-id="fda5b-107">The file is in JPEG format.</span></span> <span data-ttu-id="fda5b-108">O diretório no qual o arquivo é criado é especificado pelo valor da propriedade [**IWiaVideo:: ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) da interface [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) .</span><span class="sxs-lookup"><span data-stu-id="fda5b-108">The directory in which the file is created is specified by the value of the [**IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) property of the [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) interface.</span></span>

> [!Note]  
> <span data-ttu-id="fda5b-109">A aquisição de imagens do Windows (WIA) não oferece suporte a dispositivos de vídeo no Windows Server 2003, Windows Vista ou posterior.</span><span class="sxs-lookup"><span data-stu-id="fda5b-109">Windows Image Acquisition (WIA) does not support video devices in Windows Server 2003, Windows Vista, or later.</span></span> <span data-ttu-id="fda5b-110">Para essas versões do Windows, use o [DirectShow](/previous-versions//ms783323(v=vs.85)) para adquirir imagens do vídeo.</span><span class="sxs-lookup"><span data-stu-id="fda5b-110">For those versions of the Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) to acquire images from video.</span></span>

 

 

 
