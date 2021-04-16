---
title: Método OnComplete do INapServerCallback (NapSystemHealthValidator. h)
description: Usado por SHVs para sinalizar a conclusão da solicitação assíncrona.
ms.assetid: 959ee4ac-7c29-4013-a174-24abc6a580c7
keywords:
- Método OnComplete NAP
- Método OnComplete NAP, interface INapServerCallback
- Interface INapServerCallback NAP, método OnComplete
topic_type:
- apiref
api_name:
- INapServerCallback.OnComplete
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef846d3d9dc2d6618f0eca9f097d74222606eb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456022"
---
# <a name="inapservercallbackoncomplete-method"></a><span data-ttu-id="a6682-106">Método INapServerCallback:: OnComplete</span><span class="sxs-lookup"><span data-stu-id="a6682-106">INapServerCallback::OnComplete method</span></span>

> [!Note]  
> <span data-ttu-id="a6682-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="a6682-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a6682-108">O método **INapServerCallback:: OnComplete** é usado por SHVs para sinalizar a conclusão da solicitação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="a6682-108">The **INapServerCallback::OnComplete** method is used by SHVs to signal asynchronous request completion.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6682-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6682-109">Syntax</span></span>


```C++
HRESULT OnComplete(
  [in] INapSystemHealthValidationRequest *request,
  [in] HRESULT                           errorCode
);
```



## <a name="parameters"></a><span data-ttu-id="a6682-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6682-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6682-111">*solicitação* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="a6682-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6682-112">Um ponteiro para um objeto [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) que representa uma solicitação de validação.</span><span class="sxs-lookup"><span data-stu-id="a6682-112">A pointer to an [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) object that represents a validation request.</span></span>

</dd> <dt>

<span data-ttu-id="a6682-113">*ErrorCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a6682-113">*errorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6682-114">Um [**código de erro NAP**](nap-error-constants.md) que indica o motivo pelo qual a validação não pôde ser executada.</span><span class="sxs-lookup"><span data-stu-id="a6682-114">A [**NAP error code**](nap-error-constants.md) that indicates the reason why the validation could not be performed.</span></span>

> [!Note]  
> <span data-ttu-id="a6682-115">Normalmente, o valor de retorno do método [**INapSystemHealthValidationRequest:: SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md) é passado para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a6682-115">Typically, the return value of the [**INapSystemHealthValidationRequest::SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md) method is passed to this parameter.</span></span> <span data-ttu-id="a6682-116">No entanto, se **SetSoHResponse** não puder ser chamado devido a uma falha de reprocessamento, o valor retornado pelo comando com falha será passado.</span><span class="sxs-lookup"><span data-stu-id="a6682-116">However, if **SetSoHResponse** could not be called due to a reprocessing failure, the value returned by the failed command is passed.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6682-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6682-117">Return value</span></span>

<span data-ttu-id="a6682-118">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="a6682-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="a6682-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a6682-119">Return code</span></span>                                                                                     | <span data-ttu-id="a6682-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="a6682-120">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="a6682-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a6682-121"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="a6682-122">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a6682-122">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a6682-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="a6682-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="a6682-124">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="a6682-124">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="a6682-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a6682-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="a6682-126">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="a6682-126">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a6682-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6682-127">Remarks</span></span>

<span data-ttu-id="a6682-128">Os validadores devem retornar S \_ OK se a validação de [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) puder ser concluída, independentemente de o **SoHRequest** ter passado a verificação de integridade.</span><span class="sxs-lookup"><span data-stu-id="a6682-128">Validators must return S\_OK if the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) validation could be completed, regardless of whether the **SoHRequest** passed the health check.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6682-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6682-129">Requirements</span></span>



| <span data-ttu-id="a6682-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6682-130">Requirement</span></span> | <span data-ttu-id="a6682-131">Valor</span><span class="sxs-lookup"><span data-stu-id="a6682-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6682-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6682-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a6682-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a6682-133">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="a6682-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6682-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a6682-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a6682-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a6682-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6682-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6682-137"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6682-137"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="a6682-138">INSERI</span><span class="sxs-lookup"><span data-stu-id="a6682-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a6682-139"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a6682-139"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="a6682-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a6682-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6682-141"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6682-141"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="a6682-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6682-142">See also</span></span>

<dl> <span data-ttu-id="a6682-143"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="a6682-143"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="a6682-144">**INapServerCallback**</span><span class="sxs-lookup"><span data-stu-id="a6682-144">**INapServerCallback**</span></span>](inapservercallback.md)
</dt> <dt>

[<span data-ttu-id="a6682-145">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="a6682-145">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





