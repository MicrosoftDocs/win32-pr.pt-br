---
title: Controle Calendar (referência de elemento de interface do usuário do MSAA)
description: Os controles de calendário fornecem uma maneira simples e intuitiva para um usuário selecionar uma data de uma interface familiar.
ms.assetid: cfb1e420-bb8f-4100-9c83-304d11573c0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63acb3ca83f6b7e71740acee4232e081e11594e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822450"
---
# <a name="calendar-control-msaa-ui-element-reference"></a>Controle Calendar (referência de elemento de interface do usuário do MSAA)

> [!Note]  
> Este tópico descreve os objetos de **controle de calendário** para fins de referência de elemento de interface do usuário do MSAA. Como criar objetos de **controle de calendário** em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.

 

Os controles de calendário fornecem uma maneira simples e intuitiva para um usuário selecionar uma data de uma interface familiar.

O nome de classe da janela para um controle de calendário mensal é a \_ classe calendário mensal, que é definida como "SysMonthCal32" em commctrl. h. As informações neste tópico aplicam-se ao controle de calendário mensal na versão 5 do commctrl. h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Os controles de calendário dão suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

Os controles de calendário dão suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propriedade                                                                 | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | A propriedade **ChildCount** é zero.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | A propriedade **Name** é obtida do controle de texto estático que rotula o controle Calendar. Ao criar controles, os desenvolvedores de servidor devem garantir que um controle de texto estático preceda imediatamente o controle que ele rotula dentro da ordem de tabulação.                                                                                                                                                                                                                 |
| [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | A propriedade **Parent** é uma janela ( [**\_ \_ janela do sistema de funções**](object-roles.md) ) que circunda o controle e tem a mesma propriedade **Name** e o nome da classe Window que o controle.                                                                                                                                                                                                                                                             |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | A propriedade **role** é [**\_ \_ cliente do sistema de função**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                               |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | A propriedade de **estado** é uma combinação de um ou mais dos [valores](object-state-constants.md)a seguir sistema de estado [**\_ \_ invisível**](object-state-constants.md) sistema de estado \| [**\_ \_ indisponível**](object-state-constants.md) sistema de Estados \| [**focalizado sistema estado \_ \_ focado**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





