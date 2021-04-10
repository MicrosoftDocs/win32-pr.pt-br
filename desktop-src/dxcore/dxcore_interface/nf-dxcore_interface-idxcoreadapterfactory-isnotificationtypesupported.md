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
# <a name="idxcoreadapterfactoryisnotificationtypesupported-method"></a><span data-ttu-id="eb234-103">Método IDXCoreAdapterFactory:: IsNotificationTypeSupported</span><span class="sxs-lookup"><span data-stu-id="eb234-103">IDXCoreAdapterFactory::IsNotificationTypeSupported method</span></span>

<span data-ttu-id="eb234-104">Determina se um tipo de notificação especificado é suportado pelo sistema operacional (SO).</span><span class="sxs-lookup"><span data-stu-id="eb234-104">Determines whether a specified notification type is supported by the operating system (OS).</span></span> <span data-ttu-id="eb234-105">Para obter diretrizes de programação e exemplos de código, consulte [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="eb234-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb234-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb234-106">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsNotificationTypeSupported(
  DXCoreNotificationType notificationType) = 0;
```

## <a name="parameters"></a><span data-ttu-id="eb234-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb234-107">Parameters</span></span>

### <a name="notificationtype"></a><span data-ttu-id="eb234-108">notificationType</span><span class="sxs-lookup"><span data-stu-id="eb234-108">notificationType</span></span>

<span data-ttu-id="eb234-109">Tipo: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span><span class="sxs-lookup"><span data-stu-id="eb234-109">Type: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span></span>

<span data-ttu-id="eb234-110">O tipo de notificação que você está consultando sobre o suporte para.</span><span class="sxs-lookup"><span data-stu-id="eb234-110">The type of notification that you're querying about support for.</span></span> <span data-ttu-id="eb234-111">Consulte a tabela em [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) para obter informações sobre os tipos de notificação.</span><span class="sxs-lookup"><span data-stu-id="eb234-111">See the table in [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) for info about the notification types.</span></span>

## <a name="returns"></a><span data-ttu-id="eb234-112">Retornos</span><span class="sxs-lookup"><span data-stu-id="eb234-112">Returns</span></span>

<span data-ttu-id="eb234-113">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="eb234-113">Type: **bool**</span></span>

<span data-ttu-id="eb234-114">Retorna  `true`   se o tipo de notificação é suportado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="eb234-114">Returns `true` if the notification type is supported by the system.</span></span> <span data-ttu-id="eb234-115">Caso contrário, retorna  `false` .</span><span class="sxs-lookup"><span data-stu-id="eb234-115">Otherwise, returns `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb234-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb234-116">Remarks</span></span>

<span data-ttu-id="eb234-117">Você pode chamar **IsNotificationTypeSupported** para determinar se um determinado tipo de notificação é conhecido por esta versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="eb234-117">You can call **IsNotificationTypeSupported** to determine whether a given notification type is known to this version of the OS.</span></span> <span data-ttu-id="eb234-118">Por exemplo, um tipo de notificação que é apresentado em uma versão específica do Windows é desconhecido para versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="eb234-118">For example, a notification type that's introduced in a particular version of Windows is unknown to previous versions of Windows.</span></span>

## <a name="see-also"></a><span data-ttu-id="eb234-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb234-119">See also</span></span>

<span data-ttu-id="eb234-120">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [referência de DXCore](../dxcore-reference.md), [GUIDs de atributo do adaptador DXCore](../dxcore-adapter-attribute-guids.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="eb234-120">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>