---
description: Define ou obtém o estado das cotas de disco do volume.
title: Propriedade DiskQuotaControl.QuotaState
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
ms.openlocfilehash: 3580ad47a5ec6a5d0276dc0e30a4a6463aca2fb3
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843187"
---
# <a name="diskquotacontrolquotastate-property"></a><span data-ttu-id="e9a21-103">Propriedade DiskQuotaControl.QuotaState</span><span class="sxs-lookup"><span data-stu-id="e9a21-103">DiskQuotaControl.QuotaState property</span></span>

<span data-ttu-id="e9a21-104">Define ou obtém o estado das cotas de disco do volume.</span><span class="sxs-lookup"><span data-stu-id="e9a21-104">Sets or gets the state of the volume's disk quotas.</span></span>

<span data-ttu-id="e9a21-105">Essa propriedade é leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e9a21-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9a21-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9a21-106">Syntax</span></span>


```JScript
iQuotaState = DiskQuotaControl.QuotaState
DiskQuotaControl.QuotaState = iQuotaState
```



## <a name="property-value"></a><span data-ttu-id="e9a21-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e9a21-107">Property value</span></span>

<span data-ttu-id="e9a21-108">Essa propriedade pode ser definida como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e9a21-108">This property can be set to one of the following values.</span></span>



| <span data-ttu-id="e9a21-109">Estado</span><span class="sxs-lookup"><span data-stu-id="e9a21-109">State</span></span>          | <span data-ttu-id="e9a21-110">Valor</span><span class="sxs-lookup"><span data-stu-id="e9a21-110">Value</span></span> | <span data-ttu-id="e9a21-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="e9a21-111">Description</span></span>               |
|----------------|-------|---------------------------|
| <span data-ttu-id="e9a21-112">dqStateDisable</span><span class="sxs-lookup"><span data-stu-id="e9a21-112">dqStateDisable</span></span> | <span data-ttu-id="e9a21-113">0</span><span class="sxs-lookup"><span data-stu-id="e9a21-113">0</span></span>     | <span data-ttu-id="e9a21-114">As cotas de disco estão desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="e9a21-114">Disk quotas are disabled.</span></span> |
| <span data-ttu-id="e9a21-115">dqStateTrack</span><span class="sxs-lookup"><span data-stu-id="e9a21-115">dqStateTrack</span></span>   | <span data-ttu-id="e9a21-116">1</span><span class="sxs-lookup"><span data-stu-id="e9a21-116">1</span></span>     | <span data-ttu-id="e9a21-117">As cotas de disco estão desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="e9a21-117">Disk quotas are disabled.</span></span> |
| <span data-ttu-id="e9a21-118">dqStateEnforce</span><span class="sxs-lookup"><span data-stu-id="e9a21-118">dqStateEnforce</span></span> | <span data-ttu-id="e9a21-119">2</span><span class="sxs-lookup"><span data-stu-id="e9a21-119">2</span></span>     | <span data-ttu-id="e9a21-120">Impor limite de cota.</span><span class="sxs-lookup"><span data-stu-id="e9a21-120">Enforce quota limit.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="e9a21-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9a21-121">Requirements</span></span>



| <span data-ttu-id="e9a21-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9a21-122">Requirement</span></span> | <span data-ttu-id="e9a21-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e9a21-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9a21-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9a21-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e9a21-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e9a21-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e9a21-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9a21-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e9a21-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e9a21-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e9a21-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e9a21-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9a21-129"><dt>Shell32.dll (versão 5.0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e9a21-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9a21-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9a21-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9a21-131">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="e9a21-131">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




