---
description: Bloqueia ou libera a mídia.
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
ms.openlocfilehash: 4f9bce4e9e46d76c3426271af16c28026c242fa9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103837646"
---
# <a name="lockmedia-method-of-the-msvm_diskettedrive-class"></a><span data-ttu-id="0698b-103">Método LockMedia da \_ classe DisketteDrive Msvm</span><span class="sxs-lookup"><span data-stu-id="0698b-103">LockMedia method of the Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="0698b-104">Bloqueia ou libera a mídia.</span><span class="sxs-lookup"><span data-stu-id="0698b-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="0698b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0698b-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="0698b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0698b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0698b-107">*Bloquear* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0698b-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0698b-108">**true** para bloquear a mídia; **false** para liberar a mídia.</span><span class="sxs-lookup"><span data-stu-id="0698b-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0698b-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0698b-109">Return value</span></span>

<span data-ttu-id="0698b-110">Retorna um 0 em caso de êxito; caso contrário, retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="0698b-110">Returns a 0 on success; otherwise, returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="0698b-111">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="0698b-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0698b-112">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="0698b-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0698b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0698b-113">Requirements</span></span>



| <span data-ttu-id="0698b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0698b-114">Requirement</span></span> | <span data-ttu-id="0698b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0698b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0698b-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0698b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0698b-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0698b-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="0698b-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0698b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0698b-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0698b-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="0698b-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="0698b-120">Namespace</span></span><br/>                | <span data-ttu-id="0698b-121">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="0698b-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0698b-122">MOF</span><span class="sxs-lookup"><span data-stu-id="0698b-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0698b-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0698b-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0698b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0698b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0698b-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0698b-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0698b-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0698b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0698b-127">**Msvm \_ DisketteDrive**</span><span class="sxs-lookup"><span data-stu-id="0698b-127">**Msvm\_DisketteDrive**</span></span>](msvm-diskettedrive.md)
</dt> </dl>

 

 




