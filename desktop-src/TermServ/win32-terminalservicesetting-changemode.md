---
title: Método altermode da classe Win32_TerminalServiceSetting
description: O método Altermode define o tipo de licenciamento do servidor atual de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: 293483ee-51ce-4cd4-ba13-6c7c02bbdbbf
ms.tgt_platform: multiple
keywords:
- Método altermode Serviços de Área de Trabalho Remota
- Método altermode Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método ChangeMode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.ChangeMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880fcab8aa68e49c6b3c00278b90635686de6168
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369560"
---
# <a name="changemode-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="fe469-106">Método altermode da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="fe469-106">ChangeMode method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="fe469-107">O método **altermode** define o tipo de licenciamento do servidor atual de Host da Sessão da Área de Trabalho Remota (host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="fe469-107">The **ChangeMode** method sets the licensing type of the current Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe469-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe469-108">Syntax</span></span>


```mof
uint32 ChangeMode(
  [in] uint32 LicensingType
);
```



## <a name="parameters"></a><span data-ttu-id="fe469-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe469-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe469-110">*Licenciamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fe469-110">*LicensingType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe469-111">O tipo de licenciamento a ser definido com base no modo de servidor Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="fe469-111">The licensing type to set based on the RD Session Host server mode.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="fe469-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="fe469-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="fe469-113">Servidor de Host da Sessão RD pessoal.</span><span class="sxs-lookup"><span data-stu-id="fe469-113">Personal RD Session Host server.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="fe469-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="fe469-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="fe469-115">Área de trabalho remota para administração.</span><span class="sxs-lookup"><span data-stu-id="fe469-115">Remote desktop for administration.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="fe469-116"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="fe469-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="fe469-117">Por dispositivo/por estação.</span><span class="sxs-lookup"><span data-stu-id="fe469-117">Per device/per seat.</span></span> <span data-ttu-id="fe469-118">Válido para servidores de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="fe469-118">Valid for application servers.</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="fe469-119"><span id="4"></span>**quatro**</span><span class="sxs-lookup"><span data-stu-id="fe469-119"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="fe469-120">Por Usuário.</span><span class="sxs-lookup"><span data-stu-id="fe469-120">Per User.</span></span> <span data-ttu-id="fe469-121">Válido para servidores de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="fe469-121">Valid for application servers.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe469-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fe469-122">Return value</span></span>

<span data-ttu-id="fe469-123">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="fe469-123">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="fe469-124">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="fe469-124">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe469-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe469-125">Remarks</span></span>

<span data-ttu-id="fe469-126">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="fe469-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fe469-127">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fe469-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fe469-128">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="fe469-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fe469-129">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fe469-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe469-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe469-130">Requirements</span></span>



| <span data-ttu-id="fe469-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe469-131">Requirement</span></span> | <span data-ttu-id="fe469-132">Valor</span><span class="sxs-lookup"><span data-stu-id="fe469-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe469-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe469-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fe469-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe469-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fe469-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe469-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fe469-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe469-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fe469-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="fe469-137">Namespace</span></span><br/>                | <span data-ttu-id="fe469-138">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="fe469-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="fe469-139">MOF</span><span class="sxs-lookup"><span data-stu-id="fe469-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe469-140"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe469-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe469-141">DLL</span><span class="sxs-lookup"><span data-stu-id="fe469-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe469-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe469-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe469-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe469-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe469-144">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="fe469-144">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

