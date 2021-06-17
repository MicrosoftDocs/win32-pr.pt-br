---
title: Atributos com vários valores (Windows Media Format SDK 11)
description: Saiba mais sobre atributos com vários valores no SDK Windows Media Format 11. Alguns atributos de item de mídia podem ter vários valores.
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- Windows Media Format SDK,atributos
- ASF (Advanced Systems Format), attributes
- ASF (Formato de Sistemas Avançados), atributos
- atributos, vários valores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9466cd3f993cc1b12f27bc162e5188e6d45404b
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262688"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a>Atributos com vários valores (Windows Media Format SDK 11)

Alguns dos atributos predefinidos podem ter vários valores atribuídos a eles. Por exemplo, **Artist** é um atributo que pode ter vários valores. Você pode chamar [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) várias vezes para adicionar quantos valores **de** Artista você precisar. Se você fizer várias chamadas para **AddAttribute** para atributos que não suportam vários valores, o método poderá retornar um código de erro ou simplesmente ignorar sua solicitação.

A tabela a seguir lista os atributos que suportam vários valores. Alguns atributos podem ter vários valores somente em arquivos ASF, enquanto outros podem ter vários valores em arquivos ASF e MP3.



| Atributo                                                 | Suporte para vários valores |
|-----------------------------------------------------------|-----------------------------|
| [**Autor**](author.md)                                  | ASF, MP3                    |
| [**WM/AlbumArtist**](wm-albumartist.md)                  | ASF                         |
| [**WM/AlbumCoverURL**](wm-albumcoverurl.md)              | ASF                         |
| [**WM/Categoria**](wm-category.md)                        | ASF                         |
| [**WM/Composer**](wm-composer.md)                        | ASF, MP3                    |
| [**WM/Wm/Wm**](wm-conductor.md)                      | ASF                         |
| [**WM/Director**](wm-director.md)                        | ASF                         |
| [**WM/Gênero**](wm-genre.md)                              | ASF                         |
| [**WM/GenreID**](wm-genreid.md)                          | ASF                         |
| [**WM/Language**](wm-language.md)                        | ASF, MP3                    |
| [**\_WM/Synchronizado**](wm-lyrics-synchronised.md) | ASF, MP3                    |
| [**WM/Wm/Wm**](wm-mood.md)                                | ASF, MP3                    |
| [**WM/Picture**](wmpicture.md)                           | ASF, MP3                    |
| [**WM/Produtor**](wm-producer.md)                        | ASF                         |
| [**WM/PromotionURL**](wm-promotionurl.md)                | ASF                         |
| [**WM/UserWebURL**](wm-userweburl.md)                    | ASF, MP3                    |
| [**WM/Writer**](wm-writer.md)                            | ASF, MP3                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> </dl>

 

 




