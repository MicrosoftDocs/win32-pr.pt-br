---
title: Método getpatchproperties da classe Win32_RDMSVirtualDesktopCollection
description: Recupera as propriedades de um trabalho de provisionamento de atualização de software para as máquinas virtuais em uma coleção de áreas de trabalho virtuais.
ms.assetid: 9f228d89-0613-49c7-8169-48491c3a2d9b
ms.tgt_platform: multiple
keywords:
- Método getpatchproperties Serviços de Área de Trabalho Remota
- Método getpatchproperties Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Serviços de Área de Trabalho Remota, método getpatchproperties
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetPatchProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f0ca45c97512818aa5f8a9ea851d18fa5554c32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499510"
---
# <a name="getpatchproperties-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="d7f2f-106">Método getpatchproperties da classe Win32 \_ RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="d7f2f-106">GetPatchProperties method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="d7f2f-107">Recupera as propriedades de um trabalho de provisionamento de atualização de software para as máquinas virtuais em uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="d7f2f-107">Retrieves the properties of a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f2f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7f2f-108">Syntax</span></span>


```mof
uint32 GetPatchProperties(
  [out] DATETIME StartTime,
  [out] DATETIME ForceLogOffTime,
  [out] string   JobGuid,
  [out] uint32   State
);
```



## <a name="parameters"></a><span data-ttu-id="d7f2f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7f2f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7f2f-110">*StartTime* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d7f2f-110">*StartTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f2f-111">A data e a hora para instalar as atualizações.</span><span class="sxs-lookup"><span data-stu-id="d7f2f-111">The date and time to install the updates.</span></span>

</dd> <dt>

<span data-ttu-id="d7f2f-112">*ForceLogOffTime* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d7f2f-112">*ForceLogOffTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f2f-113">A data e a hora em que o sistema fará logoff dos usuários das máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="d7f2f-113">The date and time on which the system will log off users of the virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="d7f2f-114">*JobGuid* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d7f2f-114">*JobGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f2f-115">Um **GUID** que identifica exclusivamente o trabalho de provisionamento.</span><span class="sxs-lookup"><span data-stu-id="d7f2f-115">A **GUID** that uniquely identifies the provisioning job.</span></span>

</dd> <dt>

<span data-ttu-id="d7f2f-116">*Estado* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d7f2f-116">*State* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f2f-117">O estado do trabalho de provisionamento.</span><span class="sxs-lookup"><span data-stu-id="d7f2f-117">The state of the provisioning job.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7f2f-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7f2f-118">Return value</span></span>

<span data-ttu-id="d7f2f-119">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="d7f2f-119">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7f2f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7f2f-120">Requirements</span></span>



| <span data-ttu-id="d7f2f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7f2f-121">Requirement</span></span> | <span data-ttu-id="d7f2f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d7f2f-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f2f-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7f2f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d7f2f-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d7f2f-124">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="d7f2f-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7f2f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d7f2f-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d7f2f-126">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="d7f2f-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="d7f2f-127">Namespace</span></span><br/>                | <span data-ttu-id="d7f2f-128">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="d7f2f-128">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="d7f2f-129">MOF</span><span class="sxs-lookup"><span data-stu-id="d7f2f-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7f2f-130"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7f2f-130"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7f2f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d7f2f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7f2f-132"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7f2f-132"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="d7f2f-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7f2f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f2f-134">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="d7f2f-134">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





