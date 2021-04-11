---
title: Interface INapEnforcementClientConnection (NapEnforcementClient. h)
description: Permitir o gerenciamento de conexão do cliente. | Interface INapEnforcementClientConnection (NapEnforcementClient. h)
ms.assetid: 96b94995-24b8-47ed-880e-6182d1bfe925
keywords:
- INapEnforcementClientConnection da interface NAP
- INapEnforcementClientConnection interface NAP, descrita
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5f132da021e7970ec2f15a872091c101cd5c42
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172672"
---
# <a name="inapenforcementclientconnection-interface"></a><span data-ttu-id="cbba2-106">Interface INapEnforcementClientConnection</span><span class="sxs-lookup"><span data-stu-id="cbba2-106">INapEnforcementClientConnection interface</span></span>

> [!Note]  
> <span data-ttu-id="cbba2-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="cbba2-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="cbba2-108">O **INapEnforcementClientConnection** fornece métodos que permitem o gerenciamento de conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="cbba2-108">The **INapEnforcementClientConnection** provides methods that allow for client connection management.</span></span>

> [!Note]  
> <span data-ttu-id="cbba2-109">[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) herda todos os métodos dessa interface e deve ser usado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="cbba2-109">[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="cbba2-110">Membros</span><span class="sxs-lookup"><span data-stu-id="cbba2-110">Members</span></span>

<span data-ttu-id="cbba2-111">A interface **INapEnforcementClientConnection** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cbba2-111">The **INapEnforcementClientConnection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cbba2-112">**INapEnforcementClientConnection** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cbba2-112">**INapEnforcementClientConnection** also has these types of members:</span></span>

-   [<span data-ttu-id="cbba2-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="cbba2-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cbba2-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="cbba2-114">Methods</span></span>

<span data-ttu-id="cbba2-115">A interface **INapEnforcementClientConnection** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="cbba2-115">The **INapEnforcementClientConnection** interface has these methods.</span></span>



| <span data-ttu-id="cbba2-116">Método</span><span class="sxs-lookup"><span data-stu-id="cbba2-116">Method</span></span>                                                                                                                           | <span data-ttu-id="cbba2-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="cbba2-117">Description</span></span>                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbba2-118">**INapEnforcementClientConnection:: GetConnectionID**</span><span class="sxs-lookup"><span data-stu-id="cbba2-118">**INapEnforcementClientConnection::GetConnectionId**</span></span>](inapenforcementclientconnection-getconnectionid-method.md)               | <span data-ttu-id="cbba2-119">Obtém a ID de conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="cbba2-119">Gets the connection ID of the client.</span></span><br/>                                                                                          |
| [<span data-ttu-id="cbba2-120">**INapEnforcementClientConnection:: CorrelationId**</span><span class="sxs-lookup"><span data-stu-id="cbba2-120">**INapEnforcementClientConnection::GetCorrelationId**</span></span>](inapenforcementclientconnection-getcorrelationid-method.md)             | <span data-ttu-id="cbba2-121">Obtém a ID usada para correlacionar SoH-solicitações e as respostas SoH.</span><span class="sxs-lookup"><span data-stu-id="cbba2-121">Gets the ID used to correlate SoH-requests and SoH-responses.</span></span><br/>                                                                  |
| [<span data-ttu-id="cbba2-122">**INapEnforcementClientConnection::GetEnforcerPrivateData**</span><span class="sxs-lookup"><span data-stu-id="cbba2-122">**INapEnforcementClientConnection::GetEnforcerPrivateData**</span></span>](inapenforcementclientconnection-getenforcerprivatedata-method.md) | <span data-ttu-id="cbba2-123">Usado pelo imforcer para obter dados privados.</span><span class="sxs-lookup"><span data-stu-id="cbba2-123">Used by the enforcer to get private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="cbba2-124">**INapEnforcementClientConnection:: GetFlags**</span><span class="sxs-lookup"><span data-stu-id="cbba2-124">**INapEnforcementClientConnection::GetFlags**</span></span>](inapenforcementclientconnection-getflags-method.md)                             | <span data-ttu-id="cbba2-125">Obtém o valor do sinalizador que diferencia respostas de primeira vez de respostas devido a SoHRequests armazenados em cache pelos imforçadores.</span><span class="sxs-lookup"><span data-stu-id="cbba2-125">Gets the value of the flag that differentiates first-time responses from responses due to SoHRequests cached by the enforcers.</span></span><br/> |
| [<span data-ttu-id="cbba2-126">**INapEnforcementClientConnection::GetIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="cbba2-126">**INapEnforcementClientConnection::GetIsolationInfo**</span></span>](inapenforcementclientconnection-getisolationinfo-method.md)             | <span data-ttu-id="cbba2-127">Usado obtenha as informações de isolamento do cliente.</span><span class="sxs-lookup"><span data-stu-id="cbba2-127">Used get the isolation information of the client.</span></span><br/>                                                                              |
| [<span data-ttu-id="cbba2-128">**INapEnforcementClientConnection:: getmaxsize**</span><span class="sxs-lookup"><span data-stu-id="cbba2-128">**INapEnforcementClientConnection::GetMaxSize**</span></span>](inapenforcementclientconnection-getmaxsize-method.md)                         | <span data-ttu-id="cbba2-129">Obtém o tamanho máximo do pacote SoH para este cliente.</span><span class="sxs-lookup"><span data-stu-id="cbba2-129">Gets the maximum size of the SoH packet for this client.</span></span><br/>                                                                       |
| [<span data-ttu-id="cbba2-130">**INapEnforcementClientConnection::GetPrivateData**</span><span class="sxs-lookup"><span data-stu-id="cbba2-130">**INapEnforcementClientConnection::GetPrivateData**</span></span>](inapenforcementclientconnection-getprivatedata-method.md)                 | <span data-ttu-id="cbba2-131">Usado pelo NapAgent para obter dados privados.</span><span class="sxs-lookup"><span data-stu-id="cbba2-131">Used by the NapAgent to get private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="cbba2-132">**INapEnforcementClientConnection::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="cbba2-132">**INapEnforcementClientConnection::GetSoHRequest**</span></span>](inapenforcementclientconnection-getsohrequest-method.md)                   | <span data-ttu-id="cbba2-133">Obtém a solicitação SoH.</span><span class="sxs-lookup"><span data-stu-id="cbba2-133">Gets the SoH Request.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="cbba2-134">**INapEnforcementClientConnection::GetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="cbba2-134">**INapEnforcementClientConnection::GetSoHResponse**</span></span>](inapenforcementclientconnection-getsohresponse-method.md)                 | <span data-ttu-id="cbba2-135">Obtém o SoH-Response recebido pelo cliente de imposição.</span><span class="sxs-lookup"><span data-stu-id="cbba2-135">Gets the SoH-Response received by the enforcement client.</span></span><br/>                                                                      |
| [<span data-ttu-id="cbba2-136">**INapEnforcementClientConnection::GetStringCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="cbba2-136">**INapEnforcementClientConnection::GetStringCorrelationId**</span></span>](inapenforcementclientconnection-getstringcorrelationid-method.md) | <span data-ttu-id="cbba2-137">Obtém a versão da cadeia de caracteres da CorrelationId.</span><span class="sxs-lookup"><span data-stu-id="cbba2-137">Gets the string version of the CorrelationId.</span></span> <span data-ttu-id="cbba2-138">Usado principalmente para fins de log.</span><span class="sxs-lookup"><span data-stu-id="cbba2-138">Used primarily for logging purposes.</span></span><br/>                                             |
| [<span data-ttu-id="cbba2-139">**INapEnforcementClientConnection:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="cbba2-139">**INapEnforcementClientConnection::Initialize**</span></span>](inapenforcementclientconnection-initialize-method.md)                         | <span data-ttu-id="cbba2-140">Inicializa a conexão.</span><span class="sxs-lookup"><span data-stu-id="cbba2-140">Initializes the connection.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="cbba2-141">**INapEnforcementClientConnection:: setconnectionid**</span><span class="sxs-lookup"><span data-stu-id="cbba2-141">**INapEnforcementClientConnection::SetConnectionId**</span></span>](inapenforcementclientconnection-setconnectionid-method.md)               | <span data-ttu-id="cbba2-142">Define a ID de conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="cbba2-142">Sets the connection ID of the client.</span></span><br/>                                                                                          |
| [<span data-ttu-id="cbba2-143">**INapEnforcementClientConnection:: CorrelationId**</span><span class="sxs-lookup"><span data-stu-id="cbba2-143">**INapEnforcementClientConnection::SetCorrelationId**</span></span>](inapenforcementclientconnection-setcorrelationid-method.md)             | <span data-ttu-id="cbba2-144">Define a ID usada para correlacionar SoH-solicitações e as respostas SoH.</span><span class="sxs-lookup"><span data-stu-id="cbba2-144">Sets the ID used to correlate SoH-requests and SoH-responses.</span></span><br/>                                                                  |
| [<span data-ttu-id="cbba2-145">**INapEnforcementClientConnection::SetEnforcerPrivateData**</span><span class="sxs-lookup"><span data-stu-id="cbba2-145">**INapEnforcementClientConnection::SetEnforcerPrivateData**</span></span>](inapenforcementclientconnection-setenforcerprivatedata-method.md) | <span data-ttu-id="cbba2-146">Usado pelo imforcer para definir dados privados.</span><span class="sxs-lookup"><span data-stu-id="cbba2-146">Used by the enforcer to set private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="cbba2-147">**INapEnforcementClientConnection:: SetFlags**</span><span class="sxs-lookup"><span data-stu-id="cbba2-147">**INapEnforcementClientConnection::SetFlags**</span></span>](inapenforcementclientconnection-setflags-method.md)                             | <span data-ttu-id="cbba2-148">Define o sinalizador que diferencia respostas de primeira vez de respostas devido ao SoHRequests armazenado em cache por imforcers.</span><span class="sxs-lookup"><span data-stu-id="cbba2-148">Sets the flag that differentiates first-time responses from responses due to SoHRequests cached by enforcers.</span></span><br/>                  |
| [<span data-ttu-id="cbba2-149">**INapEnforcementClientConnection::SetIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="cbba2-149">**INapEnforcementClientConnection::SetIsolationInfo**</span></span>](inapenforcementclientconnection-setisolationinfo-method.md)             | <span data-ttu-id="cbba2-150">Usado pelo NapAgent para definir as informações de isolamento do cliente.</span><span class="sxs-lookup"><span data-stu-id="cbba2-150">Used by the NapAgent to set the isolation information of the client.</span></span><br/>                                                           |
| [<span data-ttu-id="cbba2-151">**INapEnforcementClientConnection:: setmaxsize**</span><span class="sxs-lookup"><span data-stu-id="cbba2-151">**INapEnforcementClientConnection::SetMaxSize**</span></span>](inapenforcementclientconnection-setmaxsize-method.md)                         | <span data-ttu-id="cbba2-152">Define o tamanho máximo do pacote SoH para esse cliente.</span><span class="sxs-lookup"><span data-stu-id="cbba2-152">Sets the maximum size of the SoH packet for this client.</span></span><br/>                                                                       |
| [<span data-ttu-id="cbba2-153">**INapEnforcementClientConnection::SetPrivateData**</span><span class="sxs-lookup"><span data-stu-id="cbba2-153">**INapEnforcementClientConnection::SetPrivateData**</span></span>](inapenforcementclientconnection-setprivatedata-method.md)                 | <span data-ttu-id="cbba2-154">Usado pelo NapAgent para definir dados privados.</span><span class="sxs-lookup"><span data-stu-id="cbba2-154">Used by the NapAgent to set private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="cbba2-155">**INapEnforcementClientConnection::SetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="cbba2-155">**INapEnforcementClientConnection::SetSoHRequest**</span></span>](inapenforcementclientconnection-setsohrequest-method.md)                   | <span data-ttu-id="cbba2-156">Define a solicitação SoH.</span><span class="sxs-lookup"><span data-stu-id="cbba2-156">Sets the SoH Request.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="cbba2-157">**INapEnforcementClientConnection::SetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="cbba2-157">**INapEnforcementClientConnection::SetSoHResponse**</span></span>](inapenforcementclientconnection-setsohresponse-method.md)                 | <span data-ttu-id="cbba2-158">Define o SoH-Response e é usado pelo cliente de imposição no recebimento de um pacote.</span><span class="sxs-lookup"><span data-stu-id="cbba2-158">Sets the SoH-Response and is used by the enforcement client on receiving a packet.</span></span><br/>                                             |



 

## <a name="requirements"></a><span data-ttu-id="cbba2-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbba2-159">Requirements</span></span>



| <span data-ttu-id="cbba2-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbba2-160">Requirement</span></span> | <span data-ttu-id="cbba2-161">Valor</span><span class="sxs-lookup"><span data-stu-id="cbba2-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbba2-162">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbba2-162">Minimum supported client</span></span><br/> | <span data-ttu-id="cbba2-163">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cbba2-163">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cbba2-164">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbba2-164">Minimum supported server</span></span><br/> | <span data-ttu-id="cbba2-165">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cbba2-165">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cbba2-166">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cbba2-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbba2-167"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbba2-167"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="cbba2-168">INSERI</span><span class="sxs-lookup"><span data-stu-id="cbba2-168">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cbba2-169"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cbba2-169"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="cbba2-170">DLL</span><span class="sxs-lookup"><span data-stu-id="cbba2-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbba2-171"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbba2-171"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="cbba2-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbba2-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbba2-173">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="cbba2-173">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="cbba2-174">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="cbba2-174">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

