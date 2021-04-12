---
title: Método SetServiceLocation da classe Win32_SessionDirectoryVMMPlugin
description: Define o local do serviço para o plug-in.
ms.assetid: e886a40b-9ea9-4159-a2ea-776160559410
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetServiceLocation
- Método SetServiceLocation Serviços de Área de Trabalho Remota, classe Win32_SessionDirectoryVMMPlugin
- Classe Win32_SessionDirectoryVMMPlugin Serviços de Área de Trabalho Remota, método SetServiceLocation
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetServiceLocation
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64c16a6bbe802052f53d28d4cd8cc2b9ab559b61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499503"
---
# <a name="setservicelocation-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="78091-106">Método SetServiceLocation da classe Win32 \_ SessionDirectoryVMMPlugin</span><span class="sxs-lookup"><span data-stu-id="78091-106">SetServiceLocation method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="78091-107">Define o local do serviço para o plug-in.</span><span class="sxs-lookup"><span data-stu-id="78091-107">Sets the service location for the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="78091-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78091-108">Syntax</span></span>


```mof
uint32 SetServiceLocation(
  [in] string sServiceLocation
);
```



## <a name="parameters"></a><span data-ttu-id="78091-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78091-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78091-110">*sServiceLocation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78091-110">*sServiceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78091-111">O local do serviço que o plug-in deve contatar.</span><span class="sxs-lookup"><span data-stu-id="78091-111">The service location that the plug-in should contact.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78091-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="78091-112">Return value</span></span>

<span data-ttu-id="78091-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="78091-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="78091-114">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="78091-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="78091-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78091-115">Requirements</span></span>



| <span data-ttu-id="78091-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="78091-116">Requirement</span></span> | <span data-ttu-id="78091-117">Valor</span><span class="sxs-lookup"><span data-stu-id="78091-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78091-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78091-118">Minimum supported client</span></span><br/> | <span data-ttu-id="78091-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="78091-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="78091-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78091-120">Minimum supported server</span></span><br/> | <span data-ttu-id="78091-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78091-121">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="78091-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="78091-122">Namespace</span></span><br/>                | <span data-ttu-id="78091-123">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="78091-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="78091-124">MOF</span><span class="sxs-lookup"><span data-stu-id="78091-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78091-125"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78091-125"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="78091-126">DLL</span><span class="sxs-lookup"><span data-stu-id="78091-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78091-127"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78091-127"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78091-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="78091-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78091-129">**\_SessionDirectoryVMMPlugin Win32**</span><span class="sxs-lookup"><span data-stu-id="78091-129">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





