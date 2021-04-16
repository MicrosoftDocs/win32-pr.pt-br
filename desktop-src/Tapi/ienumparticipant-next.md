---
description: O próximo método obtém o próximo número especificado de elementos na sequência de enumeração. Esse método é ocultado das linguagens de Visual Basic e script.
ms.assetid: bd94f592-ac6f-48b7-8190-352a5e18f224
title: 'Método IEnumParticipant:: Next (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89586370d01aaac54f05242e0eb3c53eb938c47b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779312"
---
# <a name="ienumparticipantnext-method"></a><span data-ttu-id="ce985-104">Método IEnumParticipant:: Next</span><span class="sxs-lookup"><span data-stu-id="ce985-104">IEnumParticipant::Next method</span></span>

<span data-ttu-id="ce985-105">\[A **seguir** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ce985-105">\[**Next** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ce985-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="ce985-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ce985-107">O **próximo** método obtém o próximo número especificado de elementos na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="ce985-107">The **Next** method gets the next specified number of elements in the enumeration sequence.</span></span> <span data-ttu-id="ce985-108">Esse método é ocultado das linguagens de Visual Basic e script.</span><span class="sxs-lookup"><span data-stu-id="ce985-108">This method is hidden from Visual Basic and scripting languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce985-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce985-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG         celt,
  [out] ITParticipant **ppElements,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="ce985-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce985-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce985-111">*celt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce985-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce985-112">Número de elementos solicitados.</span><span class="sxs-lookup"><span data-stu-id="ce985-112">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="ce985-113">*ppElements* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ce985-113">*ppElements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce985-114">Ponteiro para interfaces [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) .</span><span class="sxs-lookup"><span data-stu-id="ce985-114">Pointer to [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="ce985-115">*pceltFetched* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ce985-115">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce985-116">Ponteiro para o número de elementos realmente fornecidos.</span><span class="sxs-lookup"><span data-stu-id="ce985-116">Pointer to number of elements actually supplied.</span></span> <span data-ttu-id="ce985-117">Poderá ser **NULL** se *celt* for um.</span><span class="sxs-lookup"><span data-stu-id="ce985-117">May be **NULL** if *celt* is one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce985-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ce985-118">Return value</span></span>

<span data-ttu-id="ce985-119">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="ce985-119">This method can return one of these values.</span></span>



| <span data-ttu-id="ce985-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ce985-120">Return code</span></span>                                                                                   | <span data-ttu-id="ce985-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce985-121">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="ce985-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ce985-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ce985-123">O método retornou *celt* número de elementos.</span><span class="sxs-lookup"><span data-stu-id="ce985-123">Method returned *celt* number of elements.</span></span><br/>           |
| <dl> <span data-ttu-id="ce985-124"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="ce985-124"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="ce985-125">O número de elementos restantes era menor que *celt*.</span><span class="sxs-lookup"><span data-stu-id="ce985-125">Number of elements remaining was less than *celt*.</span></span><br/>   |
| <dl> <span data-ttu-id="ce985-126"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="ce985-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ce985-127">O parâmetro *ppElements* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="ce985-127">The *ppElements* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="ce985-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ce985-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ce985-129">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="ce985-129">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ce985-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce985-130">Remarks</span></span>

<span data-ttu-id="ce985-131">A TAPI chama o método [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) na interface [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) retornada por **IEnumParticipant:: Next**.</span><span class="sxs-lookup"><span data-stu-id="ce985-131">TAPI calls the [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method on the [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) interface returned by **IEnumParticipant::Next**.</span></span> <span data-ttu-id="ce985-132">O aplicativo deve chamar [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) na interface **ITAgentHandler** para liberar recursos associados a ela.</span><span class="sxs-lookup"><span data-stu-id="ce985-132">The application must call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the **ITAgentHandler** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce985-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce985-133">Requirements</span></span>



| <span data-ttu-id="ce985-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce985-134">Requirement</span></span> | <span data-ttu-id="ce985-135">Valor</span><span class="sxs-lookup"><span data-stu-id="ce985-135">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce985-136">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="ce985-136">TAPI version</span></span><br/> | <span data-ttu-id="ce985-137">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="ce985-137">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ce985-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce985-138">Header</span></span><br/>       | <dl> <span data-ttu-id="ce985-139"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce985-139"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="ce985-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce985-140">Library</span></span><br/>      | <dl> <span data-ttu-id="ce985-141"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce985-141"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ce985-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ce985-142">DLL</span></span><br/>          | <dl> <span data-ttu-id="ce985-143"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce985-143"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ce985-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce985-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce985-145">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="ce985-145">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="ce985-146">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="ce985-146">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

