---
title: Controle guia (referência de elemento de interface do usuário do MSAA)
description: Um controle guia define várias páginas para a mesma área de uma janela ou caixa de diálogo.
ms.assetid: 664dd109-3c4a-4106-9b92-e10ec5a33463
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78fe3216194da590b0c0802343afc41b1f7765c13d194e533163f9af2c22b287
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505656"
---
# <a name="tab-control-msaa-ui-element-reference"></a>Controle guia (referência de elemento de interface do usuário do MSAA)

> [!Note]  
> Este tópico descreve os objetos de **controle de guia** para fins de referência de elemento da interface do usuário do MSAA. Como criar objetos de **controle de guia** em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.

 

Um controle guia define várias páginas para a mesma área de uma janela ou caixa de diálogo. Cada página consiste em um conjunto de informações ou um grupo de controles que um aplicativo exibe quando o usuário seleciona a guia correspondente. o sistema operacional Windows usa controles guia para exibir os botões da barra de tarefas, com exceção do botão **iniciar** .

O nome de classe da janela para um controle guia é WC \_ TABCONTROL, que é definido como "SysTabControl" em commctrl. h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Um controle guia dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Método                                                                    | Comentários                                                                                                  |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | O método [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) clica na guia de página. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                           |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                           |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                           |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                           |



 

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

Um controle guia dá suporte às seguintes propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propriedade                                                                             | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obter \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | A propriedade **DefaultAction** é "switch".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**obter \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obter \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obter \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obter \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | A propriedade **KeyboardShortcut** é a tecla de acesso do controle guia, que é um caractere sublinhado no texto da janela do controle. Essa cadeia de caracteres contém o caractere de chave de acesso anexado à cadeia de caracteres "Alt +".                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | A propriedade **Name** é obtida no texto da janela do controle (ou legenda), que é exibido dentro do controle guia.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | A propriedade **Parent** é uma janela ( [**sistema de função \_ \_ PAGETABLIST**](object-roles.md) ) que circunda o controle e tem o mesmo nome de classe de janela que o controle.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | A propriedade **role** é [**\_ System role \_ PAGETAB**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**obter \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | A propriedade de **estado** é uma combinação de um ou mais dos [valores](object-state-constants.md)a seguir: estado do sistema de estado [**\_ \_ invisível**](object-state-constants.md) do sistema de estado selecionado sistema de estado \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ marcado**](object-state-constants.md) sistema de estado \| [**\_ \_ foco**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Observações

Os controles guia retornam incorretamente S \_ OK do método [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) quando chamado com o sinalizador [**SELFLAG \_ TAKEFOCUS**](selflag.md) . Controles de guia não podem assumir o foco do teclado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





