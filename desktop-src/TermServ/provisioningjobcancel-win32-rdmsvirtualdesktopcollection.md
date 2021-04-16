---
title: Método ProvisioningJobCancel da classe Win32_RDMSVirtualDesktopCollection
description: Cancela um trabalho de provisionamento de área de trabalho virtual.
ms.assetid: 933ea0f3-b916-4e70-89de-597f9eb23976
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ProvisioningJobCancel
- Método ProvisioningJobCancel Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Serviços de Área de Trabalho Remota, método ProvisioningJobCancel
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobCancel
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f414bcdc264d682817898bae98fcf60a716452
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105768544"
---
# <a name="provisioningjobcancel-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="de9d8-106">Método ProvisioningJobCancel da classe Win32 \_ RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="de9d8-106">ProvisioningJobCancel method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="de9d8-107">Cancela um trabalho de provisionamento de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="de9d8-107">Cancels a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="de9d8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de9d8-108">Syntax</span></span>


```mof
uint32 ProvisioningJobCancel(
  [in] string JobGuid
);
```



## <a name="parameters"></a><span data-ttu-id="de9d8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de9d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de9d8-110">*JobGuid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="de9d8-110">*JobGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de9d8-111">O **GUID** que identifica exclusivamente o trabalho de provisionamento a ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="de9d8-111">The **GUID** that uniquely identifies the provisioning job to cancel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de9d8-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="de9d8-112">Return value</span></span>

<span data-ttu-id="de9d8-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="de9d8-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="de9d8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de9d8-114">Requirements</span></span>



| <span data-ttu-id="de9d8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="de9d8-115">Requirement</span></span> | <span data-ttu-id="de9d8-116">Valor</span><span class="sxs-lookup"><span data-stu-id="de9d8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="de9d8-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de9d8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="de9d8-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="de9d8-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="de9d8-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de9d8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="de9d8-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="de9d8-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="de9d8-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="de9d8-121">Namespace</span></span><br/>                | <span data-ttu-id="de9d8-122">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="de9d8-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="de9d8-123">MOF</span><span class="sxs-lookup"><span data-stu-id="de9d8-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de9d8-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de9d8-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="de9d8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="de9d8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de9d8-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de9d8-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="de9d8-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="de9d8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de9d8-128">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="de9d8-128">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





