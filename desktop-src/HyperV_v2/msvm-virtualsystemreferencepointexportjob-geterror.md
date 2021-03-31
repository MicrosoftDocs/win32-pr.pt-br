---
description: Recupera o erro.
ms.assetid: a30cb74a-4e41-4981-b355-6f46b4b75ce6
title: Método GetError da classe Msvm_VirtualSystemReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b26995171059389f7f7afb3fb90e3506b39affd5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104011916"
---
# <a name="geterror-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="eb612-103">Método GetError da \_ classe Msvm VirtualSystemReferencePointExportJob</span><span class="sxs-lookup"><span data-stu-id="eb612-103">GetError method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="eb612-104">Recupera o erro.</span><span class="sxs-lookup"><span data-stu-id="eb612-104">Retrieves the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb612-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb612-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="eb612-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb612-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb612-107">*Erro* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="eb612-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb612-108">O erro recuperado.</span><span class="sxs-lookup"><span data-stu-id="eb612-108">The error retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb612-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb612-109">Return value</span></span>

<span data-ttu-id="eb612-110">Em caso de sucesso, retorna um 0; caso contrário, o contém um erro.</span><span class="sxs-lookup"><span data-stu-id="eb612-110">On success, returns a 0; otherwise, contains an error.</span></span>

<dl> <dt>

<span data-ttu-id="eb612-111">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="eb612-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="eb612-112">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="eb612-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="eb612-113">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="eb612-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="eb612-114">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="eb612-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="eb612-115">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="eb612-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="eb612-116">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="eb612-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="eb612-117">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="eb612-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="eb612-118">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="eb612-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="eb612-119">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="eb612-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="eb612-120">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="eb612-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="eb612-121">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="eb612-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="eb612-122">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="eb612-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="eb612-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb612-123">Requirements</span></span>



| <span data-ttu-id="eb612-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb612-124">Requirement</span></span> | <span data-ttu-id="eb612-125">Valor</span><span class="sxs-lookup"><span data-stu-id="eb612-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb612-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb612-126">Minimum supported client</span></span><br/> | <span data-ttu-id="eb612-127">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="eb612-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="eb612-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb612-128">Minimum supported server</span></span><br/> | <span data-ttu-id="eb612-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="eb612-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="eb612-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="eb612-130">Namespace</span></span><br/>                | <span data-ttu-id="eb612-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="eb612-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="eb612-132">MOF</span><span class="sxs-lookup"><span data-stu-id="eb612-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb612-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb612-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb612-134">DLL</span><span class="sxs-lookup"><span data-stu-id="eb612-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb612-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eb612-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eb612-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb612-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb612-137">**Msvm \_ VirtualSystemReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="eb612-137">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




