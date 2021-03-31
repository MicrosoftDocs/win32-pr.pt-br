---
title: Ordem de Precedência
description: Ordem de Precedência
ms.assetid: 3865ea8a-2489-4714-9a05-d1082589841f
keywords:
- Metaarquivos do Windows Media, ordem de precedência
- Metaarquivos do Windows Media, precedência
- metaarquivos, ordem de precedência
- metaarquivos, precedência
- Windows Media, metaarquivos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9161d1e43f61ae1b1a7231c640e33c4c6ec6527f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005171"
---
# <a name="order-of-precedence"></a>Ordem de Precedência

Nem todos os atributos de elemento de metarquivo são criados como iguais. Alguns atributos de elemento de metarquivo substituem outros atributos de elemento. Atributos de elemento podem ser substituídos por atributos de elemento semelhantes, dependendo da posição e da ordem. Todos os atributos de uma playlist de metarquivo substituem aqueles contidos em um arquivo de mídia do Windows referenciado. Um atributo que substitui outro tem precedência mais alta.

A hierarquia, precedência mais alta para a mais baixa, é mostrada na tabela a seguir. O item de precedência mais alta nunca é substituído.



| Escopo                    | Hierarquia                                   |
|--------------------------|---------------------------------------------|
| "Conteúdo DRM assinado"     | Nunca substituído.                           |
| Escopo do elemento **ref**    | Substituído apenas por conteúdo DRM assinado.      |
| Escopo do elemento de **entrada**  | Substitui os elementos das categorias abaixo. |
| Escopo **ASX**            | Substitui elementos do arquivo de mídia.              |
| Escopo do arquivo de mídia do Windows | Substituído por todos os itens acima.             |



 

-   "Conteúdo DRM assinado"-objeto de assinatura digital.

    Os atributos de conteúdo DRM assinado substituirão todos os outros. Por exemplo, as informações de direitos autorais de "conteúdo DRM assinado" não serão substituídas. Ele será sempre transmitido e apresentado.

-   Escopo do elemento **ref**

    Os atributos do elemento **ref** substituirão outros atributos de elemento, mas não o conteúdo DRM assinado.

-   Escopo de **entrada**

    Os atributos do elemento de **entrada** serão substituídos pelo atributo **ref** element, mas substituirão outros atributos Element. Os metadados de **título** do elemento de **entrada** são exibidos em vez das informações de título do arquivo de mídia.

-   Escopo **ASX**

    Todas as propriedades que são inseridas no metarquivo substituem aquelas contidas no arquivo do Windows Media. Atributos do elemento de **entrada** substituem atributos de elemento **ASX** . Enquanto o clipe de mídia referenciado do elemento de **entrada** está sendo reproduzido, os metadados do **título** do elemento de **entrada** são exibidos em vez das informações de título do elemento **ASX** .

-   Escopo do arquivo de mídia do Windows

    Os atributos do arquivo de mídia do Windows são substituídos por qualquer atributo de metarquivo. Os metadados do arquivo de mídia são exibidos somente se não houver nenhum metadado definido para esse elemento no metarquivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando listas de reprodução de metarquivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Playlists de metarquivo**](metafile-playlists.md)
</dt> <dt>

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guia de metarquivo do Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




