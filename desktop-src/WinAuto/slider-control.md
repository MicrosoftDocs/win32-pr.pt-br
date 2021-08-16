---
title: Controle Slider (referência de elemento de interface do usuário do MSAA)
description: Um controle deslizante, também chamado de controle TrackBar, permite que um usuário selecione um intervalo de valores movendo um controle deslizante. Os controles de volume no sistema operacional Windows são controles deslizantes.
ms.assetid: 8df4ed1d-d63c-49d7-94f1-df2113643484
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23d92799a8a644d5e5e00c695d628cb827ba60f73cc3a0d7b7f5dc505a6c2c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118564424"
---
# <a name="slider-control-msaa-ui-element-reference"></a>Controle Slider (referência de elemento de interface do usuário do MSAA)

> [!Note]  
> Este tópico descreve os objetos de **controle Slider** para fins de referência de elemento da interface do usuário do MSAA. Como criar objetos de **controle Slider** em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.

 

Um controle deslizante, também chamado de controle TrackBar, permite que um usuário selecione um intervalo de valores movendo um controle deslizante. Os controles de volume no sistema operacional Windows são controles deslizantes.

O nome da classe Window para um controle Slider é TRACKBAR \_ Class, que é definido como "msctls \_ TrackBar" em commctrl. h.

O conteúdo das propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) depende de o controle deslizante ser vertical ou horizontal e em quais das seguintes partes do controle deslizante é consultado pelo cliente:

-   Janela de controle deslizante
-   Thumb Slider
-   Área sombreada acima (ou para
-   Área sombreada abaixo (ou à direita) do controle deslizante

## <a name="iaccessible-methods"></a>Métodos IAccessible

Um controle deslizante dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

Um controle deslizante dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**obter \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [**obter \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [**obter \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**obter \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**Get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)— a propriedade **KeyboardShortcut** é a chave de acesso da janela de controle deslizante, que é um caractere sublinhado no texto do rótulo do controle deslizante. A cadeia de caracteres retornada contém o caractere de chave de acesso anexado à cadeia de caracteres "Alt +".
-   [**Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)— a propriedade **Name** depende da parte do controle deslizante que é consultado.

    As partes de um controle deslizante vertical têm os seguintes nomes:

    

    | Parte do controle deslizante                    | Nome                                |
    |--------------------------------|-------------------------------------|
    | Janela de controle deslizante                  | Controle de texto estático usado como um rótulo |
    | Thumb Slider                   | Propostas                          |
    | Área sombreada acima do controle deslizante | "Page Up"                           |
    | Área sombreada abaixo do controle deslizante | "Page Down"                         |

    

     

    As partes de um controle deslizante horizontal têm os seguintes nomes:

    

    | Parte do controle deslizante                              | Nome                                |
    |------------------------------------------|-------------------------------------|
    | Janela de controle deslizante                            | Controle de texto estático usado como um rótulo |
    | Thumb Slider                             | Propostas                          |
    | Área sombreada à esquerda do controle deslizante Thumb  | "Página à esquerda"                         |
    | Área sombreada à direita do controle deslizante | "Direita da página"                        |

    

     

-   [**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)— a propriedade **Parent** dos botões de seta, scroll Thumb e a área sombreada em ambos os lados do Thumb é a janela Slider. A propriedade **Parent** da janela Slider é uma janela ( [**\_ \_ janela do sistema de funções**](object-roles.md) ) que envolve o controle e tem a mesma propriedade de **nome** e nome de classe de janela.
-   [**Get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)— a propriedade **role** depende da parte do controle deslizante que é consultado. 

    | Parte do controle deslizante                                     | [Função](object-roles.md)                                                |
    |-------------------------------------------------|-------------------------------------------------------------------------|
    | Janela de controle deslizante                                   | [**\_controle deslizante do sistema de funções \_**](object-roles.md)         |
    | Thumb Slider                                    | [**\_indicador do sistema de funções \_**](object-roles.md)   |
    | Áreas sombreadas em qualquer lado do controle deslizante | [**\_pressão do sistema de funções \_**](object-roles.md) |

    

     

-   [**Get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)— os [valores](object-state-constants.md) para a propriedade **State** dependem da parte do controle deslizante que é consultado. 

    | Parte do controle deslizante                                     | Valores de estado possíveis                                                                                                                                                                                                                                                                                                                                                                                                           |
    |-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Janela de controle deslizante                                   | [**Estado \_ sistema \_ invisível**](object-state-constants.md) sistema de estado \| [**\_ \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) sistema de \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) estado focado System normal |
    | Thumb Slider                                    | Zero (0), o que significa que o objeto está visível ou estado sistema de estado [**\_ \_ invisível**](object-state-constants.md) sistema \| [**\_ \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ normal**](object-state-constants.md)                                                                                                                       |
    | Áreas sombreadas em qualquer lado do controle deslizante | Zero (0), o que significa que o objeto está visível ou estado sistema de estado [**\_ \_ invisível**](object-state-constants.md) sistema \| [**\_ \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ normal**](object-state-constants.md)                                                                                                                       |

    

     

-   [**Get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)— a propriedade **Value** da janela Slider indica a posição do Thumb e é uma cadeia de caracteres que contém um inteiro de "0" por meio de "100".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Barra de rolagem**](scroll-bar.md)
</dt> </dl>

 

 




