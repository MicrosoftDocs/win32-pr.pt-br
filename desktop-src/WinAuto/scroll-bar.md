---
title: Barra de rolagem (Referência de elemento de interface do usuário MSAA)
description: As barras de rolagem permitem que um usuário escolha a direção e a distância para percorrer as informações em uma janela ou caixa de listagem relacionada. O nome da classe de janela para uma barra de rolagem é \ 0034; SCROLLBAR \ 0034;.
ms.assetid: a4ec1708-d751-4526-bd69-9796c43872a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6acb609ee56d6e766a2f94cf75406211741ba0a711699f4e8c912790dc71cffe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734326"
---
# <a name="scroll-bar-msaa-ui-element-reference"></a>Barra de rolagem (Referência de elemento de interface do usuário MSAA)

> [!Note]  
> Este tópico descreve objetos **da Barra de Rolagem** para fins de Referência de Elemento de Interface do Usuário da MSAA. Como criar objetos **da Barra de** Rolagem em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência de API para a estrutura de interface do usuário que você está usando.

 

As barras de rolagem permitem que um usuário escolha a direção e a distância para percorrer as informações em uma janela ou caixa de listagem relacionada. O nome da classe de janela para uma barra de rolagem é "SCROLLBAR".

O conteúdo das propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) depende se a barra de rolagem é vertical ou horizontal e em qual das seguintes partes da barra de rolagem está sendo consultada pelo cliente:

-   A própria barra de rolagem
-   O botão de seta para a parte superior ou direita
-   O botão de seta para baixo ou para a esquerda
-   A caixa de rolagem (thumb)
-   A página para cima ou a região direita da página
-   A página para baixo ou a região esquerda da página

## <a name="iaccessible-methods"></a>Métodos IAccessible

Uma barra de rolagem dá suporte aos seguintes métodos [**IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)— o próprio objeto da barra de rolagem e o thumb de rolagem não são suportados pelo **método accDoDefaultAction.**

    Para as outras partes da barra de rolagem em uma barra de rolagem vertical, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) chama [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com a mensagem [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll) com *wParam definido* com os valores a seguir.

    

    | Botão/Região       | Vaule        |
    |---------------------|--------------|
    | Botão de seta superior    | \_SBLT   |
    | Botão de seta inferior | LINEDOWN do SB \_ |
    | Page up região      | PAGEUP de SB \_   |
    | Page down região    | SB \_ PAGEDOWN |

    

     

    Para as outras partes da barra de rolagem em uma barra de rolagem horizontal, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) chama [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com a mensagem [**WM \_ HSCROLL**](/windows/desktop/Controls/wm-hscroll) com *wParam definido* com os valores a seguir.

    

    | Botão/Região      | Valor         |
    |--------------------|---------------|
    | Botão de seta para a esquerda  | SB \_ LINELEFT  |
    | Botão de seta para direita | SB \_ LINERIGHT |
    | Região esquerda da página   | SB \_ PAGELEFT  |
    | Região direita da página  | SB \_ PAGERIGHT |

    

     

-   [**Acchittest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**Acclocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**Accnavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>Propriedades IAccessible

Uma barra de rolagem dá suporte às [**seguintes propriedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)— a **propriedade ChildCount para** o objeto da barra de rolagem é cinco. Para as outras partes da barra de rolagem, a **propriedade ChildCount** é zero.
-   [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)— o próprio objeto da barra de rolagem e o thumb de rolagem não são suportados pela **propriedade DefaultAction.** A **propriedade DefaultAction** para os botões de seta e as áreas sombreadas em ambos os lados do botão de rolagem é "Pressionar".
-   [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)— a propriedade **Description** depende da parte da barra de rolagem consultada.

    As partes de uma barra de rolagem vertical têm as descrições a seguir.

    

    | Parte                | Descrição                                                                         |
    |---------------------|-------------------------------------------------------------------------------------|
    | Barra de rolagem em si   | "Usado para alterar a área de exibição vertical"                                          |
    | Botão de seta superior    | "Move a posição vertical para cima uma linha"                                           |
    | Botão de seta inferior | "Move a posição vertical para baixo uma linha"                                         |
    | Role o botão de rolagem        | "Indica a posição vertical atual e pode ser arrastado para alterá-la diretamente" |
    | Page up região      | "Move a posição vertical para cima algumas linhas"                                  |
    | Page down região    | "Indica a posição vertical atual e pode ser arrastado para alterá-la diretamente" |

    

     

    As partes de uma barra de rolagem horizontal têm as descrições a seguir.

    

    | Parte               | Descrição                                                                           |
    |--------------------|---------------------------------------------------------------------------------------|
    | Barra de rolagem em si  | "Usado para alterar a área de exibição horizontal"                                          |
    | Botão de seta para a esquerda  | "Move a posição horizontal para a esquerda de uma coluna"                                       |
    | Botão de seta para direita | "Move a posição horizontal para a direita de uma coluna"                                      |
    | Role o botão de rolagem       | "Indica a posição horizontal atual e pode ser arrastado para alterá-la diretamente" |
    | Região esquerda da página   | "Move a posição horizontal à esquerda de algumas colunas"                              |
    | Região direita da página  | "Indica a posição vertical atual e pode ser arrastado para alterá-la diretamente"   |

    

     

-   [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)— a **propriedade Name** depende da parte da barra de rolagem consultada.

    As partes de uma barra de rolagem vertical têm os seguintes nomes.

    | Parte                | Nome        |
    |---------------------|-------------|
    | Janela da barra de rolagem   | "Vertical"  |
    | Botão de seta superior    | "Line up"   |
    | Botão de seta inferior | "Linha para baixo" |
    | Role o botão de rolagem        | "Posição"  |
    | Page up região      | "Page up"   |
    | Page down região    | "Page down" |

    

     

    As partes de uma barra de rolagem horizontal têm os nomes a seguir.

    

    | Parte               | Nome           |
    |--------------------|----------------|
    | Janela de barra de rolagem  | Na   |
    | Botão de seta para a esquerda  | "Coluna à esquerda"  |
    | Botão de seta para direita | "Coluna à direita" |
    | Rolar o polegar       | Propostas     |
    | Região direita da página  | "Direita da página"   |
    | Região esquerda da página   | "Página à esquerda"    |

    

     

-   [**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)— a propriedade **Parent** dos botões de seta, scroll Thumb e a área sombreada em qualquer lado do Thumb é a janela da barra de rolagem. A propriedade **Parent** da janela da barra de rolagem é uma janela (janela do sistema de funções \_ \_ ) que envolve o controle e tem a mesma propriedade de **nome** e nome de classe de janela.
-   [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)– a propriedade de **função** depende da parte da barra de rolagem que é consultada. As partes de uma barra de rolagem têm as seguintes funções. 

    | Parte                                                  | Função                                                                    |
    |-------------------------------------------------------|-------------------------------------------------------------------------|
    | Barra de rolagem em si                                     | [**\_barra de rolagem do sistema de funções \_**](object-roles.md)   |
    | Botões de seta superior, inferior, esquerdo e direito              | [**\_pressão do sistema de funções \_**](object-roles.md) |
    | Rolar o polegar                                          | [**\_indicador do sistema de funções \_**](object-roles.md)   |
    | Páginas acima, Page Down, página à esquerda e à direita da página | [**\_pressão do sistema de funções \_**](object-roles.md) |

    

     

-   [**Get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)— a propriedade **State** de cada componente da barra de rolagem inclui uma combinação dos [valores](object-state-constants.md)a seguir.

    | Estado                                                                                 | Valor                                                                                                                                                                                                                       |
    |---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**sistema de estado \_ \_ invisível**](object-state-constants.md)     | Para a barra de rolagem, isso indica que a barra de rolagem vertical ou horizontal especificada não existe. Para as regiões Page Up ou Page Down, isso indica que o Thumb está posicionado de modo que a região não exista. |
    | [**Estado do \_ sistema \_ fora da tela**](object-state-constants.md)     | Para a barra de rolagem, isso indica que a janela é dimensionada de modo que a barra de rolagem vertical ou horizontal especificada não seja exibida no momento.                                                                         |
    | [**sistema de estado \_ \_ pressionado**](object-state-constants.md)         | O botão de seta ou a região da página é pressionado.                                                                                                                                                                                 |
    | [**sistema de estado \_ \_ indisponível**](object-state-constants.md) | O componente está desabilitado.                                                                                                                                                                                                  |

    

     

-   [**Get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)— a propriedade **Value** da janela da barra de rolagem indica a posição da barra de rolagem e é uma cadeia de caracteres que contém um inteiro de "0" a "100".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 