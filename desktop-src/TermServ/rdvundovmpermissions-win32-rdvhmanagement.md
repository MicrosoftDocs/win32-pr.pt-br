---
title: Método RdvUndoVMPermissions da classe Win32_RdvhManagement
description: Reverte as permissões definidas por RdvSetupVMPermissions na máquina virtual especificada.
ms.assetid: 3331430e-7427-42f7-ab09-27fece8dc3ca
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RdvUndoVMPermissions
- Método RdvUndoVMPermissions Serviços de Área de Trabalho Remota, classe Win32_RdvhManagement
- Classe Win32_RdvhManagement Serviços de Área de Trabalho Remota, método RdvUndoVMPermissions
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvUndoVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1dc8892435522dcd2c7457fe4b74a0d9671740
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455863"
---
# <a name="rdvundovmpermissions-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="2b85e-106">Método RdvUndoVMPermissions da classe Win32 \_ RdvhManagement</span><span class="sxs-lookup"><span data-stu-id="2b85e-106">RdvUndoVMPermissions method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="2b85e-107">Reverte as permissões definidas por [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md) na máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="2b85e-107">Reverts permissions set by [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md) on the specified virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b85e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b85e-108">Syntax</span></span>


```mof
uint32 RdvUndoVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a><span data-ttu-id="2b85e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b85e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b85e-110">*VmName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2b85e-110">*VmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b85e-111">Nome da máquina virtual na qual as permissões são desfeitas.</span><span class="sxs-lookup"><span data-stu-id="2b85e-111">Name of the virtual machine to undo permissions on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b85e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2b85e-112">Return value</span></span>

<span data-ttu-id="2b85e-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="2b85e-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="2b85e-114">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="2b85e-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b85e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b85e-115">Requirements</span></span>



| <span data-ttu-id="2b85e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b85e-116">Requirement</span></span> | <span data-ttu-id="2b85e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="2b85e-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b85e-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b85e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2b85e-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2b85e-119">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="2b85e-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b85e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2b85e-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2b85e-121">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="2b85e-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="2b85e-122">Namespace</span></span><br/>                | <span data-ttu-id="2b85e-123">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="2b85e-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="2b85e-124">MOF</span><span class="sxs-lookup"><span data-stu-id="2b85e-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b85e-125"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b85e-125"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="2b85e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2b85e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b85e-127"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b85e-127"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b85e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b85e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b85e-129">**\_RdvhManagement Win32**</span><span class="sxs-lookup"><span data-stu-id="2b85e-129">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





