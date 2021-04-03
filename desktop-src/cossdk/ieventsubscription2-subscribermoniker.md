---
description: O moniker de assinantes.
ms.assetid: d33d8c80-3251-4ec7-9cf3-d0b60d91ed5a
title: Propriedade IEventSubscription2SubscriberMoniker
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.SubscriberMoniker
- IEventSubscription2.get_SubscriberMoniker
- IEventSubscription2.put_SubscriberMoniker
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9496a3046b4bb0e99a88322892e557588a92aab8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646350"
---
# <a name="ieventsubscription2subscribermoniker-property"></a><span data-ttu-id="35d12-103">Propriedade IEventSubscription2:: SubscriberMoniker</span><span class="sxs-lookup"><span data-stu-id="35d12-103">IEventSubscription2::SubscriberMoniker property</span></span>

<span data-ttu-id="35d12-104">O moniker do Assinante.</span><span class="sxs-lookup"><span data-stu-id="35d12-104">The subscriber's moniker.</span></span>

<span data-ttu-id="35d12-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="35d12-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="35d12-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="35d12-106">Syntax</span></span>


```C++
HRESULT put_SubscriberMoniker(
  [in]          BSTR bstrMoniker
);

HRESULT get_SubscriberMoniker(
  [out, retval] BSTR *pbstrMoniker
);
```



## <a name="property-value"></a><span data-ttu-id="35d12-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="35d12-107">Property value</span></span>

<span data-ttu-id="35d12-108">Uma cadeia de caracteres do moniker que especifica o Assinante.</span><span class="sxs-lookup"><span data-stu-id="35d12-108">A moniker string specifying the subscriber.</span></span>

## <a name="error-codes"></a><span data-ttu-id="35d12-109">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="35d12-109">Error codes</span></span>

<span data-ttu-id="35d12-110">Esse método pode retornar os valores de retorno padrão E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e \_ falha e S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="35d12-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="35d12-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35d12-111">Requirements</span></span>



| <span data-ttu-id="35d12-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="35d12-112">Requirement</span></span> | <span data-ttu-id="35d12-113">Valor</span><span class="sxs-lookup"><span data-stu-id="35d12-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="35d12-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35d12-114">Minimum supported client</span></span><br/> | <span data-ttu-id="35d12-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="35d12-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="35d12-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35d12-116">Minimum supported server</span></span><br/> | <span data-ttu-id="35d12-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="35d12-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="35d12-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="35d12-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35d12-119">**IEventSubscription2**</span><span class="sxs-lookup"><span data-stu-id="35d12-119">**IEventSubscription2**</span></span>](ieventsubscription2.md)
</dt> </dl>

 

 




