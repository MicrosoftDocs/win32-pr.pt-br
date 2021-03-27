---
description: Este tópico descreve uma nova exibição no Windows Explorer, chamada exibição de conteúdo, que exibe o conteúdo mais relevante para cada item.
title: Exibição de conteúdo por tipo de arquivo ou tipo
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E01A6726-14C4-4c00-81D4-AE1008088678
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 81982d2242a7ea466c10e7d0ee37d899eea3e687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662442"
---
# <a name="content-view-by-file-type-or-kind"></a>Exibição de conteúdo por tipo de arquivo ou tipo

Este tópico descreve uma nova exibição no Windows Explorer, chamada exibição de conteúdo, que exibe o conteúdo mais relevante para cada item. Usando um conjunto de chaves do registro, os itens podem definir uma lista de propriedades e um layout que o Shell usa para a exibição de conteúdo. O Shell recupera as chaves do registro usando a matriz de [Associação](fa-perceivedtypes.md)do item.

## <a name="how-does-the-content-view-work"></a>Como funciona a exibição de conteúdo?

No Windows 7 e posterior, a exibição de conteúdo usa uma lógica de redimensionamento que descarta Propriedades quando o tamanho da janela diminui, para garantir que as propriedades mais críticas ainda tenham espaço para serem legíveis. A captura de tela a seguir ilustra a exibição de conteúdo dos resultados da pesquisa que contêm música, imagens e documentos.

![exibição de conteúdo dos resultados da pesquisa que contêm música, imagens e documentos](images/content-view/contentviewsearchresults.png)

Algumas fontes de dados do Shell usam a exibição de conteúdo por padrão, mas os usuários podem selecionar o modo de exibição de conteúdo clicando no botão de **controle exibir** no Windows Explorer. Uma fonte de dados do Shell estende o namespace do Shell e expõe os itens em um armazenamento de dados. Os itens em um armazenamento de dados podem ser indexados pelo sistema de pesquisa do Windows usando um manipulador de protocolo.

## <a name="how-to-implement-the-content-view"></a>Como implementar o modo de exibição de conteúdo

Ao registrar um novo [tipo de arquivo](fa-file-types.md) ou [manipulador de protocolo](../search/-search-3x-wds-extidx-prot-implementing.md), você pode aproveitar o modo de exibição de conteúdo usando uma das duas abordagens diferentes. Você pode usar um conjunto existente de propriedades e padrão de layout, ou pode criar sua própria combinação.

Você pode usar uma entrada de registro para associar o tipo de arquivo ou o item a um [tipo](../properties/building-property-handlers-user-friendly-kind-names.md)predefinido, que é uma propriedade que você pode considerar como uma categoria de conteúdo. Ao associar o tipo de arquivo ou o item a alguns desses tipos, você herdará automaticamente os padrões de layout da exibição de conteúdo e as listas de propriedades do tipo. O Windows define padrões de layout de exibição de conteúdo e listas de propriedades para os seguintes tipos: documentos, email, pasta, música, imagem e genérico. Esse tipo de associação é incentivado. Ele permite que você forneça a experiência consistente que um usuário espera para itens semelhantes.

Para obter mais informações, consulte [tipos de arquivo](fa-file-types.md) e nomes de [tipo](../properties/building-property-handlers-user-friendly-kind-names.md) e [como registrar uma exibição de conteúdo exclusiva conjunto de propriedades e padrão de layout para o tipo de arquivo ou item](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md).

## <a name="additional-resources"></a>Recursos adicionais

-   Para obter a documentação de referência de propriedade, consulte [System. Kind](../properties/props-system-kind.md)e [System. KindText](../properties/props-system-kindtext.md).
-   Para obter a documentação de referência da PropList, consulte [System. PropList. ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md)e [System. PropList. ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[registro de Aplicativo](app-registration.md)
</dt> <dt>

[Tipos de arquivo](fa-file-types.md)
</dt> <dt>

[Como funcionam as associações de arquivo](fa-how-work.md)
</dt> <dt>

[Verificador de tipo de arquivo](file-type-verifier.md)
</dt> <dt>

[Manipuladores de tipo de arquivo](fa-file-extensions.md)
</dt> <dt>

[Identificadores programáticos](fa-progids.md)
</dt> <dt>

[Tipos observados](fa-perceivedtypes.md)
</dt> <dt>

[Matrizes de associação](fa-associationarray.md)
</dt> </dl>

 

 
