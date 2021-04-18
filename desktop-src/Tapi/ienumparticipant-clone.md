---
description: O método clone cria outro enumerador que contém o mesmo estado de enumeração que o atual. Esse método é ocultado das linguagens de Visual Basic e script.
ms.assetid: 551e0ddc-7ebf-4fc2-a155-0c9ee2f406d4
title: 'Método IEnumParticipant:: clone (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5b094f47738fd23f2762b7012a4e23c8b89da57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780606"
---
# <a name="ienumparticipantclone-method"></a><span data-ttu-id="ee1e0-104">Método IEnumParticipant:: clone</span><span class="sxs-lookup"><span data-stu-id="ee1e0-104">IEnumParticipant::Clone method</span></span>

<span data-ttu-id="ee1e0-105">\[O **clone** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ee1e0-105">\[**Clone** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ee1e0-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="ee1e0-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ee1e0-107">O método **clone** cria outro enumerador que contém o mesmo estado de enumeração que o atual.</span><span class="sxs-lookup"><span data-stu-id="ee1e0-107">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span> <span data-ttu-id="ee1e0-108">Esse método é ocultado das linguagens de Visual Basic e script.</span><span class="sxs-lookup"><span data-stu-id="ee1e0-108">This method is hidden from Visual Basic and scripting languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee1e0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee1e0-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumParticipant **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="ee1e0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee1e0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee1e0-111">*ppEnum* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ee1e0-111">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee1e0-112">Ponteiro para a nova interface [**IEnumParticipant**](ienumparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="ee1e0-112">Pointer to new [**IEnumParticipant**](ienumparticipant.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee1e0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee1e0-113">Return value</span></span>

<span data-ttu-id="ee1e0-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="ee1e0-114">This method can return one of these values.</span></span>



| <span data-ttu-id="ee1e0-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ee1e0-115">Return code</span></span>                                                                                   | <span data-ttu-id="ee1e0-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee1e0-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="ee1e0-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ee1e0-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ee1e0-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ee1e0-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ee1e0-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="ee1e0-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ee1e0-120">O parâmetro *ppEnum* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="ee1e0-120">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="ee1e0-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ee1e0-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ee1e0-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="ee1e0-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="ee1e0-123"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="ee1e0-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="ee1e0-124">Falha por motivos desconhecidos.</span><span class="sxs-lookup"><span data-stu-id="ee1e0-124">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="ee1e0-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee1e0-125">Remarks</span></span>

<span data-ttu-id="ee1e0-126">A TAPI chama o método [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) na interface [**IEnumParticipant**](ienumparticipant.md) retornada por **IEnumParticipant:: clone**.</span><span class="sxs-lookup"><span data-stu-id="ee1e0-126">TAPI calls the [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method on the [**IEnumParticipant**](ienumparticipant.md) interface returned by **IEnumParticipant::Clone**.</span></span> <span data-ttu-id="ee1e0-127">O aplicativo deve chamar [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) na interface **IEnumParticipant** para liberar recursos associados a ela.</span><span class="sxs-lookup"><span data-stu-id="ee1e0-127">The application must call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the **IEnumParticipant** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee1e0-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee1e0-128">Requirements</span></span>



| <span data-ttu-id="ee1e0-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee1e0-129">Requirement</span></span> | <span data-ttu-id="ee1e0-130">Valor</span><span class="sxs-lookup"><span data-stu-id="ee1e0-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee1e0-131">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="ee1e0-131">TAPI version</span></span><br/> | <span data-ttu-id="ee1e0-132">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="ee1e0-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ee1e0-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee1e0-133">Header</span></span><br/>       | <dl> <span data-ttu-id="ee1e0-134"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee1e0-134"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="ee1e0-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee1e0-135">Library</span></span><br/>      | <dl> <span data-ttu-id="ee1e0-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee1e0-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ee1e0-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ee1e0-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="ee1e0-138"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee1e0-138"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ee1e0-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee1e0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee1e0-140">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="ee1e0-140">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="ee1e0-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="ee1e0-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

