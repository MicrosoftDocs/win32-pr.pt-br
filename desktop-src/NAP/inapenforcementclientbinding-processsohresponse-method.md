---
title: Método INapEnforcementClientBinding ProcessSoHResponse (NapEnforcementClient. h)
description: É usado por clientes de imposição para processar um SoHResponse sempre que eles recebem um blob de dados SoHResponse do servidor de imposição.
ms.assetid: 6ff6d2c5-9ebe-4d8c-aa27-03147e2e1122
keywords:
- Método ProcessSoHResponse NAP
- Método ProcessSoHResponse NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, método ProcessSoHResponse
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.ProcessSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ac8c87314ca1e28163428bf53e4a1fc6e31106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499830"
---
# <a name="inapenforcementclientbindingprocesssohresponse-method"></a><span data-ttu-id="8f9c3-106">INapEnforcementClientBinding: método rocessSoHResponse de:P</span><span class="sxs-lookup"><span data-stu-id="8f9c3-106">INapEnforcementClientBinding::ProcessSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="8f9c3-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="8f9c3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8f9c3-108">O método **INapEnforcementClientBinding::P rocesssohresponse** é usado pelos clientes de imposição para processar um SoHResponse sempre que eles recebem um blob de dados SoHResponse do servidor de imposição.</span><span class="sxs-lookup"><span data-stu-id="8f9c3-108">The **INapEnforcementClientBinding::ProcessSoHResponse** method is used by enforcement clients to process an SoHResponse whenever they receive an SoHResponse data blob from the enforcement server.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f9c3-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f9c3-109">Syntax</span></span>


```C++
HRESULT ProcessSoHResponse(
  [in] INapEnforcementClientConnection *connection
);
```



## <a name="parameters"></a><span data-ttu-id="8f9c3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f9c3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f9c3-111">*conexão* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="8f9c3-111">*connection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f9c3-112">Um ponteiro COM para a interface [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) da conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="8f9c3-112">A COM pointer to the [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface of the client connection.</span></span> <span data-ttu-id="8f9c3-113">O NapAgent não mantém referências ao objeto associado a essa interface após a conclusão dessa chamada de método.</span><span class="sxs-lookup"><span data-stu-id="8f9c3-113">The NapAgent does not hold references to the object associated with this interface after this method call completes.</span></span>

<span data-ttu-id="8f9c3-114">Você deve usar uma conexão estabelecida anteriormente para processar blobs de dados SOHResponse.</span><span class="sxs-lookup"><span data-stu-id="8f9c3-114">You must use a previously established connection for processing SOHResponse data blobs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f9c3-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8f9c3-115">Return value</span></span>

<span data-ttu-id="8f9c3-116">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="8f9c3-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="8f9c3-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8f9c3-117">Return code</span></span>                                                                                             | <span data-ttu-id="8f9c3-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f9c3-118">Description</span></span>                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8f9c3-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8f9c3-119"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="8f9c3-120">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="8f9c3-120">The operation is successful.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="8f9c3-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8f9c3-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="8f9c3-122">Nenhuma conexão foi criada anteriormente no cliente de imposição.</span><span class="sxs-lookup"><span data-stu-id="8f9c3-122">No connections have previously been created on the enforcement client.</span></span> <br/>                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="8f9c3-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="8f9c3-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="8f9c3-124">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="8f9c3-124">Permissions error, access denied.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="8f9c3-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8f9c3-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="8f9c3-126">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="8f9c3-126">System resource limit, could not perform the operation.</span></span><br/>                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="8f9c3-127"><dt>**\_pacote NAP E \_ inválido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8f9c3-127"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl>  | <span data-ttu-id="8f9c3-128">Se esse valor for retornado, o cliente de imposição deverá descartar o pacote se o NapAgent retornar um \_ pacote NAP E \_ inválido \_ .</span><span class="sxs-lookup"><span data-stu-id="8f9c3-128">If this value is returned the enforcement client must drop the packet if the NapAgent returns NAP\_E\_INVALID\_PACKET.</span></span> <span data-ttu-id="8f9c3-129">Nesse caso, o aplicador deve assumir que o servidor ao qual está se comunicando não é habilitado para NAP e remover a conexão da lista ativa (ou seja, notificar o NapAgent de um estado de conexão).</span><span class="sxs-lookup"><span data-stu-id="8f9c3-129">In this case, the enforcer must assume that the server it is talking to is not NAP-enabled and remove the connection from the active list (i.e. notify the NapAgent of a connection state down).</span></span><br/> |
| <dl> <span data-ttu-id="8f9c3-130"><dt>**ID de NAP \_ E não \_ correspondente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8f9c3-130"><dt>**NAP\_E\_MISMATCHED\_ID**</dt></span></span> </dl>   | <span data-ttu-id="8f9c3-131">Se esse valor for retornado, isso indica que a ID de correlação no pacote de SoH-Response não correspondeu à resposta SoH-Response pendente.</span><span class="sxs-lookup"><span data-stu-id="8f9c3-131">If this value is returned it indicates that the correlation id in the SoH-Response packet did not match the outstanding SoH-Response.</span></span> <span data-ttu-id="8f9c3-132">Nesse caso, o aplicador deve descartar o pacote e aguardar outro pacote de SoH-Response mais recente.</span><span class="sxs-lookup"><span data-stu-id="8f9c3-132">In this case, the enforcer should drop the packet and wait for another newer SoH-Response packet.</span></span><br/> <span data-ttu-id="8f9c3-133">Isso pode ser causado por uma resposta a uma mensagem de solicitação mais antiga.</span><span class="sxs-lookup"><span data-stu-id="8f9c3-133">This may be caused by a response to an older request message.</span></span><br/>        |
| <dl> <span data-ttu-id="8f9c3-134"><dt>**NAP \_ E \_ não \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="8f9c3-134"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="8f9c3-135">O imforçador não foi inicializado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="8f9c3-135">The enforcer has not been previously initialized.</span></span><br/>                                                                                                                                                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="8f9c3-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f9c3-136">Remarks</span></span>

<span data-ttu-id="8f9c3-137">O NapAgent consulta o blob de dados SoH-Response do objeto de conexão, processa-o e define a decisão resultante (por exemplo,</span><span class="sxs-lookup"><span data-stu-id="8f9c3-137">The NapAgent queries the SoH-Response data blob from the connection object, processes it, and sets the resulting decision (eg.</span></span> <span data-ttu-id="8f9c3-138">acesso completo/restrito/etc.) no objeto de conexão.</span><span class="sxs-lookup"><span data-stu-id="8f9c3-138">full/restricted access/etc) on the connection object.</span></span>

<span data-ttu-id="8f9c3-139">O cliente de imposição deve chamar o método [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) antes de chamar este ou qualquer outro método da interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="8f9c3-139">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f9c3-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f9c3-140">Requirements</span></span>



| <span data-ttu-id="8f9c3-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f9c3-141">Requirement</span></span> | <span data-ttu-id="8f9c3-142">Valor</span><span class="sxs-lookup"><span data-stu-id="8f9c3-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f9c3-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f9c3-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8f9c3-144">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8f9c3-144">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8f9c3-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f9c3-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8f9c3-146">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8f9c3-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8f9c3-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8f9c3-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f9c3-148"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f9c3-148"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="8f9c3-149">INSERI</span><span class="sxs-lookup"><span data-stu-id="8f9c3-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8f9c3-150"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8f9c3-150"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="8f9c3-151">DLL</span><span class="sxs-lookup"><span data-stu-id="8f9c3-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f9c3-152"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f9c3-152"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="8f9c3-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f9c3-153">See also</span></span>

<dl> <span data-ttu-id="8f9c3-154"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="8f9c3-154"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="8f9c3-155">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="8f9c3-155">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="8f9c3-156">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="8f9c3-156">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





