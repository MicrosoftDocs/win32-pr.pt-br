---
title: Barra de rolagem (referência de elemento da interface do usuário do MSAA)
description: As barras de rolagem permitem que um usuário escolha a direção e a distância para rolar as informações em uma janela ou caixa de listagem relacionada. O nome da classe da janela para uma barra de rolagem é \ 0034; SCROLLBAR \ 0034;.
ms.assetid: a4ec1708-d751-4526-bd69-9796c43872a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df381e0d532991f164f2c17d0a261dd3c5006619
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008309"
---
# <a name="scroll-bar-msaa-ui-element-reference"></a>Barra de rolagem (referência de elemento da interface do usuário do MSAA)

> [!Note]  
> Este tópico descreve os objetos da **barra de rolagem** para fins de referência de elemento da interface do usuário do MSAA. Como criar objetos de **barra de rolagem** em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.

 

As barras de rolagem permitem que um usuário escolha a direção e a distância para rolar as informações em uma janela ou caixa de listagem relacionada. O nome da classe da janela para uma barra de rolagem é "SCROLLBAR".

O conteúdo das propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) depende se a barra de rolagem é vertical ou horizontal e em quais das seguintes partes da barra de rolagem está sendo consultada pelo cliente:

-   A barra de rolagem em si
-   O botão de seta superior ou direita
-   O botão de seta para baixo ou para a esquerda
-   A caixa de rolagem (Thumb)
-   A região Page Up ou direita da página
-   A página para baixo ou a região esquerda da página

## <a name="iaccessible-methods"></a>Métodos IAccessible

Uma barra de rolagem dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)— o próprio objeto de barra de rolagem e o Thumb Scroll não dão suporte ao método **accDoDefaultAction** .

    Para as outras partes da barra de rolagem em uma barra de rolagem vertical, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) [**chama a mensagem com**](/windows/desktop/api/winuser/nf-winuser-postmessagea) a mensagem [**\_ VSCROLL do WM**](/windows/desktop/Controls/wm-vscroll) com *wParam* definido com os valores a seguir.

    

    | Botão/região       | Valor        |
    |---------------------|--------------|
    | Botão de seta superior    | linha de SB \_   |
    | Botão de seta para baixo | SB \_ LINEDOWN |
    | Região de página acima      | SB \_ PageUp   |
    | Região de página abaixo    | SB \_ PageDown |

    

     

    Para as outras partes da barra de rolagem em uma barra de rolagem horizontal, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) [**chama a mensagem com**](/windows/desktop/api/winuser/nf-winuser-postmessagea) a mensagem [**\_ HSCROLL do WM**](/windows/desktop/Controls/wm-hscroll) com *wParam* definido com os valores a seguir.

    

    | Botão/região      | Valor         |
    |--------------------|---------------|
    | Botão de seta para a esquerda  | SB \_ LINELEFT  |
    | Botão de seta para direita | SB \_ LINERIGHT |
    | Região esquerda da página   | SB \_ PAGELEFT  |
    | Região direita da página  | SB \_ fixada |

    

     

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

Uma barra de rolagem dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**Get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)— a propriedade **ChildCount** para o objeto da barra de rolagem é cinco. Para as outras partes da barra de rolagem, a propriedade **ChildCount** é zero.
-   [**obter \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)– o próprio objeto de barra de rolagem e o Thumb Scroll não dão suporte à propriedade **DefaultAction** . A propriedade **DefaultAction** para os botões de seta e as áreas sombreadas em ambos os lados do polegar Thumb é "pressionar".
-   [**Get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)— a propriedade **Description** depende da parte da barra de rolagem que é consultada.

    As partes de uma barra de rolagem vertical têm as seguintes descrições.

    

    | Parte                | Descrição                                                                         |
    |---------------------|-------------------------------------------------------------------------------------|
    | Barra de rolagem em si   | "Usado para alterar a área de exibição vertical"                                          |
    | Botão de seta superior    | "Move a posição vertical uma linha acima"                                           |
    | Botão de seta para baixo | "Move a posição vertical uma linha abaixo"                                         |
    | Rolar o polegar        | "Indica a posição vertical atual e pode ser arrastado para alterá-la diretamente" |
    | Região de página acima      | "Move a posição vertical para cima em duas linhas"                                  |
    | Região de página abaixo    | "Indica a posição vertical atual e pode ser arrastado para alterá-la diretamente" |

    

     

    As partes de uma barra de rolagem horizontal têm as seguintes descrições.

    

    | Parte               | Descrição                                                                           |
    |--------------------|---------------------------------------------------------------------------------------|
    | Barra de rolagem em si  | "Usado para alterar a área de exibição horizontal"                                          |
    | Botão de seta para a esquerda  | "Move a posição horizontal uma coluna para a esquerda"                                       |
    | Botão de seta para direita | ' Move a posição horizontal uma coluna à direita "                                      |
    | Rolar o polegar       | "Indica a posição horizontal atual e pode ser arrastada para alterá-la diretamente" |
    | Região esquerda da página   | "Move a posição horizontal para a esquerda de duas colunas"                              |
    | Região direita da página  | "Indica a posição vertical atual e pode ser arrastado para alterá-la diretamente"   |

    

     

-   [**obter \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**obter \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)— a propriedade **Name** depende da parte da barra de rolagem que é consultada.

    As partes de uma barra de rolagem vertical têm os nomes a seguir.

    | Parte                | Nome        |
    |---------------------|-------------|
    | Janela de barra de rolagem   | Vertical  |
    | Botão de seta superior    | "Alinhar"   |
    | Botão de seta para baixo | "Linha abaixo" |
    | Rolar o polegar        | Propostas  |
    | Região de página acima      | "Page Up"   |
    | Região de página abaixo    | "Page Down" |

    

     

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

 

 