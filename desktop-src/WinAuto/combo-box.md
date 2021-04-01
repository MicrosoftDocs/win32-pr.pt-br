---
title: Caixa de combinação (referência de elemento de interface do usuário do MSAA)
description: Uma caixa de combinação é uma caixa de listagem combinada com um controle estático ou um controle de edição que exibe o item atualmente selecionado na parte da caixa de listagem da caixa de combinação.
ms.assetid: 3fb2c0b0-507f-4520-845b-b3fbfd9e7b60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce42bb3b0316b0fb2668fed23564b8f904fc793
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636101"
---
# <a name="combo-box-msaa-ui-element-reference"></a>Caixa de combinação (referência de elemento de interface do usuário do MSAA)

> [!Note]  
> Este tópico descreve os objetos da **caixa de combinação** para fins de referência de elemento da interface do usuário do MSAA. A criação de objetos de **caixa de combinação** em várias estruturas de interface do usuário não é descrita aqui. Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.

 

Uma caixa de combinação é uma caixa de listagem combinada com um controle estático ou um controle de edição que exibe o item atualmente selecionado na parte da caixa de listagem da caixa de combinação. A parte da caixa de listagem do controle é exibida sempre ou somente na lista suspensa quando o usuário seleciona a seta suspensa (que é um botão de ação) ao lado do controle. Se o campo de seleção for um controle de edição, o usuário poderá inserir informações que não estejam na lista; caso contrário, o usuário só poderá selecionar itens na lista.

O nome da classe da janela para uma caixa de combinação é "COMBOBOX".

O conteúdo das propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) depende de quais das seguintes partes da caixa de combinação são consultadas pelo cliente:

-   A janela da caixa de combinação
-   O controle de edição ou controle de texto estático
-   A seta suspensa (que é um botão de ação)
-   A caixa de listagem
-   Os itens da lista na caixa de listagem

## <a name="iaccessible-methods"></a>Métodos IAccessible

As caixas de combinação dão suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)
-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

As caixas de combinação dão suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**obter \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)– a tabela a seguir mostra o valor de contagem filho para diferentes partes da caixa de combinação. 

    | Parte da caixa de combinação   | ChildCount               |
    |------------------|--------------------------|
    | Janela de caixa de combinação | 3                        |
    | Controle de edição     | 0                        |
    | Seta suspensa  | 0                        |
    | Caixa de listagem         | O número de itens de lista |
    | Item de lista        | 0                        |

    

     

-   [**Get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)– a tabela a seguir mostra a propriedade **DefaultAction** para diferentes partes de uma caixa de combinação. 

    | Parte da caixa de combinação   | DefaultAction                                                  |
    |------------------|----------------------------------------------------------------|
    | Janela de caixa de combinação | Nenhum                                                           |
    | Controle de edição     | Nenhum                                                           |
    | Seta suspensa  | "Open" ou "Close" dependendo do estado da lista suspensa |
    | Caixa de listagem         | Nenhum                                                           |
    | Item de lista        | "Clique duplo"                                                 |

    

     

-   [**obter \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [**obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [**obter \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**obter \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**Get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)– a tabela a seguir mostra a propriedade **KeyboardShortcut** para diferentes partes de uma caixa de combinação. 

    | Parte da caixa de combinação   | KeyboardShortcut               |
    |------------------|--------------------------------|
    | Janela de caixa de combinação | Chave de acesso do rótulo associado |
    | Controle de edição     | Nenhum                           |
    | Seta suspensa  | "Alt + seta para baixo"               |
    | Caixa de listagem         | Nenhum                           |
    | Item de lista        | Nenhum                           |

    

     

    A tecla de acesso para uma caixa de combinação é o caractere sublinhado no texto de um controle de texto estático associado que rotula a caixa de combinação. Por exemplo, em uma caixa de diálogo aberta padrão que abre arquivos, como no Microsoft WordPad, a caixa de combinação rotulada "arquivos do tipo:" tem o **KeyboardShortcut** "Alt + t".

-   [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)– a tabela a seguir mostra a propriedade **Name** para diferentes partes de uma caixa de combinação. 

    | Parte da caixa de combinação   | Nome                                                           |
    |------------------|----------------------------------------------------------------|
    | Janela de caixa de combinação | Controle de texto estático usado como um rótulo                            |
    | Controle de edição     | Controle de texto estático usado como um rótulo                            |
    | Seta suspensa  | "Open" ou "Close" dependendo do estado da lista suspensa |
    | Caixa de listagem         | Rótulo associado                                               |
    | Item de lista        | Texto do item de lista                                          |

    

     

    A propriedade **Name** de uma caixa de combinação, seu controle de edição filho e sua caixa de listagem filho é o texto de um controle de texto estático associado que rotula a caixa de combinação. Por exemplo, em uma caixa de diálogo aberta padrão que abre arquivos, como no WordPad, as propriedades de **nome** para as duas caixas de combinação são "examinar:" e "arquivos do tipo:".

-   [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)– a tabela a seguir mostra o valor pai de diferentes partes de uma caixa de combinação. 

    | Parte da caixa de combinação                        | Pai                                                                                                                                                                                                         |
    |---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Janela de caixa de combinação                      | Uma janela com a propriedade **role** da [**\_ \_ janela do sistema de função**](object-roles.md) que circunda a caixa de combinação e tem a mesma propriedade **Name** e o nome da classe Window que a caixa de combinação. |
    | Controle de edição (ou controle de texto estático) | A janela da caixa de combinação.                                                                                                                                                                                          |
    | Seta suspensa                       | A janela da caixa de combinação.                                                                                                                                                                                          |
    | Janela pai da caixa de listagem                | A janela da caixa de combinação. Essa janela envolve a caixa de listagem.                                                                                                                                                      |
    | Caixa de listagem                              | A janela pai da caixa de listagem.                                                                                                                                                                                    |
    | Item de lista                             | A caixa de listagem.                                                                                                                                                                                                  |

    

     

-   [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)– a tabela a seguir mostra a propriedade de **função** para diferentes partes de uma caixa de combinação. 

    | Parte da caixa de combinação                        | [Função](object-roles.md)                                                                                                               |
    |---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
    | Janela de caixa de combinação                      | [**\_ComboBox do sistema de funções \_**](object-roles.md)                                                                    |
    | Controle de edição (ou controle de texto estático) | [**Função \_ do \_Texto do sistema**](object-roles.md) ou [ **sistema de função \_ \_ STATICTEXT**](object-roles.md) |
    | Seta suspensa                       | [**\_pressão do sistema de funções \_**](object-roles.md)                                                                |
    | Caixa de listagem                              | [**\_lista do sistema de funções \_**](object-roles.md)                                                                            |
    | Item de lista                             | [**\_ListItem do sistema de funções \_**](object-roles.md)                                                                    |

    

     

-   [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)– a tabela a seguir mostra a propriedade **State** para diferentes partes de uma caixa de combinação. 

    | Parte da caixa de combinação   | [Estados possíveis](object-state-constants.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
    |------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Janela de caixa de combinação | [**Estado \_ sistema \_ invisível**](object-state-constants.md) sistema de estado \| [**\_ \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) sistema de estado com \| [**\_ \_ foco**](object-state-constants.md) sistema de Estados \| [**\_ \_ normal**](object-state-constants.md) sistema de estado \| [**\_ \_ expandido**](object-state-constants.md) sistema de estado EXPANDED \| [**\_ \_ recolhido**](object-state-constants.md) |
    | Controle de edição     | [**Estado \_ sistema \_ invisível**](object-state-constants.md) sistema de estado \| [**\_ \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) sistema de \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) estado focado System normal                                                                                                                                                                         |
    | Seta suspensa  | 0, o que significa que o botão está visível e não é pressionado; ou [**sistema de estado \_ \_ pressionou**](object-state-constants.md) sistema de estado \| [**\_ \_ invisíveis**](object-state-constants.md) \| sistema de estado invisível \_ \_ normal                                                                                                                                                                                                                                                                                                                                                    |
    | Caixa de listagem         | [**Estado \_ sistema \_ Invisible**](object-state-constants.md) sistema de estado \| [**\_ \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) sistema \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) de estado previsível System Sistema Estadual de estado flutuante normal                                                                                      |
    | Item de lista        | [**Estado \_ sistema estado invisível sistema de estado \_ invisível**](object-state-constants.md) sistema de estado \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ focalizado**](object-state-constants.md) sistema de Estados \| [**\_ \_ selecionáveis**](object-state-constants.md) sistema de estado \| [**\_ \_ selecionado**](object-state-constants.md) System \| [**\_ \_ normal**](object-state-constants.md)                                                                                        |

    

     

-   [**Get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)– a tabela a seguir mostra a propriedade **Value** para diferentes partes de uma caixa de combinação. 

    | Parte da caixa de combinação   | Valor                                |
    |------------------|--------------------------------------|
    | Janela de caixa de combinação | Texto do item de lista selecionado no momento |
    | Controle de edição     | Texto do item de lista selecionado no momento |
    | Seta suspensa  | Nenhum                                 |
    | Caixa de listagem         | Nenhum                                 |
    | Item de lista        | Nenhum                                 |

    

     

## <a name="notes"></a>Observações

-   Quando [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) é chamado com o [**sinalizador \_ Next NAVDIR**](navigation-constants.md) na parte da caixa de listagem de uma caixa de combinação, ele navega incorretamente para a janela da bandeja quando deve retornar **VT \_ Empty**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




