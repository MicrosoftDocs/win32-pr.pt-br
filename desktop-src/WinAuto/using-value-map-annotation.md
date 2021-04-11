---
title: Usando anotação de mapa de valor
description: Para o código de exemplo, consulte exemplo de anotação de mapa de valor.
ms.assetid: 29be74c7-a7c2-41f4-8b94-5771988b74ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a3e8d003d863372e21a413fad56bc93b977ee3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366069"
---
# <a name="using-value-map-annotation"></a>Usando anotação de mapa de valor

**Para criar um mapa de valor**

1.  **Crie uma cadeia de caracteres de mapeamento.**

    Uma cadeia de caracteres de mapeamento é uma lista dos valores numéricos de um controle que correspondem a uma cadeia de caracteres legível em Unicode. Ele começa com "A:" seguido de um número que indica o tipo de índice usado. Somente índices de imagem têm suporte; Portanto, o tipo de índice é sempre 0.

    A cadeia de caracteres é seguida por: índice: pares de resultados. O "índice" é um número que representa um índice de imagem para uma exibição de List-View ou de árvore ou o valor de um controle deslizante.

    O valor resultante é um número obtido ao mapear a propriedade de função ou estado para um controle de exibição de lista ou de árvore. Esses números são expressos em decimal ou hexadecimal com um prefixo "0x".

    A cadeia de caracteres de mapeamento sempre termina com um dois pontos finais (":").

    Veja a seguir um exemplo de um mapa de anotação para as propriedades State e role de uma caixa de seleção em um controle de exibição de lista ou de árvore. Há dois itens na exibição que representam as caixas de seleção e cada uma tem imagens correspondentes ao estado marcado e desmarcado.

    ```C++
    LPCWSTR g_ListOrTreeStateMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x00" // Image 0 is normal !
    L":1:0x10" // Image 1 is checked - STATE_SYSTEM_CHECKED (0x10) !
    L":";

    LPCWSTR g_ListOrTreeRoleMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x2C" // Image 0 is a check box - ROLE_SYSTEM_CHECKBUTTON
    (0x2c) !
    L":1:0x2C" // image 1 is also a check box !
    L":";
    ```

    

    Para valores de função e estado válidos, consulte [funções de objeto](object-roles.md) e constantes de estado do [objeto](object-state-constants.md).

    O valor do índice pode ser negativo quando você mapeia as propriedades de um controle deslizante.

    Quando você mapeia um valor ou uma propriedade de descrição, o resultado é uma cadeia de caracteres. As cadeias de caracteres não estão entre aspas e os dois-pontos atuam como delimitadores.

    Para obter mais informações, consulte [formato do mapa de anotação](value-map-annotation.md).

2.  **Crie o Gerenciador de anotações e obtenha um ponteiro para sua** interface [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)**.**

    Veja a seguir um exemplo de como criar o Gerenciador de anotações.

    ```C++
    IAccPropServices * pAccPropSvc = NULL;
    HRESULT hr = CoCreateInstance(CLSID_AccPropServices, NULL,
    CLSCTX_SERVER, IID_IAccPropServices, (void**) & pAccPropSvc));
    
    ```

    

3.  **Anexe a cadeia de caracteres de mapeamento ao controle.**

    Chame [**IAccPropServices:: SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr), passando o **HWND** do controle e um ponteiro para a cadeia de caracteres de mapeamento.

    O parâmetro *IdProp* será um dos seguintes.

    

    | Parâmetro                   | Usado para                                                |
    |-----------------------------|---------------------------------------------------------|
    | MSAAPROPID \_ ROLEMAP         | Para definir um mapa de função para exibição de lista ou controles de exibição de árvore.  |
    | MSAAPROPID \_ STATEMAP        | Para definir um mapa de estado para exibição de lista ou controles de exibição de árvore. |
    | PROPID \_ ACC \_ DESCRIPTIONMAP | Para definir um mapa de descrição para exibição de lista ou exibições de árvore.   |
    | \_VALUEMAP MSAAPROPID        | Para definir um mapa de valor em controles deslizantes.                  |

    

     

4.  **Limpar.**

    Antes de destruir qualquer controle de mapa de valor anotado (por exemplo, ao manipular o [WM \_ Destroy](../winmsg/wm-destroy.md)), você deve limpar as propriedades previamente registradas e liberar o Gerenciador de anotações.

    Para fazer isso, chame [**IAccPropServices:: ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) conforme apropriado e solte o ponteiro para [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices).

Para o código de exemplo, consulte [exemplo de anotação de mapa de valor](value-map-annotation-sample.md).

 

 