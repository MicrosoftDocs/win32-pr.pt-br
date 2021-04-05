---
title: Método INapEnforcementClientBinding GetSoHRequest (NapEnforcementClient. h)
description: É usado pelo cliente de imposição para recuperar uma solicitação SoH para uma conexão específica.
ms.assetid: 6fce6e84-ce03-48f2-957b-a41efe044fc5
keywords:
- Método GetSoHRequest NAP
- Método GetSoHRequest NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, método GetSoHRequest
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9fed4872df7ab328ab241b070a9eeb07907de85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918240"
---
# <a name="inapenforcementclientbindinggetsohrequest-method"></a><span data-ttu-id="e5d35-106">Método INapEnforcementClientBinding:: GetSoHRequest</span><span class="sxs-lookup"><span data-stu-id="e5d35-106">INapEnforcementClientBinding::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="e5d35-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="e5d35-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e5d35-108">O método **INapEnforcementClientBinding:: GetSoHRequest** é usado pelo cliente de imposição para recuperar uma solicitação soh para uma conexão específica.</span><span class="sxs-lookup"><span data-stu-id="e5d35-108">The **INapEnforcementClientBinding::GetSoHRequest** method is used by the enforcement client to retrieve an SoH-request for a particular connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5d35-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5d35-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [in]  INapEnforcementClientConnection *connection,
  [out] BOOL                            *retriggerHint
);
```



## <a name="parameters"></a><span data-ttu-id="e5d35-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5d35-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5d35-111">*conexão* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="e5d35-111">*connection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5d35-112">Um ponteiro COM para uma interface [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="e5d35-112">A COM pointer to an [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface.</span></span> <span data-ttu-id="e5d35-113">O NapAgent não mantém referências ao objeto associado a essa interface após a conclusão do método.</span><span class="sxs-lookup"><span data-stu-id="e5d35-113">The NapAgent does not hold references to the object associated with this interface after the method completes.</span></span>

</dd> <dt>

<span data-ttu-id="e5d35-114">*retriggerHint* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e5d35-114">*retriggerHint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5d35-115">Um ponteiro para um **bool** que indica se a conexão deve ser disparada novamente.</span><span class="sxs-lookup"><span data-stu-id="e5d35-115">A pointer to a **BOOL** that indicates if the connection should be re-triggered.</span></span> <span data-ttu-id="e5d35-116">Será **verdadeiro** se o [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) tiver sido alterado desde que essa função foi chamada pela última vez [**ou se o**](nap-datatypes.md) acessador tiver expirado.</span><span class="sxs-lookup"><span data-stu-id="e5d35-116">It is **TRUE** if the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) has changed since this function was last called or if [**ProbationTime**](nap-datatypes.md) has expired.</span></span> <span data-ttu-id="e5d35-117">Caso contrário, **false** será retornado.</span><span class="sxs-lookup"><span data-stu-id="e5d35-117">Otherwise, **FALSE** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5d35-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e5d35-118">Return value</span></span>

<span data-ttu-id="e5d35-119">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="e5d35-119">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="e5d35-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e5d35-120">Return code</span></span>                                                                                             | <span data-ttu-id="e5d35-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5d35-121">Description</span></span>                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="e5d35-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e5d35-122"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="e5d35-123">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="e5d35-123">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="e5d35-124"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="e5d35-124"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="e5d35-125">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="e5d35-125">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="e5d35-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e5d35-126"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="e5d35-127">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="e5d35-127">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="e5d35-128"><dt>**NAP \_ E \_ não \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="e5d35-128"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="e5d35-129">O imforçador não foi inicializado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e5d35-129">The enforcer has not been previously initialized.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="e5d35-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5d35-130">Remarks</span></span>

<span data-ttu-id="e5d35-131">O NapAgent define o [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) no objeto de conexão.</span><span class="sxs-lookup"><span data-stu-id="e5d35-131">The NapAgent sets the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) on the connection object.</span></span>

<span data-ttu-id="e5d35-132">Se um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) estava pendente nessa conexão, ele é Descartado e os SHAs são notificados de **SoHRequests** órfãos.</span><span class="sxs-lookup"><span data-stu-id="e5d35-132">If an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) was outstanding on this connection, then it is discarded, and the SHAs are notified of orphaned **SoHRequests**.</span></span>

<span data-ttu-id="e5d35-133">O cliente de imposição deve chamar o método [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) antes de chamar este ou qualquer outro método da interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="e5d35-133">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5d35-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5d35-134">Requirements</span></span>



| <span data-ttu-id="e5d35-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5d35-135">Requirement</span></span> | <span data-ttu-id="e5d35-136">Valor</span><span class="sxs-lookup"><span data-stu-id="e5d35-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5d35-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5d35-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e5d35-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e5d35-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e5d35-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5d35-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e5d35-140">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e5d35-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e5d35-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5d35-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5d35-142"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5d35-142"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="e5d35-143">INSERI</span><span class="sxs-lookup"><span data-stu-id="e5d35-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e5d35-144"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e5d35-144"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="e5d35-145">DLL</span><span class="sxs-lookup"><span data-stu-id="e5d35-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5d35-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5d35-146"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="e5d35-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5d35-147">See also</span></span>

<dl> <span data-ttu-id="e5d35-148"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="e5d35-148"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="e5d35-149">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="e5d35-149">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> </dl>

 

 





