---
title: Método INapEnforcementClientBinding NotifySoHChangeFailure (NapEnforcementClient. h)
description: É usado pelo cliente de imposição para informar ao NapAgent que ele não pôde processar um NotifySoHChange de INapEnforcementClientCallback anterior.
ms.assetid: 2de1626c-ffda-4191-90c4-72d0275965d9
keywords:
- Método NotifySoHChangeFailure NAP
- Método NotifySoHChangeFailure NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, método NotifySoHChangeFailure
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifySoHChangeFailure
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af23fd41e5a8b97064c089062eae13e93cf9ff0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455995"
---
# <a name="inapenforcementclientbindingnotifysohchangefailure-method"></a><span data-ttu-id="fa2d7-106">Método INapEnforcementClientBinding:: NotifySoHChangeFailure</span><span class="sxs-lookup"><span data-stu-id="fa2d7-106">INapEnforcementClientBinding::NotifySoHChangeFailure method</span></span>

> [!Note]  
> <span data-ttu-id="fa2d7-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="fa2d7-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fa2d7-108">O método **INapEnforcementClientBinding:: NotifySoHChangeFailure** é usado pelo cliente de imposição para informar ao NapAgent que ele não pôde processar um [**INapEnforcementClientCallback:: NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)anterior.</span><span class="sxs-lookup"><span data-stu-id="fa2d7-108">The **INapEnforcementClientBinding::NotifySoHChangeFailure** method is used by the enforcement client to inform the NapAgent that it could not process a previous [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fa2d7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa2d7-109">Syntax</span></span>


```C++
HRESULT NotifySoHChangeFailure();
```



## <a name="parameters"></a><span data-ttu-id="fa2d7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa2d7-110">Parameters</span></span>

<span data-ttu-id="fa2d7-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fa2d7-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa2d7-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa2d7-112">Return value</span></span>

<span data-ttu-id="fa2d7-113">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="fa2d7-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="fa2d7-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fa2d7-114">Return code</span></span>                                                                                             | <span data-ttu-id="fa2d7-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa2d7-115">Description</span></span>                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="fa2d7-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fa2d7-116"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="fa2d7-117">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="fa2d7-117">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="fa2d7-118"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="fa2d7-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="fa2d7-119">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="fa2d7-119">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="fa2d7-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fa2d7-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="fa2d7-121">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="fa2d7-121">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="fa2d7-122"><dt>**NAP \_ E \_ não \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="fa2d7-122"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="fa2d7-123">O imforçador não foi inicializado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="fa2d7-123">The enforcer has not been previously initialized.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="fa2d7-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa2d7-124">Remarks</span></span>

<span data-ttu-id="fa2d7-125">Como resultado desse método, chame o NapAgent repetições aplicando a alteração SoH em um momento posterior chamando [**INapEnforcementClientCallback:: NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) novamente.</span><span class="sxs-lookup"><span data-stu-id="fa2d7-125">As a result of this method call the NapAgent retries applying the SoH change at a later time by calling [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) again.</span></span> <span data-ttu-id="fa2d7-126">Depois que o cliente de imposição tiver chamado [**INapEnforcementClientBinding:: GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md), ele deverá aplicar a alteração, ou seja, nenhuma falha será tratada pelo NapAgent após esse ponto.</span><span class="sxs-lookup"><span data-stu-id="fa2d7-126">Once the enforcement client has called [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md), it then must apply the change, i.e. no failures are handled by the NapAgent after this point.</span></span>

<span data-ttu-id="fa2d7-127">O cliente de imposição deve chamar o método [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) antes de chamar este ou qualquer outro método da interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="fa2d7-127">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa2d7-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa2d7-128">Requirements</span></span>



| <span data-ttu-id="fa2d7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa2d7-129">Requirement</span></span> | <span data-ttu-id="fa2d7-130">Valor</span><span class="sxs-lookup"><span data-stu-id="fa2d7-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa2d7-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa2d7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="fa2d7-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa2d7-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fa2d7-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa2d7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="fa2d7-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fa2d7-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fa2d7-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa2d7-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa2d7-136"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa2d7-136"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="fa2d7-137">INSERI</span><span class="sxs-lookup"><span data-stu-id="fa2d7-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fa2d7-138"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fa2d7-138"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="fa2d7-139">DLL</span><span class="sxs-lookup"><span data-stu-id="fa2d7-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa2d7-140"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa2d7-140"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="fa2d7-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa2d7-141">See also</span></span>

<dl> <span data-ttu-id="fa2d7-142"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="fa2d7-142"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="fa2d7-143">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="fa2d7-143">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="fa2d7-144">**INapEnforcementClientBinding::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="fa2d7-144">**INapEnforcementClientBinding::GetSoHRequest**</span></span>](inapenforcementclientbinding-getsohrequest-method.md)
</dt> <dt>

[<span data-ttu-id="fa2d7-145">**INapEnforcementClientCallback::NotifySoHChange**</span><span class="sxs-lookup"><span data-stu-id="fa2d7-145">**INapEnforcementClientCallback::NotifySoHChange**</span></span>](inapenforcementclientcallback-notifysohchange-method.md)
</dt> </dl>

 

 





