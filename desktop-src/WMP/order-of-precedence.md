---
title: Ordem de Precedência
description: Ordem de Precedência
ms.assetid: 3865ea8a-2489-4714-9a05-d1082589841f
keywords:
- Windows Metadados de mídia, ordem de precedência
- Windows Metadados de mídia, precedência
- metafiles, ordem de precedência
- metafiles, precedência
- Windows Mídia, metadados
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 12b55f34dd18fa6122d3f1588111aaffe374f2d87c06ef9100cbac057efd4bd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467986"
---
# <a name="order-of-precedence"></a>Ordem de Precedência

Nem todos os atributos de elemento de metadados são criados igualmente. Alguns atributos de elemento de metadados substituem outros atributos de elemento. Atributos de elemento podem ser substituídos por atributos de elemento semelhantes, dependendo da posição e da ordem. Todos os atributos de uma playlist de metadados substituem aqueles contidos em um arquivo Windows Mídia referenciado. Um atributo que substitui outro tem precedência mais alta.

A hierarquia, precedência mais alta para a mais baixa, é mostrada na tabela a seguir. O item de precedência mais alta nunca é substituído.



| Escopo                    | Hierarquia                                   |
|--------------------------|---------------------------------------------|
| "Conteúdo drm assinado"     | Nunca substituído.                           |
| **Escopo do** elemento REF    | Substituído apenas pelo conteúdo drm assinado.      |
| **Escopo do** elemento ENTRY  | Substitui os elementos das categorias abaixo. |
| **Escopo do ASX**            | Substitui elementos de arquivo de mídia.              |
| Windows Escopo do arquivo de mídia | Substituído por todos os acima.             |



 

-   "Conteúdo drm assinado" – objeto de assinatura digital.

    Atributos de conteúdo drm assinado substituirão todos os outros. Por exemplo, as informações de direitos autorais de "Conteúdo drm assinado" não serão substituídos. Ele sempre será transmitido e apresentado.

-   **Escopo do** elemento REF

    Os atributos do **elemento REF** substituirão outros atributos de elemento, mas não o conteúdo drm assinado.

-   **Escopo ENTRY**

    Os atributos do **elemento ENTRY** serão substituídos pelo atributo de elemento **REF,** mas substituirão outros atributos de elemento. **Os** metadados TITLE do **elemento ENTRY** são exibidos em vez das informações de título do arquivo de mídia.

-   **Escopo do ASX**

    Todas as propriedades inseridas no metadado substituem aquelas contidas no arquivo Windows Media. Atributos do elemento **ENTRY** substituem **atributos de elemento ASX.** Enquanto o **clipe de** mídia referenciado do elemento ENTRY está sendo exibido, os metadados **TITLE** do elemento **ENTRY** são exibidos em vez de informações de título do **elemento ASX.**

-   Windows Escopo do arquivo de mídia

    Os atributos do arquivo Windows Media são substituídos por quaisquer atributos de metadados. Os metadados do arquivo de mídia serão exibidos somente se não houver metadados definidos para esse elemento no metadado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando playlists de metadados**](creating-metafile-playlists.md)
</dt> <dt>

[**Playlists de metadados**](metafile-playlists.md)
</dt> <dt>

[**Windows Referência de elementos de metadados de mídia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guia de metadados de mídia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




