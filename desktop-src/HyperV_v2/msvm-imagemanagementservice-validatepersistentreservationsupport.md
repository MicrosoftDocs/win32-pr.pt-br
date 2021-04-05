---
description: Valida se um sistema de arquivos pode dar suporte a um disco rígido virtual com reservas persistentes habilitadas.
ms.assetid: c5fed9d5-0fa6-4b96-ae6e-84468b011e2a
title: Método ValidatePersistentReservationSupport da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ValidatePersistentReservationSupport
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 596e5cf840ee65dc0b3ad5315462db4666c8b262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921019"
---
# <a name="validatepersistentreservationsupport-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="89dcb-103">Método ValidatePersistentReservationSupport da \_ classe imagens Msvm</span><span class="sxs-lookup"><span data-stu-id="89dcb-103">ValidatePersistentReservationSupport method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="89dcb-104">Valida se um sistema de arquivos pode dar suporte a um disco rígido virtual com reservas persistentes habilitadas.</span><span class="sxs-lookup"><span data-stu-id="89dcb-104">Validates whether a file system can support a virtual hard disk with persistent reservations enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="89dcb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89dcb-105">Syntax</span></span>


```mof
uint32 ValidatePersistentReservationSupport(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="89dcb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89dcb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89dcb-107">*Caminho* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="89dcb-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89dcb-108">Um caminho totalmente qualificado que especifica o local de um arquivo de imagem de disco ou um diretório no qual um arquivo de imagem de disco pode ser colocado.</span><span class="sxs-lookup"><span data-stu-id="89dcb-108">A fully-qualified path that specifies the location of a disk image file or a directory in which a disk image file might be placed.</span></span>

</dd> <dt>

<span data-ttu-id="89dcb-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="89dcb-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89dcb-110">Uma referência ao trabalho (pode ser NULL se a tarefa for concluída com êxito).</span><span class="sxs-lookup"><span data-stu-id="89dcb-110">A reference to the job (can be null if the task is completed succesfully).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89dcb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="89dcb-111">Return value</span></span>

<span data-ttu-id="89dcb-112">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="89dcb-112">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="89dcb-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="89dcb-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="89dcb-114">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="89dcb-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="89dcb-115">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="89dcb-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="89dcb-116">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="89dcb-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="89dcb-117">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="89dcb-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="89dcb-118">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="89dcb-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="89dcb-119">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="89dcb-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="89dcb-120">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="89dcb-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="89dcb-121">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="89dcb-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="89dcb-122">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="89dcb-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="89dcb-123">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="89dcb-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="89dcb-124">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="89dcb-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="89dcb-125">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="89dcb-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="89dcb-126">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="89dcb-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="89dcb-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89dcb-127">Requirements</span></span>



| <span data-ttu-id="89dcb-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="89dcb-128">Requirement</span></span> | <span data-ttu-id="89dcb-129">Valor</span><span class="sxs-lookup"><span data-stu-id="89dcb-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89dcb-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89dcb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="89dcb-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="89dcb-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="89dcb-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89dcb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="89dcb-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="89dcb-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="89dcb-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="89dcb-134">Namespace</span></span><br/>                | <span data-ttu-id="89dcb-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="89dcb-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="89dcb-136">MOF</span><span class="sxs-lookup"><span data-stu-id="89dcb-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89dcb-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89dcb-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="89dcb-138">DLL</span><span class="sxs-lookup"><span data-stu-id="89dcb-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89dcb-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="89dcb-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="89dcb-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="89dcb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89dcb-141">**Msvm \_ imagens**</span><span class="sxs-lookup"><span data-stu-id="89dcb-141">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




