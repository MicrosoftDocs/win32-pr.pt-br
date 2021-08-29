---
title: Anotação de mapa de valor
description: Anotação de mapa de valor
ms.assetid: f7c9304a-0eed-4a73-ab06-56723f3cfa5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f378742ce01458d930ee510baf4c6317f2e182cdd41642c4d22928d9777fe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052224"
---
# <a name="value-map-annotation"></a>Anotação de mapa de valor

Com a anotação de mapa de valor, você pode usar uma cadeia de caracteres de mapeamento para indicar como o índice de imagem de um item em uma exibição de lista ou de árvore corresponde à sua função ou estado. Por exemplo, uma cadeia de caracteres de mapeamento pode indicar que um índice de imagem de exibição de lista 0 é mapeado para uma função de caixa de seleção, enquanto o índice de imagem 1 é mapeado para uma função de botão de opção.

Você também pode usar a anotação de mapa de valor para especificar cadeias de caracteres que são mapeadas para os valores numéricos em um controle deslizante.

## <a name="when-to-use-this-technique"></a>Quando usar essa técnica

Considere o uso da anotação de mapa de valor nas situações a seguir.

-   Quando uma exibição de lista ou exibição de árvore de desenho proprietário incorpora o uso de imagens, e você deseja fornecer uma descrição personalizada acessível (Propriedade de [**Descrição**](description-property.md) ) com base nessa imagem. A ilustração a seguir mostra um exemplo.

    ![ilustração do menu Iniciar, em que os ícones fornecem pistas visuais ao conteúdo](images/iconlist.gif)

-   Quando um modo de exibição de lista ou árvore de desenho proprietário incorpora o uso de imagens para fazer com que os itens de árvore ou lista atuem como controles simples, geralmente caixas de seleção ou botões de opção, e você deseja mapear a imagem para uma função. A captura de tela a seguir mostra um exemplo.

    ![captura de tela das opções do Internet Explorer para definir o valor de caixas de seleção e botões de opção](images/customlist.gif)

-   Quando um controle deslizante é usado para selecionar um valor que pode ser descrito como algo diferente de um inteiro simples, como na captura de tela a seguir, em que a configuração de resolução de tela é descrita por uma cadeia de caracteres.

    ![captura de tela de um controle deslizante que é usado para definir a resolução da tela](images/slider.gif)

Com a anotação de mapa de valor, uma cadeia de caracteres de mapeamento indica como o índice de imagem da lista ou da árvore corresponde à sua função ou estado. Ou, pode indicar como o valor numérico de um controle deslizante corresponde a uma cadeia de caracteres. Por exemplo, uma cadeia de caracteres de mapeamento pode indicar que um índice de imagem de exibição de lista 0 mapeia para uma função de caixa de seleção e índice de imagem 1 mapeia para uma função de botão de opção. Use [**IAccPropServices:: SetHwndPropStr ()**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) para anexar a cadeia de caracteres de mapeamento ao controle.

Como o conhecimento específico do controle é necessário para dar suporte ao mapeamento de valor, há um número limitado de controles e propriedades que dão suporte à anotação de mapa de valor, incluindo mapas de valor do controle deslizante, exibições de lista e exibições de árvore.

## <a name="slider-value-map"></a>Mapa do valor do controle deslizante

**Propid \_ A ACC \_ VALUEMAP** contém um mapeamento de posições de controle deslizante internas para cadeias de caracteres legíveis. Essa propriedade tem suporte pelo proxy de controle deslizante Oleacc.dll. Se o valor do controle deslizante atual for encontrado no mapa de valores, a cadeia de caracteres correspondente será exposta como o valor em vez da cadeia de caracteres percentual padrão (por exemplo, "50").

## <a name="list-view-and-tree-view"></a>Exibição de lista e exibição de árvore

**Propid \_ ACC \_ ROLEMAP**, **Propid \_ ACC \_ STATEMAP** e **Propid \_ ACC \_ DESCRIPTONMAP** fornecem mapeamentos de índices de imagem de estado para valores de função e estado. Esses mapas permitem que esses índices de imagem sejam mapeados para as funções apropriadas (geralmente, o [**\_ botão de \_ opção do sistema de função**](object-roles.md) ou o sistema de [**função \_ \_ CHECKBUTTON**](object-roles.md)) e bits de estado adicionais (geralmente [**estado do \_ sistema \_ marcado**](object-state-constants.md)).

Para obter mais informações sobre a anotação de mapa de valor, consulte os seguintes tópicos:

-   [Usando anotação de mapa de valor](using-value-map-annotation.md)
-   [Exemplo de anotação de mapa de valor](value-map-annotation-sample.md)

## <a name="annotation-map-format"></a>Formato do mapa de anotação

A tabela a seguir descreve os campos que são incluídos em um mapa de anotação.



| Campo               | Descrição                                                                                                                                                                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Um                 | Indica que um esquema de codificação específico é usado. Prefixos adicionais podem ter suporte para esquemas de codificação futuros.                                                                                                                                                          |
| Caractere delimitador | Geralmente, dois-pontos (:) é usado, mas pode ser outro caractere, exceto **NULL** ou um espaço vazio. Como esse caractere será usado como um delimitador para os campos restantes, ele não pode ser usado como parte de um valor no mapa.                                               |
| 0, 1 ou 2          | Um valor que indica qual chave está sendo usada. Para exibição de árvore e mapas de estado e função de exibição de lista, essa chave pode ser 0 (índice de imagem), 1 (índice de imagem de estado) ou 2 (índice de imagem de sobreposição). Para controles deslizantes e outros que não oferecem uma opção de chaves, esse valor deve ser 0. |
| Caractere delimitador | :                                                                                                                                                                                                                                                                             |
| Pares chave-valor     | Cada par consiste em uma cadeia de caracteres de chave e um caractere delimitador. A cadeia de caracteres chave é um número e pode estar em formato decimal ou hexadecimal (com um prefixo "0x" à esquerda).                                                                                                            |
| Cadeia de caracteres de valor        | Para mapas de valor, esta é uma cadeia de caracteres. Para mapas de função e de estado, é um número (decimal ou hexadecimal).                                                                                                                                                                         |
| Caractere delimitador | :                                                                                                                                                                                                                                                                             |



 

Por exemplo, um mapa pode ser semelhante ao seguinte:


```C++
A:0:0:Cold:1:Warm:3:Hot:
```



Quando esse mapa de valor é aplicado a um controle deslizante, um valor de "quente" será exposto quando o controle deslizante estiver na posição 1. Como o valor 2 não está incluído neste exemplo, o valor padrão dessa posição será exposto. Para um controle deslizante, o padrão seria um valor percentual, como 33.

 

 




