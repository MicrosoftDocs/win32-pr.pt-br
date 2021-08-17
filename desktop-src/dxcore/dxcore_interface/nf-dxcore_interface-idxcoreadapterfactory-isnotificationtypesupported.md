---
title: IDXCoreAdapterFactory::IsNotificationTypeSupported
description: Determina se um tipo de notificação especificado é suportado pelo sistema operacional (SO).
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0c5097f89583f0f6b04e0e8fb033446aae45743a8fb5a7fe9134f34bcc5e05fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118700"
---
# <a name="idxcoreadapterfactoryisnotificationtypesupported-method"></a>Método IDXCoreAdapterFactory::IsNotificationTypeSupported

Determina se um tipo de notificação especificado é suportado pelo sistema operacional (SO). Para obter diretrizes de programação e exemplos de código, consulte [Usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Sintaxe

```cpp
virtual bool STDMETHODCALLTYPE IsNotificationTypeSupported(
  DXCoreNotificationType notificationType) = 0;
```

## <a name="parameters"></a>Parâmetros

### <a name="notificationtype"></a>notificationType

Tipo: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**

O tipo de notificação para o qual você está consultando sobre o suporte. Consulte a tabela em [DXCoreNotificationType para](./ne-dxcore_interface-dxcorenotificationtype.md) obter informações sobre os tipos de notificação.

## <a name="returns"></a>Retornos

Tipo: **bool**

Retorna `true` se o tipo de notificação é suportado pelo sistema. Caso contrário, retorna `false`.

## <a name="remarks"></a>Comentários

Você pode chamar **IsNotificationTypeSupported** para determinar se um determinado tipo de notificação é conhecido por essa versão do sistema operacional. Por exemplo, um tipo de notificação introduzido em uma versão específica do Windows é desconhecido para versões anteriores do Windows.

## <a name="see-also"></a>Confira também

[IDXCoreAdapterFactory,](./nn-dxcore_interface-idxcoreadapterfactory.md) [Referência de DXCore,](../dxcore-reference.md)GUIDs de atributo de adaptador [DXCore,](../dxcore-adapter-attribute-guids.md)usando [DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)