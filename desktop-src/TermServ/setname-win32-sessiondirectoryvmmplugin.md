---
title: Método SetName da classe Win32_SessionDirectoryVMMPlugin
description: Define o nome do plug-in.
ms.assetid: 8af4abca-f147-4027-91fb-4d669b58caa4
ms.tgt_platform: multiple
keywords:
- Método SetName Serviços de Área de Trabalho Remota
- Método SetName Serviços de Área de Trabalho Remota, classe Win32_SessionDirectoryVMMPlugin
- Classe Win32_SessionDirectoryVMMPlugin Serviços de Área de Trabalho Remota, método SetName
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetName
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc9902e8d5931f0800dc6c62d36815f4f78db73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295781"
---
# <a name="setname-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="d8499-106">Método SetName da classe Win32 \_ SessionDirectoryVMMPlugin</span><span class="sxs-lookup"><span data-stu-id="d8499-106">SetName method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="d8499-107">Define o nome do plug-in.</span><span class="sxs-lookup"><span data-stu-id="d8499-107">Sets the name of the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8499-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8499-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string sName
);
```



## <a name="parameters"></a><span data-ttu-id="d8499-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8499-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8499-110">*sname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8499-110">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8499-111">O nome do plug-in.</span><span class="sxs-lookup"><span data-stu-id="d8499-111">The name of the plug-in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8499-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8499-112">Return value</span></span>

<span data-ttu-id="d8499-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="d8499-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="d8499-114">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="d8499-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8499-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8499-115">Requirements</span></span>



| <span data-ttu-id="d8499-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8499-116">Requirement</span></span> | <span data-ttu-id="d8499-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d8499-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8499-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8499-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d8499-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d8499-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d8499-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8499-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d8499-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d8499-121">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="d8499-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="d8499-122">Namespace</span></span><br/>                | <span data-ttu-id="d8499-123">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="d8499-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="d8499-124">MOF</span><span class="sxs-lookup"><span data-stu-id="d8499-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8499-125"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8499-125"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8499-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d8499-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8499-127"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8499-127"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8499-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8499-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8499-129">**\_SessionDirectoryVMMPlugin Win32**</span><span class="sxs-lookup"><span data-stu-id="d8499-129">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





