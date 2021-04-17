---
title: Método INapSystemHealthValidationRequest GetSoHResponse (NapSystemHealthValidator. h)
description: Recupera o SoHResponse.
ms.assetid: 7db9d134-5cd4-4a6c-8576-843b9a920864
keywords:
- Método GetSoHResponse NAP
- Método GetSoHResponse NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, método GetSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc10174edc2bcb9df8e61c98305e42633d2b984b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759624"
---
# <a name="inapsystemhealthvalidationrequestgetsohresponse-method"></a><span data-ttu-id="1def1-106">Método INapSystemHealthValidationRequest:: GetSoHResponse</span><span class="sxs-lookup"><span data-stu-id="1def1-106">INapSystemHealthValidationRequest::GetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="1def1-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="1def1-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1def1-108">O método **INapSystemHealthValidationRequest:: GetSoHResponse** recupera o [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="1def1-108">The **INapSystemHealthValidationRequest::GetSoHResponse** method retrieves the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

## <a name="syntax"></a><span data-ttu-id="1def1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1def1-109">Syntax</span></span>


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="1def1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1def1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1def1-111">*sohResponse* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1def1-111">*sohResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1def1-112">Um ponteiro para um ponteiro para o [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh)recebido.</span><span class="sxs-lookup"><span data-stu-id="1def1-112">A pointer to a pointer to the received [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1def1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1def1-113">Return value</span></span>

<span data-ttu-id="1def1-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="1def1-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="1def1-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1def1-115">Return code</span></span>                                                                                     | <span data-ttu-id="1def1-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="1def1-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="1def1-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1def1-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="1def1-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1def1-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1def1-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="1def1-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="1def1-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="1def1-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="1def1-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1def1-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="1def1-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="1def1-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1def1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1def1-123">Requirements</span></span>



| <span data-ttu-id="1def1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1def1-124">Requirement</span></span> | <span data-ttu-id="1def1-125">Valor</span><span class="sxs-lookup"><span data-stu-id="1def1-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1def1-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1def1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1def1-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1def1-127">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="1def1-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1def1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1def1-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1def1-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1def1-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1def1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1def1-131"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="1def1-131"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="1def1-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="1def1-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1def1-133"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1def1-133"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="1def1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1def1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1def1-135"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1def1-135"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="1def1-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="1def1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1def1-137">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="1def1-137">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





