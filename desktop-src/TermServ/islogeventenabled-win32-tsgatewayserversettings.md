---
title: Método IsLogEventEnabled da classe Win32_TSGatewayServerSettings
description: Indica se o tipo de log de eventos especificado está habilitado.
ms.assetid: 4abfc56f-871a-44ef-9998-da88949a0a2d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método IsLogEventEnabled
- Método IsLogEventEnabled Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método IsLogEventEnabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsLogEventEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acefe60a9ba50c49146d25c7bccddf706f198c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105796297"
---
# <a name="islogeventenabled-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="bd45c-106">Método IsLogEventEnabled da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="bd45c-106">IsLogEventEnabled method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="bd45c-107">Indica se o tipo de log de eventos especificado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="bd45c-107">Indicates whether the specified event log type is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd45c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd45c-108">Syntax</span></span>


```mof
uint32 IsLogEventEnabled(
  [in]  string  EventName,
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="bd45c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd45c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd45c-110">*Eventoname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bd45c-110">*EventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd45c-111">Nome do tipo de log de eventos.</span><span class="sxs-lookup"><span data-stu-id="bd45c-111">Name of the event log type.</span></span> <span data-ttu-id="bd45c-112">Esse valor deve ser recuperado usando o método [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="bd45c-112">This value should be retrieved by using the [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) method.</span></span>

<dt>

<span data-ttu-id="bd45c-113">LogChannelDisconnect</span><span class="sxs-lookup"><span data-stu-id="bd45c-113">LogChannelDisconnect</span></span>
</dt> <dd>

<span data-ttu-id="bd45c-114">Usuário desconectado do recurso com êxito.</span><span class="sxs-lookup"><span data-stu-id="bd45c-114">User successfully disconnected from the resource.</span></span>

</dd> <dt>

<span data-ttu-id="bd45c-115">LogFailedChannelConnect</span><span class="sxs-lookup"><span data-stu-id="bd45c-115">LogFailedChannelConnect</span></span>
</dt> <dd>

<span data-ttu-id="bd45c-116">O usuário não pôde se conectar ao recurso.</span><span class="sxs-lookup"><span data-stu-id="bd45c-116">User failed to connect to the resource.</span></span>

</dd> <dt>

<span data-ttu-id="bd45c-117">LogFailureNetworkAccessCheck</span><span class="sxs-lookup"><span data-stu-id="bd45c-117">LogFailureNetworkAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="bd45c-118">Falha na autorização de conexão do usuário.</span><span class="sxs-lookup"><span data-stu-id="bd45c-118">User failed connection authorization.</span></span>

</dd> <dt>

<span data-ttu-id="bd45c-119">LogFailureResourceAccessCheck</span><span class="sxs-lookup"><span data-stu-id="bd45c-119">LogFailureResourceAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="bd45c-120">Falha na autorização de recursos do usuário.</span><span class="sxs-lookup"><span data-stu-id="bd45c-120">User failed resource authorization.</span></span>

</dd> <dt>

<span data-ttu-id="bd45c-121">LogSuccessChannelConnect</span><span class="sxs-lookup"><span data-stu-id="bd45c-121">LogSuccessChannelConnect</span></span>
</dt> <dd>

<span data-ttu-id="bd45c-122">Usuário conectado com êxito ao recurso.</span><span class="sxs-lookup"><span data-stu-id="bd45c-122">User successfully connected to the resource.</span></span>

</dd> <dt>

<span data-ttu-id="bd45c-123">LogSuccessfulNetworkAccessCheck</span><span class="sxs-lookup"><span data-stu-id="bd45c-123">LogSuccessfulNetworkAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="bd45c-124">O usuário passou com êxito na autorização de conexão.</span><span class="sxs-lookup"><span data-stu-id="bd45c-124">User successfully passed connection authorization.</span></span>

</dd> <dt>

<span data-ttu-id="bd45c-125">LogSuccessfulResourceAccessCheck</span><span class="sxs-lookup"><span data-stu-id="bd45c-125">LogSuccessfulResourceAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="bd45c-126">Usuário aprovado com êxito na autorização de recursos.</span><span class="sxs-lookup"><span data-stu-id="bd45c-126">User successfully passed resource authorization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="bd45c-127">*Habilitado* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bd45c-127">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd45c-128">Indica se o tipo de log de eventos especificado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="bd45c-128">Indicates whether the specified event log type is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd45c-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bd45c-129">Return value</span></span>

<span data-ttu-id="bd45c-130">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="bd45c-130">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="bd45c-131">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="bd45c-131">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="bd45c-132">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bd45c-132">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bd45c-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd45c-133">Remarks</span></span>

<span data-ttu-id="bd45c-134">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="bd45c-134">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="bd45c-135">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="bd45c-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bd45c-136">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bd45c-136">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bd45c-137">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="bd45c-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bd45c-138">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bd45c-138">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd45c-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd45c-139">Requirements</span></span>



| <span data-ttu-id="bd45c-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd45c-140">Requirement</span></span> | <span data-ttu-id="bd45c-141">Valor</span><span class="sxs-lookup"><span data-stu-id="bd45c-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd45c-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd45c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="bd45c-143">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bd45c-143">None supported</span></span><br/>                                                                |
| <span data-ttu-id="bd45c-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd45c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="bd45c-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd45c-145">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bd45c-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="bd45c-146">Namespace</span></span><br/>                | <span data-ttu-id="bd45c-147">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="bd45c-147">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="bd45c-148">MOF</span><span class="sxs-lookup"><span data-stu-id="bd45c-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd45c-149"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd45c-149"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd45c-150">DLL</span><span class="sxs-lookup"><span data-stu-id="bd45c-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd45c-151"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd45c-151"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bd45c-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd45c-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd45c-153">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="bd45c-153">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="bd45c-154">**GetLogEventName**</span><span class="sxs-lookup"><span data-stu-id="bd45c-154">**GetLogEventName**</span></span>](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 

