---
description: O GUID do aplicativo do objeto da classe de evento.
ms.assetid: 0d19183a-429c-4564-b6a5-f06481d27e00
title: 'Propriedade IEventSubscription3:: EventClassApplicationID'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.EventClassApplicationID
- IEventSubscription3.get_EventClassApplicationID
- IEventSubscription3.put_EventClassApplicationID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3e80a8d8f557c80a1b2605328728260eb8ae7bd7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089311"
---
# <a name="ieventsubscription3eventclassapplicationid-property"></a><span data-ttu-id="9a0d8-103">Propriedade IEventSubscription3:: EventClassApplicationID</span><span class="sxs-lookup"><span data-stu-id="9a0d8-103">IEventSubscription3::EventClassApplicationID property</span></span>

<span data-ttu-id="9a0d8-104">O GUID do aplicativo do objeto da classe de evento.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-104">The application GUID of the event class object.</span></span>

<span data-ttu-id="9a0d8-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a0d8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a0d8-106">Syntax</span></span>


```C++
HRESULT put_EventClassApplicationID(
  [in]          BSTR bstrEventClassApplicationID
);

HRESULT get_EventClassApplicationID(
  [out, retval] BSTR *pbstrEventClassApplicationID
);
```



## <a name="property-value"></a><span data-ttu-id="9a0d8-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="9a0d8-107">Property value</span></span>

<span data-ttu-id="9a0d8-108">Uma cadeia de caracteres que contém o GUID do aplicativo de classe de evento.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-108">A string containing the GUID of the event class application.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9a0d8-109">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="9a0d8-109">Error codes</span></span>

<span data-ttu-id="9a0d8-110">Esse método pode retornar os valores de retorno padrão E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e \_ falha e S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a0d8-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a0d8-111">Requirements</span></span>



| <span data-ttu-id="9a0d8-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a0d8-112">Requirement</span></span> | <span data-ttu-id="9a0d8-113">Valor</span><span class="sxs-lookup"><span data-stu-id="9a0d8-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="9a0d8-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a0d8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="9a0d8-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9a0d8-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9a0d8-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a0d8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="9a0d8-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9a0d8-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9a0d8-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a0d8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a0d8-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="9a0d8-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




