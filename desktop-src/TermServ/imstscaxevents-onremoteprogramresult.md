---
title: Método IMsTscAxEvents OnRemoteProgramResult
description: Chamado quando um programa do RemoteApp retorna um resultado para o controle de cliente.
ms.assetid: 5bc9570f-14fb-4b6f-a7dd-c1bce3ef19e0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnRemoteProgramResult
- Método OnRemoteProgramResult Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnRemoteProgramResult
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramResult
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880e4fb3f6453114415f5bcc07a0afb9c176a1bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085767"
---
# <a name="imstscaxeventsonremoteprogramresult-method"></a><span data-ttu-id="be127-106">Método IMsTscAxEvents:: OnRemoteProgramResult</span><span class="sxs-lookup"><span data-stu-id="be127-106">IMsTscAxEvents::OnRemoteProgramResult method</span></span>

<span data-ttu-id="be127-107">Chamado quando um programa do RemoteApp retorna um resultado para o controle de cliente.</span><span class="sxs-lookup"><span data-stu-id="be127-107">Called when a RemoteApp program returns a result to the client control.</span></span>

## <a name="syntax"></a><span data-ttu-id="be127-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be127-108">Syntax</span></span>


```C++
VOID OnRemoteProgramResult(
  [in] BSTR                bstrRemoteProgram,
  [in] RemoteProgramResult lError,
  [in] VARIANT_BOOL        vbIsExecutable
);
```



## <a name="parameters"></a><span data-ttu-id="be127-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be127-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be127-110">*bstrRemoteProgram* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="be127-110">*bstrRemoteProgram* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be127-111">O nome do programa RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="be127-111">The name of the RemoteApp program.</span></span>

</dd> <dt>

<span data-ttu-id="be127-112">*lError* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="be127-112">*lError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be127-113">O resultado da tentativa de iniciar o programa RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="be127-113">The result of the attempt to launch the RemoteApp program.</span></span>

<dt>

<span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>

<span data-ttu-id="be127-114"><span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>**remoteAppResultOk** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="be127-114"><span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>**remoteAppResultOk** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="be127-115">O programa do RemoteApp foi iniciado com êxito.</span><span class="sxs-lookup"><span data-stu-id="be127-115">The RemoteApp program launched successfully.</span></span>

</dd> <dt>

<span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>

<span data-ttu-id="be127-116"><span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>**remoteAppResultLocked** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="be127-116"><span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>**remoteAppResultLocked** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="be127-117">A sessão remota está bloqueada e o programa RemoteApp não pode ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="be127-117">The remote session is locked and the RemoteApp program cannot be launched.</span></span> <span data-ttu-id="be127-118">O usuário deve inserir suas credenciais para desbloquear a sessão e, em seguida, iniciar o programa RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="be127-118">The user must enter their credentials to unlock the session, and then launch the RemoteApp program.</span></span>

</dd> <dt>

<span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>

<span data-ttu-id="be127-119"><span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>**remoteAppResultProtocolError** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="be127-119"><span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>**remoteAppResultProtocolError** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="be127-120">O programa RemoteApp retornou um erro de protocolo.</span><span class="sxs-lookup"><span data-stu-id="be127-120">The RemoteApp program returned a protocol error.</span></span>

</dd> <dt>

<span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>

<span data-ttu-id="be127-121"><span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>**remoteAppResultNotInWhitelist** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="be127-121"><span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>**remoteAppResultNotInWhitelist** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="be127-122">O programa RemoteApp não está na lista aprovada do servidor de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="be127-122">The RemoteApp program is not in the approved list of the RD Session Host server.</span></span>

</dd> <dt>

<span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>

<span data-ttu-id="be127-123"><span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>**remoteAppResultNetworkPathDenied** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="be127-123"><span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>**remoteAppResultNetworkPathDenied** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="be127-124">O caminho de rede para o programa RemoteApp foi negado.</span><span class="sxs-lookup"><span data-stu-id="be127-124">The network path to the RemoteApp program was denied.</span></span>

</dd> <dt>

<span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>

<span data-ttu-id="be127-125"><span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>**remoteAppResultFileNotFound** (5 (0x5))</span><span class="sxs-lookup"><span data-stu-id="be127-125"><span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>**remoteAppResultFileNotFound** (5 (0x5))</span></span>


</dt> <dd>

<span data-ttu-id="be127-126">O arquivo de programa do RemoteApp não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="be127-126">The RemoteApp program file was not found.</span></span>

</dd> <dt>

<span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>

<span data-ttu-id="be127-127"><span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>**remoteAppResultFailure** (6 (0x6))</span><span class="sxs-lookup"><span data-stu-id="be127-127"><span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>**remoteAppResultFailure** (6 (0x6))</span></span>


</dt> <dd>

<span data-ttu-id="be127-128">Falha ao iniciar o programa RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="be127-128">The RemoteApp program failed to launch.</span></span>

</dd> <dt>

<span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>

<span data-ttu-id="be127-129"><span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>**remoteAppResultHookNotLoaded** (7 (0x7))</span><span class="sxs-lookup"><span data-stu-id="be127-129"><span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>**remoteAppResultHookNotLoaded** (7 (0x7))</span></span>


</dt> <dd>

<span data-ttu-id="be127-130">O programa RemoteApp não pode ser iniciado porque a sessão está exibindo a área de trabalho segura no momento.</span><span class="sxs-lookup"><span data-stu-id="be127-130">The RemoteApp program cannot be launched because the session is currently displaying the secure desktop.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="be127-131">*vbIsExecutable* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="be127-131">*vbIsExecutable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be127-132">Indica se o programa RemoteApp foi iniciado diretamente, usando o nome do executável ou indiretamente, usando uma associação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="be127-132">Indicates whether the RemoteApp program was launched directly, by using the executable name or indirectly, by using a file association.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be127-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="be127-133">Return value</span></span>

<span data-ttu-id="be127-134">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="be127-134">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be127-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="be127-135">Remarks</span></span>

<span data-ttu-id="be127-136">Implemente esse método em seu coletor de eventos para receber uma notificação de que um programa do RemoteApp retornou um resultado.</span><span class="sxs-lookup"><span data-stu-id="be127-136">Implement this method in your event sink to receive notification that a RemoteApp program returned a result.</span></span>

<span data-ttu-id="be127-137">Esse método é chamado imediatamente depois que o controle ActiveX tenta iniciar o programa RemoteApp e o parâmetro *lError* indica o resultado da tentativa.</span><span class="sxs-lookup"><span data-stu-id="be127-137">This method is called immediately after the ActiveX control attempts to launch the RemoteApp program, and the *lError* parameter indicates the result of the attempt.</span></span>

## <a name="requirements"></a><span data-ttu-id="be127-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be127-138">Requirements</span></span>



| <span data-ttu-id="be127-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="be127-139">Requirement</span></span> | <span data-ttu-id="be127-140">Valor</span><span class="sxs-lookup"><span data-stu-id="be127-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be127-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be127-141">Minimum supported client</span></span><br/> | <span data-ttu-id="be127-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="be127-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="be127-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be127-143">Minimum supported server</span></span><br/> | <span data-ttu-id="be127-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be127-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="be127-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="be127-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="be127-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be127-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="be127-147">DLL</span><span class="sxs-lookup"><span data-stu-id="be127-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be127-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be127-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="be127-149">IID</span><span class="sxs-lookup"><span data-stu-id="be127-149">IID</span></span><br/>                      | <span data-ttu-id="be127-150">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="be127-150">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="be127-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="be127-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be127-152">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="be127-152">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





