---
title: IDXCoreAdapterList::IsStale
description: Determina se as alterações feitas neste sistema resultaram no desatualização deste objeto da lista de adaptadores DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 68b4e4ba6f3434f76ea5b4a2a98ae4e83486f61e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105793751"
---
# <a name="idxcoreadapterlistisstale-method"></a>Método IDXCoreAdapterList:: isobsoleto

Determina se as alterações feitas neste sistema resultaram no desatualização deste objeto da lista de adaptadores DXCore. Para obter diretrizes de programação e exemplos de código, consulte [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Syntax

```cpp
virtual bool STDMETHODCALLTYPE IsStale() = 0;
```

## <a name="returns"></a>Retornos

Tipo: **bool**

Retorna  `true`   se, desde a geração da lista, ocorreram alterações nas condições do sistema que poderiam fazer com que essa lista de adaptadores se torne obsoleta. Caso contrário, retorna  `false` .

## <a name="remarks"></a>Comentários

Você pode sondar **isobsoleta** para determinar se as condições de alteração do sistema levaram a esta lista ficando desatualizadas. Se **isobsoleto** retornar `true` uma vez, ele retornará `true` para o tempo de vida restante do objeto de lista do adaptador DXCore. Um objeto de lista obsoleto ainda é considerado obsoleto mesmo que as condições do sistema retornem a um estado que corresponda à lista (as mesmas condições obtêm-se agora como era quando a lista foi gerada pela primeira vez).

## <a name="see-also"></a>Confira também

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)