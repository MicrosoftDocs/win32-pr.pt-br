---
title: Método DumpVmInfo da classe Win32_TSVm
description: Esse membro é para fins de teste interno e não deve ser usado em seu código.
ms.assetid: 40cb4fdc-f657-47c6-8daa-684a12be30e4
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método DumpVmInfo
- Método DumpVmInfo Serviços de Área de Trabalho Remota, classe Win32_TSVm
- Classe Win32_TSVm Serviços de Área de Trabalho Remota, método DumpVmInfo
topic_type:
- apiref
api_name:
- Win32_TSVm.DumpVmInfo
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a2d02a1d4ea07bd045da2850a4d7ccb0069977a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645236"
---
# <a name="dumpvminfo-method-of-the-win32_tsvm-class"></a><span data-ttu-id="cd2fc-106">Método DumpVmInfo da classe Win32 \_ TSVm</span><span class="sxs-lookup"><span data-stu-id="cd2fc-106">DumpVmInfo method of the Win32\_TSVm class</span></span>

<span data-ttu-id="cd2fc-107">Esse membro é para fins de teste interno e não deve ser usado em seu código.</span><span class="sxs-lookup"><span data-stu-id="cd2fc-107">This member is for internal testing purposes, and should not be used in your code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd2fc-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd2fc-108">Syntax</span></span>


```mof
uint32 DumpVmInfo();
```



## <a name="parameters"></a><span data-ttu-id="cd2fc-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd2fc-109">Parameters</span></span>

<span data-ttu-id="cd2fc-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cd2fc-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cd2fc-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cd2fc-111">Return value</span></span>

<span data-ttu-id="cd2fc-112">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="cd2fc-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="cd2fc-113">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="cd2fc-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd2fc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd2fc-114">Requirements</span></span>



| <span data-ttu-id="cd2fc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd2fc-115">Requirement</span></span> | <span data-ttu-id="cd2fc-116">Valor</span><span class="sxs-lookup"><span data-stu-id="cd2fc-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd2fc-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd2fc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cd2fc-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="cd2fc-118">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="cd2fc-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd2fc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cd2fc-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd2fc-120">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="cd2fc-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd2fc-121">Namespace</span></span><br/>                | <span data-ttu-id="cd2fc-122">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="cd2fc-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="cd2fc-123">MOF</span><span class="sxs-lookup"><span data-stu-id="cd2fc-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd2fc-124"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd2fc-124"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="cd2fc-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cd2fc-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd2fc-126"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd2fc-126"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd2fc-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd2fc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd2fc-128">**\_TSVm Win32**</span><span class="sxs-lookup"><span data-stu-id="cd2fc-128">**Win32\_TSVm**</span></span>](win32-tsvm.md)
</dt> </dl>

 

 





