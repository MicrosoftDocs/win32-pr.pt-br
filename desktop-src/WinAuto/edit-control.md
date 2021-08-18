---
title: Controle Editar (Referência de elemento de interface do usuário MSAA)
description: Editar controles permitem que um usuário veja e edite texto.
ms.assetid: a42c73f2-4005-4db9-84bc-637c9c4310f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3844dcdf99f925813765ae46494b0ff70345c086f3845304fff0e53d70f07d22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829840"
---
# <a name="edit-control-msaa-ui-element-reference"></a>Controle Editar (Referência de elemento de interface do usuário MSAA)

> [!Note]  
> Este tópico descreve Editar **objetos de controle** para fins de referência de elemento de interface do usuário da MSAA. Como criar objetos **editar controle** em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência de API para a estrutura de interface do usuário que você está usando.

 

Editar controles permitem que um usuário veja e edite texto. Controles de edição são criados com muitos estilos diferentes, como ES \_ MULTILINE. Esse estilo cria um controle de edição multilinha, como a área de cliente do Bloco de notas e o ES READONLY, que cria um controle de \_ edição somente leitura.

Microsoft Active Accessibility faz uma distinção entre controles de edição criados com o nome de classe de janela "EDIT" e controles de edição rich criados com o nome de classe de janela "RichEdit" ou "RichEdit20A".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Os controles de edição suportam os seguintes métodos [**IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**Acchittest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**Acclocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**Accnavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**Accselect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades IAccessible

Os controles de edição são suportados com as seguintes propriedades [**IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propriedade                                                                             | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | A **propriedade KeyboardShortcut** é a chave de acesso do controle de edição, que é um caractere sublinhado no texto do rótulo do controle de edição. Por exemplo, em uma caixa de diálogo Abrir Arquivo padrão, como no WordPad, **o KeyboardShortcut** para o controle de edição rotulado como "Filename:" é "Alt+n".                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | A **propriedade Name** é o texto de um controle de texto estático que rotula o controle de edição. Por exemplo, em uma caixa de diálogo Abrir Arquivo padrão, como no WordPad, a propriedade **Name** do controle de edição é "Nome do arquivo:".                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | A **propriedade Parent** é uma janela ( ROLE SYSTEM [**\_ \_ WINDOW**](object-roles.md) ) que envolve o controle e tem a mesma propriedade **Name** e o mesmo nome de classe de janela que o controle.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | A **propriedade Role** é ROLE SYSTEM [**\_ \_ TEXT.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | A **propriedade State** é uma combinação de um ou mais dos seguintes valores: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE SYSTEM FOCUSABLE [](object-state-constants.md)STATE FOCUSABLE STATE SYSTEM \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ READONLY**](object-state-constants.md) STATE \| [**\_ \_ PROTECTED**](object-state-constants.md) STATE SYSTEM \| [**\_ \_ NORMAL**](object-state-constants.md)<br/> |
| [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | A **propriedade Value** é uma única cadeia de caracteres que contém o texto no controle de edição. No entanto, se o controle for protegido por senha, **a propriedade Value** retornará E \_ ACCESSDENIED. Para controles de edição multilinha, a cadeia de caracteres contém um retorno de carro e um caractere de nova linha no final de cada linha.                                                                                                                                                                                                                                                                                                                               |



 

## <a name="notes"></a>Observações

-   Microsoft Active Accessibility não dá suporte à seleção do texto contido em controles de edição e edição rich porque o texto é exposto como uma cadeia de caracteres na propriedade **Value do** objeto.
-   O controle de edição rich fornecido pelo Riched20.dll (que é usado em editores de texto, como WordPad no Windows 98) não envia nenhum WinEvents quando a posição do aponto é alterada durante a seleção de texto. Quando os usuários pressionam shift e teclas de seta para selecionar texto, o objeto de acionador não dispara [**o EVENT \_ OBJECT \_ LOCATIONCHANGE**](event-constants.md) WinEvent. Quando a seleção é definida programaticamente por meio de mensagens de edição rich, o objeto de cursor não envia eventos para indicar sua nova posição.

    Todos os aplicativos que usam Riched20.dll apresentam esse problema. Aplicativos que usam versões anteriores do controle de edição rich enviam eventos corretamente com base na seleção.

-   O **valor estado** para controles de edição de senha sempre inclui o sinalizador de bit STATE SYSTEM [**\_ \_ PROTECTED**](object-state-constants.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[IAccessible Interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





