---
title: IDXCoreAdapter
description: A interface **IDXCoreAdapter**   implementa métodos para recuperar detalhes sobre um item de adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0930ce76353d556f7839f476ec8979823eac3a6c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084820"
---
# <a name="idxcoreadapter-interface"></a>Interface IDXCoreAdapter

A interface **IDXCoreAdapter**   implementa métodos para recuperar detalhes sobre um item de adaptador. **IDXCoreAdapter** herda da interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Para obter diretrizes de programação e exemplos de código, consulte [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).

## <a name="remarks"></a>Comentários

As propriedades de um adaptador são estabelecidas no momento em que o adaptador é iniciado e são imutáveis durante o tempo de vida do adaptador. Isso é diferente do estado de um adaptador, que pode ser consultado ou definido, e os valores que podem ser alterados ao longo do tempo.

## <a name="see-also"></a>Confira também

[Referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)