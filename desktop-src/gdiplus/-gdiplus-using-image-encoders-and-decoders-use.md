---
description: O Windows GDI+ fornece a classe Image e a classe bitmap para armazenar imagens na memória e manipular imagens na memória.
ms.assetid: f9a5b4b1-4e25-42c8-a96b-a3104841e5f3
title: Usando codificadores de imagem e decodificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c55c75e00b3d624d27ba888ae26afb3a5ee0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090322"
---
# <a name="using-image-encoders-and-decoders"></a>Usando codificadores de imagem e decodificadores

O Windows GDI+ fornece a classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e a classe [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) para armazenar imagens na memória e manipular imagens na memória. O GDI+ grava imagens em arquivos de disco com a ajuda de codificadores de imagem e carrega imagens de arquivos de disco com a ajuda de decodificadores de imagem. Um codificador converte os dados em um objeto de **imagem** ou **bitmap** em um formato de arquivo de disco designado. Um decodificador traduz os dados em um arquivo de disco para o formato exigido pelos objetos **Image** e **bitmap** . O GDI+ tem codificadores internos e decodificadores que dão suporte aos seguintes tipos de arquivo:

-   BMP
-   GIF
-   JPEG
-   PNG
-   TIFF

O GDI+ também tem decodificadores internos que dão suporte aos seguintes tipos de arquivo:

-   WINDOWS MANAGEMENT FRAMEWORK
-   EMF
-   ICON

Os tópicos a seguir abordam os codificadores e decodificadores mais detalhadamente:

-   [Listando codificadores instalados](-gdiplus-listing-installed-encoders-use.md)
-   [Listando decodificadores instalados](-gdiplus-listing-installed-decoders-use.md)
-   [Recuperando o identificador de classe para um codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)
-   [Determinando os parâmetros com suporte de um codificador](-gdiplus-determining-the-parameters-supported-by-an-encoder-use.md)
-   [Convertendo uma imagem BMP em uma imagem PNG](-gdiplus-converting-a-bmp-image-to-a-png-image-use.md)
-   [Definindo o nível de compactação JPEG](-gdiplus-setting-jpeg-compression-level-use.md)
-   [Transformando uma imagem JPEG sem perda de informações](-gdiplus-transforming-a-jpeg-image-without-loss-of-information-use.md)
-   [Criar e salvar uma imagem de vários quadros](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)
-   [Copiando quadros individuais de uma imagem de Multiple-Frame](-gdiplus-copying-individual-frames-from-a-multiple-frame-image-use.md)

 

 



