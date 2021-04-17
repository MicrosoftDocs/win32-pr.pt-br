---
description: 'O método QueryVendorInfo recupera uma cadeia de caracteres que contém informações do fornecedor. Esse método implementa o método IBaseFilter:: QueryVendorInfo.'
ms.assetid: 083c0556-d516-4daf-8621-e158ea78b5a3
title: Método CBaseFilter. QueryVendorInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryVendorInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1786477c042bb1d9ecc6340056a771141d0a3c74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752718"
---
# <a name="cbasefilterqueryvendorinfo-method"></a><span data-ttu-id="c009e-104">Método CBaseFilter. QueryVendorInfo</span><span class="sxs-lookup"><span data-stu-id="c009e-104">CBaseFilter.QueryVendorInfo method</span></span>

<span data-ttu-id="c009e-105">O `QueryVendorInfo` método recupera uma cadeia de caracteres que contém informações do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="c009e-105">The `QueryVendorInfo` method retrieves a string containing vendor information.</span></span> <span data-ttu-id="c009e-106">Esse método implementa o método [**IBaseFilter:: QueryVendorInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryvendorinfo) .</span><span class="sxs-lookup"><span data-stu-id="c009e-106">This method implements the [**IBaseFilter::QueryVendorInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryvendorinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c009e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c009e-107">Syntax</span></span>


```C++
HRESULT QueryVendorInfo(
   LPWSTR *pVendorInfo
);
```



## <a name="parameters"></a><span data-ttu-id="c009e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c009e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c009e-109">*pVendorInfo*</span><span class="sxs-lookup"><span data-stu-id="c009e-109">*pVendorInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="c009e-110">Endereço de uma variável que recebe um ponteiro para uma cadeia de caracteres largos contendo as informações do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="c009e-110">Address of a variable that receives a pointer to a wide-character string containing the vendor information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c009e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c009e-111">Return value</span></span>

<span data-ttu-id="c009e-112">Retorna E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="c009e-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c009e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c009e-113">Remarks</span></span>

<span data-ttu-id="c009e-114">Para fornecer informações de fornecedor para um filtro, substitua esse método.</span><span class="sxs-lookup"><span data-stu-id="c009e-114">To provide vendor information for a filter, override this method.</span></span> <span data-ttu-id="c009e-115">Se você implementar esse método, use a função **CoTaskMemAlloc** para alocar memória para a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c009e-115">If you implement this method, use the **CoTaskMemAlloc** function to allocate memory for the string.</span></span> <span data-ttu-id="c009e-116">O chamador é responsável por chamar a função **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="c009e-116">The caller is responsible for calling the **CoTaskMemFree** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c009e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c009e-117">Requirements</span></span>



| <span data-ttu-id="c009e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c009e-118">Requirement</span></span> | <span data-ttu-id="c009e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c009e-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c009e-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c009e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c009e-121"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c009e-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c009e-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c009e-122">Library</span></span><br/> | <dl> <span data-ttu-id="c009e-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c009e-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c009e-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c009e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c009e-125">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="c009e-125">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




