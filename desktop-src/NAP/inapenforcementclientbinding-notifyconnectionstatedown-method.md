---
title: Método INapEnforcementClientBinding NotifyConnectionStateDown (NapEnforcementClient. h)
description: É usado para informar ao NapAgent que uma conexão com um cliente de imposição foi desativada.
ms.assetid: 504c61c1-c8f9-46b8-87cd-c1f04846f0b3
keywords:
- Método NotifyConnectionStateDown NAP
- Método NotifyConnectionStateDown NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, método NotifyConnectionStateDown
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifyConnectionStateDown
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3129883342f493fd56a4cc81513910e8789ca4f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499856"
---
# <a name="inapenforcementclientbindingnotifyconnectionstatedown-method"></a><span data-ttu-id="f3639-106">Método INapEnforcementClientBinding:: NotifyConnectionStateDown</span><span class="sxs-lookup"><span data-stu-id="f3639-106">INapEnforcementClientBinding::NotifyConnectionStateDown method</span></span>

> [!Note]  
> <span data-ttu-id="f3639-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="f3639-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f3639-108">O método **INapEnforcementClientBinding:: NotifyConnectionStateDown** é usado para informar ao NapAgent que uma conexão a um cliente de imposição foi desativada.</span><span class="sxs-lookup"><span data-stu-id="f3639-108">The **INapEnforcementClientBinding::NotifyConnectionStateDown** method is used to inform the NapAgent that a connection to an enforcement client has gone down.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3639-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3639-109">Syntax</span></span>


```C++
HRESULT NotifyConnectionStateDown(
  [in] INapEnforcementClientConnection *downCxn
);
```



## <a name="parameters"></a><span data-ttu-id="f3639-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3639-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3639-111">*downCxn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f3639-111">*downCxn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3639-112">Um ponteiro COM para a interface [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) da conexão inoperante.</span><span class="sxs-lookup"><span data-stu-id="f3639-112">A COM pointer to the [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface of the down connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3639-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f3639-113">Return value</span></span>

<span data-ttu-id="f3639-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="f3639-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="f3639-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f3639-115">Return code</span></span>                                                                                             | <span data-ttu-id="f3639-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3639-116">Description</span></span>                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f3639-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f3639-117"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="f3639-118">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="f3639-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="f3639-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="f3639-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="f3639-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="f3639-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f3639-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f3639-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="f3639-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="f3639-122">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="f3639-123"><dt>**NAP \_ E \_ não \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="f3639-123"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="f3639-124">O imforçador não foi inicializado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f3639-124">The enforcer has not been previously initialized.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="f3639-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3639-125">Remarks</span></span>

<span data-ttu-id="f3639-126">Quando qualquer uma das conexões estabelecidas por um cliente de imposição for desativada, o cliente de imposição deverá remover a conexão de sua lista ativa e informar o NapAgent usando esse método.</span><span class="sxs-lookup"><span data-stu-id="f3639-126">When any of the connections established by an enforcement client go down, the enforcement client should remove the connection from its active list and inform the NapAgent using this method.</span></span> <span data-ttu-id="f3639-127">Assim que essa chamada retorna, o objeto de conexão pode ser liberado e liberado.</span><span class="sxs-lookup"><span data-stu-id="f3639-127">As soon as this call returns, the connection object can be released and freed.</span></span> <span data-ttu-id="f3639-128">O NapAgent não conterá referências ao objeto de conexão.</span><span class="sxs-lookup"><span data-stu-id="f3639-128">The NapAgent will not hold references to the connection object.</span></span>

<span data-ttu-id="f3639-129">Como resultado dessa notificação, o NapAgent atualiza seu estado NAP do sistema, conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="f3639-129">As a result of this notification, the NapAgent updates its system NAP state as appropriate.</span></span>

<span data-ttu-id="f3639-130">O cliente de imposição deve chamar o método [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) antes de chamar este ou qualquer outro método da interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="f3639-130">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3639-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3639-131">Requirements</span></span>



| <span data-ttu-id="f3639-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3639-132">Requirement</span></span> | <span data-ttu-id="f3639-133">Valor</span><span class="sxs-lookup"><span data-stu-id="f3639-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3639-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3639-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f3639-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f3639-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f3639-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3639-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f3639-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f3639-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f3639-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f3639-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3639-139"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3639-139"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="f3639-140">INSERI</span><span class="sxs-lookup"><span data-stu-id="f3639-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f3639-141"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f3639-141"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="f3639-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f3639-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3639-143"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3639-143"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="f3639-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3639-144">See also</span></span>

<dl> <span data-ttu-id="f3639-145"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="f3639-145"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="f3639-146">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="f3639-146">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> </dl>

 

 





