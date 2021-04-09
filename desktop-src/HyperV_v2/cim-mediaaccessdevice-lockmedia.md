---
description: Bloqueia e desbloqueia a mídia em um dispositivo de acesso removível.
ms.assetid: 357ee552-82d0-4201-bcc2-0acf208e16a0
title: Método LockMedia da classe CIM_MediaAccessDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 12c4aa6c6ba9e57a2ab88e58624b246fb98065f3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104011911"
---
# <a name="lockmedia-method-of-the-cim_mediaaccessdevice-class"></a><span data-ttu-id="fbbe0-103">Método LockMedia da \_ classe MEDIAACCESSDEVICE CIM</span><span class="sxs-lookup"><span data-stu-id="fbbe0-103">LockMedia method of the CIM\_MediaAccessDevice class</span></span>

<span data-ttu-id="fbbe0-104">Bloqueia e desbloqueia a mídia em um dispositivo de acesso removível.</span><span class="sxs-lookup"><span data-stu-id="fbbe0-104">Locks and unlocks the media in a removeable access device.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbbe0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fbbe0-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="fbbe0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbbe0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbbe0-107">*Bloquear* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fbbe0-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbbe0-108">Se **for true**, bloqueará a mídia.</span><span class="sxs-lookup"><span data-stu-id="fbbe0-108">If **TRUE**, locks the media.</span></span> <span data-ttu-id="fbbe0-109">Se **for false**, libera a mídia.</span><span class="sxs-lookup"><span data-stu-id="fbbe0-109">If **FALSE**, releases the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbbe0-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fbbe0-110">Return value</span></span>

<span data-ttu-id="fbbe0-111">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="fbbe0-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbbe0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbbe0-112">Requirements</span></span>



| <span data-ttu-id="fbbe0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbbe0-113">Requirement</span></span> | <span data-ttu-id="fbbe0-114">Valor</span><span class="sxs-lookup"><span data-stu-id="fbbe0-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbbe0-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbbe0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fbbe0-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fbbe0-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="fbbe0-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbbe0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fbbe0-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fbbe0-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="fbbe0-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="fbbe0-119">Namespace</span></span><br/>                | <span data-ttu-id="fbbe0-120">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="fbbe0-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fbbe0-121">MOF</span><span class="sxs-lookup"><span data-stu-id="fbbe0-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbbe0-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fbbe0-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbbe0-123">DLL</span><span class="sxs-lookup"><span data-stu-id="fbbe0-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbbe0-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fbbe0-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fbbe0-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbbe0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbbe0-126">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="fbbe0-126">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

 




