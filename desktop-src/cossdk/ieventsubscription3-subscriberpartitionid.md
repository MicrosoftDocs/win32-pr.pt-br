---
description: O GUID da partição do Assinante.
ms.assetid: 0b2411d3-cdc1-492c-a54f-ca3d3bd8b953
title: 'Propriedade IEventSubscription3:: SubscriberPartitionID'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.SubscriberPartitionID
- IEventSubscription3.get_SubscriberPartitionID
- IEventSubscription3.put_SubscriberPartitionID
api_type:
- COM
api_location: ''
ms.openlocfilehash: b09c41ac1b3a90c3275daf7afa0cd90fe2bb905c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164161"
---
# <a name="ieventsubscription3subscriberpartitionid-property"></a><span data-ttu-id="0704f-103">Propriedade IEventSubscription3:: SubscriberPartitionID</span><span class="sxs-lookup"><span data-stu-id="0704f-103">IEventSubscription3::SubscriberPartitionID property</span></span>

<span data-ttu-id="0704f-104">O GUID da partição do Assinante.</span><span class="sxs-lookup"><span data-stu-id="0704f-104">The partition GUID of the subscriber.</span></span>

<span data-ttu-id="0704f-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0704f-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0704f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0704f-106">Syntax</span></span>


```C++
HRESULT put_SubscriberPartitionID(
  [in]          BSTR bstrSubscriberPartitionID
);

HRESULT get_SubscriberPartitionID(
  [out, retval] BSTR *pbstrSubscriberPartitionID
);
```



## <a name="property-value"></a><span data-ttu-id="0704f-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0704f-107">Property value</span></span>

<span data-ttu-id="0704f-108">Uma cadeia de caracteres que contém o GUID da partição do Assinante.</span><span class="sxs-lookup"><span data-stu-id="0704f-108">A string containing the GUID of the subscriber partition.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0704f-109">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="0704f-109">Error codes</span></span>

<span data-ttu-id="0704f-110">Esse método pode retornar os valores de retorno padrão E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e \_ falha e S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0704f-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="0704f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0704f-111">Requirements</span></span>



| <span data-ttu-id="0704f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="0704f-112">Requirement</span></span> | <span data-ttu-id="0704f-113">Valor</span><span class="sxs-lookup"><span data-stu-id="0704f-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0704f-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0704f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0704f-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0704f-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0704f-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0704f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0704f-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0704f-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0704f-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="0704f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0704f-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="0704f-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




