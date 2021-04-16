---
title: Enumeração de DRM_HTTP_STATUS (Drmexternals. h)
description: O \_ tipo de enumeração de status http DRM \_ define um intervalo de Estados para uma solicitação de DRM.
ms.assetid: 9e0fb060-3fbf-45d0-872b-4d666ea9a88d
keywords:
- Formato de mídia do Windows de enumeração de DRM_HTTP_STATUS
- Formato de mídia do Windows de enumeração
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93d61803cab6cb80932402e429e77228a1611fd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757643"
---
# <a name="drm_http_status-enumeration-drmexternalsh"></a><span data-ttu-id="6b1eb-105">Enumeração de DRM_HTTP_STATUS (Drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="6b1eb-105">DRM_HTTP_STATUS enumeration (Drmexternals.h)</span></span>

<span data-ttu-id="6b1eb-106">O tipo de enumeração de **\_ \_ status http DRM** define um intervalo de Estados para uma solicitação de [*DRM*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="6b1eb-106">The **DRM\_HTTP\_STATUS** enumeration type defines a range of states for a [*DRM*](wmformat-glossary.md) request.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b1eb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b1eb-107">Syntax</span></span>


```C++
typedef enum DRM_HTTP_STATUS { 
  HTTP_NOTINITIATED  = 0,
  HTTP_CONNECTING    = 1,
  HTTP_REQUESTING    = 2,
  HTTP_RECEIVING     = 3,
  HTTP_COMPLETED     = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="6b1eb-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="6b1eb-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6b1eb-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP não \_ iniciado**</span><span class="sxs-lookup"><span data-stu-id="6b1eb-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP\_NOTINITIATED**</span></span>
</dt> <dd>

<span data-ttu-id="6b1eb-110">As operações HTTP não foram iniciadas.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-110">The HTTP operations have not been initiated.</span></span>

</dd> <dt>

<span data-ttu-id="6b1eb-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**\_conexão http**</span><span class="sxs-lookup"><span data-stu-id="6b1eb-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**HTTP\_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="6b1eb-112">A conexão está sendo estabelecida.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-112">The connection is being established.</span></span>

</dd> <dt>

<span data-ttu-id="6b1eb-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**\_solicitando http**</span><span class="sxs-lookup"><span data-stu-id="6b1eb-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP\_REQUESTING**</span></span>
</dt> <dd>

<span data-ttu-id="6b1eb-114">Os dados estão sendo solicitados.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-114">Data is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="6b1eb-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**recebimento de HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="6b1eb-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**HTTP\_RECEIVING**</span></span>
</dt> <dd>

<span data-ttu-id="6b1eb-116">Os dados estão sendo recebidos.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-116">Data is being received.</span></span>

</dd> <dt>

<span data-ttu-id="6b1eb-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="6b1eb-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP\_COMPLETED**</span></span>
</dt> <dd>

<span data-ttu-id="6b1eb-118">As operações HTTP foram concluídas.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-118">The HTTP operations are complete.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b1eb-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b1eb-119">Remarks</span></span>

<span data-ttu-id="6b1eb-120">Essa enumeração é usada pela estrutura [**de \_ \_ status individual do WM**](wm-individualize-status.md) .</span><span class="sxs-lookup"><span data-stu-id="6b1eb-120">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](wm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b1eb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b1eb-121">Requirements</span></span>



| <span data-ttu-id="6b1eb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b1eb-122">Requirement</span></span> | <span data-ttu-id="6b1eb-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6b1eb-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b1eb-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b1eb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6b1eb-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6b1eb-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6b1eb-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b1eb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6b1eb-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6b1eb-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6b1eb-128">Versão</span><span class="sxs-lookup"><span data-stu-id="6b1eb-128">Version</span></span><br/>                  | <span data-ttu-id="6b1eb-129">SDK do Windows Media Format 7 ou versões posteriores do SDK</span><span class="sxs-lookup"><span data-stu-id="6b1eb-129">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="6b1eb-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b1eb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b1eb-131"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b1eb-131"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b1eb-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b1eb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b1eb-133">**\_status de individualização de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="6b1eb-133">**DRM\_INDIVIDUALIZATION\_STATUS**</span></span>](drm-individualization-status.md)
</dt> <dt>

[<span data-ttu-id="6b1eb-134">**Tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="6b1eb-134">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





