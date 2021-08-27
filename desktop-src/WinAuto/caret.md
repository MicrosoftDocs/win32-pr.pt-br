---
title: Circunflexo (referência de elemento de interface do usuário MSAA)
description: O cursor é uma linha, bloco ou bitmap piscando na área do cliente de uma janela ou em um controle que aceita entrada de teclado.
ms.assetid: f2c48c36-1859-4e0a-8833-3ca90b4da323
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287f846940a9180885da84cf8a030672b1473eab
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467293"
---
# <a name="caret-msaa-ui-element-reference"></a>Circunflexo (referência de elemento de interface do usuário MSAA)

> [!Note]  
> Este tópico descreve os Cursors para fins de referência de elemento da interface do usuário do MSAA. Como usar os Cursors em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.

 

O cursor é uma linha, bloco ou bitmap piscando na área do cliente de uma janela ou em um controle que aceita entrada de teclado. Indica o local no qual o texto ou os gráficos são inseridos. Como apenas uma janela de cada vez tem o foco do teclado, há apenas um cursor no sistema.

## <a name="iaccessible-methods"></a>Métodos IAccessible

O cursor dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

O cursor dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :




| Propriedade | Comentários | 
|----------|----------|
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a> | A propriedade <strong>ChildCount</strong> é zero. | 
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a> | A propriedade <strong>Name</strong> é "Edit". | 
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a> | A propriedade de <strong>função</strong> é <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>. | 
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a> | Os valores possíveis para a propriedade <strong>State</strong> incluem:<ul><li>Zero, o que significa que o cursor está visível</li><li><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></li></ul> | 




 

## <a name="notes"></a>Observações

-   Ao contrário de outros elementos da interface do usuário, o objeto de cursor não tem um identificador de janela associado. Para obter acesso ao objeto de cursor, os clientes devem definir um [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) e aguardar o objeto de cursor gerar eventos.
-   o objeto de cursor no controle rich edit fornecido pelo Riched20.dll (que é usado em editores de texto como o Microsoft WordPad no Windows 98) não envia nenhum [WinEvents](winevents-infrastructure.md) quando sua posição é alterada durante a seleção de texto. Quando os usuários pressionam SHIFT e teclas de seta para selecionar texto, o objeto de cursor não dispara o [**objeto de evento \_ \_ LOCATIONCHANGE**](event-constants.md) WinEvent. Da mesma forma, quando a seleção é definida programaticamente por meio de mensagens de edição avançadas, o objeto de cursor não envia nenhum evento para indicar sua nova posição.

    Todos os aplicativos que usam Riched20.dll apresentam esse problema. Os aplicativos que usam versões anteriores do controle de edição rico enviam eventos corretamente com base na seleção.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




