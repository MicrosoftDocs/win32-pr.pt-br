---
title: Método UpdateDirectConnectLicenseServer da classe Win32_TerminalServiceSetting
description: O UpdateDirectConnectLicenseServer não está mais disponível.
ms.assetid: 0b6e0dba-e23b-4c8d-8021-93d802501359
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método UpdateDirectConnectLicenseServer
- Método UpdateDirectConnectLicenseServer Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método UpdateDirectConnectLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.UpdateDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2249dd00b44955a4e2712b8b7bf746793e89d57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757588"
---
# <a name="updatedirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="eaef7-106">Método UpdateDirectConnectLicenseServer da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="eaef7-106">UpdateDirectConnectLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="eaef7-107">\[O **UpdateDirectConnectLicenseServer** não está mais disponível para uso a partir do Windows Server 2008 R2.\]</span><span class="sxs-lookup"><span data-stu-id="eaef7-107">\[**UpdateDirectConnectLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="eaef7-108">**Windows Server 2008:** Atualiza a lista de servidores de licença de descoberta.</span><span class="sxs-lookup"><span data-stu-id="eaef7-108">**Windows Server 2008:** Updates the list of discovery license servers.</span></span> <span data-ttu-id="eaef7-109">A lista de servidores é delimitada por ponto e vírgula (";").</span><span class="sxs-lookup"><span data-stu-id="eaef7-109">The server list is delimited by semicolons (";").</span></span>

## <a name="syntax"></a><span data-ttu-id="eaef7-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eaef7-110">Syntax</span></span>


```mof
uint32 UpdateDirectConnectLicenseServer(
  [in] string LicenseServerList
);
```



## <a name="parameters"></a><span data-ttu-id="eaef7-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eaef7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaef7-112">*LicenseServerList* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eaef7-112">*LicenseServerList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eaef7-113">Lista de servidores de licença.</span><span class="sxs-lookup"><span data-stu-id="eaef7-113">List of license servers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaef7-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eaef7-114">Return value</span></span>

<span data-ttu-id="eaef7-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="eaef7-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="eaef7-116">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="eaef7-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaef7-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="eaef7-117">Remarks</span></span>

<span data-ttu-id="eaef7-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="eaef7-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="eaef7-119">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="eaef7-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="eaef7-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="eaef7-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="eaef7-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="eaef7-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="eaef7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eaef7-122">Requirements</span></span>



| <span data-ttu-id="eaef7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaef7-123">Requirement</span></span> | <span data-ttu-id="eaef7-124">Valor</span><span class="sxs-lookup"><span data-stu-id="eaef7-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eaef7-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eaef7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="eaef7-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="eaef7-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="eaef7-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eaef7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="eaef7-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eaef7-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eaef7-129">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="eaef7-129">End of client support</span></span><br/>    | <span data-ttu-id="eaef7-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="eaef7-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="eaef7-131">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="eaef7-131">End of server support</span></span><br/>    | <span data-ttu-id="eaef7-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eaef7-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eaef7-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="eaef7-133">Namespace</span></span><br/>                | <span data-ttu-id="eaef7-134">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="eaef7-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="eaef7-135">MOF</span><span class="sxs-lookup"><span data-stu-id="eaef7-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eaef7-136"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eaef7-136"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="eaef7-137">DLL</span><span class="sxs-lookup"><span data-stu-id="eaef7-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaef7-138"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eaef7-138"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaef7-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="eaef7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaef7-140">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="eaef7-140">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

