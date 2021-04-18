---
title: Método Export da classe Win32_TSVm
description: Recupera as informações de monitoramento da sessão de máquina virtual.
ms.assetid: 7996651c-aa7c-4fde-84a6-928b27c8c5b8
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método de exportação
- Método de exportação Serviços de Área de Trabalho Remota, classe Win32_TSVm
- Classe de Win32_TSVm Serviços de Área de Trabalho Remota, método de exportação
topic_type:
- apiref
api_name:
- Win32_TSVm.Export
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d94b24af5563f9cdb668e269c260e8fe19049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764747"
---
# <a name="export-method-of-the-win32_tsvm-class"></a><span data-ttu-id="fcfe5-106">Método Export da classe Win32 \_ TSVm</span><span class="sxs-lookup"><span data-stu-id="fcfe5-106">Export method of the Win32\_TSVm class</span></span>

<span data-ttu-id="fcfe5-107">Recupera as informações de monitoramento da sessão de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-107">Retrieves the virtual machine session monitoring information.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcfe5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fcfe5-108">Syntax</span></span>


```mof
uint32 Export(
  [in]  string ExportFolderPath,
  [out] string ExportJobObjectPath
);
```



## <a name="parameters"></a><span data-ttu-id="fcfe5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fcfe5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcfe5-110">*ExportFolderPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fcfe5-110">*ExportFolderPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcfe5-111">Caminho para onde a máquina virtual será exportada.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-111">Path to where the virtual machine will be exported.</span></span>

</dd> <dt>

<span data-ttu-id="fcfe5-112">*ExportJobObjectPath* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fcfe5-112">*ExportJobObjectPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fcfe5-113">Em um êxito, retorna o caminho do objeto HyperV ConcreteJob.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-113">On a success returns the HyperV ConcreteJob object path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcfe5-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fcfe5-114">Return value</span></span>

<span data-ttu-id="fcfe5-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="fcfe5-116">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcfe5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcfe5-117">Requirements</span></span>



| <span data-ttu-id="fcfe5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcfe5-118">Requirement</span></span> | <span data-ttu-id="fcfe5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="fcfe5-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcfe5-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fcfe5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fcfe5-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fcfe5-121">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="fcfe5-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fcfe5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fcfe5-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fcfe5-123">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="fcfe5-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="fcfe5-124">Namespace</span></span><br/>                | <span data-ttu-id="fcfe5-125">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="fcfe5-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="fcfe5-126">MOF</span><span class="sxs-lookup"><span data-stu-id="fcfe5-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fcfe5-127"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fcfe5-127"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="fcfe5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="fcfe5-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcfe5-129"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcfe5-129"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcfe5-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="fcfe5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcfe5-131">**\_TSVm Win32**</span><span class="sxs-lookup"><span data-stu-id="fcfe5-131">**Win32\_TSVm**</span></span>](win32-tsvm.md)
</dt> </dl>

 

 





