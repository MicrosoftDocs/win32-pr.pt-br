---
title: Caixa de diálogo (referência de elemento de interface do usuário do MSAA)
description: Uma caixa de diálogo é uma janela temporária que um aplicativo cria para recuperar a entrada do usuário.
ms.assetid: 7d132c2c-eab1-4132-b2b6-fa1f8b142f58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75214998ac54659196bd64100b806e5768df176e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641158"
---
# <a name="dialog-box-msaa-ui-element-reference"></a>Caixa de diálogo (referência de elemento de interface do usuário do MSAA)

> [!Note]  
> Este tópico descreve os objetos da **caixa de diálogo** para fins de referência de elemento da interface do usuário do MSAA. A criação de objetos de **caixa de diálogo** em várias estruturas de interface do usuário não é descrita aqui. Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.

 

Uma caixa de diálogo é uma janela temporária que um aplicativo cria para recuperar a entrada do usuário. Um aplicativo usa caixas de diálogo para solicitar ao usuário informações adicionais sobre os comandos que o usuário escolheu em um menu. Uma caixa de diálogo contém um ou mais controles (janelas filhas) com os quais o usuário digita texto, escolhe opções ou direciona a ação do comando.

O nome da classe de janela para caixas de diálogo é " \# 32770".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Uma caixa de diálogo dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Método                                                                    | Comentários                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Se a caixa de diálogo contiver um botão de ação padrão, o método [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) chamará [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com a mensagem de botão [**BM \_ Click**](/windows/desktop/Controls/bm-click) para clicar no botão Push padrão. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                                                                        |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                                                                        |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                                                                        |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                                                                        |



 

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

Uma caixa de diálogo dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propriedade                                                                                 | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)                 | A propriedade **ChildCount** é igual ao número de controles de janela filho na caixa de diálogo.                                                                                                                                                                                                                                                                                                                                                                           |
| [**obter \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)           | Se a caixa de diálogo contiver um botão de ação padrão, a propriedade **DefaultAction** será "pressionar".                                                                                                                                                                                                                                                                                                                                                                             |
| [**obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obter \_ accKeyboardShortcut**](/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Normalmente, as caixas de diálogo não têm atalhos de teclado. Se o texto da janela da caixa de diálogo contiver um caractere de e comercial (&), o Microsoft Acessibilidade Ativa retornará uma cadeia de caracteres não nula como a propriedade **KeyboardShortcut** .                                                                                                                                                                                                                                        |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                             | A propriedade **Name** é o texto da janela, ou legenda, que é exibido na barra de título da caixa de diálogo.                                                                                                                                                                                                                                                                                                                                                              |
| [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                         | A propriedade **Parent** é uma janela ( [**\_ \_ janela do sistema de funções**](object-roles.md) ) que envolve a caixa de diálogo e tem a mesma propriedade de **nome** e nome de classe de janela que a caixa de diálogo.                                                                                                                                                                                                                                                        |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                             | A propriedade **role** é [**caixa \_ de \_ diálogo do sistema de função**](object-roles.md) ou sistema de [**função \_ \_ PROPERTYPAGE**](object-roles.md).                                                                                                                                                                                                                                                                                                 |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                           | A propriedade de **estado** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md):[**estado \_ sistema \_ invisível**](object-state-constants.md) \| [**estado \_ sistema \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) sistema estado \| [**\_ \_ foco**](object-state-constants.md)<br/> |



 

## <a name="remarks"></a>Comentários

O objeto Dialog não oferece suporte ao método [**Get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) . Para obter um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para um controle em uma caixa de diálogo, os clientes devem obter o identificador de janela do controle e, em seguida, chamar [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

