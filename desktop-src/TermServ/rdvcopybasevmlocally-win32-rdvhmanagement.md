---
title: Método RdvCopyBaseVmLocally da classe Win32_RdvhManagement
description: Copia uma máquina virtual de base local para um servidor de host de virtualização de área de trabalho remota (RDV) especificado.
ms.assetid: 13c0c629-42c6-4689-9740-f13f31688e42
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RdvCopyBaseVmLocally
- Método RdvCopyBaseVmLocally Serviços de Área de Trabalho Remota, classe Win32_RdvhManagement
- Classe Win32_RdvhManagement Serviços de Área de Trabalho Remota, método RdvCopyBaseVmLocally
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCopyBaseVmLocally
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d96e01038a4b41edcf32a6a5a9b353403fa6021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369872"
---
# <a name="rdvcopybasevmlocally-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="d1b5c-106">Método RdvCopyBaseVmLocally da classe Win32 \_ RdvhManagement</span><span class="sxs-lookup"><span data-stu-id="d1b5c-106">RdvCopyBaseVmLocally method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="d1b5c-107">Copia uma máquina virtual de base local para um servidor de host de virtualização de área de trabalho remota (RDV) especificado.</span><span class="sxs-lookup"><span data-stu-id="d1b5c-107">Copies a local base virtual machine to a specified remote desktop virtualization (RDV) host server.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1b5c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1b5c-108">Syntax</span></span>


```mof
uint32 RdvCopyBaseVmLocally(
  [in] string BaseVmLocation,
  [in] string FarmName,
  [in] string GoldCacheLocation
);
```



## <a name="parameters"></a><span data-ttu-id="d1b5c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1b5c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1b5c-110">*BaseVmLocation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1b5c-110">*BaseVmLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1b5c-111">O local da máquina virtual base.</span><span class="sxs-lookup"><span data-stu-id="d1b5c-111">The base virtual machine location.</span></span>

</dd> <dt>

<span data-ttu-id="d1b5c-112">*Farmname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1b5c-112">*FarmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1b5c-113">O nome do farm de host para o qual copiar.</span><span class="sxs-lookup"><span data-stu-id="d1b5c-113">The name of the host farm to copy to.</span></span>

</dd> <dt>

<span data-ttu-id="d1b5c-114">*GoldCacheLocation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1b5c-114">*GoldCacheLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1b5c-115">O local do cache dourado.</span><span class="sxs-lookup"><span data-stu-id="d1b5c-115">The gold cache location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1b5c-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d1b5c-116">Return value</span></span>

<span data-ttu-id="d1b5c-117">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="d1b5c-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="d1b5c-118">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="d1b5c-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1b5c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1b5c-119">Requirements</span></span>



| <span data-ttu-id="d1b5c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1b5c-120">Requirement</span></span> | <span data-ttu-id="d1b5c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d1b5c-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1b5c-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1b5c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d1b5c-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d1b5c-123">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="d1b5c-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1b5c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d1b5c-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d1b5c-125">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="d1b5c-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1b5c-126">Namespace</span></span><br/>                | <span data-ttu-id="d1b5c-127">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="d1b5c-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="d1b5c-128">MOF</span><span class="sxs-lookup"><span data-stu-id="d1b5c-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1b5c-129"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1b5c-129"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="d1b5c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d1b5c-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1b5c-131"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1b5c-131"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1b5c-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1b5c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1b5c-133">**\_RdvhManagement Win32**</span><span class="sxs-lookup"><span data-stu-id="d1b5c-133">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





