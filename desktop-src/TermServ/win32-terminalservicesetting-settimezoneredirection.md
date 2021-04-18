---
title: Método SetTimeZoneRedirection da classe Win32_TerminalServiceSetting
description: O método SetTimeZoneRedirection define a propriedade TimeZoneRedirection, que permite que o computador cliente redirecione suas configurações de fuso horário para a sessão de Serviços de Área de Trabalho Remota.
ms.assetid: 4ae149b7-b7de-4530-a142-7253dd1e0d07
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetTimeZoneRedirection
- Método SetTimeZoneRedirection Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método SetTimeZoneRedirection
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetTimeZoneRedirection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2761567c724abf129ac881188bc468b228d7fd11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766940"
---
# <a name="settimezoneredirection-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="38888-106">Método SetTimeZoneRedirection da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="38888-106">SetTimeZoneRedirection method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="38888-107">O método **SetTimeZoneRedirection** define a propriedade **TimeZoneRedirection** , que permite que o computador cliente redirecione suas configurações de fuso horário para a sessão de serviços de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="38888-107">The **SetTimeZoneRedirection** method sets the **TimeZoneRedirection** property, which allows the client computer to redirect its time zone settings to the Remote Desktop Services session.</span></span>

## <a name="syntax"></a><span data-ttu-id="38888-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38888-108">Syntax</span></span>


```mof
uint32 SetTimeZoneRedirection(
  [in] uint32 TimeZoneRedirection
);
```



## <a name="parameters"></a><span data-ttu-id="38888-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38888-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38888-110">*TimeZoneRedirection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="38888-110">*TimeZoneRedirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38888-111">O novo valor para a propriedade **TimeZoneRedirection** .</span><span class="sxs-lookup"><span data-stu-id="38888-111">The new value for the **TimeZoneRedirection** property.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="38888-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="38888-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="38888-113">Desabilita a propriedade **TimeZoneRedirection** .</span><span class="sxs-lookup"><span data-stu-id="38888-113">Disables the **TimeZoneRedirection** property.</span></span> <span data-ttu-id="38888-114">Nenhum redirecionamento de fuso horário ocorre.</span><span class="sxs-lookup"><span data-stu-id="38888-114">No time zone redirection occurs.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="38888-115"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="38888-115"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="38888-116">Habilita a propriedade **TimeZoneRedirection** .</span><span class="sxs-lookup"><span data-stu-id="38888-116">Enables the **TimeZoneRedirection** property.</span></span> <span data-ttu-id="38888-117">O fuso horário do cliente é redirecionado para o fuso horário da sessão.</span><span class="sxs-lookup"><span data-stu-id="38888-117">The client's time zone is redirected to the session's time zone.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38888-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="38888-118">Return value</span></span>

<span data-ttu-id="38888-119">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="38888-119">Returns 0 on success; otherwise returns a WMI error code.</span></span> <span data-ttu-id="38888-120">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="38888-120">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="38888-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="38888-121">Remarks</span></span>

<span data-ttu-id="38888-122">Por padrão, o fuso horário para a sessão de Serviços de Área de Trabalho Remota é o mesmo que o fuso horário do servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="38888-122">By default, the time zone for the Remote Desktop Services session is the same as the time zone for the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="38888-123">Os computadores cliente não podem redirecionar informações de fuso horário.</span><span class="sxs-lookup"><span data-stu-id="38888-123">Client computers cannot redirect time zone information.</span></span>

<span data-ttu-id="38888-124">Se o redirecionamento de fuso horário estiver desabilitado, as novas sessões herdarão o fuso horário do servidor.</span><span class="sxs-lookup"><span data-stu-id="38888-124">If time zone redirection is disabled, new sessions inherit the server time zone.</span></span> <span data-ttu-id="38888-125">Quando uma sessão é reconectada, a sessão retém o fuso horário que tinha antes de se desconectar.</span><span class="sxs-lookup"><span data-stu-id="38888-125">When a session reconnects, the session retains the time zone it had prior to disconnecting.</span></span>

<span data-ttu-id="38888-126">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="38888-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="38888-127">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="38888-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="38888-128">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="38888-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="38888-129">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="38888-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="38888-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38888-130">Requirements</span></span>



| <span data-ttu-id="38888-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="38888-131">Requirement</span></span> | <span data-ttu-id="38888-132">Valor</span><span class="sxs-lookup"><span data-stu-id="38888-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38888-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38888-133">Minimum supported client</span></span><br/> | <span data-ttu-id="38888-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38888-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="38888-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38888-135">Minimum supported server</span></span><br/> | <span data-ttu-id="38888-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38888-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="38888-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="38888-137">Namespace</span></span><br/>                | <span data-ttu-id="38888-138">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="38888-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="38888-139">MOF</span><span class="sxs-lookup"><span data-stu-id="38888-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38888-140"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38888-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="38888-141">DLL</span><span class="sxs-lookup"><span data-stu-id="38888-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38888-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38888-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38888-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="38888-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38888-144">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="38888-144">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

