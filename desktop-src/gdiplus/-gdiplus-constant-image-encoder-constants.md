---
description: Os métodos Image::Save e Image::SaveAdd Methods da classe Image recebem um objeto EncoderParameters que contém uma matriz de objetos EncoderParameter.
ms.assetid: babc89f0-aea5-4341-8cf9-40d11e73fb10
title: Constantes do codificador de imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a47f533a490fe3428964c9e469df6fbe89800f95bfe89daf7bf05d6c49a75c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248880"
---
# <a name="image-encoder-constants"></a>Constantes do codificador de imagem

Os [métodos Image::Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) e [Image::SaveAdd Methods](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) da classe Image recebem um objeto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) que contém uma matriz de objetos [**EncoderParameter.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) [](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) Cada **objeto EncoderParameter** tem um membro de dados GUID que especifica a categoria de parâmetro. As constantes a seguir, definidas em Gdiplusimaging.h, representam GUIDs que especificam as várias categorias de parâmetro.

-   EncoderChrominanceTable
-   EncoderColorDepth
-   EncoderColorSpace
-   EncoderCompression
-   EncoderLuminanceTable
-   EncoderQuality
-   EncoderRenderMethod
-   EncoderSaveFlag
-   EncoderScanMethod
-   EncoderTransformation
-   EncoderVersion
-   EncoderImageItems
-   EncoderSaveAsCMYK

 

 
