---
title: AccessibleObjectFromPointReturnedNullIAccessible
description: AccessibleObjectFromPointReturnedNullIAccessible
ms.assetid: DF786659-8ADC-4EB0-A606-8B80C139691A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71963ad564454dcb90266b4fe4c63ba7282dbc514ab286629798420ff1db9f6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327691"
---
# <a name="accessibleobjectfrompointreturnednulliaccessible"></a>AccessibleObjectFromPointReturnedNullIAccessible

## <a name="text"></a>Texto

AccessibleObjectFromPoint ( {0} , {1} ) retornou NULL

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

O endereço da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do elemento de interface do usuário obtida para as coordenadas fornecidas é nulo.

## <a name="possible-causes"></a>Possíveis causas

-   A interação do usuário durante a verificação, como a movimentação do foco para um HWND não-alvo, interfere no processo de verificação.
-   Uma implementação de MSAA incorreta ou inválida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Navegação por meio de teste de clique e local da tela](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




