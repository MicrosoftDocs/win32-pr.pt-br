---
description: Para exibir uma imagem rasterizada (bitmap) na tela, você precisa de um objeto Image e de um objeto Graphics.
ms.assetid: 8c1a26d9-b640-4f38-8276-10c4464525f2
title: Carregando e exibindo bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: ab2405462db5017215893d50d93dc0b228633cfb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2021
ms.locfileid: "104968764"
---
# <a name="loading-and-displaying-bitmaps"></a>Carregando e exibindo bitmaps

Consulte também o [aplicativo de exemplo do WIC Viewer GDI+](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus).

Para exibir uma imagem rasterizada (bitmap) na tela, você precisa de um objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e de um objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Passe o nome de um arquivo (ou um ponteiro para um fluxo) para um construtor de **imagem** . Depois de criar um objeto **Image** , passe o endereço desse objeto **Image** para o método **DrawImage** de um objeto **Graphics** .

O exemplo a seguir cria um objeto de [**imagem**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) de um arquivo JPEG e, em seguida, desenha a imagem com seu canto superior esquerdo em (60, 10):

```cpp
Image image(L"Grapes.jpg");
graphics.DrawImage(&image, 60, 10);
```

A ilustração a seguir mostra a imagem desenhada no local especificado.

![captura de tela de uma janela que contém uma imagem, com um texto explicativo para o ponto de origem ](images/imageposition1.png)

A classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) fornece métodos básicos para carregar e exibir imagens rasterizadas e imagens vetoriais. A classe [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) , que herda da classe **Image** , fornece métodos mais especializados para carregar, exibir e manipular imagens rasterizadas. Por exemplo, você pode construir um objeto de **bitmap** a partir de um identificador de ícone (HICON).

O exemplo a seguir obtém um identificador para um ícone e, em seguida, usa esse identificador para construir um objeto de [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) . O código exibe o ícone passando o endereço do objeto de **bitmap** para o método **DrawImage** de um objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

```cpp
HICON hIcon = LoadIcon(NULL, IDI_APPLICATION);
Bitmap bitmap(hIcon);
graphics.DrawImage(&bitmap, 10, 10);
```

## <a name="see-also"></a>Confira também

[Aplicativo de exemplo do Visualizador de WIC GDI+](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus)
