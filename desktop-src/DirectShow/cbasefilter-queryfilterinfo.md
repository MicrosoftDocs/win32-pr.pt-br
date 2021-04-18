---
description: 'O método QueryFilterInfo recupera informações sobre o filtro. Esse método implementa o método IBaseFilter:: QueryFilterInfo.'
ms.assetid: 0c25aa9e-933c-4c45-a1cc-ffc9253dd561
title: Método CBaseFilter. QueryFilterInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryFilterInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a706663c1fb39e0e2e84b4097ec620f9e608843
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752515"
---
# <a name="cbasefilterqueryfilterinfo-method"></a><span data-ttu-id="e63ec-104">Método CBaseFilter. QueryFilterInfo</span><span class="sxs-lookup"><span data-stu-id="e63ec-104">CBaseFilter.QueryFilterInfo method</span></span>

<span data-ttu-id="e63ec-105">O `QueryFilterInfo` método recupera informações sobre o filtro.</span><span class="sxs-lookup"><span data-stu-id="e63ec-105">The `QueryFilterInfo` method retrieves information about the filter.</span></span> <span data-ttu-id="e63ec-106">Esse método implementa o método [**IBaseFilter:: QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) .</span><span class="sxs-lookup"><span data-stu-id="e63ec-106">This method implements the [**IBaseFilter::QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e63ec-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e63ec-107">Syntax</span></span>


```C++
HRESULT QueryFilterInfo(
   FILTER_INFO *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="e63ec-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e63ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e63ec-109">*pInfo*</span><span class="sxs-lookup"><span data-stu-id="e63ec-109">*pInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="e63ec-110">Ponteiro para uma estrutura de [**\_ informações de filtro**](/windows/win32/api/strmif/ns-strmif-filter_info) .</span><span class="sxs-lookup"><span data-stu-id="e63ec-110">Pointer to a [**FILTER\_INFO**](/windows/win32/api/strmif/ns-strmif-filter_info) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e63ec-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e63ec-111">Return value</span></span>

<span data-ttu-id="e63ec-112">Retorna S \_ OK ou o \_ ponteiro.</span><span class="sxs-lookup"><span data-stu-id="e63ec-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="e63ec-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e63ec-113">Remarks</span></span>

<span data-ttu-id="e63ec-114">Esse método copia o nome do filtro da variável de membro [**CBaseFilter:: m \_ pname**](cbasefilter-m-pname.md) para o membro **achName** da estrutura de \_ informações de filtro.</span><span class="sxs-lookup"><span data-stu-id="e63ec-114">This method copies the filter's name from the [**CBaseFilter::m\_pName**](cbasefilter-m-pname.md) member variable into the **achName** member of the FILTER\_INFO structure.</span></span> <span data-ttu-id="e63ec-115">Se **m \_ pname** for **nulo**, o método definirá **achName** como L ' \\ 0 '.</span><span class="sxs-lookup"><span data-stu-id="e63ec-115">If **m\_pName** is **NULL**, the method sets **achName** to L'\\0'.</span></span>

<span data-ttu-id="e63ec-116">O método define o membro **pGraph** da estrutura de \_ informações de filtro igual à variável de membro [**CBaseFilter:: m \_ pGraph**](cbasefilter-m-pgraph.md) e incrementa a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="e63ec-116">The method sets the **pGraph** member of the FILTER\_INFO structure equal to the [**CBaseFilter::m\_pGraph**](cbasefilter-m-pgraph.md) member variable, and increments the reference count.</span></span> <span data-ttu-id="e63ec-117">O chamador deve liberar a interface.</span><span class="sxs-lookup"><span data-stu-id="e63ec-117">The caller must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e63ec-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e63ec-118">Requirements</span></span>



| <span data-ttu-id="e63ec-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e63ec-119">Requirement</span></span> | <span data-ttu-id="e63ec-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e63ec-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e63ec-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e63ec-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e63ec-122"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e63ec-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e63ec-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e63ec-123">Library</span></span><br/> | <dl> <span data-ttu-id="e63ec-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e63ec-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e63ec-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e63ec-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e63ec-126">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="e63ec-126">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




