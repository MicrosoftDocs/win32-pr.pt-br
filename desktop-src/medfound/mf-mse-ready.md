---
description: Define os diferentes Estados prontos da extensão de origem de mídia.
ms.assetid: 7455B92F-CC2D-4743-935D-F5EBFD834397
title: Enumeração de MF_MSE_READY
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_READY
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: bff2155a2cb2cb21d4c25d868f95472f47f15b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828622"
---
# <a name="mf_mse_ready-enumeration"></a><span data-ttu-id="f69e1-103">\_ \_ Enumeração pronta do MF MSE</span><span class="sxs-lookup"><span data-stu-id="f69e1-103">MF\_MSE\_READY enumeration</span></span>

<span data-ttu-id="f69e1-104">Define os diferentes Estados prontos da extensão de origem de mídia.</span><span class="sxs-lookup"><span data-stu-id="f69e1-104">Defines the different ready states of the Media Source Extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="f69e1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f69e1-105">Syntax</span></span>


```C++
typedef enum _MF_MSE_READY { 
  MF_MSE_READY_CLOSED  = 1,
  MF_MSE_READY_OPEN    = 2,
  MF_MSE_READY_ENDED   = 3
} MF_MSE_READY;
```



## <a name="constants"></a><span data-ttu-id="f69e1-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="f69e1-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f69e1-107"><span id="MF_MSE_READY_CLOSED"></span><span id="mf_mse_ready_closed"></span>**MF \_ MSE \_ pronto \_ fechado**</span><span class="sxs-lookup"><span data-stu-id="f69e1-107"><span id="MF_MSE_READY_CLOSED"></span><span id="mf_mse_ready_closed"></span>**MF\_MSE\_READY\_CLOSED**</span></span>
</dt> <dd>

<span data-ttu-id="f69e1-108">A origem da mídia está fechada.</span><span class="sxs-lookup"><span data-stu-id="f69e1-108">The media source is closed.</span></span>

</dd> <dt>

<span data-ttu-id="f69e1-109"><span id="MF_MSE_READY_OPEN"></span><span id="mf_mse_ready_open"></span>**MF \_ MSE \_ pronto \_ aberto**</span><span class="sxs-lookup"><span data-stu-id="f69e1-109"><span id="MF_MSE_READY_OPEN"></span><span id="mf_mse_ready_open"></span>**MF\_MSE\_READY\_OPEN**</span></span>
</dt> <dd>

<span data-ttu-id="f69e1-110">A origem da mídia está aberta.</span><span class="sxs-lookup"><span data-stu-id="f69e1-110">The media source is open.</span></span>

</dd> <dt>

<span data-ttu-id="f69e1-111"><span id="MF_MSE_READY_ENDED"></span><span id="mf_mse_ready_ended"></span>**o MF \_ MSE \_ pronto \_ terminou**</span><span class="sxs-lookup"><span data-stu-id="f69e1-111"><span id="MF_MSE_READY_ENDED"></span><span id="mf_mse_ready_ended"></span>**MF\_MSE\_READY\_ENDED**</span></span>
</dt> <dd>

<span data-ttu-id="f69e1-112">A origem da mídia foi encerrada.</span><span class="sxs-lookup"><span data-stu-id="f69e1-112">The media source is ended.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f69e1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f69e1-113">Requirements</span></span>



| <span data-ttu-id="f69e1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f69e1-114">Requirement</span></span> | <span data-ttu-id="f69e1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f69e1-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f69e1-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f69e1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f69e1-117">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f69e1-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f69e1-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f69e1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f69e1-119">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="f69e1-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f69e1-120">INSERI</span><span class="sxs-lookup"><span data-stu-id="f69e1-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f69e1-121"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f69e1-121"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f69e1-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="f69e1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f69e1-123">Enumerações de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f69e1-123">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




