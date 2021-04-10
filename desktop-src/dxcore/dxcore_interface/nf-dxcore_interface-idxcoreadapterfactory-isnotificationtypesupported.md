---
title: IDXCoreAdapterFactory::IsNotificationTypeSupported
description: Determina se um tipo de notificação especificado é suportado pelo sistema operacional (SO).
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 78730167e7ec139733ee1e4011d2e5e59c32782b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294337"
---
# <a name="idxcoreadapterfactoryisnotificationtypesupported-method"></a>Método IDXCoreAdapterFactory:: IsNotificationTypeSupported

Determina se um tipo de notificação especificado é suportado pelo sistema operacional (SO). Para obter diretrizes de programação e exemplos de código, consulte [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Sintaxe

```cpp
virtual bool STDMETHODCALLTYPE IsNotificationTypeSupported(
  DXCoreNotificationType notificationType) = 0;
```

## <a name="parameters"></a>Parâmetros

### <a name="notificationtype"></a>notificationType

Tipo: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**

O tipo de notificação que você está consultando sobre o suporte para. Consulte a tabela em [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) para obter informações sobre os tipos de notificação.

## <a name="returns"></a>Retornos

Tipo: **bool**

Retorna  `true`   se o tipo de notificação é suportado pelo sistema. Caso contrário, retorna  `false` .

## <a name="remarks"></a>Comentários

Você pode chamar **IsNotificationTypeSupported** para determinar se um determinado tipo de notificação é conhecido por esta versão do sistema operacional. Por exemplo, um tipo de notificação que é apresentado em uma versão específica do Windows é desconhecido para versões anteriores do Windows.

## <a name="see-also"></a>Confira também

[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [referência de DXCore](../dxcore-reference.md), [GUIDs de atributo do adaptador DXCore](../dxcore-adapter-attribute-guids.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)