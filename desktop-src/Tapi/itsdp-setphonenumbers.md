---
description: O método SetPhoneNumbers define uma matriz de números de telefone associados a um blob de conferência.
ms.assetid: 674c08df-7e91-4f19-9d65-4bc6e7af117b
title: 'Método ITSdp:: SetPhoneNumbers (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30ec2820d8d033ac2eed9d9287c3ca52c9deb316
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789859"
---
# <a name="itsdpsetphonenumbers-method"></a><span data-ttu-id="5281c-103">Método ITSdp:: SetPhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="5281c-103">ITSdp::SetPhoneNumbers method</span></span>

<span data-ttu-id="5281c-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5281c-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5281c-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="5281c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5281c-106">O método **SetPhoneNumbers** define uma matriz de números de telefone associados a um blob de conferência.</span><span class="sxs-lookup"><span data-stu-id="5281c-106">The **SetPhoneNumbers** method sets an array of phone numbers associated with a conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="5281c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5281c-107">Syntax</span></span>


```C++
HRESULT SetPhoneNumbers(
  [in] VARIANT Numbers,
  [in] VARIANT Names
);
```



## <a name="parameters"></a><span data-ttu-id="5281c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5281c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5281c-109">*Números* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="5281c-109">*Numbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5281c-110">SAFEARRAY de números de telefone de listagem do **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="5281c-110">SAFEARRAY of **BSTR** s listing phone numbers.</span></span>

</dd> <dt>

<span data-ttu-id="5281c-111">*Nomes* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="5281c-111">*Names* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5281c-112">SAFEARRAY de nomes de listagem **BSTR** s.</span><span class="sxs-lookup"><span data-stu-id="5281c-112">SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5281c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5281c-113">Return value</span></span>

<span data-ttu-id="5281c-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="5281c-114">This method can return one of these values.</span></span>



| <span data-ttu-id="5281c-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5281c-115">Return code</span></span>                                                                                   | <span data-ttu-id="5281c-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="5281c-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="5281c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5281c-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5281c-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="5281c-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5281c-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5281c-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="5281c-120">O parâmetro de *números* ou *nomes* não é válido.</span><span class="sxs-lookup"><span data-stu-id="5281c-120">The *Numbers* or *Names* parameter is not valid.</span></span><br/>     |
| <dl> <span data-ttu-id="5281c-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5281c-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5281c-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="5281c-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="5281c-123"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="5281c-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="5281c-124">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="5281c-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="5281c-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="5281c-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="5281c-126">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="5281c-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="5281c-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="5281c-127">Remarks</span></span>

<span data-ttu-id="5281c-128">As listas que os *números* e *nomes* apontam têm o mesmo comprimento.</span><span class="sxs-lookup"><span data-stu-id="5281c-128">The lists that *Numbers* and *Names* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="5281c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5281c-129">Requirements</span></span>



| <span data-ttu-id="5281c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="5281c-130">Requirement</span></span> | <span data-ttu-id="5281c-131">Valor</span><span class="sxs-lookup"><span data-stu-id="5281c-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5281c-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="5281c-132">TAPI version</span></span><br/> | <span data-ttu-id="5281c-133">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="5281c-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5281c-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5281c-134">Header</span></span><br/>       | <dl> <span data-ttu-id="5281c-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="5281c-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="5281c-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5281c-136">Library</span></span><br/>      | <dl> <span data-ttu-id="5281c-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5281c-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5281c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5281c-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="5281c-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5281c-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5281c-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="5281c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5281c-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="5281c-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




