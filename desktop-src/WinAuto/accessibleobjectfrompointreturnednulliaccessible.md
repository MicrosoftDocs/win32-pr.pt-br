---
title: AccessibleObjectFromPointReturnedNullIAccessible
description: AccessibleObjectFromPointReturnedNullIAccessible
ms.assetid: DF786659-8ADC-4EB0-A606-8B80C139691A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c5807fa04f69271f2a2d38e7014b1cd17d4eaa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292756"
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

 

 




