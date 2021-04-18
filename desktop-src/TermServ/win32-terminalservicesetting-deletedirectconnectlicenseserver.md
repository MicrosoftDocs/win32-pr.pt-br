---
title: Método DeleteDirectConnectLicenseServer da classe Win32_TerminalServiceSetting
description: O DeleteDirectConnectLicenseServer não está mais disponível.
ms.assetid: 190316ab-b8ed-4102-8346-42603d6451e6
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método DeleteDirectConnectLicenseServer
- Método DeleteDirectConnectLicenseServer Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método DeleteDirectConnectLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.DeleteDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1929ee4294040e80ec9bb633bd70d4709b3e56b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105800000"
---
# <a name="deletedirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="eef24-106">Método DeleteDirectConnectLicenseServer da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="eef24-106">DeleteDirectConnectLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="eef24-107">\[O **DeleteDirectConnectLicenseServer** não está mais disponível para uso a partir do Windows Server 2008 R2.\]</span><span class="sxs-lookup"><span data-stu-id="eef24-107">\[**DeleteDirectConnectLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="eef24-108">**Windows Server 2008:** Remove um servidor de licença do registro.</span><span class="sxs-lookup"><span data-stu-id="eef24-108">**Windows Server 2008:** Removes a license server from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="eef24-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eef24-109">Syntax</span></span>


```mof
uint32 DeleteDirectConnectLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="eef24-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eef24-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eef24-111">*LicenseServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eef24-111">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eef24-112">Nome do servidor de licença a ser removido.</span><span class="sxs-lookup"><span data-stu-id="eef24-112">Name of the license server to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eef24-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eef24-113">Return value</span></span>

<span data-ttu-id="eef24-114">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="eef24-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="eef24-115">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="eef24-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="eef24-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="eef24-116">Remarks</span></span>

<span data-ttu-id="eef24-117">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="eef24-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="eef24-118">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="eef24-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="eef24-119">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="eef24-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="eef24-120">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="eef24-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="eef24-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eef24-121">Requirements</span></span>



| <span data-ttu-id="eef24-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="eef24-122">Requirement</span></span> | <span data-ttu-id="eef24-123">Valor</span><span class="sxs-lookup"><span data-stu-id="eef24-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eef24-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eef24-124">Minimum supported client</span></span><br/> | <span data-ttu-id="eef24-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="eef24-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="eef24-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eef24-126">Minimum supported server</span></span><br/> | <span data-ttu-id="eef24-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eef24-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eef24-128">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="eef24-128">End of client support</span></span><br/>    | <span data-ttu-id="eef24-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="eef24-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="eef24-130">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="eef24-130">End of server support</span></span><br/>    | <span data-ttu-id="eef24-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eef24-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eef24-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="eef24-132">Namespace</span></span><br/>                | <span data-ttu-id="eef24-133">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="eef24-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="eef24-134">MOF</span><span class="sxs-lookup"><span data-stu-id="eef24-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eef24-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eef24-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="eef24-136">DLL</span><span class="sxs-lookup"><span data-stu-id="eef24-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eef24-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eef24-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eef24-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="eef24-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eef24-139">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="eef24-139">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

