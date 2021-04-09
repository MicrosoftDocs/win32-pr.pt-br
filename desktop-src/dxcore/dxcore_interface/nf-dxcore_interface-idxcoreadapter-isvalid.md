---
title: IDXCoreAdapter::IsValid
description: Determina se este objeto de adaptador DXCore ainda é válido.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: f58d8607b75253efda2e111eb358f576d36b65f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007926"
---
# <a name="idxcoreadapterisvalid-method"></a>Método IDXCoreAdapter:: IsValid

Determina se este objeto de adaptador DXCore ainda é válido. Para obter diretrizes de programação e exemplos de código, consulte [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Syntax

```cpp
virtual bool STDMETHODCALLTYPE IsValid() = 0;
```

## <a name="returns"></a>Retornos

Tipo: **bool**

Retorna  `true`   se este objeto de adaptador DXCore ainda é válido. Caso contrário, retorna  `false` .

## <a name="see-also"></a>Confira também

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)