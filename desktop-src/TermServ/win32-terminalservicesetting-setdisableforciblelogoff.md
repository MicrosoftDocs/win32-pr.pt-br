---
title: Método SetDisableForcibleLogoff da classe Win32_TerminalServiceSetting
description: Não há suporte para o método.
ms.assetid: 1b7ac0f2-c242-4ca8-bc4d-8111e63851eb
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetDisableForcibleLogoff
- Método SetDisableForcibleLogoff Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método SetDisableForcibleLogoff
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetDisableForcibleLogoff
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4ae62db188d0e3aa31ffd8e3993e793e9bb2bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455042"
---
# <a name="setdisableforciblelogoff-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="4ee01-106">Método SetDisableForcibleLogoff da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="4ee01-106">SetDisableForcibleLogoff method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="4ee01-107">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="4ee01-107">This method is not supported.</span></span>

<span data-ttu-id="4ee01-108">**Windows Vista e Windows Server 2008:** Habilita ou desabilita se um administrador que fez logon no console pode ser forçado a fazer logoff.</span><span class="sxs-lookup"><span data-stu-id="4ee01-108">**Windows Vista and Windows Server 2008:** Enables or disables whether an administrator logged onto the console can be forcibly logged off.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ee01-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ee01-109">Syntax</span></span>


```mof
uint32 SetDisableForcibleLogoff(
  [in] uint32 DisableForcibleLogoff
);
```



## <a name="parameters"></a><span data-ttu-id="4ee01-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ee01-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ee01-111">*DisableForcibleLogoff* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ee01-111">*DisableForcibleLogoff* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ee01-112">Sinalizador desabilitando ou habilitando a propriedade **DisableForcibleLogoff** , que determina se um administrador que está conectado ao console pode ser forçado a fazer logoff.</span><span class="sxs-lookup"><span data-stu-id="4ee01-112">Flag disabling or enabling the **DisableForcibleLogoff** property, which determines whether an administrator that is logged on to the console can be forcibly logged off.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="4ee01-113"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="4ee01-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="4ee01-114">Desabilite a propriedade.</span><span class="sxs-lookup"><span data-stu-id="4ee01-114">Disable the property.</span></span> <span data-ttu-id="4ee01-115">O administrador conectado pode ser forçado a fazer logoff.</span><span class="sxs-lookup"><span data-stu-id="4ee01-115">The connected administrator can be forcibly logged off.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="4ee01-116"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="4ee01-116"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="4ee01-117">Habilite a propriedade.</span><span class="sxs-lookup"><span data-stu-id="4ee01-117">Enable the property.</span></span> <span data-ttu-id="4ee01-118">Não é possível efetuar logoff forçado do administrador conectado.</span><span class="sxs-lookup"><span data-stu-id="4ee01-118">The connected administrator cannot be forcibly logged off.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ee01-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4ee01-119">Return value</span></span>

<span data-ttu-id="4ee01-120">Retorna êxito em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="4ee01-120">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="4ee01-121">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="4ee01-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ee01-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ee01-122">Requirements</span></span>



| <span data-ttu-id="4ee01-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ee01-123">Requirement</span></span> | <span data-ttu-id="4ee01-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4ee01-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ee01-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ee01-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4ee01-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ee01-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4ee01-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ee01-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4ee01-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ee01-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4ee01-129">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4ee01-129">End of client support</span></span><br/>    | <span data-ttu-id="4ee01-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ee01-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4ee01-131">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="4ee01-131">End of server support</span></span><br/>    | <span data-ttu-id="4ee01-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ee01-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4ee01-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ee01-133">Namespace</span></span><br/>                | <span data-ttu-id="4ee01-134">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="4ee01-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="4ee01-135">MOF</span><span class="sxs-lookup"><span data-stu-id="4ee01-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ee01-136"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ee01-136"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ee01-137">DLL</span><span class="sxs-lookup"><span data-stu-id="4ee01-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ee01-138"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ee01-138"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ee01-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ee01-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ee01-140">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="4ee01-140">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





