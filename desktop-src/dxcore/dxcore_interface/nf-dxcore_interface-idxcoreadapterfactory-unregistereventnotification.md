---
title: IDXCoreAdapterFactory::UnregisterEventNotification
description: Cancela o registro de uma notificação que você registrou anteriormente para o.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6bb12126769a914680ea17ac9e6060346001c795
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366505"
---
# <a name="idxcoreadapterfactoryunregistereventnotification-method"></a><span data-ttu-id="80aa4-103">Método IDXCoreAdapterFactory:: UnregisterEventNotification</span><span class="sxs-lookup"><span data-stu-id="80aa4-103">IDXCoreAdapterFactory::UnregisterEventNotification method</span></span>

<span data-ttu-id="80aa4-104">Cancela o registro de uma notificação que você registrou anteriormente para o.</span><span class="sxs-lookup"><span data-stu-id="80aa4-104">Unregisters from a notification that you previously registered for.</span></span> <span data-ttu-id="80aa4-105">Para obter diretrizes de programação e exemplos de código, consulte [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="80aa4-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="80aa4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80aa4-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE UnregisterEventNotification(
  uint32_t eventCookie) = 0;
```

## <a name="parameters"></a><span data-ttu-id="80aa4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80aa4-107">Parameters</span></span>

### <a name="eventcookie"></a><span data-ttu-id="80aa4-108">eventCookie</span><span class="sxs-lookup"><span data-stu-id="80aa4-108">eventCookie</span></span>

<span data-ttu-id="80aa4-109">Tipo: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="80aa4-109">Type: **uint32_t**</span></span>

<span data-ttu-id="80aa4-110">O valor do cookie (retornado quando você chamou [IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)) que representa um registro anterior para o qual você deseja cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="80aa4-110">The cookie value (returned when you called [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)) representing a prior registration that you now wish to unregister for.</span></span>

## <a name="returns"></a><span data-ttu-id="80aa4-111">Retornos</span><span class="sxs-lookup"><span data-stu-id="80aa4-111">Returns</span></span>

<span data-ttu-id="80aa4-112">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="80aa4-112">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="80aa4-113">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="80aa4-113">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="80aa4-114">Caso contrário, ele retorna um [código de erro](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="80aa4-114">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="80aa4-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="80aa4-115">Return value</span></span>|<span data-ttu-id="80aa4-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="80aa4-116">Description</span></span>|
|-|-|
|<span data-ttu-id="80aa4-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="80aa4-117">E_INVALIDARG</span></span>|<span data-ttu-id="80aa4-118">O valor de *eventCookie* não é um cookie válido que representa um registro anterior.</span><span class="sxs-lookup"><span data-stu-id="80aa4-118">The value of *eventCookie* is not a valid cookie representing a prior registration.</span></span>|

## <a name="remarks"></a><span data-ttu-id="80aa4-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="80aa4-119">Remarks</span></span>

<span data-ttu-id="80aa4-120">**UnregisterEventNotification** retorna somente após a conclusão de todos os retornos de chamada pendentes/em andamento para este registro.</span><span class="sxs-lookup"><span data-stu-id="80aa4-120">**UnregisterEventNotification** returns only after all pending/in-progress callbacks for this registration have completed.</span></span> <span data-ttu-id="80aa4-121">DXCore garante que nenhum novo retorno de chamada ocorrerá para esse registro depois que **UnregisterEventNotification** for retornado.</span><span class="sxs-lookup"><span data-stu-id="80aa4-121">DXCore guarantees that no new callbacks will occur for this registration after **UnregisterEventNotification** has returned.</span></span> <span data-ttu-id="80aa4-122">No entanto, para evitar um deadlock, se você chamar **UnregisterEventNotification** de dentro de seu retorno de chamada, o **UnregisterEventNotification** não aguardará a conclusão do retorno de chamada ativo.</span><span class="sxs-lookup"><span data-stu-id="80aa4-122">However, to avoid a deadlock, if you call **UnregisterEventNotification** from within your callback, then **UnregisterEventNotification** doesn't wait for the active callback to complete.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="80aa4-123">Antes de destruir o objeto DXCore representado pelo argumento *dxCoreObject* passado para [IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), você deve usar o valor de cookie para cancelar o registro desse objeto de notificações chamando **UnregisterEventNotification**.</span><span class="sxs-lookup"><span data-stu-id="80aa4-123">Before you destroy the DXCore object represented by the *dxCoreObject* argument passed to [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), you must use the cookie value to unregister that object from notifications by calling **UnregisterEventNotification**.</span></span> <span data-ttu-id="80aa4-124">Se você não fizer isso, uma exceção fatal será gerada quando a situação for detectada.</span><span class="sxs-lookup"><span data-stu-id="80aa4-124">If you don't do that, then a fatal exception is raised when the situation is detected.</span></span>

<span data-ttu-id="80aa4-125">Depois que você cancela o registro de um valor de cookie, esse valor é qualificado para ser retornado por um registro subsequente</span><span class="sxs-lookup"><span data-stu-id="80aa4-125">Once you unregister a cookie value, that value is then eligible for being returned by a subsequent registration</span></span>

## <a name="see-also"></a><span data-ttu-id="80aa4-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="80aa4-126">See also</span></span>

<span data-ttu-id="80aa4-127">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory:: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="80aa4-127">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>