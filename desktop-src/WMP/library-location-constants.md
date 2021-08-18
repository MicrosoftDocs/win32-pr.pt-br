---
title: Constantes de localização da biblioteca
description: Constantes de localização da biblioteca
ms.assetid: 88ff9b91-6b21-4f7d-ae13-e8456a3e0f75
keywords:
- Windows Media Player online, constantes de local da biblioteca
- lojas online, constantes de localização da biblioteca
- tipo 1 lojas online, constantes de localização da biblioteca
- Windows Media Player online, locais
- lojas online, locais
- tipo 1 lojas online, locais
- Windows Media Player biblioteca, constantes de localização
- biblioteca, constantes de localização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a677f405ff36030647618a83bd0b8b952dae254a756cebc48e4c3210e5fcde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135358"
---
# <a name="library-location-constants"></a>Constantes de localização da biblioteca

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

As constantes de local da biblioteca são variáveis de cadeia de caracteres globais definidas em contentpartner.h. Eles são usados por determinados métodos das interfaces [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) e [IWMPContentPartnerCallback](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback) e por determinados métodos [do objeto](external-object-for-type-1-online-stores.md) Externo. Essas constantes são usadas para indicar os tipos a seguir.

-   Tipo de local da biblioteca: esse é o tipo de exibição de biblioteca que está sendo exibido pelo Windows Media Player. Por exemplo, o Player pode estar exibindo uma exibição de um álbum específico (g szCPAlbumID) ou a exibição de todos os \_ gêneros (g \_ szAllCPGenreIDs).
-   Tipo de item selecionado: esse é o tipo de item selecionado na exibição de biblioteca. Por exemplo, o usuário pode selecionar um álbum específico (g \_ szCPAlbumID) na exibição de todos os álbums.
-   Tipo de lista: esse é o tipo de lista que está sendo solicitada do plug-in do parceiro de conteúdo. Por exemplo, Windows Media Player pode solicitar ao plug-in para fornecer uma lista de itens associados a uma playlist específica (g \_ szCPListID).
-   Tipo de item de lista: o tipo de item de lista individual que está sendo solicitado do plug-in do parceiro de conteúdo. Por exemplo, Windows Media Player pode solicitar ao plug-in para fornecer a lista de faixas \_ (g szCPTrackID) em uma playlist específica.

A tabela a seguir fornece o nome e o valor de cada constante e uma breve descrição do local ou tipo da biblioteca. No código C ou C++ compilado com o arquivo de título contentpartner.h, você pode usar o nome ou o valor de uma constante. Usar o nome é preferível porque o compilador detectará erro de ortagem. No script (por exemplo, ao chamar os métodos do [objeto Externo),](external-object-for-type-1-online-stores.md) você não pode usar o nome de uma constante; você deve usar o valor .



| Nome                              | Valor                        | Local ou tipo                                                                                                                                                   |
|-----------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ szUnknownLocation              | UnknownLocation              | Um conjunto de faixas que não é um álbum nem uma playlist. Windows Media Player também usa essa constante no evento raro em que não pode determinar um local válido. |
| g \_ szRootLocation                 | RootLocation                 | O nó superior no controle de exibição de árvore da biblioteca                                                                                                                      |
| g \_ szFlyoutMenu                   | FlyoutMenu                   | Menu de flyout da loja online atual                                                                                                                             |
| g \_ szOnlineStore                  | OnlineStore                  | Todas as lojas online                                                                                                                                                  |
| g \_ szCPListID                     | CPListID                     | Uma lista individual                                                                                                                                                 |
| g \_ szAllCPListIDs                 | AllCPListIDs                 | Todas as listas                                                                                                                                                          |
| g \_ szCPTrackID                    | CPTrackID                    | Uma faixa individual                                                                                                                                                |
| g \_ szAllCPTrackIDs                | AllCPTrackIDs                | Todas as faixas                                                                                                                                                         |
| g \_ szCPArtistID                   | CPArtistID                   | Um artista individual                                                                                                                                               |
| g \_ szAllCPArtistIDs               | AllCPArtistIDs               | Todos os artista                                                                                                                                                        |
| g \_ szCPAlbumID                    | CPAlbumID                    | Um álbum individual                                                                                                                                                |
| g \_ szAllCPAlbumIDs                | AllCPAlbumIDs                | Todos os álbums                                                                                                                                                         |
| g \_ szCPGenreID                    | CPGenreID                    | Um gênero individual                                                                                                                                                |
| g \_ szAllCPGenreIDs                | AllCPGenreIDs                | Todos os gêneros                                                                                                                                                         |
| g \_ szCPAlbumSubGenreID            | CPAlbumSubGenreID            | Um subgênero individual                                                                                                                                             |
| g \_ szAllCPAlbumSubGenreIDs        | AllCPAlbumSubGenreIDs        | Todos os subgêneros                                                                                                                                                      |
| g \_ szReleaseDateYear              | ReleaseDateYear              | Um ano individual em que o conteúdo do catálogo foi lançado                                                                                                               |
| g \_ szAllReleaseDateYears          | AllReleaseDateYears          | Todos os anos em que o conteúdo do catálogo foi lançado                                                                                                                        |
| g \_ szCPRadioID                    | CPRadioID                    | Um fluxo de rádio individual                                                                                                                                         |
| g \_ szAllCPRadioIDs                | AllCPRadioIDs                | Todos os fluxos de rádio                                                                                                                                                  |
| g \_ szAuthor                       | Autor                       | Um autor individual                                                                                                                                               |
| g \_ szAllAuthors                   | AllAuthors                   | Todos os autores                                                                                                                                                        |
| g \_ szWMParentalRating             | WMParentalRating             | Uma classificação de pais individual                                                                                                                                      |
| g \_ szAllWMParentalRatings         | AllWMParentalRatings         | Todas as classificações de pais                                                                                                                                               |
| g \_ szUserEffectiveRatingStars     | UserEffectiveRatingStars     | Uma classificação de usuário individual, medida como um número de estrelas                                                                                                           |
| g \_ szAllUserEffectiveRatingStarss | AllUserEffectiveRatingStarss | Todas as classificações de usuário                                                                                                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**External. addToBasket**](external-addtobasket.md)
</dt> <dt>

[**Externo. comprar**](external-buy.md)
</dt> <dt>

[**External. changeView**](external-changeview.md)
</dt> <dt>

[**External. changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**Externo. download**](external-download.md)
</dt> <dt>

[**External. libraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**External. Play**](external-play.md)
</dt> <dt>

[**IWMPContentPartner:: GetCommands**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands)
</dt> <dt>

[**IWMPContentPartner::GetListContents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[**IWMPContentPartner:: GetTemplate**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[**IWMPContentPartner::InvokeCommand**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand)
</dt> <dt>

[**IWMPContentPartnerCallback::ChangeView**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-changeview)
</dt> </dl>

 

 




