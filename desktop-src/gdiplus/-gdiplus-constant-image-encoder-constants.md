---
description: 'Os métodos Image:: Save Methods e Image:: SaveAdd Methods da classe Image recebem um objeto EncoderParameters que contém uma matriz de objetos EncoderParameter.'
ms.assetid: babc89f0-aea5-4341-8cf9-40d11e73fb10
title: Constantes do codificador de imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8130b90ad7f1d559ca480a581a0b157ff152fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165475"
---
# <a name="image-encoder-constants"></a>Constantes do codificador de imagem

Os métodos [Image:: Save Methods](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) e [Image:: SaveAdd Methods](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) da classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) recebem um objeto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) que contém uma matriz de objetos [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) . Cada objeto **EncoderParameter** tem um membro de dados GUID que especifica a categoria de parâmetro. As constantes a seguir, definidas em Gdiplusimaging. h, representam GUIDs que especificam as várias categorias de parâmetro.

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

 

 
