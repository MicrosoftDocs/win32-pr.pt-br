---
title: Texto estático (referência de elemento de interface do usuário do MSAA)
description: Os controles de texto estáticos fornecem uma maneira conveniente de exibir texto em caixas de diálogo e outras janelas. Controles de texto estáticos geralmente servem como rótulos para outros controles.
ms.assetid: 2c4b29bc-54e6-4c96-93a3-1fcb96d68269
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f35581a9b305f28782d8faeac81105afb0d5147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822989"
---
# <a name="static-text-msaa-ui-element-reference"></a>Texto estático (referência de elemento de interface do usuário do MSAA)

Os controles de texto estáticos fornecem uma maneira conveniente de exibir texto em caixas de diálogo e outras janelas. Controles de texto estáticos geralmente servem como rótulos para outros controles.

O nome de classe da janela para um controle de texto estático é "estático".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Os controles de texto estáticos dão suporte aos seguintes métodos de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

Os controles de texto estáticos dão suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propriedade                                                                             | Comentários                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                               |
| [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | A propriedade **ChildCount** é zero.                                                                                                                                                                                                                                                          |
| [**obter \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                               |
| [**obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                               |
| [**obter \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                               |
| [**obter \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                               |
| [**obter \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | A propriedade **KeyboardShortcut** é a chave de acesso, que é o caractere sublinhado no texto que ativa o controle associado ao texto estático. A cadeia de caracteres retornada contém o caractere de chave de acesso anexado à cadeia de caracteres "Alt +".                                           |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | A propriedade **Name** é igual ao texto no controle de texto estático.                                                                                                                                                                                                                     |
| [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | A propriedade **Parent** é uma janela ( [**\_ \_ janela do sistema de funções**](object-roles.md) ) que circunda o controle e tem a mesma propriedade **Name** e o nome da classe Window que o controle.                                                                                   |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | A propriedade **role** é [**\_ System role \_ STATICTEXT**](object-roles.md).                                                                                                                                                                                             |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | A propriedade **State** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md): [**estado \_ sistema \_ somente leitura**](object-state-constants.md) sistema de estado \| [**\_ \_ invisível**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Observações

-   O método [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) retorna DISP \_ E \_ MEMBERNOTFOUND quando ele é chamado com [**SELFLAG \_ TAKEFOCUS**](selflag.md) em um objeto de texto estático.
-   Os controles estáticos com o \_ estilo de ícone SS retornam dados inválidos na propriedade **Name** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





