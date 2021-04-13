---
title: Método AddDirectConnectLicenseServer da classe Win32_TerminalServiceSetting
description: O AddDirectConnectLicenseServer não está mais disponível.
ms.assetid: 7920fd28-0fa3-4f96-bec3-d9e37c97920c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método AddDirectConnectLicenseServer
- Método AddDirectConnectLicenseServer Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método AddDirectConnectLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.AddDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be9bba23f5c0bfc69b4c8d7951ab38eac6690b84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369865"
---
# <a name="adddirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="3afd2-106">Método AddDirectConnectLicenseServer da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="3afd2-106">AddDirectConnectLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="3afd2-107">\[O **AddDirectConnectLicenseServer** não está mais disponível para uso a partir do Windows Server 2008 R2.\]</span><span class="sxs-lookup"><span data-stu-id="3afd2-107">\[**AddDirectConnectLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="3afd2-108">**Windows Server 2008:** Configura um novo servidor de licença e adiciona o servidor de licença ao registro para descoberta por servidores Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="3afd2-108">**Windows Server 2008:** Configures a new license server and adds the license server to the registry for discovery by Remote Desktop Session Host (RD Session Host) servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="3afd2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3afd2-109">Syntax</span></span>


```mof
uint32 AddDirectConnectLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="3afd2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3afd2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3afd2-111">*LicenseServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3afd2-111">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3afd2-112">Nome do servidor de licença a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="3afd2-112">Name of the license server to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3afd2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3afd2-113">Return value</span></span>

<span data-ttu-id="3afd2-114">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="3afd2-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="3afd2-115">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="3afd2-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3afd2-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3afd2-116">Remarks</span></span>

<span data-ttu-id="3afd2-117">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="3afd2-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3afd2-118">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3afd2-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3afd2-119">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="3afd2-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3afd2-120">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3afd2-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3afd2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3afd2-121">Requirements</span></span>



| <span data-ttu-id="3afd2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3afd2-122">Requirement</span></span> | <span data-ttu-id="3afd2-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3afd2-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3afd2-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3afd2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3afd2-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3afd2-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="3afd2-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3afd2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3afd2-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3afd2-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3afd2-128">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3afd2-128">End of client support</span></span><br/>    | <span data-ttu-id="3afd2-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3afd2-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="3afd2-130">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="3afd2-130">End of server support</span></span><br/>    | <span data-ttu-id="3afd2-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3afd2-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3afd2-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="3afd2-132">Namespace</span></span><br/>                | <span data-ttu-id="3afd2-133">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="3afd2-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="3afd2-134">MOF</span><span class="sxs-lookup"><span data-stu-id="3afd2-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3afd2-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3afd2-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="3afd2-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3afd2-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3afd2-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3afd2-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3afd2-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="3afd2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3afd2-139">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="3afd2-139">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

