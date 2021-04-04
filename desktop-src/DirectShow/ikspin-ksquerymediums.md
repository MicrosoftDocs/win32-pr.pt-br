---
description: O método KsQueryMediums recupera os meios com suporte por um PIN.
ms.assetid: 554bf968-6054-4f9d-95db-facf0444641f
title: 'Método IKsPin:: KsQueryMediums (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin.KsQueryMediums
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: f037317b49bc54f5ea9db5b7a4ae039ec0a9970d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645918"
---
# <a name="ikspinksquerymediums-method"></a><span data-ttu-id="a183e-103">Método IKsPin:: KsQueryMediums</span><span class="sxs-lookup"><span data-stu-id="a183e-103">IKsPin::KsQueryMediums method</span></span>

<span data-ttu-id="a183e-104">O `KsQueryMediums` método recupera os meios com suporte por um PIN.</span><span class="sxs-lookup"><span data-stu-id="a183e-104">The `KsQueryMediums` method retrieves the mediums supported by a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="a183e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a183e-105">Syntax</span></span>


```C++
HRESULT KsQueryMediums(
  [out] KSMULTIPLE_ITEM **ppmi
);
```



## <a name="parameters"></a><span data-ttu-id="a183e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a183e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a183e-107">*PPMI* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a183e-107">*ppmi* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a183e-108">Endereço de um ponteiro para uma estrutura de [**\_ Item KSMULTIPLE**](ksmultiple-item.md) .</span><span class="sxs-lookup"><span data-stu-id="a183e-108">Address of a pointer to a [**KSMULTIPLE\_ITEM**](ksmultiple-item.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a183e-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a183e-109">Return value</span></span>

<span data-ttu-id="a183e-110">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a183e-110">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="a183e-111">Se falhar, ele retornará um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a183e-111">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a183e-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="a183e-112">Remarks</span></span>

<span data-ttu-id="a183e-113">Esse método retorna uma estrutura de [**\_ Item KSMULTIPLE**](ksmultiple-item.md) alocada para tarefa, que é seguida por zero ou mais estruturas [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) .</span><span class="sxs-lookup"><span data-stu-id="a183e-113">This method returns a task-allocated [**KSMULTIPLE\_ITEM**](ksmultiple-item.md) structure, which is followed by zero or more [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) structures.</span></span> <span data-ttu-id="a183e-114">O membro **Count** da estrutura **do \_ Item KSMULTIPLE** especifica o número de estruturas **REGPINMEDIUM** .</span><span class="sxs-lookup"><span data-stu-id="a183e-114">The **Count** member of the **KSMULTIPLE\_ITEM** structure specifies the number of **REGPINMEDIUM** structures.</span></span> <span data-ttu-id="a183e-115">Cada estrutura **REGPINMEDIUM** define um meio com suporte do PIN.</span><span class="sxs-lookup"><span data-stu-id="a183e-115">Each **REGPINMEDIUM** structure defines a medium supported by the pin.</span></span>

<span data-ttu-id="a183e-116">O chamador deve liberar as estruturas retornadas, usando a função **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="a183e-116">The caller must free the returned structures, using the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="a183e-117">Você deve incluir KS. h antes de ksproxy. h.</span><span class="sxs-lookup"><span data-stu-id="a183e-117">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="examples"></a><span data-ttu-id="a183e-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a183e-118">Examples</span></span>

<span data-ttu-id="a183e-119">A função auxiliar a seguir tenta corresponder a um PIN em uma mídia especificada.</span><span class="sxs-lookup"><span data-stu-id="a183e-119">The following helper function attempts to match a pin against a specified medium.</span></span>


```C++
HRESULT FindMatchingMedium(
    IPin *pPin, 
    REGPINMEDIUM *pMedium, 
    bool *pfMatch)
{
    IKsPin* pKsPin = NULL;
    KSMULTIPLE_ITEM *pmi;

    *pfMatch = false;
    HRESULT hr = pPin->QueryInterface(IID_IKsPin, (void **)&pKsPin);
    if (FAILED(hr)) 
        return hr;  // Pin does not support IKsPin.

    hr = pKsPin->KsQueryMediums(&pmi);
    pKsPin->Release();
    if (FAILED(hr))
        return hr;  // Pin does not support mediums.

    if (pmi->Count) 
    {
        // Use pointer arithmetic to reference the first medium structure.
        REGPINMEDIUM *pTemp = (REGPINMEDIUM*)(pmi + 1);
        for (ULONG i = 0; i < pmi->Count; i++, pTemp++) 
        {
            if (pMedium->clsMedium == pTemp->clsMedium) 
            {
                *pfMatch = true;
                break;
            }
        }
    }        
    CoTaskMemFree(pmi);
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="a183e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a183e-120">Requirements</span></span>



| <span data-ttu-id="a183e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a183e-121">Requirement</span></span> | <span data-ttu-id="a183e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a183e-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a183e-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a183e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a183e-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a183e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a183e-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a183e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a183e-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a183e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a183e-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a183e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a183e-128"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="a183e-128"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="a183e-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a183e-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="a183e-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a183e-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a183e-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="a183e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a183e-132">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="a183e-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="a183e-133">**Interface IKsPin**</span><span class="sxs-lookup"><span data-stu-id="a183e-133">**IKsPin Interface**</span></span>](ikspin.md)
</dt> <dt>

[<span data-ttu-id="a183e-134">Filtros de driver de classe WDM</span><span class="sxs-lookup"><span data-stu-id="a183e-134">WDM Class Driver Filters</span></span>](wdm-class-driver-filters.md)
</dt> </dl>

 

 




