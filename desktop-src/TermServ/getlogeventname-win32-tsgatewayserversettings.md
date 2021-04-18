---
title: Método GetLogEventName da classe Win32_TSGatewayServerSettings
description: Retorna o nome do evento de log para o índice de evento de log especificado.
ms.assetid: ca31ef8e-ab84-4132-a6d2-232b1e69230a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetLogEventName
- Método GetLogEventName Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método GetLogEventName
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetLogEventName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e9c608b7a12d3de48d75ecd5651df94d0267fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105781024"
---
# <a name="getlogeventname-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="b9339-106">Método GetLogEventName da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="b9339-106">GetLogEventName method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="b9339-107">Retorna o nome do evento de log para o índice de evento de log especificado.</span><span class="sxs-lookup"><span data-stu-id="b9339-107">Returns the log event name for the specified log event index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9339-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9339-108">Syntax</span></span>


```mof
uint32 GetLogEventName(
  [in]  uint32 EventIndex,
  [out] string EventName
);
```



## <a name="parameters"></a><span data-ttu-id="b9339-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9339-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9339-110">*EventIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b9339-110">*EventIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9339-111">Índice do evento de log.</span><span class="sxs-lookup"><span data-stu-id="b9339-111">Index of the log event.</span></span> <span data-ttu-id="b9339-112">O valor deve estar entre zero e o valor da propriedade **MaxLogEvents** .</span><span class="sxs-lookup"><span data-stu-id="b9339-112">The value must be between zero and the value of the **MaxLogEvents** property.</span></span>

</dd> <dt>

<span data-ttu-id="b9339-113">*Eventoname* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b9339-113">*EventName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9339-114">Nome do evento especificado.</span><span class="sxs-lookup"><span data-stu-id="b9339-114">Name of the specified event.</span></span> <span data-ttu-id="b9339-115">A lista a seguir exibe os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="b9339-115">The following list displays the possible values.</span></span>

<dt>

<span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>

<span data-ttu-id="b9339-116"><span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>**LogChannelDisconnect**</span><span class="sxs-lookup"><span data-stu-id="b9339-116"><span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>**LogChannelDisconnect**</span></span>


</dt> <dd>

<span data-ttu-id="b9339-117">Usuário desconectado do recurso com êxito.</span><span class="sxs-lookup"><span data-stu-id="b9339-117">User successfully disconnected from the resource.</span></span>

</dd> <dt>

<span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>

<span data-ttu-id="b9339-118"><span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>**LogFailureChannelConnect**</span><span class="sxs-lookup"><span data-stu-id="b9339-118"><span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>**LogFailureChannelConnect**</span></span>


</dt> <dd>

<span data-ttu-id="b9339-119">O usuário não pôde se conectar ao recurso.</span><span class="sxs-lookup"><span data-stu-id="b9339-119">User failed to connect to the resource.</span></span>

</dd> <dt>

<span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>

<span data-ttu-id="b9339-120"><span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>**LogFailureConnectionAuthorizationCheck**</span><span class="sxs-lookup"><span data-stu-id="b9339-120"><span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>**LogFailureConnectionAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="b9339-121">Falha na autorização de conexão do usuário.</span><span class="sxs-lookup"><span data-stu-id="b9339-121">User failed connection authorization.</span></span>

</dd> <dt>

<span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>

<span data-ttu-id="b9339-122"><span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>**LogFailureResourceAuthorizationCheck**</span><span class="sxs-lookup"><span data-stu-id="b9339-122"><span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>**LogFailureResourceAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="b9339-123">Falha na autorização de recursos do usuário.</span><span class="sxs-lookup"><span data-stu-id="b9339-123">User failed resource authorization.</span></span>

</dd> <dt>

<span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>

<span data-ttu-id="b9339-124"><span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>**LogSuccessfulChannelConnect**</span><span class="sxs-lookup"><span data-stu-id="b9339-124"><span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>**LogSuccessfulChannelConnect**</span></span>


</dt> <dd>

<span data-ttu-id="b9339-125">Usuário conectado com êxito ao recurso.</span><span class="sxs-lookup"><span data-stu-id="b9339-125">User successfully connected to the resource.</span></span>

</dd> <dt>

<span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>

<span data-ttu-id="b9339-126"><span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>**LogSuccessfulConnectionAuthorizationCheck**</span><span class="sxs-lookup"><span data-stu-id="b9339-126"><span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>**LogSuccessfulConnectionAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="b9339-127">O usuário passou com êxito na autorização de conexão.</span><span class="sxs-lookup"><span data-stu-id="b9339-127">User successfully passed connection authorization.</span></span>

</dd> <dt>

<span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>

<span data-ttu-id="b9339-128"><span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>**LogSuccessfulResourceAuthorizationCheck**</span><span class="sxs-lookup"><span data-stu-id="b9339-128"><span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>**LogSuccessfulResourceAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="b9339-129">Usuário aprovado com êxito na autorização de recursos.</span><span class="sxs-lookup"><span data-stu-id="b9339-129">User successfully passed resource authorization.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9339-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b9339-130">Return value</span></span>

<span data-ttu-id="b9339-131">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="b9339-131">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b9339-132">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="b9339-132">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b9339-133">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b9339-133">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b9339-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9339-134">Remarks</span></span>

<span data-ttu-id="b9339-135">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="b9339-135">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b9339-136">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b9339-136">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b9339-137">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b9339-137">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b9339-138">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="b9339-138">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b9339-139">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b9339-139">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b9339-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9339-140">Requirements</span></span>



| <span data-ttu-id="b9339-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9339-141">Requirement</span></span> | <span data-ttu-id="b9339-142">Valor</span><span class="sxs-lookup"><span data-stu-id="b9339-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9339-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9339-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b9339-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b9339-144">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b9339-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9339-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b9339-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9339-146">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b9339-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9339-147">Namespace</span></span><br/>                | <span data-ttu-id="b9339-148">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="b9339-148">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b9339-149">MOF</span><span class="sxs-lookup"><span data-stu-id="b9339-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9339-150"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9339-150"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9339-151">DLL</span><span class="sxs-lookup"><span data-stu-id="b9339-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9339-152"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9339-152"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b9339-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9339-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9339-154">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="b9339-154">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="b9339-155">**EnableLogEvent**</span><span class="sxs-lookup"><span data-stu-id="b9339-155">**EnableLogEvent**</span></span>](enablelogevent-win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="b9339-156">**IsLogEventEnabled**</span><span class="sxs-lookup"><span data-stu-id="b9339-156">**IsLogEventEnabled**</span></span>](islogeventenabled-win32-tsgatewayserversettings.md)
</dt> </dl>

 

