---
description: Localiza um \_ objeto Msvm MountedStorageImage para um determinado caminho de imagem de disco.
ms.assetid: 498ed285-2b5b-472b-b0ee-649c97b61274
title: Método FindMountedStorageImageInstance da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.FindMountedStorageImageInstance
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80462fb57be8c3f89764774ea68e73a988f11643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501916"
---
# <a name="findmountedstorageimageinstance-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="20d7a-103">Método FindMountedStorageImageInstance da \_ classe imagens Msvm</span><span class="sxs-lookup"><span data-stu-id="20d7a-103">FindMountedStorageImageInstance method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="20d7a-104">Localiza um objeto [**Msvm \_ MountedStorageImage**](msvm-mountedstorageimage.md) para um determinado caminho de imagem de disco.</span><span class="sxs-lookup"><span data-stu-id="20d7a-104">Finds an [**Msvm\_MountedStorageImage**](msvm-mountedstorageimage.md) object for a given disk image path.</span></span>

## <a name="syntax"></a><span data-ttu-id="20d7a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20d7a-105">Syntax</span></span>


```mof
uint32 FindMountedStorageImageInstance(
  [in]  string                       SelectionCriterion,
  [in]  uint16                       CriterionType,
  [out] Msvm_MountedStorageImage REF Image
);
```



## <a name="parameters"></a><span data-ttu-id="20d7a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20d7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20d7a-107">*SelectionCriterion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20d7a-107">*SelectionCriterion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20d7a-108">Um caminho totalmente qualificado que especifica o local de um arquivo de imagem de disco.</span><span class="sxs-lookup"><span data-stu-id="20d7a-108">A fully-qualified path that specifies the location of a disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="20d7a-109">*Critériotype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20d7a-109">*CriterionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20d7a-110">O tipo de critério a ser pesquisado ao localizar a imagem do disco.</span><span class="sxs-lookup"><span data-stu-id="20d7a-110">The type of criterion to look for when finding the disk image.</span></span>

<dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20d7a-111">**desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="20d7a-111">**unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>

<span data-ttu-id="20d7a-112">**Caminho** (2)</span><span class="sxs-lookup"><span data-stu-id="20d7a-112">**Path** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="20d7a-113">*Imagem* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="20d7a-113">*Image* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20d7a-114">Uma referência ao [**Msvm \_ MountedStorageImage**](msvm-mountedstorageimage.md) (pode ser NULL se a imagem não estiver montada).</span><span class="sxs-lookup"><span data-stu-id="20d7a-114">A reference to the [**Msvm\_MountedStorageImage**](msvm-mountedstorageimage.md) (can be null if the image is not mounted).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20d7a-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="20d7a-115">Return value</span></span>

<span data-ttu-id="20d7a-116">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="20d7a-116">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="20d7a-117">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="20d7a-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="20d7a-118">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="20d7a-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="20d7a-119">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="20d7a-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="20d7a-120">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="20d7a-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="20d7a-121">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="20d7a-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="20d7a-122">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="20d7a-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="20d7a-123">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="20d7a-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="20d7a-124">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="20d7a-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="20d7a-125">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="20d7a-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="20d7a-126">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="20d7a-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="20d7a-127">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="20d7a-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="20d7a-128">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="20d7a-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="20d7a-129">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="20d7a-129">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="20d7a-130">**Objeto não encontrado** (32789)</span><span class="sxs-lookup"><span data-stu-id="20d7a-130">**Object not found** (32789)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="20d7a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20d7a-131">Requirements</span></span>



| <span data-ttu-id="20d7a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="20d7a-132">Requirement</span></span> | <span data-ttu-id="20d7a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="20d7a-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20d7a-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20d7a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="20d7a-135">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="20d7a-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="20d7a-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20d7a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="20d7a-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="20d7a-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="20d7a-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="20d7a-138">Namespace</span></span><br/>                | <span data-ttu-id="20d7a-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="20d7a-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="20d7a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="20d7a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20d7a-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20d7a-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="20d7a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="20d7a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20d7a-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="20d7a-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="20d7a-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="20d7a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20d7a-145">**Msvm \_ imagens**</span><span class="sxs-lookup"><span data-stu-id="20d7a-145">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




