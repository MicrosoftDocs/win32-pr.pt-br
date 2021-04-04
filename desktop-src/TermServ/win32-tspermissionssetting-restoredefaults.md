---
title: Método RestoreDefaults da classe Win32_TSPermissionsSetting (Netfw. h)
description: Restaura os valores padrão do conjunto de permissões para o terminal.
ms.assetid: bdd01290-7c7c-4355-85dc-ade51b2abd94
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RestoreDefaults
- Método RestoreDefaults Serviços de Área de Trabalho Remota, classe Win32_TSPermissionsSetting
- Classe Win32_TSPermissionsSetting Serviços de Área de Trabalho Remota, método RestoreDefaults
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.RestoreDefaults
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 073a8f8267ab9e7f7cbd50f15f4f3f20594d2e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824316"
---
# <a name="restoredefaults-method-of-the-win32_tspermissionssetting-class"></a><span data-ttu-id="4941c-106">Método RestoreDefaults da classe Win32 \_ TSPermissionsSetting</span><span class="sxs-lookup"><span data-stu-id="4941c-106">RestoreDefaults method of the Win32\_TSPermissionsSetting class</span></span>

<span data-ttu-id="4941c-107">O método **RestoreDefaults** restaura os valores padrão do conjunto de permissões para o terminal.</span><span class="sxs-lookup"><span data-stu-id="4941c-107">The **RestoreDefaults** method restores the default permission set values for the terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="4941c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4941c-108">Syntax</span></span>


```mof
uint32 RestoreDefaults();
```



## <a name="parameters"></a><span data-ttu-id="4941c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4941c-109">Parameters</span></span>

<span data-ttu-id="4941c-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4941c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4941c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4941c-111">Return value</span></span>

<span data-ttu-id="4941c-112">Retorna êxito em caso de êxito, caso contrário, falha.</span><span class="sxs-lookup"><span data-stu-id="4941c-112">Returns Success on success, otherwise Failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="4941c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4941c-113">Remarks</span></span>

<span data-ttu-id="4941c-114">As permissões padrão são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="4941c-114">Default permissions are the following:</span></span>

-   <span data-ttu-id="4941c-115">As contas do assistente de ajuda de administradores, sistema e Área de Trabalho Remota têm todas as [permissões de serviços de área de trabalho remota](terminal-services-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="4941c-115">The Administrators, System, and Remote Desktop Help Assistant accounts have all [Remote Desktop Services Permissions](terminal-services-permissions.md).</span></span>
-   <span data-ttu-id="4941c-116">A conta Área de Trabalho Remota usuários tem logon, conexão, informações de consulta e permissão para enviar mensagem.</span><span class="sxs-lookup"><span data-stu-id="4941c-116">The Remote Desktop Users account has Logon, Connect, Query Information, and Send Message permission.</span></span>
-   <span data-ttu-id="4941c-117">O serviço local e as contas de serviço de rede têm informações de consulta e a permissão Enviar mensagem.</span><span class="sxs-lookup"><span data-stu-id="4941c-117">The Local Service and Network Service accounts have Query Information, and Send Message permission.</span></span>

<span data-ttu-id="4941c-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4941c-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4941c-119">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4941c-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4941c-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="4941c-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4941c-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4941c-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4941c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4941c-122">Requirements</span></span>



| <span data-ttu-id="4941c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4941c-123">Requirement</span></span> | <span data-ttu-id="4941c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4941c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4941c-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4941c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4941c-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4941c-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4941c-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4941c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4941c-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4941c-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4941c-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="4941c-129">Namespace</span></span><br/>                | <span data-ttu-id="4941c-130">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="4941c-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="4941c-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4941c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4941c-132"><dt>Netfw. h</dt></span><span class="sxs-lookup"><span data-stu-id="4941c-132"><dt>Netfw.h</dt></span></span> </dl>      |
| <span data-ttu-id="4941c-133">MOF</span><span class="sxs-lookup"><span data-stu-id="4941c-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4941c-134"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4941c-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4941c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="4941c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4941c-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4941c-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4941c-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="4941c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4941c-138">**\_TSPermissionsSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="4941c-138">**Win32\_TSPermissionsSetting**</span></span>](win32-tspermissionssetting.md)
</dt> </dl>

 

