---
description: Os critérios de filtro que regem a assinatura.
ms.assetid: cfc3ba9e-0566-45fd-917f-34842b8ff377
title: 'Propriedade IEventSubscription2:: FilterCriteria'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.FilterCriteria
- IEventSubscription2.get_FilterCriteria
- IEventSubscription2.put_FilterCriteria
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1443a89433cff91a298e8c390fce8f1f64b99f1b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089500"
---
# <a name="ieventsubscription2filtercriteria-property"></a><span data-ttu-id="efe6a-103">Propriedade IEventSubscription2:: FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="efe6a-103">IEventSubscription2::FilterCriteria property</span></span>

<span data-ttu-id="efe6a-104">Os critérios de filtro que regem a assinatura.</span><span class="sxs-lookup"><span data-stu-id="efe6a-104">The filter criteria governing the subscription.</span></span>

<span data-ttu-id="efe6a-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="efe6a-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="efe6a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="efe6a-106">Syntax</span></span>


```C++
HRESULT put_FilterCriteria(
  [in]          BSTR bstrFilterCriteria
);

HRESULT get_FilterCriteria(
  [out, retval] BSTR *pbstrFilterCriteria
);
```



## <a name="property-value"></a><span data-ttu-id="efe6a-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="efe6a-107">Property value</span></span>

<span data-ttu-id="efe6a-108">Os critérios de filtro ou o CLSID para uma classe que implementa [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter).</span><span class="sxs-lookup"><span data-stu-id="efe6a-108">The filter criteria or the CLSID for a class implementing [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter).</span></span>

## <a name="error-codes"></a><span data-ttu-id="efe6a-109">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="efe6a-109">Error codes</span></span>

<span data-ttu-id="efe6a-110">Esse método pode retornar os valores de retorno padrão E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e \_ falha e S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="efe6a-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="efe6a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efe6a-111">Requirements</span></span>



| <span data-ttu-id="efe6a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="efe6a-112">Requirement</span></span> | <span data-ttu-id="efe6a-113">Valor</span><span class="sxs-lookup"><span data-stu-id="efe6a-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="efe6a-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efe6a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="efe6a-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="efe6a-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="efe6a-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efe6a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="efe6a-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="efe6a-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="efe6a-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="efe6a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efe6a-119">**IEventSubscription2**</span><span class="sxs-lookup"><span data-stu-id="efe6a-119">**IEventSubscription2**</span></span>](ieventsubscription2.md)
</dt> </dl>

 

 




