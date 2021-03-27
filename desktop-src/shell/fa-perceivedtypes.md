---
description: Um tipo percebido é uma categoria de tipos de arquivo que permite identificar o tipo de arquivo para Windows (e aplicativos) como sendo uma imagem, áudio, documento ou outro tipo.
title: Tipos observados (o Shell do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 56d4c495-a886-4723-88ca-5b7753398062
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6136389c717fd4e27621a4d7f9f4cf2895c4116
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104989132"
---
# <a name="perceived-types-the-windows-shell"></a>Tipos observados (o Shell do Windows)

Um tipo percebido é uma categoria de tipos de arquivo que permite identificar o tipo de arquivo para Windows (e aplicativos) como sendo uma imagem, áudio, documento ou outro tipo. Os tipos observados são usados para várias finalidades, incluindo a determinação do tipo de pasta, que é usado para definir as configurações de exibição padrão. Por exemplo, uma pasta cheia de arquivos que são da imagem do tipo percebido é atribuída a um modo de exibição padrão de miniaturas.

Este tópico é organizado da seguinte maneira:

-   [Sobre tipos observados](#about-perceived-types)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="about-perceived-types"></a>Sobre tipos observados

Os tipos observados, definidos como valores percebido, são semelhantes aos tipos de arquivo, exceto pelo fato de que eles se referem a categorias amplas de tipos de formato de arquivo em vez de tipos de arquivo específicos. Por exemplo, imagem, texto, áudio e compactado são tipos percebidos. Os tipos de arquivo (geralmente tipos de arquivo públicos) podem ser atribuídos a um tipo percebido e sempre devem ser atribuídos um sempre que houver um que seja apropriado. Por exemplo, o arquivo de imagem Types. bmp,. png,. jpg e. gif também são da imagem de tipo percebida.

Os tipos observados padrão são os seguintes:

-   Pasta
-   Texto
-   Imagem
-   Áudio
-   Vídeo
-   Compressed
-   Documento
-   Sistema
-   Aplicativo
-   Gamemedia
-   Contatos

## <a name="additional-resources"></a>Recursos adicionais

-   Para obter informações sobre como registrar tipos observados, consulte [registro de aplicativo](app-registration.md).
-   Para obter uma lista de tipos observados padrão, consulte a enumeração [**percebida**](/windows/win32/api/shtypes/ne-shtypes-perceived) .
-   Para recuperar o tipo percebido de um arquivo com base em sua extensão de nome de arquivo, consulte a função [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[registro de Aplicativo](app-registration.md)
</dt> <dt>

[Tipos de arquivo](fa-file-types.md)
</dt> <dt>

[Como funcionam as associações de arquivo](fa-how-work.md)
</dt> <dt>

[Exibição de conteúdo por tipo de arquivo ou tipo](prophand-content-view.md)
</dt> <dt>

[Verificador de tipo de arquivo](file-type-verifier.md)
</dt> <dt>

[Manipuladores de tipo de arquivo](fa-file-extensions.md)
</dt> <dt>

[Identificadores programáticos](fa-progids.md)
</dt> <dt>

[Matrizes de associação](fa-associationarray.md)
</dt> </dl>

 

 



