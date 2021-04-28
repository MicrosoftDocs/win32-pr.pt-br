---
description: Método GetError da classe Msvm_VirtualSystemReferencePointExportJob – recupera o erro.
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
ms.openlocfilehash: d1311e4e56b6396266ece72277e8ddadcdb9d835
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109334"
---
# <a name="geterror-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="b5a28-103">Método GetError da \_ classe Msvm VirtualSystemReferencePointExportJob</span><span class="sxs-lookup"><span data-stu-id="b5a28-103">GetError method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="b5a28-104">Recupera o erro.</span><span class="sxs-lookup"><span data-stu-id="b5a28-104">Retrieves the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5a28-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5a28-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="b5a28-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5a28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5a28-107">*Erro* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="b5a28-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5a28-108">O erro recuperado.</span><span class="sxs-lookup"><span data-stu-id="b5a28-108">The error retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5a28-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b5a28-109">Return value</span></span>

<span data-ttu-id="b5a28-110">Em caso de sucesso, retorna um 0; caso contrário, o contém um erro.</span><span class="sxs-lookup"><span data-stu-id="b5a28-110">On success, returns a 0; otherwise, contains an error.</span></span>

<dl> <dt>

<span data-ttu-id="b5a28-111">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="b5a28-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b5a28-112">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="b5a28-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b5a28-113">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="b5a28-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b5a28-114">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="b5a28-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b5a28-115">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="b5a28-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b5a28-116">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="b5a28-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b5a28-117">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="b5a28-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b5a28-118">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="b5a28-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b5a28-119">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="b5a28-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b5a28-120">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="b5a28-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b5a28-121">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="b5a28-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b5a28-122">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="b5a28-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b5a28-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5a28-123">Requirements</span></span>



| <span data-ttu-id="b5a28-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5a28-124">Requirement</span></span> | <span data-ttu-id="b5a28-125">Valor</span><span class="sxs-lookup"><span data-stu-id="b5a28-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5a28-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5a28-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b5a28-127">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="b5a28-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b5a28-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5a28-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b5a28-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b5a28-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b5a28-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5a28-130">Namespace</span></span><br/>                | <span data-ttu-id="b5a28-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b5a28-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b5a28-132">MOF</span><span class="sxs-lookup"><span data-stu-id="b5a28-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5a28-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5a28-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5a28-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b5a28-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5a28-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b5a28-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b5a28-136">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b5a28-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5a28-137">**Msvm \_ VirtualSystemReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="b5a28-137">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




