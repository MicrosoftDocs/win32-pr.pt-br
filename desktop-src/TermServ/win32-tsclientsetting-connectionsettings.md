---
title: Método ConnectionSettings da classe Win32_TSClientSetting
description: O método ConnectionSettings define as configurações de sessão que se aplicam ao processo de conexão e logon.
ms.assetid: 603807fe-f341-4358-a3b0-0300785cbdb1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ConnectionSettings
- Método ConnectionSettings Serviços de Área de Trabalho Remota, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Serviços de Área de Trabalho Remota, método ConnectionSettings
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.ConnectionSettings
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec255f00656684751b750e92d7a3df8290e3573e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499340"
---
# <a name="connectionsettings-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="9d926-106">Método ConnectionSettings da classe Win32 \_ TSClientSetting</span><span class="sxs-lookup"><span data-stu-id="9d926-106">ConnectionSettings method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="9d926-107">O método **ConnectionSettings** define as configurações de sessão que se aplicam ao processo de conexão e logon.</span><span class="sxs-lookup"><span data-stu-id="9d926-107">The **ConnectionSettings** method sets the session settings that apply to the connection and logon process.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d926-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d926-108">Syntax</span></span>


```mof
uint32 ConnectionSettings(
  [in] uint32 ConnectClientDrivesAtLogon,
  [in] uint32 ConnectPrinterAtLogon,
  [in] uint32 DefaultToClientPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="9d926-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d926-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d926-110">*ConnectClientDrivesAtLogon* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9d926-110">*ConnectClientDrivesAtLogon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d926-111">Sinalizador habilitando ou desabilitando a propriedade **ConnectClientDrivesAtLogon** que especifica se as unidades do cliente são conectadas automaticamente durante o procedimento de logon.</span><span class="sxs-lookup"><span data-stu-id="9d926-111">Flag enabling or disabling the **ConnectClientDrivesAtLogon** property which specifies whether the client's drives are automatically connected during the logon procedure.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="9d926-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="9d926-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="9d926-113">As unidades do cliente não são conectadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="9d926-113">The client's drives are not automatically connected.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="9d926-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="9d926-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="9d926-115">As unidades do cliente são conectadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="9d926-115">The client's drives are automatically connected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9d926-116">*ConnectPrinterAtLogon* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9d926-116">*ConnectPrinterAtLogon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d926-117">Sinalizador habilitando ou desabilitando a propriedade **ConnectPrinterAtLogon** , que especifica se todas as impressoras de cliente locais mapeadas são automaticamente conectadas durante o procedimento de logon.</span><span class="sxs-lookup"><span data-stu-id="9d926-117">Flag enabling or disabling the **ConnectPrinterAtLogon** property, which specifies whether all mapped local client printers are automatically connected during the logon procedure.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="9d926-118"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="9d926-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="9d926-119">Todas as impressoras locais mapeadas não são conectadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="9d926-119">All mapped local printers are not automatically connected.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="9d926-120"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="9d926-120"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="9d926-121">Todas as impressoras locais mapeadas são conectadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="9d926-121">All mapped local printers are automatically connected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9d926-122">*DefaultToClientPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9d926-122">*DefaultToClientPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d926-123">Sinalizador habilitando ou desabilitando a propriedade **DefaultToClientPrinter** que especifica se os trabalhos de impressão são enviados automaticamente para a impressora local do cliente.</span><span class="sxs-lookup"><span data-stu-id="9d926-123">Flag enabling or disabling the **DefaultToClientPrinter** property which specifies whether print jobs are automatically sent to the client's local printer.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="9d926-124"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="9d926-124"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="9d926-125">Os trabalhos de impressão não são enviados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="9d926-125">Print jobs are not automatically sent.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="9d926-126"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="9d926-126"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="9d926-127">Os trabalhos de impressão são enviados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="9d926-127">Print jobs are automatically sent.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d926-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9d926-128">Return value</span></span>

<span data-ttu-id="9d926-129">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="9d926-129">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="9d926-130">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="9d926-130">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="9d926-131">O método retornará um erro se as configurações de conexão do usuário forem substituídas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="9d926-131">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d926-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d926-132">Remarks</span></span>

<span data-ttu-id="9d926-133">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9d926-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9d926-134">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9d926-134">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9d926-135">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="9d926-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9d926-136">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9d926-136">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d926-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d926-137">Requirements</span></span>



| <span data-ttu-id="9d926-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d926-138">Requirement</span></span> | <span data-ttu-id="9d926-139">Valor</span><span class="sxs-lookup"><span data-stu-id="9d926-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d926-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d926-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9d926-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d926-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9d926-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d926-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9d926-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d926-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9d926-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d926-144">Namespace</span></span><br/>                | <span data-ttu-id="9d926-145">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="9d926-145">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9d926-146">MOF</span><span class="sxs-lookup"><span data-stu-id="9d926-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d926-147"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d926-147"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d926-148">DLL</span><span class="sxs-lookup"><span data-stu-id="9d926-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d926-149"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d926-149"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d926-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d926-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d926-151">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="9d926-151">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

