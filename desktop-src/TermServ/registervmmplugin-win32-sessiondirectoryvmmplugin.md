---
title: Método RegisterVMMPlugin da classe Win32_SessionDirectoryVMMPlugin
description: Registra um novo plug-in do VMM.
ms.assetid: 8fa6109e-6320-4ad1-b313-f100d8383f85
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RegisterVMMPlugin
- Método RegisterVMMPlugin Serviços de Área de Trabalho Remota, classe Win32_SessionDirectoryVMMPlugin
- Classe Win32_SessionDirectoryVMMPlugin Serviços de Área de Trabalho Remota, método RegisterVMMPlugin
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.RegisterVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381be34f9398147b323fa99093479da48adfd480
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369426"
---
# <a name="registervmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="28c4d-106">Método RegisterVMMPlugin da classe Win32 \_ SessionDirectoryVMMPlugin</span><span class="sxs-lookup"><span data-stu-id="28c4d-106">RegisterVMMPlugin method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="28c4d-107">Registra um novo plug-in do VMM.</span><span class="sxs-lookup"><span data-stu-id="28c4d-107">Registers a new VMM plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="28c4d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28c4d-108">Syntax</span></span>


```mof
uint32 RegisterVMMPlugin(
  [in] string  sName,
  [in] string  sProvider,
  [in] string  sServiceLocation,
  [in] string  sClassID,
  [in] sint32  Priority = ,
  [in] boolean Enabled = 
);
```



## <a name="parameters"></a><span data-ttu-id="28c4d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28c4d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28c4d-110">*sname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="28c4d-110">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28c4d-111">O nome do plug-in.</span><span class="sxs-lookup"><span data-stu-id="28c4d-111">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="28c4d-112">*sProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="28c4d-112">*sProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28c4d-113">O nome do provedor de plug-in.</span><span class="sxs-lookup"><span data-stu-id="28c4d-113">The name of the plug-in provider.</span></span>

</dd> <dt>

<span data-ttu-id="28c4d-114">*sServiceLocation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="28c4d-114">*sServiceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28c4d-115">O local do serviço que o plug-in deve contatar.</span><span class="sxs-lookup"><span data-stu-id="28c4d-115">The service location that the plug-in should contact.</span></span>

</dd> <dt>

<span data-ttu-id="28c4d-116">*sClassID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="28c4d-116">*sClassID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28c4d-117">O identificador de classe do plug-in.</span><span class="sxs-lookup"><span data-stu-id="28c4d-117">The class identifier of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="28c4d-118">*Prioridade* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="28c4d-118">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28c4d-119">A prioridade do plug-in.</span><span class="sxs-lookup"><span data-stu-id="28c4d-119">The priority of the plug-in.</span></span> <span data-ttu-id="28c4d-120">Quanto maior o valor, maior a prioridade do plug-in.</span><span class="sxs-lookup"><span data-stu-id="28c4d-120">The higher the value, the higher the priority of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="28c4d-121">*Habilitado* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="28c4d-121">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28c4d-122">Indica se o plug-in está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="28c4d-122">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="28c4d-123">**True** se o plug-in estiver habilitado ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="28c4d-123">**True** if the plug-in is enabled or **false** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28c4d-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="28c4d-124">Return value</span></span>

<span data-ttu-id="28c4d-125">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="28c4d-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="28c4d-126">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="28c4d-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="28c4d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28c4d-127">Requirements</span></span>



| <span data-ttu-id="28c4d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="28c4d-128">Requirement</span></span> | <span data-ttu-id="28c4d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="28c4d-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28c4d-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28c4d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="28c4d-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="28c4d-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="28c4d-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28c4d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="28c4d-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="28c4d-133">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="28c4d-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="28c4d-134">Namespace</span></span><br/>                | <span data-ttu-id="28c4d-135">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="28c4d-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="28c4d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="28c4d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28c4d-137"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="28c4d-137"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="28c4d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="28c4d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28c4d-139"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28c4d-139"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28c4d-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="28c4d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28c4d-141">**\_SessionDirectoryVMMPlugin Win32**</span><span class="sxs-lookup"><span data-stu-id="28c4d-141">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





