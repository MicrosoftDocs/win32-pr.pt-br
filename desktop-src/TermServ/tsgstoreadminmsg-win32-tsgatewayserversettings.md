---
title: Método TSGStoreAdminMsg da classe Win32_TSGatewayServerSettings
description: Atualiza a mensagem administrativa para o servidor de gateway.
ms.assetid: 84e5b967-12fd-47a7-93e4-2550c15c4491
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método TSGStoreAdminMsg
- Método TSGStoreAdminMsg Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método TSGStoreAdminMsg
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGStoreAdminMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 398a027d28970b28b4a1e7db37b5fbfee06e881e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824468"
---
# <a name="tsgstoreadminmsg-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="8949f-106">Método TSGStoreAdminMsg da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="8949f-106">TSGStoreAdminMsg method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="8949f-107">Atualiza a mensagem administrativa para o servidor de gateway.</span><span class="sxs-lookup"><span data-stu-id="8949f-107">Updates the administrative message for the gateway server.</span></span>

## <a name="syntax"></a><span data-ttu-id="8949f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8949f-108">Syntax</span></span>


```mof
uint32 TSGStoreAdminMsg(
  [in] string TSGAdmMsg,
  [in] string MsgStartTime,
  [in] string MsgEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="8949f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8949f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8949f-110">*TSGAdmMsg* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8949f-110">*TSGAdmMsg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8949f-111">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8949f-111">Type: **string**</span></span>

<span data-ttu-id="8949f-112">O texto da mensagem administrativa.</span><span class="sxs-lookup"><span data-stu-id="8949f-112">The administrative message text.</span></span>

</dd> <dt>

<span data-ttu-id="8949f-113">*MsgStartTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8949f-113">*MsgStartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8949f-114">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8949f-114">Type: **string**</span></span>

<span data-ttu-id="8949f-115">A hora de início da mensagem administrativa.</span><span class="sxs-lookup"><span data-stu-id="8949f-115">The administrative message start time.</span></span>

</dd> <dt>

<span data-ttu-id="8949f-116">*MsgEndTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8949f-116">*MsgEndTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8949f-117">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8949f-117">Type: **string**</span></span>

<span data-ttu-id="8949f-118">A hora de término da mensagem administrativa.</span><span class="sxs-lookup"><span data-stu-id="8949f-118">The administrative message end time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8949f-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8949f-119">Return value</span></span>

<span data-ttu-id="8949f-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8949f-120">Type: **uint32**</span></span>

<span data-ttu-id="8949f-121">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="8949f-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8949f-122">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="8949f-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8949f-123">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8949f-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8949f-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="8949f-124">Remarks</span></span>

<span data-ttu-id="8949f-125">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="8949f-125">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="8949f-126">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8949f-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8949f-127">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8949f-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8949f-128">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="8949f-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8949f-129">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8949f-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8949f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8949f-130">Requirements</span></span>



| <span data-ttu-id="8949f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="8949f-131">Requirement</span></span> | <span data-ttu-id="8949f-132">Valor</span><span class="sxs-lookup"><span data-stu-id="8949f-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8949f-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8949f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8949f-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8949f-134">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8949f-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8949f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8949f-136">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8949f-136">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="8949f-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="8949f-137">Namespace</span></span><br/>                | <span data-ttu-id="8949f-138">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="8949f-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="8949f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="8949f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8949f-140"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8949f-140"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="8949f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8949f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8949f-142"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8949f-142"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8949f-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="8949f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8949f-144">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="8949f-144">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

