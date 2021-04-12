---
title: Método RdvSetupVMPermissions da classe Win32_RdvhManagement
description: Define as permissões em uma máquina virtual para o usuário atual.
ms.assetid: 6ac45983-d468-4a3b-875f-48717ba23ed0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RdvSetupVMPermissions
- Método RdvSetupVMPermissions Serviços de Área de Trabalho Remota, classe Win32_RdvhManagement
- Classe Win32_RdvhManagement Serviços de Área de Trabalho Remota, método RdvSetupVMPermissions
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvSetupVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd8028a33bc772f9dd37f25a1dc22074baf771b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455145"
---
# <a name="rdvsetupvmpermissions-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="71d95-106">Método RdvSetupVMPermissions da classe Win32 \_ RdvhManagement</span><span class="sxs-lookup"><span data-stu-id="71d95-106">RdvSetupVMPermissions method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="71d95-107">Define as permissões em uma máquina virtual para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="71d95-107">Sets the permissions on a virtual machine for the current user.</span></span>

## <a name="syntax"></a><span data-ttu-id="71d95-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71d95-108">Syntax</span></span>


```mof
uint32 RdvSetupVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a><span data-ttu-id="71d95-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71d95-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71d95-110">*VmName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71d95-110">*VmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71d95-111">O nome da máquina virtual para a qual definir permissões.</span><span class="sxs-lookup"><span data-stu-id="71d95-111">The name of the virtual machine to set permissions on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71d95-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71d95-112">Return value</span></span>

<span data-ttu-id="71d95-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="71d95-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="71d95-114">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="71d95-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="71d95-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71d95-115">Requirements</span></span>



| <span data-ttu-id="71d95-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="71d95-116">Requirement</span></span> | <span data-ttu-id="71d95-117">Valor</span><span class="sxs-lookup"><span data-stu-id="71d95-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="71d95-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71d95-118">Minimum supported client</span></span><br/> | <span data-ttu-id="71d95-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="71d95-119">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="71d95-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71d95-120">Minimum supported server</span></span><br/> | <span data-ttu-id="71d95-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="71d95-121">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="71d95-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="71d95-122">Namespace</span></span><br/>                | <span data-ttu-id="71d95-123">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="71d95-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="71d95-124">MOF</span><span class="sxs-lookup"><span data-stu-id="71d95-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71d95-125"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71d95-125"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="71d95-126">DLL</span><span class="sxs-lookup"><span data-stu-id="71d95-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71d95-127"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71d95-127"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71d95-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="71d95-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71d95-129">**\_RdvhManagement Win32**</span><span class="sxs-lookup"><span data-stu-id="71d95-129">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





