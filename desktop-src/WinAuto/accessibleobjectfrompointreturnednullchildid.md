---
title: AccessibleObjectFromPointReturnedNullChildId
description: AccessibleObjectFromPointReturnedNullChildId
ms.assetid: 20511B76-736B-4B43-8DC3-4306DF74CF73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb6ebf33cdfdef7b6e32ec4b9943accc06551d5f37f625fa77cb22e01b913df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994356"
---
# <a name="accessibleobjectfrompointreturnednullchildid"></a>AccessibleObjectFromPointReturnedNullChildId

## <a name="text"></a>Texto

AccessibleObjectFromPoint ( {0} , {1} ) retornou um childID nulo

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

A childID da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do objeto obtida para as coordenadas fornecidas é nula.

## <a name="possible-causes"></a>Possíveis causas

A interação do usuário durante a verificação, como a movimentação do foco para um HWND não-alvo, interfere no processo de verificação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Navegação por meio de teste de clique e local da tela](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




