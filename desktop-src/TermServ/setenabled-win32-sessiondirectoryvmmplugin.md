---
title: Método sethabilitado da classe Win32_SessionDirectoryVMMPlugin
description: Habilita ou desabilita o plug-in.
ms.assetid: 25ce0614-5c3b-4a79-9174-1a9de1eb6c33
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método sethabilitado
- Método sethabilitado Serviços de Área de Trabalho Remota, classe Win32_SessionDirectoryVMMPlugin
- Classe Win32_SessionDirectoryVMMPlugin Serviços de Área de Trabalho Remota, método sethabilitado
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetEnabled
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7089a21f143b6f3b27fe9fe58563e6777bf2f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645177"
---
# <a name="setenabled-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="12467-106">Método sethabilitado da \_ classe Win32 SessionDirectoryVMMPlugin</span><span class="sxs-lookup"><span data-stu-id="12467-106">SetEnabled method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="12467-107">Habilita ou desabilita o plug-in.</span><span class="sxs-lookup"><span data-stu-id="12467-107">Enables or disables the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="12467-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12467-108">Syntax</span></span>


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="12467-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12467-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12467-110">*Habilitado* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12467-110">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12467-111">Indica se o plug-in está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="12467-111">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="12467-112">**True** se o plug-in estiver habilitado ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="12467-112">**True** if the plug-in is enabled or **false** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12467-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12467-113">Return value</span></span>

<span data-ttu-id="12467-114">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="12467-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="12467-115">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="12467-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="12467-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12467-116">Requirements</span></span>



| <span data-ttu-id="12467-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="12467-117">Requirement</span></span> | <span data-ttu-id="12467-118">Valor</span><span class="sxs-lookup"><span data-stu-id="12467-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12467-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12467-119">Minimum supported client</span></span><br/> | <span data-ttu-id="12467-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="12467-120">None supported</span></span><br/>                                                              |
| <span data-ttu-id="12467-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12467-121">Minimum supported server</span></span><br/> | <span data-ttu-id="12467-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="12467-122">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="12467-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="12467-123">Namespace</span></span><br/>                | <span data-ttu-id="12467-124">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="12467-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="12467-125">MOF</span><span class="sxs-lookup"><span data-stu-id="12467-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12467-126"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12467-126"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="12467-127">DLL</span><span class="sxs-lookup"><span data-stu-id="12467-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12467-128"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12467-128"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12467-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="12467-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12467-130">**\_SessionDirectoryVMMPlugin Win32**</span><span class="sxs-lookup"><span data-stu-id="12467-130">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





