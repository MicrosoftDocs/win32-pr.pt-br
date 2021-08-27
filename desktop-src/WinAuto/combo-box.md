---
title: Caixa de combinação (Referência de elemento de interface do usuário MSAA)
description: Uma caixa de combinação é uma caixa de listagem combinada com um controle estático ou um controle de edição que exibe o item selecionado no momento na parte da caixa de listagem da caixa de combinação.
ms.assetid: 3fb2c0b0-507f-4520-845b-b3fbfd9e7b60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3a8d26fa5b8cb264c06e7aa64c672e0a80e8ada7e90a152b3b941ea207cade
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071836"
---
# <a name="combo-box-msaa-ui-element-reference"></a>Caixa de combinação (Referência de elemento de interface do usuário MSAA)

> [!Note]  
> Este tópico descreve objetos **Combo Box** para fins de Referência de Elemento de Interface do Usuário da MSAA. Como criar objetos **do Combo Box** em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência de API para a estrutura de interface do usuário que você está usando.

 

Uma caixa de combinação é uma caixa de listagem combinada com um controle estático ou um controle de edição que exibe o item selecionado no momento na parte da caixa de listagem da caixa de combinação. A parte da caixa de listagem do controle é exibida em todos os momentos ou só é listada quando o usuário seleciona a seta para baixo (que é um botão de push) ao lado do controle. Se o campo de seleção for um controle de edição, o usuário poderá inserir informações que não estão na lista; caso contrário, o usuário só poderá selecionar itens na lista.

O nome da classe de janela para uma caixa de combinação é "COMBOBOX".

O conteúdo das [**propriedades IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) depende de qual das seguintes partes da caixa de combinação é consultada pelo cliente:

-   A janela da caixa de combinação
-   O controle de edição ou controle de texto estático
-   A seta para baixo (que é um botão de push)
-   A caixa de listagem
-   Os itens de lista na caixa de listagem

## <a name="iaccessible-methods"></a>Métodos IAccessible

As caixas de combinação suportam os seguintes métodos [**IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**Accdodefaultaction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)
-   [**Acchittest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**Acclocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**Accnavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**Accselect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades IAccessible

As caixas de combinação suportam as [**seguintes propriedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)— a tabela a seguir mostra o valor de contagem filho para diferentes partes da caixa de combinação. 

    | Parte da caixa de combinação   | ChildCount               |
    |------------------|--------------------------|
    | Janela caixa de combinação | 3                        |
    | Editar controle     | 0                        |
    | Seta para baixo  | 0                        |
    | Caixa de listagem         | O número de itens de lista |
    | Item de lista        | 0                        |

    

     

-   [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)— a tabela a seguir mostra a **propriedade DefaultAction** para diferentes partes de uma caixa de combinação. 

    | Parte da caixa de combinação   | Defaultaction                                                  |
    |------------------|----------------------------------------------------------------|
    | Janela caixa de combinação | Nenhum                                                           |
    | Editar controle     | Nenhum                                                           |
    | Seta para baixo  | "Abrir" ou "Fechar" dependendo do estado da lista lista listada |
    | Caixa de listagem         | Nenhum                                                           |
    | Item de lista        | "Clique duas vezes"                                                 |

    

     

-   [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)— A tabela a seguir mostra a propriedade **KeyboardShortcut** para diferentes partes de uma caixa de combinação. 

    | Parte da caixa de combinação   | KeyboardShortcut               |
    |------------------|--------------------------------|
    | Janela caixa de combinação | Chave de acesso do rótulo associado |
    | Editar controle     | Nenhum                           |
    | Seta para baixo  | "Alt+Seta para Baixo"               |
    | Caixa de listagem         | Nenhum                           |
    | Item de lista        | Nenhum                           |

    

     

    A chave de acesso para uma caixa de combinação é o caractere sublinhado no texto de um controle de texto estático associado que rotula a caixa de combinação. Por exemplo, em uma caixa de diálogo Abrir padrão que abre arquivos, como no Microsoft WordPad, a caixa de combinação rotulada "Arquivos do tipo:" tem o **KeyboardShortcut** "Alt+t".

-   [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)— a tabela a seguir mostra a **propriedade Name** para diferentes partes de uma caixa de combinação. 

    | Parte da caixa de combinação   | Nome                                                           |
    |------------------|----------------------------------------------------------------|
    | Janela caixa de combinação | Controle de texto estático usado como um rótulo                            |
    | Editar controle     | Controle de texto estático usado como um rótulo                            |
    | Seta para baixo  | "Abrir" ou "Fechar" dependendo do estado da lista lista listada |
    | Caixa de listagem         | Rótulo associado                                               |
    | Item de lista        | Texto do item de lista                                          |

    

     

    A **propriedade Name** de uma caixa de combinação, seu controle de edição filho e sua caixa de listagem filho é o texto de um controle de texto estático associado que rotula a caixa de combinação. Por exemplo, em uma caixa de diálogo Abrir padrão que  abre arquivos, como no WordPad, as propriedades Name das duas caixas de combinação são "Look in:" e "Files of type:".

-   [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)— A tabela a seguir mostra o valor pai para diferentes partes de uma caixa de combinação. 

    | Parte da caixa de combinação                        | Pai                                                                                                                                                                                                         |
    |---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Janela caixa de combinação                      | Uma janela com a **propriedade Role** de ROLE [**SYSTEM \_ \_ WINDOW**](object-roles.md) que envolve a caixa de combinação e tem a mesma propriedade **Name** e o mesmo nome de classe de janela que a caixa de combinação. |
    | Controle de edição (ou controle de texto estático) | A janela da caixa de combinação.                                                                                                                                                                                          |
    | Seta para baixo                       | A janela da caixa de combinação.                                                                                                                                                                                          |
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

 

 




