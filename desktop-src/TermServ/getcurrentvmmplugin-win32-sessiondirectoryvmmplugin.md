---
title: Método GetCurrentVMMPlugin da classe Win32_SessionDirectoryVMMPlugin
description: Obtém o plug-in de prioridade mais alta que está habilitado.
ms.assetid: 7712573f-2252-4a3c-820c-b679be5dfd46
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetCurrentVMMPlugin
- Método GetCurrentVMMPlugin Serviços de Área de Trabalho Remota, classe Win32_SessionDirectoryVMMPlugin
- Classe Win32_SessionDirectoryVMMPlugin Serviços de Área de Trabalho Remota, método GetCurrentVMMPlugin
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.GetCurrentVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7162322f4e5e3939309d64e27c93cf8d20da540c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824779"
---
# <a name="getcurrentvmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="f9c64-106">Método GetCurrentVMMPlugin da classe Win32 \_ SessionDirectoryVMMPlugin</span><span class="sxs-lookup"><span data-stu-id="f9c64-106">GetCurrentVMMPlugin method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="f9c64-107">Obtém o plug-in de prioridade mais alta que está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f9c64-107">Gets the highest priority plug-in that is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9c64-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9c64-108">Syntax</span></span>


```mof
uint32 GetCurrentVMMPlugin(
  [out] string  sName,
  [out] string  sProvider,
  [out] string  sServiceLocation,
  [out] string  sClassID,
  [out] sint32  Priority,
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="f9c64-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9c64-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9c64-110">*sname* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f9c64-110">*sName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9c64-111">O nome do plug-in.</span><span class="sxs-lookup"><span data-stu-id="f9c64-111">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="f9c64-112">*sProvider* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f9c64-112">*sProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9c64-113">O nome do provedor de plug-in.</span><span class="sxs-lookup"><span data-stu-id="f9c64-113">The name of the plug-in provider.</span></span>

</dd> <dt>

<span data-ttu-id="f9c64-114">*sServiceLocation* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f9c64-114">*sServiceLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9c64-115">O local do serviço que o plug-in deve contatar.</span><span class="sxs-lookup"><span data-stu-id="f9c64-115">The service location that the plug-in should contact.</span></span>

</dd> <dt>

<span data-ttu-id="f9c64-116">*sClassID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f9c64-116">*sClassID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9c64-117">O identificador de classe do plug-in.</span><span class="sxs-lookup"><span data-stu-id="f9c64-117">The class identifier of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="f9c64-118">*Prioridade* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="f9c64-118">*Priority* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9c64-119">A prioridade do plug-in.</span><span class="sxs-lookup"><span data-stu-id="f9c64-119">The priority of the plug-in.</span></span> <span data-ttu-id="f9c64-120">Quanto maior o valor, maior a prioridade do plug-in.</span><span class="sxs-lookup"><span data-stu-id="f9c64-120">The higher the value, the higher the priority of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="f9c64-121">*Habilitado* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f9c64-121">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9c64-122">Indica se o plug-in está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="f9c64-122">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="f9c64-123">**True** se o plug-in estiver habilitado ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="f9c64-123">**True** if the plug-in is enabled or **false** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9c64-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f9c64-124">Return value</span></span>

<span data-ttu-id="f9c64-125">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="f9c64-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f9c64-126">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="f9c64-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9c64-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9c64-127">Requirements</span></span>



| <span data-ttu-id="f9c64-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9c64-128">Requirement</span></span> | <span data-ttu-id="f9c64-129">Valor</span><span class="sxs-lookup"><span data-stu-id="f9c64-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9c64-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9c64-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f9c64-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f9c64-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f9c64-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9c64-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f9c64-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f9c64-133">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="f9c64-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="f9c64-134">Namespace</span></span><br/>                | <span data-ttu-id="f9c64-135">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="f9c64-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="f9c64-136">MOF</span><span class="sxs-lookup"><span data-stu-id="f9c64-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9c64-137"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9c64-137"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9c64-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f9c64-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9c64-139"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9c64-139"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9c64-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9c64-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9c64-141">**\_SessionDirectoryVMMPlugin Win32**</span><span class="sxs-lookup"><span data-stu-id="f9c64-141">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





