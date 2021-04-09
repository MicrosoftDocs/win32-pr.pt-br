---
title: Atributos com vários valores (SDK do Windows Media Format 11)
description: Atributos com vários valores
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- SDK do Windows Media Format, atributos
- Formato de sistema avançado (ASF), atributos
- ASF (formato de sistemas avançados), atributos
- atributos, vários valores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928aee154f9f824168ce08470702b49c23ba2c0a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008712"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a>Atributos com vários valores (SDK do Windows Media Format 11)

Alguns dos atributos predefinidos podem ter vários valores atribuídos a eles. Por exemplo, **artista** é um atributo que pode ter vários valores. Você pode chamar [**IWMHeaderInfo3:: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) várias vezes para adicionar quantos valores de **artista** forem necessários. Se você fizer várias chamadas para **AddAttribute** para atributos que não dão suporte a vários valores, o método poderá retornar um código de erro ou simplesmente ignorar a solicitação.

A tabela a seguir lista os atributos que dão suporte a vários valores. Alguns atributos podem ter vários valores somente em arquivos ASF, enquanto outros podem ter vários valores em arquivos ASF e MP3.



| Atributo                                                 | Suporte para vários valores |
|-----------------------------------------------------------|-----------------------------|
| [**Autor**](author.md)                                  | ASF, MP3                    |
| [**WM/AlbumArtist**](wm-albumartist.md)                  | ASF                         |
| [**WM/AlbumCoverURL**](wm-albumcoverurl.md)              | ASF                         |
| [**WM/categoria**](wm-category.md)                        | ASF                         |
| [**WM/Composer**](wm-composer.md)                        | ASF, MP3                    |
| [**WM/condutor**](wm-conductor.md)                      | ASF                         |
| [**WM/diretor**](wm-director.md)                        | ASF                         |
| [**WM/gênero**](wm-genre.md)                              | ASF                         |
| [**WM/Gêneroid**](wm-genreid.md)                          | ASF                         |
| [**WM/linguagem**](wm-language.md)                        | ASF, MP3                    |
| [**WM/letras de música \_ sincronizadas**](wm-lyrics-synchronised.md) | ASF, MP3                    |
| [**WM/humor**](wm-mood.md)                                | ASF, MP3                    |
| [**WM/imagem**](wmpicture.md)                           | ASF, MP3                    |
| [**WM/produtor**](wm-producer.md)                        | ASF                         |
| [**WM/PromotionURL**](wm-promotionurl.md)                | ASF                         |
| [**WM/UserWebURL**](wm-userweburl.md)                    | ASF, MP3                    |
| [**WM/gravador**](wm-writer.md)                            | ASF, MP3                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> </dl>

 

 




