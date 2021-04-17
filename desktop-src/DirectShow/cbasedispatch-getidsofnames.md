---
description: O método GetIDsOfNames mapeia um conjunto de nomes para um conjunto correspondente de DISPIDs.
ms.assetid: 0c0a2726-e89a-4eaf-aab0-e7e9e82e3c34
title: Método CBaseDispatch. GetIDsOfNames (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf11e4aa298f924b69c299c2f411dde88e28e5b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747615"
---
# <a name="cbasedispatchgetidsofnames-method"></a><span data-ttu-id="4a261-103">Método CBaseDispatch. GetIDsOfNames</span><span class="sxs-lookup"><span data-stu-id="4a261-103">CBaseDispatch.GetIDsOfNames method</span></span>

<span data-ttu-id="4a261-104">O `GetIDsOfNames` método mapeia um conjunto de nomes para um conjunto correspondente de DISPIDs.</span><span class="sxs-lookup"><span data-stu-id="4a261-104">The `GetIDsOfNames` method maps a set of names to a corresponding set of DISPIDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a261-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a261-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="4a261-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a261-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a261-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="4a261-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="4a261-108">Referência a um IID (identificador de interface) que especifica a interface.</span><span class="sxs-lookup"><span data-stu-id="4a261-108">Reference to an interface identifier (IID) that specifies the interface.</span></span>

</dd> <dt>

<span data-ttu-id="4a261-109">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="4a261-109">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="4a261-110">Endereço de uma matriz de cadeias de caracteres largos que contêm os nomes a serem mapeados.</span><span class="sxs-lookup"><span data-stu-id="4a261-110">Address of an array of wide-character strings that contain the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="4a261-111">*cNames*</span><span class="sxs-lookup"><span data-stu-id="4a261-111">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="4a261-112">Tamanho da matriz fornecida pelo parâmetro *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="4a261-112">Size of the array given by the *rgszNames* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4a261-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="4a261-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="4a261-114">Contexto de localidade no qual interpretar os nomes.</span><span class="sxs-lookup"><span data-stu-id="4a261-114">Locale context in which to interpret the names.</span></span> <span data-ttu-id="4a261-115">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4a261-115">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4a261-116">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="4a261-116">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="4a261-117">Ponteiro para uma matriz que recebe os DISPIDs.</span><span class="sxs-lookup"><span data-stu-id="4a261-117">Pointer to an array that receives the DISPIDs.</span></span> <span data-ttu-id="4a261-118">Cada elemento de recebe um identificador que corresponde a um dos nomes passados no parâmetro *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="4a261-118">Each element of receives an identifier that corresponds to one of the names passed in the *rgszNames* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a261-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a261-119">Return value</span></span>

<span data-ttu-id="4a261-120">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4a261-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4a261-121">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="4a261-121">Possible values include the following.</span></span>



| <span data-ttu-id="4a261-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4a261-122">Return code</span></span>                                                                                         | <span data-ttu-id="4a261-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="4a261-123">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="4a261-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4a261-124"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="4a261-125">Êxito.</span><span class="sxs-lookup"><span data-stu-id="4a261-125">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="4a261-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4a261-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="4a261-127">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="4a261-127">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="4a261-128"><dt>**Não receber \_ E não \_ conhecido**</dt></span><span class="sxs-lookup"><span data-stu-id="4a261-128"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl> | <span data-ttu-id="4a261-129">Um ou mais dos nomes não eram conhecidos.</span><span class="sxs-lookup"><span data-stu-id="4a261-129">One or more of the names were not known.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4a261-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a261-130">Remarks</span></span>

<span data-ttu-id="4a261-131">Esse método se comporta como o método **IDispatch:: GetIDsOfNames** , mas o parâmetro *riid* especifica a interface na qual recuperar DISPIDs.</span><span class="sxs-lookup"><span data-stu-id="4a261-131">This method behaves like the **IDispatch::GetIDsOfNames** method, but the *riid* parameter specifies the interface on which to retrieve DISPIDs.</span></span> <span data-ttu-id="4a261-132">(Na versão **IDispatch** , o parâmetro *riid* é reservado.)</span><span class="sxs-lookup"><span data-stu-id="4a261-132">(In the **IDispatch** version, the *riid* parameter is reserved.)</span></span>

<span data-ttu-id="4a261-133">Se o método retornar \_ e não \_ conhecido, os DISPIDs retornados contêm DISPID \_ desconhecido para cada entrada que corresponde a um nome desconhecido.</span><span class="sxs-lookup"><span data-stu-id="4a261-133">If the method returns DISP\_E\_UNKNOWNNAME, the returned DISPIDs contain DISPID\_UNKNOWN for each entry that corresponds to an unknown name.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a261-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a261-134">Requirements</span></span>



| <span data-ttu-id="4a261-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a261-135">Requirement</span></span> | <span data-ttu-id="4a261-136">Valor</span><span class="sxs-lookup"><span data-stu-id="4a261-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a261-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4a261-137">Header</span></span><br/>  | <dl> <span data-ttu-id="4a261-138"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a261-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4a261-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a261-139">Library</span></span><br/> | <dl> <span data-ttu-id="4a261-140"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4a261-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a261-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a261-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a261-142">**Classe CBaseDispatch**</span><span class="sxs-lookup"><span data-stu-id="4a261-142">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




