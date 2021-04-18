---
title: Enumeração de DRM_HTTP_STATUS (wmdrmsdk. h)
description: O \_ \_ tipo de enumeração de status http DRM define um intervalo de Estados http para uma solicitação de DRM.
ms.assetid: 09183ef9-4832-4469-a960-dbeb67381949
keywords:
- Formato de mídia do Windows de enumeração de DRM_HTTP_STATUS
- Formato de mídia do Windows de enumeração
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 367c5a40af45fd573f7f5033b9be3b037079cb30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764483"
---
# <a name="drm_http_status-enumeration-wmdrmsdkh"></a><span data-ttu-id="a20bc-105">Enumeração de DRM_HTTP_STATUS (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="a20bc-105">DRM_HTTP_STATUS enumeration (Wmdrmsdk.h)</span></span>

<span data-ttu-id="a20bc-106">O tipo de enumeração de **\_ \_ status http DRM** define um intervalo de Estados http para uma solicitação de DRM.</span><span class="sxs-lookup"><span data-stu-id="a20bc-106">The **DRM\_HTTP\_STATUS** enumeration type defines a range of HTTP states for a DRM request.</span></span>

## <a name="syntax"></a><span data-ttu-id="a20bc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a20bc-107">Syntax</span></span>


```C++
typedef enum DRM_HTTP_STATUS { 
  HTTP_NOTINITIATED  = 0,
  HTTP_CONNECTING    = 1,
  HTTP_REQUESTING    = 2,
  HTTP_RECEIVING     = 3,
  HTTP_COMPLETED     = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="a20bc-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="a20bc-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a20bc-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP não \_ iniciado**</span><span class="sxs-lookup"><span data-stu-id="a20bc-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP\_NOTINITIATED**</span></span>
</dt> <dd>

<span data-ttu-id="a20bc-110">As operações HTTP não foram iniciadas.</span><span class="sxs-lookup"><span data-stu-id="a20bc-110">The HTTP operations have not been initiated.</span></span>

</dd> <dt>

<span data-ttu-id="a20bc-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**\_conexão http**</span><span class="sxs-lookup"><span data-stu-id="a20bc-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**HTTP\_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="a20bc-112">A conexão está sendo estabelecida.</span><span class="sxs-lookup"><span data-stu-id="a20bc-112">The connection is being established.</span></span>

</dd> <dt>

<span data-ttu-id="a20bc-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**\_solicitando http**</span><span class="sxs-lookup"><span data-stu-id="a20bc-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP\_REQUESTING**</span></span>
</dt> <dd>

<span data-ttu-id="a20bc-114">Os dados estão sendo solicitados.</span><span class="sxs-lookup"><span data-stu-id="a20bc-114">Data is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="a20bc-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**recebimento de HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="a20bc-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**HTTP\_RECEIVING**</span></span>
</dt> <dd>

<span data-ttu-id="a20bc-116">Os dados estão sendo recebidos.</span><span class="sxs-lookup"><span data-stu-id="a20bc-116">Data is being received.</span></span>

</dd> <dt>

<span data-ttu-id="a20bc-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="a20bc-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP\_COMPLETED**</span></span>
</dt> <dd>

<span data-ttu-id="a20bc-118">As operações HTTP foram concluídas.</span><span class="sxs-lookup"><span data-stu-id="a20bc-118">The HTTP operations are complete.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a20bc-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="a20bc-119">Remarks</span></span>

<span data-ttu-id="a20bc-120">Essa enumeração é usada pela estrutura [**de \_ \_ status individual do WM**](drmwm-individualize-status.md) .</span><span class="sxs-lookup"><span data-stu-id="a20bc-120">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a20bc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a20bc-121">Requirements</span></span>



| <span data-ttu-id="a20bc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a20bc-122">Requirement</span></span> | <span data-ttu-id="a20bc-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a20bc-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a20bc-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a20bc-124">Header</span></span><br/> | <dl> <span data-ttu-id="a20bc-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="a20bc-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a20bc-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="a20bc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a20bc-127">**Tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="a20bc-127">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





