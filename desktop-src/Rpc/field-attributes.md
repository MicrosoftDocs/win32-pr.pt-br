---
title: Atributos de campo
description: Atributos de campo (atributos aplicados a campos de uma matriz, estrutura, união ou matriz de caracteres) e RPC (Chamada de Procedimento Remoto).
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

Atributos de campo são os atributos que podem ser aplicados aos campos de uma matriz, estrutura, união ou matriz de caracteres:

-   **\[**[**ignore**](/windows/desktop/Midl/ignore) **\]** , size **\[** [ **\_ is**](/windows/desktop/Midl/size-is)**\]**
-   **\[**[**max \_ é**](/windows/desktop/Midl/max-is)**\]**
-   **\[**[**length \_ é**](/windows/desktop/Midl/length-is)**\]**
-   **\[**[**primeiro \_ é**](/windows/desktop/Midl/first-is)**\]**
-   **\[**[**o último \_ é**](/windows/desktop/Midl/last-is)**\]**
-   **\[**[**switch \_ é**](/windows/desktop/Midl/switch-is)**\]**
-   **\[**[**String**](/windows/desktop/Midl/string)**\]**
-   [atributos de ponteiro](three-pointer-types.md)

Por exemplo, os atributos de campo são usados em conjunto com declarações de matriz para especificar o tamanho da matriz ou a parte da matriz que contém dados válidos. Isso é feito associando outro parâmetro, campo de estrutura ou uma expressão constante à matriz.

O **\[** [**atributo ignore**](/windows/desktop/Midl/ignore) **\]** designa campos de ponteiro a serem ignorados durante o processo de marshaling. Esse campo ignorado é definido como **NULL** no lado do receptor.

MIDL fornece *matrizes* *compatíveis, variáveis* *e* abertas. Uma matriz será chamada de compatível se seus limites são determinados em tempo de operação. O **\[** [**atributo size \_ is**](/windows/desktop/Midl/size-is) designa o limite superior no tamanho da alocação da matriz e o atributo max is designa o limite superior no valor de **\]** um índice de matriz **\[** [**\_**](/windows/desktop/Midl/max-is) **\]** válido. Para obter mais informações, consulte **\[** [**matrizes**](arrays.md) **\]** .

Uma matriz será chamada de variável se seus limites são determinados em tempo de compilação, mas o intervalo de elementos transmitidos é determinado em tempo de run. Uma matriz aberta (também chamada de matriz variável compatível) é uma matriz cujo limite superior e intervalo de elementos transmitidos são determinados em tempo de executar. Para determinar o intervalo de elementos transmitidos de uma matriz, a declaração de matriz deve incluir um comprimento é , primeiro **\[** [**\_**](/windows/desktop/Midl/length-is) **\]** **\[** [**\_ é**](/windows/desktop/Midl/first-is) **\]** ou o último atributo **\[** [**\_ é**](/windows/desktop/Midl/last-is) **\]** .

O **\[ atributo length \_ is \]** designa **\[ \_ \]** o número de elementos de matriz a serem transmitidos e o primeiro atributo is designa o índice do primeiro elemento de matriz a ser transmitido. O **\[ último \_ atributo \]** é designa o índice do último elemento de matriz a ser transmitido.

O **\[** [**atributo switch \_ is**](/windows/desktop/Midl/switch-is) **\]** field designa um discriminador de união. Quando a união é um parâmetro de procedimento, o discriminador de união deve ser outro parâmetro do mesmo procedimento. Quando a união é um campo de uma estrutura, o discriminador deve ser outro campo da estrutura no mesmo nível que o campo de união. O discriminador deve ser um tipo [**booliana**](/windows/desktop/Midl/boolean), [**char**](/windows/desktop/Midl/char-idl), [**int**](/windows/desktop/Midl/int)ou [**enum**](/windows/desktop/Midl/enum) ou um tipo que resolve para um desses tipos. Para obter mais informações, consulte [Uniões não truncadas](/windows/desktop/Midl/nonencapsulated-unions) e **\[ a opção \_ é \]**.

O atributo de campo de cadeia de caracteres designa que um caractere unidimensional ou matriz de byte, ou um ponteiro para um fluxo de caracteres ou byte terminado em zero, deve ser tratado como uma cadeia de **\[** [](/windows/desktop/Midl/string) **\]** caracteres. O atributo de cadeia de caracteres se aplica somente a matrizes unidimensionais e ponteiros. O tipo de elemento é limitado a [**char**](/windows/desktop/Midl/char-idl), [**byte**](/windows/desktop/Midl/byte), [**wchar \_ t**](/windows/desktop/Midl/wchar-t)ou um tipo nomeado que resolve para um desses tipos.

Para obter informações sobre o contexto no qual os atributos de campo aparecem, consulte [Matrizes MIDL, Estruturas](/windows/desktop/Midl/midl-arrays) [MIDL](/windows/desktop/Midl/midl-structures)e [Uniões MIDL](/windows/desktop/Midl/midl-unions).

 

 