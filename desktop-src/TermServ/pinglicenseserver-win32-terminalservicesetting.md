---
title: Método PingLicenseServer da classe Win32_TerminalServiceSetting
description: O PingLicenseServer não está mais disponível.
ms.assetid: d2a9f273-1ff9-4391-889b-a3b9c9f95c3b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método PingLicenseServer
- Método PingLicenseServer Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método PingLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.PingLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fe7277b3130c88c1aec7716c1a3bf560b81db64
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369574"
---
# <a name="pinglicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="49edc-106">Método PingLicenseServer da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="49edc-106">PingLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="49edc-107">\[O **PingLicenseServer** não está mais disponível para uso a partir do Windows Server 2008 R2.\]</span><span class="sxs-lookup"><span data-stu-id="49edc-107">\[**PingLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="49edc-108">**Windows Server 2008:** Executa ping no servidor de licença para determinar se ele é um servidor de licença válido.</span><span class="sxs-lookup"><span data-stu-id="49edc-108">**Windows Server 2008:** Pings the license server to determine if it is a valid license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="49edc-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49edc-109">Syntax</span></span>


```mof
uint32 PingLicenseServer(
  [in] string ServerName
);
```



## <a name="parameters"></a><span data-ttu-id="49edc-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49edc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49edc-111">*Nome do Server* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="49edc-111">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49edc-112">Nome do servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="49edc-112">Name of the license server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49edc-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="49edc-113">Return value</span></span>

<dl> <dt>

<span data-ttu-id="49edc-114">**S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="49edc-114">**S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="49edc-115">O servidor é um servidor de licença válido.</span><span class="sxs-lookup"><span data-stu-id="49edc-115">The server is a valid license server.</span></span>

</dd> <dt>

<span data-ttu-id="49edc-116">**\_falso**</span><span class="sxs-lookup"><span data-stu-id="49edc-116">**S\_FALSE**</span></span>
</dt> <dd>

<span data-ttu-id="49edc-117">O servidor de licença não é válido.</span><span class="sxs-lookup"><span data-stu-id="49edc-117">The license server is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49edc-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="49edc-118">Remarks</span></span>

<span data-ttu-id="49edc-119">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="49edc-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="49edc-120">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="49edc-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="49edc-121">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="49edc-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="49edc-122">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="49edc-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="49edc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49edc-123">Requirements</span></span>



| <span data-ttu-id="49edc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="49edc-124">Requirement</span></span> | <span data-ttu-id="49edc-125">Valor</span><span class="sxs-lookup"><span data-stu-id="49edc-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49edc-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49edc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="49edc-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="49edc-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="49edc-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49edc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="49edc-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49edc-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49edc-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="49edc-130">End of client support</span></span><br/>    | <span data-ttu-id="49edc-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="49edc-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="49edc-132">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="49edc-132">End of server support</span></span><br/>    | <span data-ttu-id="49edc-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49edc-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49edc-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="49edc-134">Namespace</span></span><br/>                | <span data-ttu-id="49edc-135">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="49edc-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="49edc-136">MOF</span><span class="sxs-lookup"><span data-stu-id="49edc-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49edc-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="49edc-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="49edc-138">DLL</span><span class="sxs-lookup"><span data-stu-id="49edc-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49edc-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49edc-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49edc-140">Consulte também</span><span class="sxs-lookup"><span data-stu-id="49edc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49edc-141">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="49edc-141">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

