---
title: Método setanteriority da classe Win32_SessionDirectoryVMMPlugin
description: Define a prioridade do plug-in.
ms.assetid: ddcf30cd-b87c-4869-80fc-ec92092e0df3
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método setanteriority
- Método setServiços de Área de Trabalho Remota, classe Win32_SessionDirectoryVMMPlugin
- Classe Win32_SessionDirectoryVMMPlugin Serviços de Área de Trabalho Remota, método setanteriority
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetPriority
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5d20dbc4af332d0c658f819f8e47f5b3eb4e95b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919132"
---
# <a name="setpriority-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="02385-106">Método setanteriority da classe Win32 \_ SessionDirectoryVMMPlugin</span><span class="sxs-lookup"><span data-stu-id="02385-106">SetPriority method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="02385-107">Define a prioridade do plug-in.</span><span class="sxs-lookup"><span data-stu-id="02385-107">Sets the priority of the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="02385-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02385-108">Syntax</span></span>


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a><span data-ttu-id="02385-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02385-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02385-110">*Prioridade* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="02385-110">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02385-111">A prioridade do plug-in.</span><span class="sxs-lookup"><span data-stu-id="02385-111">The priority of the plug-in.</span></span> <span data-ttu-id="02385-112">Quanto maior o valor, maior a prioridade do plug-in.</span><span class="sxs-lookup"><span data-stu-id="02385-112">The higher the value, the higher the priority of the plug-in.</span></span> <span data-ttu-id="02385-113">A prioridade é zero por padrão.</span><span class="sxs-lookup"><span data-stu-id="02385-113">The priority is zero by default.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02385-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="02385-114">Return value</span></span>

<span data-ttu-id="02385-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="02385-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="02385-116">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="02385-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="02385-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02385-117">Requirements</span></span>



| <span data-ttu-id="02385-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="02385-118">Requirement</span></span> | <span data-ttu-id="02385-119">Valor</span><span class="sxs-lookup"><span data-stu-id="02385-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="02385-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02385-120">Minimum supported client</span></span><br/> | <span data-ttu-id="02385-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="02385-121">None supported</span></span><br/>                                                              |
| <span data-ttu-id="02385-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02385-122">Minimum supported server</span></span><br/> | <span data-ttu-id="02385-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="02385-123">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="02385-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="02385-124">Namespace</span></span><br/>                | <span data-ttu-id="02385-125">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="02385-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="02385-126">MOF</span><span class="sxs-lookup"><span data-stu-id="02385-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02385-127"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02385-127"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="02385-128">DLL</span><span class="sxs-lookup"><span data-stu-id="02385-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02385-129"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02385-129"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02385-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="02385-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02385-131">**\_SessionDirectoryVMMPlugin Win32**</span><span class="sxs-lookup"><span data-stu-id="02385-131">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





