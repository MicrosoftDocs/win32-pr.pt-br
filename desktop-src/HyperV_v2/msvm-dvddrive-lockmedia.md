---
description: Bloqueia ou libera a mídia.
ms.assetid: 924bc20a-901b-4618-be49-eaacf80c9465
title: Método LockMedia da classe Msvm_DVDDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DVDDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 650a868d8e25e2ccc47271e49634827fe7d3d967
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104091893"
---
# <a name="lockmedia-method-of-the-msvm_dvddrive-class"></a><span data-ttu-id="5bac7-103">Método LockMedia da \_ classe DVDDrive Msvm</span><span class="sxs-lookup"><span data-stu-id="5bac7-103">LockMedia method of the Msvm\_DVDDrive class</span></span>

<span data-ttu-id="5bac7-104">Bloqueia ou libera a mídia.</span><span class="sxs-lookup"><span data-stu-id="5bac7-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bac7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5bac7-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="5bac7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5bac7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bac7-107">*Bloquear* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5bac7-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bac7-108">**true** para bloquear a mídia; **false** para liberar a mídia.</span><span class="sxs-lookup"><span data-stu-id="5bac7-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bac7-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5bac7-109">Return value</span></span>

<span data-ttu-id="5bac7-110">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="5bac7-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="5bac7-111">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="5bac7-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5bac7-112">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="5bac7-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5bac7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bac7-113">Requirements</span></span>



| <span data-ttu-id="5bac7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bac7-114">Requirement</span></span> | <span data-ttu-id="5bac7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5bac7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bac7-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bac7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5bac7-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5bac7-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="5bac7-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bac7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5bac7-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5bac7-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="5bac7-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="5bac7-120">Namespace</span></span><br/>                | <span data-ttu-id="5bac7-121">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5bac7-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5bac7-122">MOF</span><span class="sxs-lookup"><span data-stu-id="5bac7-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5bac7-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5bac7-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5bac7-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5bac7-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bac7-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5bac7-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5bac7-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bac7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bac7-127">**Msvm \_ DVDDrive**</span><span class="sxs-lookup"><span data-stu-id="5bac7-127">**Msvm\_DVDDrive**</span></span>](msvm-dvddrive.md)
</dt> </dl>

 

 




