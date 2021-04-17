---
title: Método GetVirtualDesktopAssignedToUser da classe Win32_RDMSVirtualDesktop
description: Recupera a área de trabalho virtual que é atribuída ao usuário especificado.
ms.assetid: cbc22c45-4492-4651-b164-a6fd717c5ab4
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetVirtualDesktopAssignedToUser
- Método GetVirtualDesktopAssignedToUser Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktop
- Classe Win32_RDMSVirtualDesktop Serviços de Área de Trabalho Remota, método GetVirtualDesktopAssignedToUser
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopAssignedToUser
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcbbbed20b6b571e8867689ac901344af8e23b93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105768554"
---
# <a name="getvirtualdesktopassignedtouser-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="beded-106">Método GetVirtualDesktopAssignedToUser da classe Win32 \_ RDMSVirtualDesktop</span><span class="sxs-lookup"><span data-stu-id="beded-106">GetVirtualDesktopAssignedToUser method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="beded-107">Recupera a área de trabalho virtual que é atribuída ao usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="beded-107">Retrieves the virtual desktop that is assigned to the specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="beded-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="beded-108">Syntax</span></span>


```mof
uint32 GetVirtualDesktopAssignedToUser(
  [in]  string CollectionAlias,
  [in]  string UserName,
  [in]  string UserDomain,
  [out] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="beded-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="beded-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beded-110">*CollectionAlias* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="beded-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beded-111">O alias da coleção de áreas de trabalho virtuais que contém a área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="beded-111">The alias of the virtual desktop collection that contain the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="beded-112">*Nome de usuário* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="beded-112">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beded-113">O nome de usuário do usuário.</span><span class="sxs-lookup"><span data-stu-id="beded-113">The username of the user.</span></span>

</dd> <dt>

<span data-ttu-id="beded-114">*UserDomain* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="beded-114">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beded-115">O nome de domínio do usuário.</span><span class="sxs-lookup"><span data-stu-id="beded-115">The domain name of the user.</span></span>

</dd> <dt>

<span data-ttu-id="beded-116">*VMName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="beded-116">*VMName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="beded-117">Recebe o nome da máquina virtual da área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="beded-117">Receives the virtual machine name of the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beded-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="beded-118">Return value</span></span>

<span data-ttu-id="beded-119">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="beded-119">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="beded-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="beded-120">Requirements</span></span>



| <span data-ttu-id="beded-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="beded-121">Requirement</span></span> | <span data-ttu-id="beded-122">Valor</span><span class="sxs-lookup"><span data-stu-id="beded-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="beded-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="beded-123">Minimum supported client</span></span><br/> | <span data-ttu-id="beded-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="beded-124">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="beded-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="beded-125">Minimum supported server</span></span><br/> | <span data-ttu-id="beded-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="beded-126">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="beded-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="beded-127">Namespace</span></span><br/>                | <span data-ttu-id="beded-128">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="beded-128">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="beded-129">MOF</span><span class="sxs-lookup"><span data-stu-id="beded-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="beded-130"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="beded-130"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="beded-131">DLL</span><span class="sxs-lookup"><span data-stu-id="beded-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="beded-132"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="beded-132"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="beded-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="beded-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beded-134">**\_RDMSVirtualDesktop Win32**</span><span class="sxs-lookup"><span data-stu-id="beded-134">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





