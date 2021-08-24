---
title: IDXCoreAdapter::IsAttributeSupported
description: Determina se este objeto de adaptador DXCore dá suporte ao atributo de adaptador especificado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 9dda05ca9dc1d3b7a7a84792c7ac122bb64144d5fdba3ad630be1a3f4d9ddf24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787076"
---
# <a name="idxcoreadapterisattributesupported-method"></a>Método IDXCoreAdapter:: IsAttributeSupported

Determina se este objeto de adaptador DXCore dá suporte ao atributo de adaptador especificado.

## <a name="syntax"></a>Sintaxe

```cpp
virtual bool STDMETHODCALLTYPE IsAttributeSupported( 
  REFGUID attributeGUID) = 0;
```

## <a name="parameters"></a>Parâmetros

### <a name="attributeguid"></a>attributeGUID

Tipo: **REFGUID**

Uma referência a um GUID de atributo de adaptador. Para obter uma lista de GUIDs de atributo, consulte [GUIDs de atributo do adaptador DXCore](../dxcore-adapter-attribute-guids.md).

## <a name="returns"></a>Retornos

Tipo: **bool**

Retorna `true` se este objeto de adaptador DXCore dá suporte ao atributo de adaptador especificado. Caso contrário, retorna `false`.

## <a name="see-also"></a>Confira também

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [referência de DXCore](../dxcore-reference.md), [GUIDs de atributo do adaptador DXCore](../dxcore-adapter-attribute-guids.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)