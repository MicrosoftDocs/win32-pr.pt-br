---
title: PFN_DXCORE_NOTIFICATION_CALLBACK
description: Uma função de retorno de chamada (implementada pelo seu aplicativo), que é chamada por um objeto DXCore para eventos de notificação.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: f86bef2d2183562b322cdc0b01ffb64d25b23bb64dd8967e09e2dd761f7654b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787096"
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

O tipo de notificação que representa essa invocação. Consulte a tabela em [DXCoreNotificationType para](./ne-dxcore_interface-dxcorenotificationtype.md) obter informações sobre quais tipos são válidos com quais tipos de objetos.

### <a name="object"></a>objeto

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

O [objeto IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) ou [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) inging a notificação.

### <a name="context-in"></a>context [in]

Tipo: **\* void**

Um ponteiro, que pode ser `nullptr` , para um objeto que contém informações de contexto.

## <a name="see-also"></a>Confira também

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [Referência de DXCore](../dxcore-reference.md), usando [DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)