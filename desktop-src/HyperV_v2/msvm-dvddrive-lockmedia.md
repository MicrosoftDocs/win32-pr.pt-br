---
description: Método LockMedia da classe Msvm_DVDDrive-bloqueia ou libera a mídia.
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
ms.openlocfilehash: e00780fbeeeec60563b31008c8e5979a09f9d173
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119144"
---
# <a name="lockmedia-method-of-the-msvm_dvddrive-class"></a><span data-ttu-id="67ec1-103">Método LockMedia da \_ classe DVDDrive Msvm</span><span class="sxs-lookup"><span data-stu-id="67ec1-103">LockMedia method of the Msvm\_DVDDrive class</span></span>

<span data-ttu-id="67ec1-104">Bloqueia ou libera a mídia.</span><span class="sxs-lookup"><span data-stu-id="67ec1-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ec1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67ec1-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="67ec1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67ec1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67ec1-107">*Bloquear* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="67ec1-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67ec1-108">**true** para bloquear a mídia; **false** para liberar a mídia.</span><span class="sxs-lookup"><span data-stu-id="67ec1-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67ec1-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="67ec1-109">Return value</span></span>

<span data-ttu-id="67ec1-110">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="67ec1-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="67ec1-111">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="67ec1-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="67ec1-112">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="67ec1-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="67ec1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67ec1-113">Requirements</span></span>



| <span data-ttu-id="67ec1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="67ec1-114">Requirement</span></span> | <span data-ttu-id="67ec1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="67ec1-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67ec1-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67ec1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="67ec1-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="67ec1-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="67ec1-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67ec1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="67ec1-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="67ec1-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="67ec1-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="67ec1-120">Namespace</span></span><br/>                | <span data-ttu-id="67ec1-121">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="67ec1-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="67ec1-122">MOF</span><span class="sxs-lookup"><span data-stu-id="67ec1-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67ec1-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67ec1-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="67ec1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="67ec1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67ec1-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="67ec1-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="67ec1-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="67ec1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67ec1-127">**Msvm \_ DVDDrive**</span><span class="sxs-lookup"><span data-stu-id="67ec1-127">**Msvm\_DVDDrive**</span></span>](msvm-dvddrive.md)
</dt> </dl>

 

 




