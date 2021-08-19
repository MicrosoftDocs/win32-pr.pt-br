---
title: Integração de informações de álbum
description: Integração de informações de álbum
ms.assetid: c59c0c1b-eddc-4061-87cc-a5c44ae0c15d
keywords:
- Windows Media Player lojas online, integração de informações de álbum
- lojas online, integração de informações de álbum
- tipo 2 lojas online, integração de informações de álbum
- Windows Media Player lojas online, integrando informações do álbum
- lojas online, integrando informações de álbum
- Digite 2 lojas online, integrando informações do álbum
- Windows Media Player, integrando informações do álbum
- Windows Media Player, integração de informações de álbum
- integração de informações de álbum
- Integrando informações do álbum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdd8c0c200d0d1779ecc9d4f90da3f3755f276431792f7a6b6450dd43e51cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055424"
---
# <a name="album-info-integration"></a>Integração de informações de álbum

Windows Media Player permite que os usuários solicitem informações detalhadas sobre o CD ou DVD do qual o conteúdo de mídia digital foi originado clicando em um botão, como **mais informações**. quando o usuário clica no botão, Windows Media Player 10 ou posteriores no repositório de música atual para exibir os detalhes do álbum. Quando isso acontece, o Player abre o painel de informações do álbum e exibe a página da Web especificada pelo atributo **URL** do elemento **AlbumInfo** do documento serviceInfo.

Windows Media Player acrescenta uma cadeia de caracteres de consulta à URL para fornecer informações para a loja online sobre o conteúdo solicitado pelo usuário. A cadeia de caracteres de consulta inclui atributos como **título**, **álbum** e **artista**, que o repositório online pode usar para determinar o álbum correto a ser exibido. A documentação de referência para o elemento **AlbumInfo** fornece a lista completa de atributos de cadeia de caracteres de consulta e suas descrições.

## <a name="guidelines-for-album-info"></a>Diretrizes para informações de álbum

Ao criar a página da Web informações do álbum, use as seguintes diretrizes:

-   A página deve identificar claramente a loja online que fornece as informações. Você pode fazer isso exibindo de forma proeminente seu logotipo, por exemplo.
-   A página deve incluir um link para a política de privacidade da sua empresa.
-   Evite a navegação de página dentro do recurso de informações do álbum sempre que possível. Você deve navegar até sua loja online para a maioria das atividades.
-   Recomendamos que você forneça informações valiosas sem exigir que o usuário instale programas ou faça logon em sua loja online.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre as lojas online do tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Elemento AlbumInfo**](albuminfo-element.md)
</dt> </dl>

 

 




