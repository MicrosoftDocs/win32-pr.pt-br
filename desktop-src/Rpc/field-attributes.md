---
title: Atributos de campo
description: Atributos de campo (atributos aplicados a campos de uma matriz, estrutura, União ou matriz de caracteres) e RPC (chamada de procedimento remoto).
ms.assetid: 4508479d-ff0a-4698-94aa-588837032067
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e6d14bab0cf14710e91fceb466111c4af32d3d2828e4b7bdacc9494fa27b7d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929995"
---
# <a name="field-attributes"></a>Atributos de campo

Os atributos de campo são os atributos que podem ser aplicados aos campos de uma matriz, estrutura, União ou matriz de caracteres:

-   **\[**[**ignorar**](/windows/desktop/Midl/ignore) **\]** , **\[** [ **tamanho \_ é**](/windows/desktop/Midl/size-is)**\]**
-   **\[**[**máximo \_ é**](/windows/desktop/Midl/max-is)**\]**
-   **\[**[**comprimento \_ é**](/windows/desktop/Midl/length-is)**\]**
-   **\[**[**primeiro \_ é**](/windows/desktop/Midl/first-is)**\]**
-   **\[**[**último \_ é**](/windows/desktop/Midl/last-is)**\]**
-   **\[**[**switch \_ é**](/windows/desktop/Midl/switch-is)**\]**
-   **\[**[**Strings**](/windows/desktop/Midl/string)**\]**
-   [atributos de ponteiro](three-pointer-types.md)

Por exemplo, os atributos de campo são usados em conjunto com declarações de matriz para especificar o tamanho da matriz ou a parte da matriz que contém dados válidos. Isso é feito associando-se outro parâmetro, campo de estrutura ou uma expressão constante com a matriz.

O **\[** atributo [**ignore**](/windows/desktop/Midl/ignore) **\]** designa os campos de ponteiro a serem ignorados durante o processo de marshaling. Esse campo ignorado é definido como **nulo** no lado do destinatário.

MIDL fornece matrizes em *conformidade*, *variáveis* e *abertas* . Uma matriz será chamada de acordo se seus limites forem determinados em tempo de execução. O **\[** atributo [**Size \_ é**](/windows/desktop/Midl/size-is) **\]** designa o limite superior no tamanho de alocação da matriz e o **\[** atributo [**Max \_ é**](/windows/desktop/Midl/max-is) **\]** designa o limite superior no valor de um índice de matriz válido. Para obter mais informações, consulte **\[** [**matrizes**](arrays.md) **\]** .

Uma matriz é chamada de variação se seus limites são determinados em tempo de compilação, mas o intervalo de elementos transmitidos é determinado em tempo de execução. Uma matriz aberta (também chamada de matriz de variação em conformidade) é uma matriz cujo limite superior e o intervalo de elementos transmitidos são determinados em tempo de execução. Para determinar o intervalo de elementos transmitidos de uma matriz, a declaração de matriz deve incluir um **\[** [**\_ comprimento**](/windows/desktop/Midl/length-is) **\]** , o **\[** [**primeiro \_ é**](/windows/desktop/Midl/first-is) **\]** , ou o **\[** [**último \_ é**](/windows/desktop/Midl/last-is) o **\]** atributo.

O **\[ tamanho \_ é \]** o atributo designa o número de elementos da matriz a serem transmitidos e o **\[ primeiro atributo \_ é \]** designa o índice do primeiro elemento da matriz a ser transmitido. O **\[ último \_ atributo \] is** designa o índice do último elemento de matriz a ser transmitido.

O **\[** atributo de campo [**switch \_ é**](/windows/desktop/Midl/switch-is) **\]** designa um discriminador Union. Quando Union é um parâmetro de procedimento, o discriminador Union deve ser outro parâmetro do mesmo procedimento. Quando Union é um campo de uma estrutura, o discriminador deve ser outro campo da estrutura no mesmo nível que o campo Union. O discriminador deve ser um tipo [**booliano**](/windows/desktop/Midl/boolean), [**Char**](/windows/desktop/Midl/char-idl), [**int**](/windows/desktop/Midl/int)ou [**enum**](/windows/desktop/Midl/enum) ou um tipo que resolva para um desses tipos. Para obter mais informações, veja [unencapsulated Unions](/windows/desktop/Midl/nonencapsulated-unions) and **\[ switch \_ is \]**.

O **\[** atributo de campo de [**cadeia de caracteres**](/windows/desktop/Midl/string) **\]** designa que um caractere unidimensional ou matriz de bytes, ou um ponteiro para um caractere de terminação zero ou um fluxo de bytes, deve ser tratado como uma cadeia de caracteres. O atributo de cadeia de caracteres aplica-se apenas a matrizes unidimensionais e ponteiros. O tipo de elemento é limitado a [**Char**](/windows/desktop/Midl/char-idl), [**byte**](/windows/desktop/Midl/byte), [**WCHAR \_ t**](/windows/desktop/Midl/wchar-t)ou a um tipo nomeado que resolve para um desses tipos.

Para obter informações sobre o contexto no qual os atributos de campo aparecem, consulte [matrizes de MIDL](/windows/desktop/Midl/midl-arrays), [estruturas de MIDL](/windows/desktop/Midl/midl-structures)e [uniões de MIDL](/windows/desktop/Midl/midl-unions).

 

 