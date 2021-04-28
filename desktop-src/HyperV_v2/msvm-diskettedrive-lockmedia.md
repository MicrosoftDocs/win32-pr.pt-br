---
description: Método LockMedia da classe Msvm_DisketteDrive-bloqueia ou libera a mídia.
ms.assetid: 90f7e06c-92d0-4742-a74d-68ae6bfc00bf
title: Método LockMedia da classe Msvm_DisketteDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5f5f87354aa7c39534e8b32c8985c5d18b55caa9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111966"
---
# <a name="lockmedia-method-of-the-msvm_diskettedrive-class"></a><span data-ttu-id="e06b6-103">Método LockMedia da \_ classe DisketteDrive Msvm</span><span class="sxs-lookup"><span data-stu-id="e06b6-103">LockMedia method of the Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="e06b6-104">Bloqueia ou libera a mídia.</span><span class="sxs-lookup"><span data-stu-id="e06b6-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="e06b6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e06b6-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="e06b6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e06b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e06b6-107">*Bloquear* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e06b6-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e06b6-108">**true** para bloquear a mídia; **false** para liberar a mídia.</span><span class="sxs-lookup"><span data-stu-id="e06b6-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e06b6-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e06b6-109">Return value</span></span>

<span data-ttu-id="e06b6-110">Retorna um 0 em caso de êxito; caso contrário, retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="e06b6-110">Returns a 0 on success; otherwise, returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="e06b6-111">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="e06b6-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e06b6-112">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="e06b6-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e06b6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e06b6-113">Requirements</span></span>



| <span data-ttu-id="e06b6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e06b6-114">Requirement</span></span> | <span data-ttu-id="e06b6-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e06b6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e06b6-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e06b6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e06b6-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e06b6-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="e06b6-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e06b6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e06b6-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e06b6-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="e06b6-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="e06b6-120">Namespace</span></span><br/>                | <span data-ttu-id="e06b6-121">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e06b6-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e06b6-122">MOF</span><span class="sxs-lookup"><span data-stu-id="e06b6-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e06b6-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e06b6-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e06b6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e06b6-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e06b6-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e06b6-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e06b6-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e06b6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e06b6-127">**Msvm \_ DisketteDrive**</span><span class="sxs-lookup"><span data-stu-id="e06b6-127">**Msvm\_DisketteDrive**</span></span>](msvm-diskettedrive.md)
</dt> </dl>

 

 




