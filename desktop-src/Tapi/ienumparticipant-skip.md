---
description: O método Skip ignora o próximo número especificado de elementos na sequência de enumeração. Esse método é ocultado das linguagens de Visual Basic e script.
ms.assetid: 7f641354-c3f5-4eb3-ad1c-98abf7694106
title: 'Método IEnumParticipant:: Skip (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dc406a69c126c25b1c554679595868a595b839b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796329"
---
# <a name="ienumparticipantskip-method"></a><span data-ttu-id="be89b-104">Método IEnumParticipant:: Skip</span><span class="sxs-lookup"><span data-stu-id="be89b-104">IEnumParticipant::Skip method</span></span>

<span data-ttu-id="be89b-105">\[O **Skip** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="be89b-105">\[**Skip** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="be89b-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="be89b-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="be89b-107">O método **Skip** ignora o próximo número especificado de elementos na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="be89b-107">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span> <span data-ttu-id="be89b-108">Esse método é ocultado das linguagens de Visual Basic e script.</span><span class="sxs-lookup"><span data-stu-id="be89b-108">This method is hidden from Visual Basic and scripting languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="be89b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be89b-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="be89b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be89b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be89b-111">*celt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="be89b-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be89b-112">Número de elementos a serem ignorados.</span><span class="sxs-lookup"><span data-stu-id="be89b-112">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be89b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="be89b-113">Return value</span></span>

<span data-ttu-id="be89b-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="be89b-114">This method can return one of these values.</span></span>



| <span data-ttu-id="be89b-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="be89b-115">Return code</span></span>                                                                                   | <span data-ttu-id="be89b-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="be89b-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="be89b-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="be89b-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="be89b-118">O número de elementos ignorados foi *celt*.</span><span class="sxs-lookup"><span data-stu-id="be89b-118">Number of elements skipped was *celt*.</span></span><br/>               |
| <dl> <span data-ttu-id="be89b-119"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="be89b-119"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="be89b-120">O número de elementos ignorados não era *celt*.</span><span class="sxs-lookup"><span data-stu-id="be89b-120">Number of elements skipped was not *celt*.</span></span><br/>           |
| <dl> <span data-ttu-id="be89b-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="be89b-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="be89b-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="be89b-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="be89b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be89b-123">Requirements</span></span>



| <span data-ttu-id="be89b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="be89b-124">Requirement</span></span> | <span data-ttu-id="be89b-125">Valor</span><span class="sxs-lookup"><span data-stu-id="be89b-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be89b-126">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="be89b-126">TAPI version</span></span><br/> | <span data-ttu-id="be89b-127">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="be89b-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="be89b-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be89b-128">Header</span></span><br/>       | <dl> <span data-ttu-id="be89b-129"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="be89b-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="be89b-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="be89b-130">Library</span></span><br/>      | <dl> <span data-ttu-id="be89b-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be89b-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="be89b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="be89b-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="be89b-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be89b-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="be89b-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="be89b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be89b-135">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="be89b-135">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="be89b-136">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="be89b-136">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




