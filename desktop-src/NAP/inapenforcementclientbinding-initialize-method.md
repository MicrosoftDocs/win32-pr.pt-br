---
title: Método de inicialização de INapEnforcementClientBinding (NapEnforcementClient. h)
description: Inicia o serviço NapAgent automaticamente.
ms.assetid: 6b51043d-a8e7-41e4-9da9-e7f18f9bd068
keywords:
- Inicializar método NAP
- Método Initialize NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, método Initialize
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4d385e47bbbfe2e315d0a93d1f92542e8328e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454907"
---
# <a name="inapenforcementclientbindinginitialize-method"></a><span data-ttu-id="48036-106">Método INapEnforcementClientBinding:: Initialize</span><span class="sxs-lookup"><span data-stu-id="48036-106">INapEnforcementClientBinding::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="48036-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="48036-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="48036-108">O método **INapEnforcementClientBinding:: Initialize** inicia o serviço NapAgent automaticamente.</span><span class="sxs-lookup"><span data-stu-id="48036-108">The **INapEnforcementClientBinding::Initialize** method starts up the NapAgent service automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="48036-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48036-109">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] EnforcementEntityId           id,
  [in] INapEnforcementClientCallback *callback
);
```



## <a name="parameters"></a><span data-ttu-id="48036-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48036-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48036-111">*ID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="48036-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48036-112">Um [**EnforcementEntityId**](nap-datatypes.md) que identifica o cliente de imposição e sua versão.</span><span class="sxs-lookup"><span data-stu-id="48036-112">An [**EnforcementEntityId**](nap-datatypes.md) that identifies the enforcement client and its version.</span></span>

</dd> <dt>

<span data-ttu-id="48036-113">*retorno de chamada* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="48036-113">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48036-114">Um ponteiro COM para uma interface [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) usada pelo NapAgent para fazer o retorno de chamada dos clientes de imposição com notificação/processo.</span><span class="sxs-lookup"><span data-stu-id="48036-114">A COM pointer to an [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) interface used by the NapAgent to callback the enforcement clients with notify/process.</span></span> <span data-ttu-id="48036-115">O NapAgent mantém uma referência ao objeto associado a essa interface até que [**INapEnforcementClientBinding:: Uninitialize**](inapenforcementclientbinding-uninitialize-method.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="48036-115">The NapAgent holds a reference to the object associated with this interface until [**INapEnforcementClientBinding::Uninitialize**](inapenforcementclientbinding-uninitialize-method.md) is called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48036-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="48036-116">Return value</span></span>

<span data-ttu-id="48036-117">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="48036-117">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="48036-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="48036-118">Return code</span></span>                                                                                                         | <span data-ttu-id="48036-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="48036-119">Description</span></span>                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="48036-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="48036-120"><dt>**S\_OK** </dt></span></span> </dl>                               | <span data-ttu-id="48036-121">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="48036-121">The operation is successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="48036-122"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="48036-122"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>                     | <span data-ttu-id="48036-123">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="48036-123">Permissions error, access denied.</span></span><br/>                                             |
| <dl> <span data-ttu-id="48036-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="48036-124"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>                      | <span data-ttu-id="48036-125">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="48036-125">System resource limit, could not perform the operation.</span></span><br/>                       |
| <dl> <span data-ttu-id="48036-126"><dt>**HRESULT (erro \_ já \_ inicializado)**</dt></span><span class="sxs-lookup"><span data-stu-id="48036-126"><dt>**HRESULT(ERROR\_ALREADY\_INITIALIZED)**</dt></span></span> </dl> | <span data-ttu-id="48036-127">Se o aplicador tiver sido inicializado anteriormente, esse código de erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="48036-127">If the enforcer has initialized previously, then this error code is returned.</span></span><br/> |
| <dl> <span data-ttu-id="48036-128"><dt>**\_E/s NAP \_ não \_ registradas**</dt></span><span class="sxs-lookup"><span data-stu-id="48036-128"><dt>**NAP\_E\_NOT\_REGISTERED**</dt></span></span> </dl>              | <span data-ttu-id="48036-129">Se o imforçador não tiver sido registrado anteriormente, esse código de erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="48036-129">If the enforcer has not registered earlier, this error code is returned.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="48036-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="48036-130">Remarks</span></span>

<span data-ttu-id="48036-131">O cliente de imposição deve chamar o método **INapEnforcementClientBinding:: Initialize** antes de chamar qualquer outro método da interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="48036-131">The enforcement client must call the **INapEnforcementClientBinding::Initialize** method before calling any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="48036-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48036-132">Requirements</span></span>



| <span data-ttu-id="48036-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="48036-133">Requirement</span></span> | <span data-ttu-id="48036-134">Valor</span><span class="sxs-lookup"><span data-stu-id="48036-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48036-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48036-135">Minimum supported client</span></span><br/> | <span data-ttu-id="48036-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48036-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="48036-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48036-137">Minimum supported server</span></span><br/> | <span data-ttu-id="48036-138">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="48036-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="48036-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48036-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="48036-140"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="48036-140"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="48036-141">INSERI</span><span class="sxs-lookup"><span data-stu-id="48036-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="48036-142"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="48036-142"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="48036-143">DLL</span><span class="sxs-lookup"><span data-stu-id="48036-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48036-144"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48036-144"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="48036-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="48036-145">See also</span></span>

<dl> <span data-ttu-id="48036-146"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="48036-146"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="48036-147">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="48036-147">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="48036-148">**INapEnforcementClientBinding:: Uninitialize**</span><span class="sxs-lookup"><span data-stu-id="48036-148">**INapEnforcementClientBinding::Uninitialize**</span></span>](inapenforcementclientbinding-uninitialize-method.md)
</dt> </dl>

 

 





