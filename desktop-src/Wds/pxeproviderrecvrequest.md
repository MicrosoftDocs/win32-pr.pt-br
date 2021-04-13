---
title: Função de retorno de chamada PxeProviderRecvRequest
description: Chamado quando uma solicitação é recebida de um cliente.
ms.assetid: 704972d5-177a-490e-881f-d2b3025babda
keywords:
- Função de retorno de chamada do PxeProviderRecvRequest serviços de implantação do Windows
topic_type:
- apiref
api_name:
- PxeProviderRecvRequest
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a173c6ba356d98dfd44beb64033f491b9c200d58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369619"
---
# <a name="pxeproviderrecvrequest-callback-function"></a><span data-ttu-id="ecf7d-104">Função de retorno de chamada PxeProviderRecvRequest</span><span class="sxs-lookup"><span data-stu-id="ecf7d-104">PxeProviderRecvRequest callback function</span></span>

<span data-ttu-id="ecf7d-105">Chamado quando uma solicitação é recebida de um cliente.</span><span class="sxs-lookup"><span data-stu-id="ecf7d-105">Called when a request is received from a client.</span></span> <span data-ttu-id="ecf7d-106">Essa função é registrada chamando a função [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) com o parâmetro *CallbackType* definido como **\_ \_ \_ solicitação de recepção de retorno de chamada PXE**.</span><span class="sxs-lookup"><span data-stu-id="ecf7d-106">This function is registered by calling the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function with the *CallbackType* parameter set to **PXE\_CALLBACK\_RECV\_REQUEST**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecf7d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ecf7d-107">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderRecvRequest(
  _In_  HANDLE          hClientRequest,
  _In_  PVOID           pPacket,
  _In_  ULONG           uPacketLen,
  _In_  PXE_ADDRESS     *pLocalAddress,
  _In_  PXE_ADDRESS     *pRemoteAddress,
  _Out_ PXE_BOOT_ACTION pAction,
  _In_  PVOID           pContext
);
```



## <a name="parameters"></a><span data-ttu-id="ecf7d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ecf7d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecf7d-109">*hClientRequest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ecf7d-109">*hClientRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecf7d-110">Identificador para uma solicitação recebida de um cliente.</span><span class="sxs-lookup"><span data-stu-id="ecf7d-110">Handle to a request received from a client.</span></span>

</dd> <dt>

<span data-ttu-id="ecf7d-111">*pPacket* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ecf7d-111">*pPacket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecf7d-112">Ponteiro para o buffer de memória que contém o pacote recebido.</span><span class="sxs-lookup"><span data-stu-id="ecf7d-112">Pointer to the memory buffer that contains the received packet.</span></span>

</dd> <dt>

<span data-ttu-id="ecf7d-113">*uPacketLen* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ecf7d-113">*uPacketLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecf7d-114">Comprimento, em bytes, do buffer apontado pelo parâmetro *pPacket* .</span><span class="sxs-lookup"><span data-stu-id="ecf7d-114">Length, in bytes, of the buffer pointed to by the *pPacket* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ecf7d-115">*pLocalAddress* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ecf7d-115">*pLocalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecf7d-116">Ponteiro para uma estrutura de [**\_ endereço PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) que contém o endereço local no qual o pacote foi recebido.</span><span class="sxs-lookup"><span data-stu-id="ecf7d-116">Pointer to a [**PXE\_ADDRESS**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) structure that contains the local address on which the packet was received.</span></span>

</dd> <dt>

<span data-ttu-id="ecf7d-117">*pRemoteAddress* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ecf7d-117">*pRemoteAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecf7d-118">Ponteiro para uma estrutura de [**\_ endereço PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) que contém o endereço de origem do pacote.</span><span class="sxs-lookup"><span data-stu-id="ecf7d-118">Pointer to a [**PXE\_ADDRESS**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) structure that contains the source address of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="ecf7d-119">*pAction* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ecf7d-119">*pAction* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ecf7d-120">Especifica a ação que o sistema deve executar.</span><span class="sxs-lookup"><span data-stu-id="ecf7d-120">Specifies the action that the system should take.</span></span>



| <span data-ttu-id="ecf7d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ecf7d-121">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="ecf7d-122">Significado</span><span class="sxs-lookup"><span data-stu-id="ecf7d-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PXE_BA_NBP"></span><span id="pxe_ba_nbp"></span><dl> <span data-ttu-id="ecf7d-123"><dt>**PXE \_ BA \_ NBP**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ecf7d-123"><dt>**PXE\_BA\_NBP**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="ecf7d-124">O provedor respondeu a um cliente com um pacote de resposta DHCP padrão que contém um caminho para o programa de inicialização de rede.</span><span class="sxs-lookup"><span data-stu-id="ecf7d-124">The provider replied to a client with a standard DHCP response packet that contains a path to the Network Boot Program.</span></span> <span data-ttu-id="ecf7d-125">Retornar essa ação significa que o provedor concluiu com êxito a solicitação do cliente chamando a função [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) pelo menos uma vez.</span><span class="sxs-lookup"><span data-stu-id="ecf7d-125">Returning this action means that the provider successfully completed the client request by calling the [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) function at least once.</span></span><br/>                        |
| <span id="PXE_BA_CUSTOM"></span><span id="pxe_ba_custom"></span><dl> <span data-ttu-id="ecf7d-126"><dt>**PXE \_ BA \_ personalizada**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ecf7d-126"><dt>**PXE\_BA\_CUSTOM**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="ecf7d-127">O provedor respondeu a um cliente usando uma resposta personalizada que não está em conformidade com as especificações de DHCP.</span><span class="sxs-lookup"><span data-stu-id="ecf7d-127">The provider replied to a client by using a custom response that does not conform to DHCP specifications.</span></span> <span data-ttu-id="ecf7d-128">Retornar essa ação significa que o provedor concluiu com êxito a solicitação do cliente chamando a função [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) pelo menos uma vez.</span><span class="sxs-lookup"><span data-stu-id="ecf7d-128">Returning this action means that the provider successfully completed the client request by calling the [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) function at least once.</span></span><br/>                                      |
| <span id="PXE_BA_IGNORE"></span><span id="pxe_ba_ignore"></span><dl> <span data-ttu-id="ecf7d-129"><dt>**PXE \_ BA \_ ignorar**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ecf7d-129"><dt>**PXE\_BA\_IGNORE**</dt> <dt>3</dt></span></span> </dl>       | <span data-ttu-id="ecf7d-130">O provedor não deseja atender à solicitação do cliente e a solicitação não deve ser passada para o próximo provedor.</span><span class="sxs-lookup"><span data-stu-id="ecf7d-130">The provider does not want to service the client request and the request should not be passed to the next provider.</span></span> <span data-ttu-id="ecf7d-131">Todos os recursos associados à solicitação do cliente são liberados e a solicitação do cliente é ignorada.</span><span class="sxs-lookup"><span data-stu-id="ecf7d-131">All resources associated with the client request are released and the client request is ignored.</span></span> <span data-ttu-id="ecf7d-132">Os provedores também podem usar esse valor se reconhecerem o cliente, mas a solicitação tiver sido malformada.</span><span class="sxs-lookup"><span data-stu-id="ecf7d-132">Providers can also use this value if they recognize the client but the request was malformed.</span></span><br/> |
| <span id="PXE_BA_REJECTED"></span><span id="pxe_ba_rejected"></span><dl> <span data-ttu-id="ecf7d-133"><dt>**PXE \_ BA \_ rejeitada**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ecf7d-133"><dt>**PXE\_BA\_REJECTED**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="ecf7d-134">O provedor não deseja atender à solicitação do cliente.</span><span class="sxs-lookup"><span data-stu-id="ecf7d-134">The provider does not want to service the client request.</span></span> <span data-ttu-id="ecf7d-135">O sistema passa a solicitação para o próximo provedor na lista de provedores registrados.</span><span class="sxs-lookup"><span data-stu-id="ecf7d-135">The system passes the request to the next provider in the list of registered providers.</span></span> <span data-ttu-id="ecf7d-136">Se esse for o último provedor na lista, todos os recursos associados à solicitação do cliente serão liberados e a solicitação do cliente será ignorada.</span><span class="sxs-lookup"><span data-stu-id="ecf7d-136">If this was the last provider in the list, then all resources associated with the client request are released and client request is ignored.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="ecf7d-137">*pContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ecf7d-137">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecf7d-138">Valor de contexto passado para a função [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="ecf7d-138">Context value passed to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecf7d-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ecf7d-139">Return value</span></span>

<span data-ttu-id="ecf7d-140">Se o provedor tiver processado com êxito a solicitação do cliente, o retorno de chamada deverá retornar o **\_ êxito do erro** e a **\_ \_ ação de inicialização PXE** apontada pelo parâmetro *pAction* conterá a ação de inicialização apropriada para essa solicitação.</span><span class="sxs-lookup"><span data-stu-id="ecf7d-140">If the provider successfully processed the client request, the callback should return **ERROR\_SUCCESS** and the **PXE\_BOOT\_ACTION** pointed to by the *pAction* parameter contains the appropriate boot action for this request.</span></span> <span data-ttu-id="ecf7d-141">Se o provedor processar a solicitação do cliente de forma assíncrona, o retorno de chamada deverá retornar o **erro e \_ /s \_ pendente** e chamar a função [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) quando a solicitação do cliente tiver sido processada.</span><span class="sxs-lookup"><span data-stu-id="ecf7d-141">If the provider will process the client request asynchronously, the callback should return **ERROR\_IO\_PENDING** and call the [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) function when the client request has been processed.</span></span> <span data-ttu-id="ecf7d-142">Em caso de falha, um código de erro apropriado deve ser retornado e o sistema continuará como se a ação de inicialização de **BA do PXE \_ \_ rejeitada** fosse especificada.</span><span class="sxs-lookup"><span data-stu-id="ecf7d-142">In case of failure, an appropriate error code should be returned and the system will proceed as if the **PXE\_BA\_REJECTED** boot action was specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecf7d-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="ecf7d-143">Remarks</span></span>

<span data-ttu-id="ecf7d-144">O tipo de pacotes visto por um provedor pode ser alterado com a função [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) .</span><span class="sxs-lookup"><span data-stu-id="ecf7d-144">The type of packets seen by a provider can be changed with the [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecf7d-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecf7d-145">Requirements</span></span>



| <span data-ttu-id="ecf7d-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecf7d-146">Requirement</span></span> | <span data-ttu-id="ecf7d-147">Valor</span><span class="sxs-lookup"><span data-stu-id="ecf7d-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ecf7d-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ecf7d-148">Minimum supported client</span></span><br/> | <span data-ttu-id="ecf7d-149">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ecf7d-149">None supported</span></span><br/>                                                          |
| <span data-ttu-id="ecf7d-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ecf7d-150">Minimum supported server</span></span><br/> | <span data-ttu-id="ecf7d-151">Windows Server 2008, Windows Server 2003 com aplicativos de área de trabalho do SP2 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="ecf7d-151">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ecf7d-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="ecf7d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecf7d-153">Funções de servidor dos serviços de implantação do Windows</span><span class="sxs-lookup"><span data-stu-id="ecf7d-153">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="ecf7d-154">**PxeRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="ecf7d-154">**PxeRegisterCallback**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> <dt>

[<span data-ttu-id="ecf7d-155">**PxeSendReply**</span><span class="sxs-lookup"><span data-stu-id="ecf7d-155">**PxeSendReply**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)
</dt> <dt>

[<span data-ttu-id="ecf7d-156">**PxeProviderSetAttribute**</span><span class="sxs-lookup"><span data-stu-id="ecf7d-156">**PxeProviderSetAttribute**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)
</dt> </dl>

 

 





