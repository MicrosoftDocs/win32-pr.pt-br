---
description: Método CBaseDispatch. GetIDsOfNames – o método GetIDsOfNames mapeia um conjunto de nomes para um conjunto correspondente de DISPIDs.
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
ms.openlocfilehash: 3f3b718c95d588ffdc7fa63902e6b26ffbf11fd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099914"
---
# <a name="cbasedispatchgetidsofnames-method"></a><span data-ttu-id="fa0ff-103">Método CBaseDispatch. GetIDsOfNames</span><span class="sxs-lookup"><span data-stu-id="fa0ff-103">CBaseDispatch.GetIDsOfNames method</span></span>

<span data-ttu-id="fa0ff-104">O `GetIDsOfNames` método mapeia um conjunto de nomes para um conjunto correspondente de DISPIDs.</span><span class="sxs-lookup"><span data-stu-id="fa0ff-104">The `GetIDsOfNames` method maps a set of names to a corresponding set of DISPIDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa0ff-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa0ff-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="fa0ff-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa0ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa0ff-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="fa0ff-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="fa0ff-108">Referência a um IID (identificador de interface) que especifica a interface.</span><span class="sxs-lookup"><span data-stu-id="fa0ff-108">Reference to an interface identifier (IID) that specifies the interface.</span></span>

</dd> <dt>

<span data-ttu-id="fa0ff-109">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="fa0ff-109">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="fa0ff-110">Endereço de uma matriz de cadeias de caracteres largos que contêm os nomes a serem mapeados.</span><span class="sxs-lookup"><span data-stu-id="fa0ff-110">Address of an array of wide-character strings that contain the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="fa0ff-111">*cNames*</span><span class="sxs-lookup"><span data-stu-id="fa0ff-111">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="fa0ff-112">Tamanho da matriz fornecida pelo parâmetro *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="fa0ff-112">Size of the array given by the *rgszNames* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="fa0ff-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="fa0ff-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="fa0ff-114">Contexto de localidade no qual interpretar os nomes.</span><span class="sxs-lookup"><span data-stu-id="fa0ff-114">Locale context in which to interpret the names.</span></span> <span data-ttu-id="fa0ff-115">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fa0ff-115">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fa0ff-116">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="fa0ff-116">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="fa0ff-117">Ponteiro para uma matriz que recebe os DISPIDs.</span><span class="sxs-lookup"><span data-stu-id="fa0ff-117">Pointer to an array that receives the DISPIDs.</span></span> <span data-ttu-id="fa0ff-118">Cada elemento de recebe um identificador que corresponde a um dos nomes passados no parâmetro *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="fa0ff-118">Each element of receives an identifier that corresponds to one of the names passed in the *rgszNames* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa0ff-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fa0ff-119">Return value</span></span>

<span data-ttu-id="fa0ff-120">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fa0ff-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="fa0ff-121">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="fa0ff-121">Possible values include the following.</span></span>



| <span data-ttu-id="fa0ff-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fa0ff-122">Return code</span></span>                                                                                         | <span data-ttu-id="fa0ff-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa0ff-123">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="fa0ff-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fa0ff-124"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="fa0ff-125">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="fa0ff-125">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="fa0ff-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fa0ff-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="fa0ff-127">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="fa0ff-127">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="fa0ff-128"><dt>**Não receber \_ E não \_ conhecido**</dt></span><span class="sxs-lookup"><span data-stu-id="fa0ff-128"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl> | <span data-ttu-id="fa0ff-129">Um ou mais dos nomes não eram conhecidos.</span><span class="sxs-lookup"><span data-stu-id="fa0ff-129">One or more of the names were not known.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fa0ff-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa0ff-130">Remarks</span></span>

<span data-ttu-id="fa0ff-131">Esse método se comporta como o método **IDispatch:: GetIDsOfNames** , mas o parâmetro *riid* especifica a interface na qual recuperar DISPIDs.</span><span class="sxs-lookup"><span data-stu-id="fa0ff-131">This method behaves like the **IDispatch::GetIDsOfNames** method, but the *riid* parameter specifies the interface on which to retrieve DISPIDs.</span></span> <span data-ttu-id="fa0ff-132">(Na versão **IDispatch** , o parâmetro *riid* é reservado.)</span><span class="sxs-lookup"><span data-stu-id="fa0ff-132">(In the **IDispatch** version, the *riid* parameter is reserved.)</span></span>

<span data-ttu-id="fa0ff-133">Se o método retornar \_ e não \_ conhecido, os DISPIDs retornados contêm DISPID \_ desconhecido para cada entrada que corresponde a um nome desconhecido.</span><span class="sxs-lookup"><span data-stu-id="fa0ff-133">If the method returns DISP\_E\_UNKNOWNNAME, the returned DISPIDs contain DISPID\_UNKNOWN for each entry that corresponds to an unknown name.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa0ff-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa0ff-134">Requirements</span></span>



| <span data-ttu-id="fa0ff-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa0ff-135">Requirement</span></span> | <span data-ttu-id="fa0ff-136">Valor</span><span class="sxs-lookup"><span data-stu-id="fa0ff-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa0ff-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa0ff-137">Header</span></span><br/>  | <dl> <span data-ttu-id="fa0ff-138"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa0ff-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fa0ff-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa0ff-139">Library</span></span><br/> | <dl> <span data-ttu-id="fa0ff-140"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="fa0ff-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa0ff-141">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fa0ff-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa0ff-142">**Classe CBaseDispatch**</span><span class="sxs-lookup"><span data-stu-id="fa0ff-142">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




