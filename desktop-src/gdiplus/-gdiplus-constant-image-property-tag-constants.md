---
description: Vários formatos de arquivo de imagem permitem armazenar metadados junto com uma imagem.
ms.assetid: 1eba4b91-bbf4-4f82-b2d7-65f331a84859
title: Constantes de marca de propriedade de imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea9a6c3b8ea7ad9f0693032d3bc779bc414d9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967784"
---
# <a name="image-property-tag-constants"></a>Constantes de marca de propriedade de imagem

Vários formatos de arquivo de imagem permitem armazenar metadados junto com uma imagem. Metadados são informações sobre uma imagem, por exemplo, título, largura, modelo de câmera e artista. O Windows GDI+ fornece uma maneira uniforme de armazenar e recuperar metadados de arquivos de imagem nos formatos TIFF, JPEG, PNG (Portable Network Graphics) e EXIF (exchangable Image File).

No GDI+, um pedaço de metadados é chamado de *item de propriedade* e um item de propriedade individual é identificado por uma constante numérica chamada de *marca de propriedade*. Você pode armazenar e recuperar metadados chamando os métodos [**Image:: SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) e [**Image:: GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) da classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e não precisa se preocupar com os detalhes de como um formato de arquivo específico armazena esses metadados.

Os tópicos a seguir listam e descrevem os itens de propriedade com suporte no GDI+. As descrições são breves e gerais para que se apliquem a uma variedade de formatos de arquivo. Para obter uma descrição detalhada de como um item de propriedade é usado em um formato de arquivo específico, consulte a especificação para esse formato de arquivo. Para obter links para várias especificações de formato de arquivo, consulte [especificações de formato de arquivo de imagem](-gdiplus-constant-image-file-format-specifications.md). Para obter mais informações sobre metadados, consulte constantes de [leitura e gravação de metadados](-gdiplus-reading-and-writing-metadata-use.md) e [**tipo de marca de propriedade de imagem**](-gdiplus-constant-image-property-tag-type-constants.md).

-   [Marcas de propriedade em ordem numérica](-gdiplus-constant-property-tags-in-numerical-order.md)
-   [Marcas de propriedade em ordem alfabética](-gdiplus-constant-property-tags-in-alphabetical-order.md)
-   [Descrições de item de propriedade](-gdiplus-constant-property-item-descriptions.md)

 

 



