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
# <a name="pfn_dxcore_notification_callback-callback"></a><span data-ttu-id="bc62a-103">PFN_DXCORE_NOTIFICATION_CALLBACK retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="bc62a-103">PFN_DXCORE_NOTIFICATION_CALLBACK callback</span></span>

<span data-ttu-id="bc62a-104">Uma função de retorno de chamada (implementada pelo seu aplicativo), que é chamada por um objeto DXCore para eventos de notificação.</span><span class="sxs-lookup"><span data-stu-id="bc62a-104">A callback function (implemented by your application), which is called by a DXCore object for notification events.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc62a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc62a-105">Syntax</span></span>

```cpp
typedef void (STDMETHODCALLTYPE *PFN_DXCORE_NOTIFICATION_CALLBACK)(
  DXCoreNotificationType notificationType,
  _In_ IUnknown *object,
  _In_opt_ void *context);
```

## <a name="parameters"></a><span data-ttu-id="bc62a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc62a-106">Parameters</span></span>

### <a name="notificationtype"></a><span data-ttu-id="bc62a-107">notificationType</span><span class="sxs-lookup"><span data-stu-id="bc62a-107">notificationType</span></span>

<span data-ttu-id="bc62a-108">Tipo: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span><span class="sxs-lookup"><span data-stu-id="bc62a-108">Type: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span></span>

<span data-ttu-id="bc62a-109">O tipo de notificação que representa esta invocação.</span><span class="sxs-lookup"><span data-stu-id="bc62a-109">The type of notification representing this invocation.</span></span> <span data-ttu-id="bc62a-110">Consulte a tabela em [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) para obter informações sobre quais tipos são válidos com quais tipos de objetos.</span><span class="sxs-lookup"><span data-stu-id="bc62a-110">See the table in [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) for info about what types are valid with which kinds of objects.</span></span>

### <a name="object"></a><span data-ttu-id="bc62a-111">objeto</span><span class="sxs-lookup"><span data-stu-id="bc62a-111">object</span></span>

<span data-ttu-id="bc62a-112">Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="bc62a-112">Type: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="bc62a-113">O objeto [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) ou [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) que gera a notificação.</span><span class="sxs-lookup"><span data-stu-id="bc62a-113">The [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) or [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) object raising the notification.</span></span>

### <a name="context-in"></a><span data-ttu-id="bc62a-114">contexto [in]</span><span class="sxs-lookup"><span data-stu-id="bc62a-114">context [in]</span></span>

<span data-ttu-id="bc62a-115">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="bc62a-115">Type: **void\***</span></span>

<span data-ttu-id="bc62a-116">Um ponteiro, que pode ser `nullptr` , para um objeto que contém informações de contexto.</span><span class="sxs-lookup"><span data-stu-id="bc62a-116">A pointer, which may be `nullptr`, to an object containing context info.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc62a-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc62a-117">See also</span></span>

<span data-ttu-id="bc62a-118">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="bc62a-118">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>