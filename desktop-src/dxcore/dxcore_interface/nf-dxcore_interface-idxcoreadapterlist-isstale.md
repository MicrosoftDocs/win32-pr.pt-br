---
title: IDXCoreAdapterList::IsStale
description: Determina se as alterações nesse sistema resultaram na desa atualidade desse objeto de lista de adaptadores DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: a40a590a76773592d5442993c75149b2349880f7681d625e777d363062f5c4be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118502567"
---
# <a name="idxcoreadapterlistisstale-method"></a>Método IDXCoreAdapterList::IsStale

Determina se as alterações nesse sistema resultaram na desa atualidade desse objeto de lista de adaptadores DXCore. Para obter diretrizes de programação e exemplos de código, consulte [Usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Sintaxe

```cpp
virtual bool STDMETHODCALLTYPE IsStale() = 0;
```

## <a name="returns"></a>Retornos

Tipo: **bool**

Retornará se, desde a geração da lista, ocorrerem alterações nas condições do sistema que causaria esta lista `true` de adaptadores se tornar desaleilado. Caso contrário, retorna `false`.

## <a name="remarks"></a>Comentários

Você pode sondar **IsStale** para determinar se a alteração das condições do sistema fez com que essa lista se tornava desaconsole. Se **IsStale retornar** uma vez, ele retornará pelo tempo de vida restante `true` do objeto de lista de `true` adaptadores DXCore. Um objeto de lista desleisado ainda será considerado desaleado mesmo se as condições do sistema retornarem a um estado que corresponde à lista (as mesmas condições agora são obtidas como quando a lista foi gerada pela primeira vez).

## <a name="see-also"></a>Confira também

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [Referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)