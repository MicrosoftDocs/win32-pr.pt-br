---
title: Método RemoveDesktopAssignment da classe Win32_RDMSDesktopAssignment
description: Remove uma atribuição de desktop.
ms.assetid: e1a8cf03-1d21-4bf4-a868-3da4d5bbf43b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RemoveDesktopAssignment
- Método RemoveDesktopAssignment Serviços de Área de Trabalho Remota, classe Win32_RDMSDesktopAssignment
- Classe Win32_RDMSDesktopAssignment Serviços de Área de Trabalho Remota, método RemoveDesktopAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.RemoveDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6645a79efc970cf7c3288d0765e9aac8cac68a89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788024"
---
# <a name="removedesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a><span data-ttu-id="1cae8-106">Método RemoveDesktopAssignment da classe Win32 \_ RDMSDesktopAssignment</span><span class="sxs-lookup"><span data-stu-id="1cae8-106">RemoveDesktopAssignment method of the Win32\_RDMSDesktopAssignment class</span></span>

<span data-ttu-id="1cae8-107">Remove uma atribuição de desktop</span><span class="sxs-lookup"><span data-stu-id="1cae8-107">Removes a desktop assignment</span></span>

## <a name="syntax"></a><span data-ttu-id="1cae8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1cae8-108">Syntax</span></span>


```mof
uint32 RemoveDesktopAssignment(
  [in] string CollectionAlias,
  [in] string DesktopName,
  [in] string UserDomain,
  [in] string UserName
);
```



## <a name="parameters"></a><span data-ttu-id="1cae8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1cae8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cae8-110">*CollectionAlias* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1cae8-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cae8-111">O alias da coleção.</span><span class="sxs-lookup"><span data-stu-id="1cae8-111">The collection alias.</span></span>

</dd> <dt>

<span data-ttu-id="1cae8-112">*Área de trabalho* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1cae8-112">*DesktopName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cae8-113">O nome da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1cae8-113">The name of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="1cae8-114">*UserDomain* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1cae8-114">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cae8-115">O nome de domínio da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="1cae8-115">The user account domain name.</span></span>

</dd> <dt>

<span data-ttu-id="1cae8-116">*Nome de usuário* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1cae8-116">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cae8-117">O nome da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="1cae8-117">The user account name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1cae8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cae8-118">Requirements</span></span>



| <span data-ttu-id="1cae8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cae8-119">Requirement</span></span> | <span data-ttu-id="1cae8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1cae8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cae8-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cae8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1cae8-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1cae8-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="1cae8-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cae8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1cae8-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1cae8-124">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="1cae8-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="1cae8-125">Namespace</span></span><br/>                | <span data-ttu-id="1cae8-126">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="1cae8-126">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="1cae8-127">MOF</span><span class="sxs-lookup"><span data-stu-id="1cae8-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1cae8-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1cae8-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="1cae8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="1cae8-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cae8-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cae8-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="1cae8-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="1cae8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cae8-132">**\_RDMSDesktopAssignment Win32**</span><span class="sxs-lookup"><span data-stu-id="1cae8-132">**Win32\_RDMSDesktopAssignment**</span></span>](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 





