---
description: O GUID da partição do objeto de classe de evento.
ms.assetid: 154849ac-350c-4b2f-bb51-ac6973f0a8fa
title: 'Propriedade IEventSubscription3:: EventClassPartitionID'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.EventClassPartitionID
- IEventSubscription3.get_EventClassPartitionID
- IEventSubscription3.put_EventClassPartitionID
api_type:
- COM
api_location: ''
ms.openlocfilehash: d41d3e2a170deffb73f1f533226421d88f150c01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501088"
---
# <a name="ieventsubscription3eventclasspartitionid-property"></a><span data-ttu-id="46a0d-103">Propriedade IEventSubscription3:: EventClassPartitionID</span><span class="sxs-lookup"><span data-stu-id="46a0d-103">IEventSubscription3::EventClassPartitionID property</span></span>

<span data-ttu-id="46a0d-104">O GUID da partição do objeto de classe de evento.</span><span class="sxs-lookup"><span data-stu-id="46a0d-104">The partition GUID of the event class object.</span></span>

<span data-ttu-id="46a0d-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="46a0d-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="46a0d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="46a0d-106">Syntax</span></span>


```C++
HRESULT put_EventClassPartitionID(
  [in]          BSTR bstrEventClassPartitionID
);

HRESULT get_EventClassPartitionID(
  [out, retval] BSTR *pbstrEventClassPartitionID
);
```



## <a name="property-value"></a><span data-ttu-id="46a0d-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="46a0d-107">Property value</span></span>

<span data-ttu-id="46a0d-108">Uma cadeia de caracteres que contém o GUID da partição da classe de evento.</span><span class="sxs-lookup"><span data-stu-id="46a0d-108">A string containing the GUID of the event class partition.</span></span>

## <a name="error-codes"></a><span data-ttu-id="46a0d-109">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="46a0d-109">Error codes</span></span>

<span data-ttu-id="46a0d-110">Esse método pode retornar os valores de retorno padrão E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e \_ falha e S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="46a0d-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="46a0d-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46a0d-111">Requirements</span></span>



| <span data-ttu-id="46a0d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="46a0d-112">Requirement</span></span> | <span data-ttu-id="46a0d-113">Valor</span><span class="sxs-lookup"><span data-stu-id="46a0d-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="46a0d-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46a0d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="46a0d-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="46a0d-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="46a0d-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46a0d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="46a0d-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="46a0d-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="46a0d-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="46a0d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46a0d-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="46a0d-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




