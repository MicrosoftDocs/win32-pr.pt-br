---
title: Controle de edição (referência de elemento de interface do usuário do MSAA)
description: Os controles de edição permitem que um usuário exiba e edite o texto.
ms.assetid: a42c73f2-4005-4db9-84bc-637c9c4310f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dde6e562b651b91376bc7d675b2b71ac999cf48
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498814"
---
# <a name="edit-control-msaa-ui-element-reference"></a>Controle de edição (referência de elemento de interface do usuário do MSAA)

> [!Note]  
> Este tópico descreve os objetos de **controle de edição** para fins de referência de elemento de interface do usuário do MSAA. Como criar objetos de **controle de edição** em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.

 

Os controles de edição permitem que um usuário exiba e edite o texto. Os controles de edição são criados com muitos estilos diferentes, como ES \_ MULTILINE. Esse estilo cria um controle de edição de várias linhas, como a área do bloco de notas do cliente, e ES \_ ReadOnly, que cria um controle de edição somente leitura.

O Microsoft Acessibilidade Ativa não faz uma distinção entre os controles de edição criados com o nome de classe de janela "EDIT" e os controles de edição avançados criados com o nome de classe de janela "RichEdit" ou "RichEdit20A".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Os controles de edição dão suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

Os controles de edição dão suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propriedade                                                                             | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**obter \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**obter \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | A propriedade **KeyboardShortcut** é a tecla de acesso do controle de edição, que é um caractere sublinhado no texto do rótulo do controle de edição. Por exemplo, em uma caixa de diálogo de abertura de arquivo padrão, como no WordPad, o **KeyboardShortcut** para o controle de edição rotulado "filename:" é "Alt + n".                                                                                                                                                                                                                                                                                                                                        |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | A propriedade **Name** é o texto de um controle de texto estático que rotula o controle de edição. Por exemplo, em uma caixa de diálogo de abertura de arquivo padrão, como no WordPad, a propriedade **Name** para o controle de edição é "nome do arquivo:".                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | A propriedade **Parent** é uma janela ( [**\_ \_ janela do sistema de funções**](object-roles.md) ) que circunda o controle e tem a mesma propriedade **Name** e o nome da classe Window que o controle.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | A propriedade **role** é [**um \_ \_ texto do sistema de função**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**obter \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | A propriedade de **estado** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md): estado do sistema estado [**\_ \_ invisível**](object-state-constants.md) sistema de estado com \| [**\_ \_ foco**](object-state-constants.md) sistema de estado de \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ leitura**](object-state-constants.md) do \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) sistema estado do sistema do estado protegido System<br/> |
| [**obter \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | A propriedade **Value** é uma única cadeia de caracteres que contém o texto no controle de edição. No entanto, se o controle for protegido por senha, a propriedade **Value** retornará E \_ ACCESSDENIED. Para controles de edição de várias linhas, a cadeia de caracteres contém um retorno de carro e um caractere de nova linha no final de cada linha.                                                                                                                                                                                                                                                                                                                               |



 

## <a name="notes"></a>Observações

-   O Microsoft Acessibilidade Ativa não oferece suporte à seleção do texto contido em controles editar e Rich Edit porque o texto é exposto como uma cadeia de caracteres na propriedade **Value** do objeto.
-   O controle rich edit fornecido pelo Riched20.dll (que é usado em editores de texto como o WordPad no Windows 98) não envia nenhum WinEvents quando a posição do cursor é alterada durante a seleção de texto. Quando os usuários pressionam SHIFT e teclas de seta para selecionar texto, o objeto de cursor não dispara o [**objeto de evento \_ \_ LOCATIONCHANGE**](event-constants.md) WinEvent. Quando a seleção é definida programaticamente por meio de mensagens de edição avançadas, o objeto de cursor não envia nenhum evento para indicar sua nova posição.

    Todos os aplicativos que usam Riched20.dll apresentam esse problema. Os aplicativos que usam versões anteriores do controle de edição rico enviam eventos corretamente com base na seleção.

-   O valor de **estado** para controles de edição de senha sempre inclui o sistema de estado de sinalizador de bits [**\_ \_ protegido**](object-state-constants.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





