---
title: Interface INapEnforcementClientBinding (NapEnforcementClient. h)
description: Os clientes de imposição usam o para se comunicar com o NapAgent.
ms.assetid: 73c5c9ad-f213-4d34-9262-996acb570a55
keywords:
- INapEnforcementClientBinding da interface NAP
- INapEnforcementClientBinding interface NAP, descrita
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23db912c08e68adb1411527c90580a5620601752
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824800"
---
# <a name="inapenforcementclientbinding-interface"></a><span data-ttu-id="72b25-105">Interface INapEnforcementClientBinding</span><span class="sxs-lookup"><span data-stu-id="72b25-105">INapEnforcementClientBinding interface</span></span>

> [!Note]  
> <span data-ttu-id="72b25-106">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="72b25-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="72b25-107">O **INapEnforcementClientBinding** fornece métodos que os clientes imposição usam para se comunicar com o NapAgent.</span><span class="sxs-lookup"><span data-stu-id="72b25-107">The **INapEnforcementClientBinding** provides methods that enforcement clients use to communicate with the NapAgent.</span></span>

## <a name="members"></a><span data-ttu-id="72b25-108">Membros</span><span class="sxs-lookup"><span data-stu-id="72b25-108">Members</span></span>

<span data-ttu-id="72b25-109">A interface **INapEnforcementClientBinding** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="72b25-109">The **INapEnforcementClientBinding** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="72b25-110">**INapEnforcementClientBinding** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="72b25-110">**INapEnforcementClientBinding** also has these types of members:</span></span>

-   [<span data-ttu-id="72b25-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="72b25-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="72b25-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="72b25-112">Methods</span></span>

<span data-ttu-id="72b25-113">A interface **INapEnforcementClientBinding** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="72b25-113">The **INapEnforcementClientBinding** interface has these methods.</span></span>



| <span data-ttu-id="72b25-114">Método</span><span class="sxs-lookup"><span data-stu-id="72b25-114">Method</span></span>                                                                                                                           | <span data-ttu-id="72b25-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="72b25-115">Description</span></span>                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72b25-116">**INapEnforcementClientBinding:: CreateConnection**</span><span class="sxs-lookup"><span data-stu-id="72b25-116">**INapEnforcementClientBinding::CreateConnection**</span></span>](inapenforcementclientbinding-createconnection-method.md)                   | <span data-ttu-id="72b25-117">Usado por imforcers para criar objetos de conexão.</span><span class="sxs-lookup"><span data-stu-id="72b25-117">Used by enforcers to create connection objects.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="72b25-118">**INapEnforcementClientBinding::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="72b25-118">**INapEnforcementClientBinding::GetSoHRequest**</span></span>](inapenforcementclientbinding-getsohrequest-method.md)                         | <span data-ttu-id="72b25-119">Usado pelo cliente de imposição quando ele precisa de uma solicitação SoH para uma conexão específica.</span><span class="sxs-lookup"><span data-stu-id="72b25-119">Used by the enforcement client when it needs an SoH-request for a particular connection.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="72b25-120">**INapEnforcementClientBinding:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="72b25-120">**INapEnforcementClientBinding::Initialize**</span></span>](inapenforcementclientbinding-initialize-method.md)                               | <span data-ttu-id="72b25-121">Inicia o serviço NapAgent.</span><span class="sxs-lookup"><span data-stu-id="72b25-121">Starts up the NapAgent service.</span></span> <span data-ttu-id="72b25-122">O cliente de imposição deve chamar esse método antes de chamar qualquer outro método dessa interface.</span><span class="sxs-lookup"><span data-stu-id="72b25-122">The enforcement client must call this method before calling any other method of this interface.</span></span><br/>                                                                            |
| [<span data-ttu-id="72b25-123">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span><span class="sxs-lookup"><span data-stu-id="72b25-123">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span></span>](inapenforcementclientbinding-notifyconnectionstatedown-method.md) | <span data-ttu-id="72b25-124">Usado para informar ao NapAgent que uma conexão com um cliente de imposição foi desativada.</span><span class="sxs-lookup"><span data-stu-id="72b25-124">Used to inform the NapAgent that a connection to an enforcement client has gone down.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="72b25-125">**INapEnforcementClientBinding::NotifySoHChangeFailure**</span><span class="sxs-lookup"><span data-stu-id="72b25-125">**INapEnforcementClientBinding::NotifySoHChangeFailure**</span></span>](inapenforcementclientbinding-notifysohchangefailure-method.md)       | <span data-ttu-id="72b25-126">Usado pelo cliente de imposição para informar ao NapAgent que ele não pôde processar um [**INapEnforcementClientCallback:: NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)anterior.</span><span class="sxs-lookup"><span data-stu-id="72b25-126">Used by the enforcement client to inform the NapAgent that it could not process a previous [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md).</span></span><br/> |
| [<span data-ttu-id="72b25-127">**INapEnforcementClientBinding::P rocessSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="72b25-127">**INapEnforcementClientBinding::ProcessSoHResponse**</span></span>](inapenforcementclientbinding-processsohresponse-method.md)               | <span data-ttu-id="72b25-128">Usado por clientes de imposição sempre que eles recebem um blob de dados de SoH-Response do servidor de imposição.</span><span class="sxs-lookup"><span data-stu-id="72b25-128">Used by enforcement clients whenever they get an SoH-Response data blob from the enforcement server.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="72b25-129">**INapEnforcementClientBinding:: Uninitialize**</span><span class="sxs-lookup"><span data-stu-id="72b25-129">**INapEnforcementClientBinding::Uninitialize**</span></span>](inapenforcementclientbinding-uninitialize-method.md)                           | <span data-ttu-id="72b25-130">Conclui o serviço NapAgent para esta conexão de cliente.</span><span class="sxs-lookup"><span data-stu-id="72b25-130">Concludes the NapAgent service for this client connection.</span></span><br/>                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="72b25-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="72b25-131">Remarks</span></span>

<span data-ttu-id="72b25-132">Todas as APIs nesta interface retornarão RPC \_ E \_ desconectadas se o NapAgent for interrompido.</span><span class="sxs-lookup"><span data-stu-id="72b25-132">All the APIs in this interface will return RPC\_E\_DISCONNECTED if the NapAgent is stopped.</span></span> <span data-ttu-id="72b25-133">Este objeto será recuperado automaticamente e reassociado ao NapAgent, depois que ele for reiniciado.</span><span class="sxs-lookup"><span data-stu-id="72b25-133">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span>

## <a name="requirements"></a><span data-ttu-id="72b25-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72b25-134">Requirements</span></span>



| <span data-ttu-id="72b25-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="72b25-135">Requirement</span></span> | <span data-ttu-id="72b25-136">Valor</span><span class="sxs-lookup"><span data-stu-id="72b25-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72b25-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72b25-137">Minimum supported client</span></span><br/> | <span data-ttu-id="72b25-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="72b25-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="72b25-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72b25-139">Minimum supported server</span></span><br/> | <span data-ttu-id="72b25-140">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="72b25-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="72b25-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72b25-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="72b25-142"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="72b25-142"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="72b25-143">INSERI</span><span class="sxs-lookup"><span data-stu-id="72b25-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="72b25-144"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="72b25-144"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="72b25-145">DLL</span><span class="sxs-lookup"><span data-stu-id="72b25-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72b25-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72b25-146"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="72b25-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="72b25-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72b25-148">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="72b25-148">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="72b25-149">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="72b25-149">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

