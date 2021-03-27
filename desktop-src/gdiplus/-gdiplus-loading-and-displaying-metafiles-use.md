---
description: A classe Image fornece métodos básicos para carregar e exibir imagens rasterizadas e imagens vetoriais. A classe Metafile, que herda da classe Image, fornece métodos mais especializados para gravar, exibir e examinar imagens vetoriais.
ms.assetid: 79b8df1b-6fc5-455b-9d08-57d64bf6bffa
title: Carregando e exibindo metaarquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5dafe6ef92e80e8487b43a22f50b44c5decd360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010474"
---
# <a name="loading-and-displaying-metafiles"></a>Carregando e exibindo metaarquivos

A classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) fornece métodos básicos para carregar e exibir imagens rasterizadas e imagens vetoriais. A classe [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , que herda da classe **Image** , fornece métodos mais especializados para gravar, exibir e examinar imagens vetoriais.

Para exibir uma imagem de vetor (metarquivo) na tela, você precisa de um objeto de [**imagem**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e um objeto de [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Passe o nome de um arquivo (ou um ponteiro para um fluxo) para um construtor de **imagem** . Depois de criar um objeto **Image** , passe o endereço desse objeto **Image** para o método **DrawImage** de um objeto **Graphics** .

O exemplo a seguir cria um objeto de [**imagem**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) de um arquivo EMF (metarquivo avançado) e, em seguida, desenha a imagem com seu canto superior esquerdo em (60, 10):


```
Image image(L"SampleMetafile.emf");
graphics.DrawImage(&image, 60, 10);
```



A ilustração a seguir mostra a imagem desenhada no local especificado.

![captura de tela de uma janela que contém uma imagem e especifica o ponto de origem](images/imageposition2.png)

 

 



