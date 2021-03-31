---
title: PFN_DXCORE_NOTIFICATION_CALLBACK
description: Uma função de retorno de chamada (implementada pelo seu aplicativo), que é chamada por um objeto DXCore para eventos de notificação.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 01d65f6907c60d6c68b612308b9105d18bbe037f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917556"
---
# <a name="pfn_dxcore_notification_callback-callback"></a>PFN_DXCORE_NOTIFICATION_CALLBACK retorno de chamada

Uma função de retorno de chamada (implementada pelo seu aplicativo), que é chamada por um objeto DXCore para eventos de notificação.

## <a name="syntax"></a>Sintaxe

```cpp
typedef void (STDMETHODCALLTYPE *PFN_DXCORE_NOTIFICATION_CALLBACK)(
  DXCoreNotificationType notificationType,
  _In_ IUnknown *object,
  _In_opt_ void *context);
```

## <a name="parameters"></a>Parâmetros

### <a name="notificationtype"></a>notificationType

Tipo: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**

O tipo de notificação que representa esta invocação. Consulte a tabela em [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) para obter informações sobre quais tipos são válidos com quais tipos de objetos.

### <a name="object"></a>object

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

O objeto [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) ou [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) que gera a notificação.

### <a name="context-in"></a>contexto [in]

Tipo: **void \***

Um ponteiro, que pode ser `nullptr` , para um objeto que contém informações de contexto.

## <a name="see-also"></a>Consulte também

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)