---
title: Método RdvMigrateVmToDifferentHost da classe Win32_RdvhManagement
description: Inicia uma migração dinâmica de uma máquina virtual para um host especificado.
ms.assetid: aa4b1e57-a97c-410b-9b9d-423a1c77de70
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RdvMigrateVmToDifferentHost
- Método RdvMigrateVmToDifferentHost Serviços de Área de Trabalho Remota, classe Win32_RdvhManagement
- Classe Win32_RdvhManagement Serviços de Área de Trabalho Remota, método RdvMigrateVmToDifferentHost
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvMigrateVmToDifferentHost
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3def1be6332397fb3830ffe8c90f324afc9f1b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644648"
---
# <a name="rdvmigratevmtodifferenthost-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="3a2a8-106">Método RdvMigrateVmToDifferentHost da classe Win32 \_ RdvhManagement</span><span class="sxs-lookup"><span data-stu-id="3a2a8-106">RdvMigrateVmToDifferentHost method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="3a2a8-107">Inicia uma migração dinâmica de uma máquina virtual para um host especificado.</span><span class="sxs-lookup"><span data-stu-id="3a2a8-107">Initiates a live migration of a virtual machine to a specified host.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a2a8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a2a8-108">Syntax</span></span>


```mof
uint32 RdvMigrateVmToDifferentHost(
  [in] string VmName,
  [in] string DestinationHost
);
```



## <a name="parameters"></a><span data-ttu-id="3a2a8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a2a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a2a8-110">*VmName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a2a8-110">*VmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a2a8-111">Nome da máquina virtual a ser migrada.</span><span class="sxs-lookup"><span data-stu-id="3a2a8-111">Name of the virtual machine to migrate.</span></span>

</dd> <dt>

<span data-ttu-id="3a2a8-112">*DestinationHost* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a2a8-112">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a2a8-113">nome do host de destino.</span><span class="sxs-lookup"><span data-stu-id="3a2a8-113">name of the destination host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a2a8-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a2a8-114">Return value</span></span>

<span data-ttu-id="3a2a8-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="3a2a8-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="3a2a8-116">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="3a2a8-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a2a8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a2a8-117">Requirements</span></span>



| <span data-ttu-id="3a2a8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a2a8-118">Requirement</span></span> | <span data-ttu-id="3a2a8-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3a2a8-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a2a8-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a2a8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3a2a8-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3a2a8-121">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="3a2a8-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a2a8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3a2a8-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3a2a8-123">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="3a2a8-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a2a8-124">Namespace</span></span><br/>                | <span data-ttu-id="3a2a8-125">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="3a2a8-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="3a2a8-126">MOF</span><span class="sxs-lookup"><span data-stu-id="3a2a8-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a2a8-127"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a2a8-127"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="3a2a8-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3a2a8-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a2a8-129"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a2a8-129"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a2a8-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a2a8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a2a8-131">**\_RdvhManagement Win32**</span><span class="sxs-lookup"><span data-stu-id="3a2a8-131">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





