---
description: Windows GDI+ fornece a classe Image e a classe Bitmap para armazenar imagens na memória e manipular imagens na memória.
ms.assetid: f9a5b4b1-4e25-42c8-a96b-a3104841e5f3
title: Usando codificadores e decodificadores de imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c3509b8fc48ff8c9ef2c52093a6fd06a4349602c6e904df24cf7e528e9f8e34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977276"
---
# <a name="using-image-encoders-and-decoders"></a>Usando codificadores e decodificadores de imagem

Windows GDI+ fornece a [**classe Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e a classe [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) para armazenar imagens na memória e manipular imagens na memória. GDI+ grava imagens em arquivos de disco com a ajuda de codificadores de imagem e carrega imagens de arquivos de disco com a ajuda de decodificadores de imagem. Um codificador converte os dados em um objeto **Image** ou **Bitmap** em um formato de arquivo de disco designado. Um decodificador converte os dados em um arquivo de disco para o formato exigido pelos objetos **Image** **e Bitmap.** GDI+ tem codificadores e decodificadores integrados que suportam os seguintes tipos de arquivo:

-   BMP
-   GIF
-   JPEG
-   PNG
-   TIFF

GDI+ também tem decodificadores integrados que suportam os seguintes tipos de arquivo:

-   WINDOWS MANAGEMENT FRAMEWORK
-   EMF
-   ICON

Os tópicos a seguir abordam os codificadores e decodificadores mais detalhadamente:

-   [Listando codificadores instalados](-gdiplus-listing-installed-encoders-use.md)
-   [Listando decodificadores instalados](-gdiplus-listing-installed-decoders-use.md)
-   [Recuperando o identificador de classe para um codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)
-   [Determinando os parâmetros com suporte por um codificador](-gdiplus-determining-the-parameters-supported-by-an-encoder-use.md)
-   [Convertendo uma imagem BMP em uma imagem PNG](-gdiplus-converting-a-bmp-image-to-a-png-image-use.md)
-   [Definindo o nível de compactação JPEG](-gdiplus-setting-jpeg-compression-level-use.md)
-   [Transformando uma imagem JPEG sem perda de informações](-gdiplus-transforming-a-jpeg-image-without-loss-of-information-use.md)
-   [Criar e salvar uma imagem de vários quadros](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)
-   [Copiando quadros individuais de uma Multiple-Frame imagem](-gdiplus-copying-individual-frames-from-a-multiple-frame-image-use.md)

 

 



