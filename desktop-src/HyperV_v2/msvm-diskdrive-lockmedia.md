---
description: Bloqueia ou desbloqueia a mídia.
ms.assetid: 805efb2d-71a7-4c74-821f-942644928ff9
title: Método LockMedia da classe Msvm_DiskDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7ddc082ca6ceb7141eaa42bdfddf7a97897a9240
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105775730"
---
# <a name="lockmedia-method-of-the-msvm_diskdrive-class"></a><span data-ttu-id="92fe4-103">Método LockMedia da \_ classe DiskDrive Msvm</span><span class="sxs-lookup"><span data-stu-id="92fe4-103">LockMedia method of the Msvm\_DiskDrive class</span></span>

<span data-ttu-id="92fe4-104">Bloqueia ou desbloqueia a mídia.</span><span class="sxs-lookup"><span data-stu-id="92fe4-104">Locks or unlocks the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="92fe4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92fe4-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="92fe4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92fe4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92fe4-107">*Bloquear* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="92fe4-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92fe4-108">**true** para bloquear a mídia; **false** para liberar a mídia.</span><span class="sxs-lookup"><span data-stu-id="92fe4-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92fe4-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="92fe4-109">Return value</span></span>

<span data-ttu-id="92fe4-110">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="92fe4-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="92fe4-111">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="92fe4-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="92fe4-112">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="92fe4-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="92fe4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92fe4-113">Requirements</span></span>



| <span data-ttu-id="92fe4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="92fe4-114">Requirement</span></span> | <span data-ttu-id="92fe4-115">Valor</span><span class="sxs-lookup"><span data-stu-id="92fe4-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92fe4-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92fe4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="92fe4-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="92fe4-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="92fe4-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92fe4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="92fe4-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="92fe4-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="92fe4-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="92fe4-120">Namespace</span></span><br/>                | <span data-ttu-id="92fe4-121">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="92fe4-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="92fe4-122">MOF</span><span class="sxs-lookup"><span data-stu-id="92fe4-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92fe4-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92fe4-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="92fe4-124">DLL</span><span class="sxs-lookup"><span data-stu-id="92fe4-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92fe4-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="92fe4-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="92fe4-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="92fe4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92fe4-127">**Msvm \_ DiskDrive**</span><span class="sxs-lookup"><span data-stu-id="92fe4-127">**Msvm\_DiskDrive**</span></span>](msvm-diskdrive.md)
</dt> </dl>

 

 




