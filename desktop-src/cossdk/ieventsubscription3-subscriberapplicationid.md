---
description: O GUID do aplicativo do Assinante.
ms.assetid: 46c91cae-ca31-4eac-baa8-d36910917f0f
title: 'Propriedade IEventSubscription3:: SubscriberApplicationID'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.SubscriberApplicationID
- IEventSubscription3.get_SubscriberApplicationID
- IEventSubscription3.put_SubscriberApplicationID
api_type:
- COM
api_location: ''
ms.openlocfilehash: c2e726d97821a7a7143f4971a4918227235adb9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163996"
---
# <a name="ieventsubscription3subscriberapplicationid-property"></a><span data-ttu-id="95f50-103">Propriedade IEventSubscription3:: SubscriberApplicationID</span><span class="sxs-lookup"><span data-stu-id="95f50-103">IEventSubscription3::SubscriberApplicationID property</span></span>

<span data-ttu-id="95f50-104">O GUID do aplicativo do Assinante.</span><span class="sxs-lookup"><span data-stu-id="95f50-104">The application GUID of the subscriber.</span></span>

<span data-ttu-id="95f50-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="95f50-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="95f50-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="95f50-106">Syntax</span></span>


```C++
HRESULT put_SubscriberApplicationID(
  [in]          BSTR bstrSubscriberApplicationID
);

HRESULT get_SubscriberApplicationID(
  [out, retval] BSTR *pbstrSubscriberApplicationID
);
```



## <a name="property-value"></a><span data-ttu-id="95f50-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="95f50-107">Property value</span></span>

<span data-ttu-id="95f50-108">Uma cadeia de caracteres que contém o GUID do aplicativo de assinante.</span><span class="sxs-lookup"><span data-stu-id="95f50-108">A string containing the GUID of the subscriber application.</span></span>

## <a name="error-codes"></a><span data-ttu-id="95f50-109">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="95f50-109">Error codes</span></span>

<span data-ttu-id="95f50-110">Esse método pode retornar os valores de retorno padrão E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e \_ falha e S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="95f50-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="95f50-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95f50-111">Requirements</span></span>



| <span data-ttu-id="95f50-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="95f50-112">Requirement</span></span> | <span data-ttu-id="95f50-113">Valor</span><span class="sxs-lookup"><span data-stu-id="95f50-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="95f50-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95f50-114">Minimum supported client</span></span><br/> | <span data-ttu-id="95f50-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="95f50-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="95f50-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95f50-116">Minimum supported server</span></span><br/> | <span data-ttu-id="95f50-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="95f50-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="95f50-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="95f50-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95f50-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="95f50-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




