---
description: Define ou Obtém o estado das cotas de disco do volume.
title: Propriedade DiskQuotaControl. Quotastate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaState
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b0766ecf-6e22-4481-a6a7-df873a277bc2
ms.openlocfilehash: 460decc1068642ae797723b31f7350082f591d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461260"
---
# <a name="diskquotacontrolquotastate-property"></a><span data-ttu-id="3871e-103">Propriedade DiskQuotaControl. Quotastate</span><span class="sxs-lookup"><span data-stu-id="3871e-103">DiskQuotaControl.QuotaState property</span></span>

<span data-ttu-id="3871e-104">Define ou Obtém o estado das cotas de disco do volume.</span><span class="sxs-lookup"><span data-stu-id="3871e-104">Sets or gets the state of the volume's disk quotas.</span></span>

<span data-ttu-id="3871e-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3871e-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3871e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3871e-106">Syntax</span></span>


```JScript
iQuotaState = DiskQuotaControl.QuotaState
DiskQuotaControl.QuotaState = iQuotaState
```



## <a name="property-value"></a><span data-ttu-id="3871e-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3871e-107">Property value</span></span>

<span data-ttu-id="3871e-108">Essa propriedade pode ser definida como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3871e-108">This property can be set to one of the following values.</span></span>



| <span data-ttu-id="3871e-109">Estado</span><span class="sxs-lookup"><span data-stu-id="3871e-109">State</span></span>          | <span data-ttu-id="3871e-110">Valor</span><span class="sxs-lookup"><span data-stu-id="3871e-110">Value</span></span> | <span data-ttu-id="3871e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="3871e-111">Description</span></span>               |
|----------------|-------|---------------------------|
| <span data-ttu-id="3871e-112">dqStateDisable</span><span class="sxs-lookup"><span data-stu-id="3871e-112">dqStateDisable</span></span> | <span data-ttu-id="3871e-113">0</span><span class="sxs-lookup"><span data-stu-id="3871e-113">0</span></span>     | <span data-ttu-id="3871e-114">As cotas de disco estão desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="3871e-114">Disk quotas are disabled.</span></span> |
| <span data-ttu-id="3871e-115">dqStateTrack</span><span class="sxs-lookup"><span data-stu-id="3871e-115">dqStateTrack</span></span>   | <span data-ttu-id="3871e-116">1</span><span class="sxs-lookup"><span data-stu-id="3871e-116">1</span></span>     | <span data-ttu-id="3871e-117">As cotas de disco estão desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="3871e-117">Disk quotas are disabled.</span></span> |
| <span data-ttu-id="3871e-118">dqStateEnforce</span><span class="sxs-lookup"><span data-stu-id="3871e-118">dqStateEnforce</span></span> | <span data-ttu-id="3871e-119">2</span><span class="sxs-lookup"><span data-stu-id="3871e-119">2</span></span>     | <span data-ttu-id="3871e-120">Impor o limite de cota.</span><span class="sxs-lookup"><span data-stu-id="3871e-120">Enforce quota limit.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="3871e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3871e-121">Requirements</span></span>



| <span data-ttu-id="3871e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3871e-122">Requirement</span></span> | <span data-ttu-id="3871e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3871e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3871e-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3871e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3871e-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3871e-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3871e-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3871e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3871e-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3871e-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3871e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3871e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3871e-129"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="3871e-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3871e-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="3871e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3871e-131">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="3871e-131">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




