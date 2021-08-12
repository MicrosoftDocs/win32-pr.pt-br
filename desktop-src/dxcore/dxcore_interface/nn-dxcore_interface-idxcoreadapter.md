---
title: IDXCoreAdapter
description: A interface **IDXCoreAdapter** implementa métodos para recuperar detalhes sobre um item de adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 18cdd8082701ea4f1a8b5a3cfa047decd0f77df81b17eebe49bf5a8a887663fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118278783"
---
# <a name="idxcoreadapter-interface"></a>Interface IDXCoreAdapter

A interface **IDXCoreAdapter** implementa métodos para recuperar detalhes sobre um item de adaptador. **IDXCoreAdapter** herda da interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Para obter diretrizes de programação e exemplos de código, consulte [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).

## <a name="remarks"></a>Comentários

As propriedades de um adaptador são estabelecidas no momento em que o adaptador é iniciado e são imutáveis durante o tempo de vida do adaptador. Isso é diferente do estado de um adaptador, que pode ser consultado ou definido, e os valores que podem ser alterados ao longo do tempo.

## <a name="see-also"></a>Confira também

[Referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)