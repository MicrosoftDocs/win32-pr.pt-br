---
title: Método IConnectionBrokerClient GetTargetInfo (Cbclient. h)
description: Solicita informações sobre o computador de destino onde a conexão deve ser redirecionada.
ms.assetid: 43970B06-8CBD-4204-94AE-090A63918A90
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetTargetInfo
- Método GetTargetInfo Serviços de Área de Trabalho Remota, interface IConnectionBrokerClient
- Serviços de Área de Trabalho Remota de interface IConnectionBrokerClient, método GetTargetInfo
topic_type:
- apiref
api_name:
- IConnectionBrokerClient.GetTargetInfo
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 366bebf398c5c776e43d5cdee4b99e28e8c580fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499238"
---
# <a name="iconnectionbrokerclientgettargetinfo-method"></a><span data-ttu-id="781d4-106">Método IConnectionBrokerClient:: GetTargetInfo</span><span class="sxs-lookup"><span data-stu-id="781d4-106">IConnectionBrokerClient::GetTargetInfo method</span></span>

<span data-ttu-id="781d4-107">Solicita informações sobre o computador de destino onde a conexão deve ser redirecionada.</span><span class="sxs-lookup"><span data-stu-id="781d4-107">Requests information about the target computer where the connection should be redirected.</span></span> <span data-ttu-id="781d4-108">Esse método é usado pelo redirecionador para obter informações de redirecionamento para a solicitação de conexão de entrada.</span><span class="sxs-lookup"><span data-stu-id="781d4-108">This method is used by the redirector to get redirection information for the incoming connection request.</span></span>

## <a name="syntax"></a><span data-ttu-id="781d4-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="781d4-109">Syntax</span></span>


```C++
HRESULT GetTargetInfo(
  [in]  CB_CONNECTION_INFO       *pConnectionInfo,
  [in]  DWORD                    Reserved,
  [in]  HANDLE                   hStatusEvent,
  [out] CB_TARGET_INFO           *pTargetInfo,
  [out] DWORD                    *pResult,
  [out] IConnectionBrokerRequest **ppCbReq
);
```



## <a name="parameters"></a><span data-ttu-id="781d4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="781d4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="781d4-111">*pConnectionInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="781d4-111">*pConnectionInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="781d4-112">O endereço de uma estrutura de [**\_ \_ informações de conexão CB**](cb-connection-info.md) que contém informações sobre a solicitação de conexão de entrada.</span><span class="sxs-lookup"><span data-stu-id="781d4-112">The address of a [**CB\_CONNECTION\_INFO**](cb-connection-info.md) structure that contains information about the incoming connection request.</span></span>

</dd> <dt>

<span data-ttu-id="781d4-113">*Reservado* \[ para no\]</span><span class="sxs-lookup"><span data-stu-id="781d4-113">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="781d4-114">Esse parâmetro é reservado para uso futuro e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="781d4-114">This parameter is reserved for future use and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="781d4-115">*hStatusEvent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="781d4-115">*hStatusEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="781d4-116">O identificador de um evento que será definido sempre que houver uma atualização do andamento da solicitação.</span><span class="sxs-lookup"><span data-stu-id="781d4-116">The handle of an event that will get set whenever there is an update to the progress of the request.</span></span> <span data-ttu-id="781d4-117">Você é responsável por criar e fechar esse evento.</span><span class="sxs-lookup"><span data-stu-id="781d4-117">You are responsible for creating and closing this event.</span></span>

</dd> <dt>

<span data-ttu-id="781d4-118">*pTargetInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="781d4-118">*pTargetInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="781d4-119">O endereço de uma estrutura de [**\_ \_ informações de destino CB**](cb-target-info.md) que recebe informações sobre o computador de destino em que a conexão de entrada deve ser redirecionada.</span><span class="sxs-lookup"><span data-stu-id="781d4-119">The address of a [**CB\_TARGET\_INFO**](cb-target-info.md) structure that receives information about the target computer where the incoming connection should be redirected.</span></span> <span data-ttu-id="781d4-120">Como esse é um método assíncrono, essa memória deve permanecer disponível até que a solicitação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="781d4-120">Because this is an asynchronous method, this memory must remain available until the request is complete.</span></span> <span data-ttu-id="781d4-121">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="781d4-121">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="781d4-122">*pResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="781d4-122">*pResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="781d4-123">O endereço de uma variável **DWORD** que recebe um código de resultado.</span><span class="sxs-lookup"><span data-stu-id="781d4-123">The address of a **DWORD** variable that receives a result code.</span></span> <span data-ttu-id="781d4-124">Como esse é um método assíncrono, essa memória deve permanecer disponível até que a solicitação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="781d4-124">Because this is an asynchronous method, this memory must remain available until the request is complete.</span></span> <span data-ttu-id="781d4-125">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="781d4-125">For more information, see Remarks.</span></span>

<span data-ttu-id="781d4-126">Esse código de resultado será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="781d4-126">This result code will be one of the following values.</span></span>

<dt>

<span data-ttu-id="781d4-127">0</span><span class="sxs-lookup"><span data-stu-id="781d4-127">0</span></span>
</dt> <dd>

<span data-ttu-id="781d4-128">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="781d4-128">Success.</span></span>

</dd> <dt>

<span data-ttu-id="781d4-129">0x0000400</span><span class="sxs-lookup"><span data-stu-id="781d4-129">0x0000400</span></span>
</dt> <dd>

<span data-ttu-id="781d4-130">O computador de destino não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="781d4-130">The destination computer could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="781d4-131">0x0000401</span><span class="sxs-lookup"><span data-stu-id="781d4-131">0x0000401</span></span>
</dt> <dd>

<span data-ttu-id="781d4-132">O computador de destino não está disponível.</span><span class="sxs-lookup"><span data-stu-id="781d4-132">The destination computer is not available.</span></span>

</dd> <dt>

<span data-ttu-id="781d4-133">0x0000402</span><span class="sxs-lookup"><span data-stu-id="781d4-133">0x0000402</span></span>
</dt> <dd>

<span data-ttu-id="781d4-134">Erro ao carregar o computador de destino.</span><span class="sxs-lookup"><span data-stu-id="781d4-134">Error loading destination computer.</span></span>

</dd> <dt>

<span data-ttu-id="781d4-135">0x0000403</span><span class="sxs-lookup"><span data-stu-id="781d4-135">0x0000403</span></span>
</dt> <dd>

<span data-ttu-id="781d4-136">Erro ao colocar o computador de destino online.</span><span class="sxs-lookup"><span data-stu-id="781d4-136">Error bringing destination computer online.</span></span>

</dd> <dt>

<span data-ttu-id="781d4-137">0x0000404</span><span class="sxs-lookup"><span data-stu-id="781d4-137">0x0000404</span></span>
</dt> <dd>

<span data-ttu-id="781d4-138">Erro ao redirecionar para o computador de destino.</span><span class="sxs-lookup"><span data-stu-id="781d4-138">Error redirecting to destination computer.</span></span>

</dd> <dt>

<span data-ttu-id="781d4-139">0x0000405</span><span class="sxs-lookup"><span data-stu-id="781d4-139">0x0000405</span></span>
</dt> <dd>

<span data-ttu-id="781d4-140">Erro ao ativar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="781d4-140">Error waking virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="781d4-141">0x0000406</span><span class="sxs-lookup"><span data-stu-id="781d4-141">0x0000406</span></span>
</dt> <dd>

<span data-ttu-id="781d4-142">Erro ao inicializar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="781d4-142">Error booting virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="781d4-143">0x0000407</span><span class="sxs-lookup"><span data-stu-id="781d4-143">0x0000407</span></span>
</dt> <dd>

<span data-ttu-id="781d4-144">Erro ao localizar o endereço IP da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="781d4-144">Error finding the IP address of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="781d4-145">0x0000408</span><span class="sxs-lookup"><span data-stu-id="781d4-145">0x0000408</span></span>
</dt> <dd>

<span data-ttu-id="781d4-146">O agente de sessão não pôde localizar nenhum computador disponível no pool.</span><span class="sxs-lookup"><span data-stu-id="781d4-146">The session broker could not find any available computers in the pool.</span></span>

</dd> <dt>

<span data-ttu-id="781d4-147">0x0000409</span><span class="sxs-lookup"><span data-stu-id="781d4-147">0x0000409</span></span>
</dt> <dd>

<span data-ttu-id="781d4-148">O agente de sessão cancelou a conexão.</span><span class="sxs-lookup"><span data-stu-id="781d4-148">The session broker canceled the connection.</span></span>

</dd> <dt>

<span data-ttu-id="781d4-149">0x0000410</span><span class="sxs-lookup"><span data-stu-id="781d4-149">0x0000410</span></span>
</dt> <dd>

<span data-ttu-id="781d4-150">O agente de sessão não pôde validar as configurações de conexão.</span><span class="sxs-lookup"><span data-stu-id="781d4-150">The session broker could not validate the connection settings.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="781d4-151">*ppCbReq* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="781d4-151">*ppCbReq* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="781d4-152">O endereço de um ponteiro de interface [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) que você usa para obter atualizações de status para uma operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="781d4-152">The address of an [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) interface pointer that you use to obtain status updates for an asynchronous operation.</span></span> <span data-ttu-id="781d4-153">Essa interface é usada em conjunto com o parâmetro *hStatusEvent* para aguardar e obter os resultados dessa operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="781d4-153">This interface is used in conjunction with the *hStatusEvent* parameter to wait for and get the results of this asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="781d4-154">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="781d4-154">Return value</span></span>

<span data-ttu-id="781d4-155">Retorna **E \_ pendente** se a solicitação assíncrona for criada.</span><span class="sxs-lookup"><span data-stu-id="781d4-155">Returns **E\_PENDING** if the asynchronous request is created.</span></span> <span data-ttu-id="781d4-156">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="781d4-156">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="781d4-157">Comentários</span><span class="sxs-lookup"><span data-stu-id="781d4-157">Remarks</span></span>

<span data-ttu-id="781d4-158">Esse método é assíncrono.</span><span class="sxs-lookup"><span data-stu-id="781d4-158">This method is asynchronous.</span></span> <span data-ttu-id="781d4-159">Os parâmetros *pTargetInfo* e *pResult* devem permanecer válidos até que o método [**IConnectionBrokerRequest:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) obtenha a **solicitação de status CB \_ \_ \_ concluída**.</span><span class="sxs-lookup"><span data-stu-id="781d4-159">The *pTargetInfo* and *pResult* parameters must remain valid until the [**IConnectionBrokerRequest::CheckStatus**](iconnectionbrokerrequest-checkstatus.md) method obtains **CB\_STATUS\_REQUEST\_COMPLETED**.</span></span>

<span data-ttu-id="781d4-160">Para obter mais informações sobre como usar esse método, consulte [como usar a API de cliente do agente de conexão de área de trabalho remota](use-the-remote-desktop-connection-broker-client-api.md).</span><span class="sxs-lookup"><span data-stu-id="781d4-160">For more information about how to use this method, see [How to use the Remote Desktop Connection Broker client API](use-the-remote-desktop-connection-broker-client-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="781d4-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="781d4-161">Requirements</span></span>



| <span data-ttu-id="781d4-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="781d4-162">Requirement</span></span> | <span data-ttu-id="781d4-163">Valor</span><span class="sxs-lookup"><span data-stu-id="781d4-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="781d4-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="781d4-164">Minimum supported client</span></span><br/> | <span data-ttu-id="781d4-165">Windows 8</span><span class="sxs-lookup"><span data-stu-id="781d4-165">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="781d4-166">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="781d4-166">Minimum supported server</span></span><br/> | <span data-ttu-id="781d4-167">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="781d4-167">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="781d4-168">parâmetro</span><span class="sxs-lookup"><span data-stu-id="781d4-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="781d4-169"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="781d4-169"><dt>Cbclient.h</dt></span></span> </dl>   |
| <span data-ttu-id="781d4-170">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="781d4-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="781d4-171"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="781d4-171"><dt>Cbclient.lib</dt></span></span> </dl> |
| <span data-ttu-id="781d4-172">DLL</span><span class="sxs-lookup"><span data-stu-id="781d4-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="781d4-173"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="781d4-173"><dt>Cbclient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="781d4-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="781d4-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="781d4-175">**IConnectionBrokerClient**</span><span class="sxs-lookup"><span data-stu-id="781d4-175">**IConnectionBrokerClient**</span></span>](iconnectionbrokerclient.md)
</dt> </dl>

 

 





