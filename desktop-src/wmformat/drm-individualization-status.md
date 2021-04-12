---
title: Enumeração de DRM_INDIVIDUALIZATION_STATUS (Drmexternals. h)
description: O \_ tipo de enumeração status de individualização de DRM \_ define os Estados válidos para individualização de DRM. | Enumeração de DRM_INDIVIDUALIZATION_STATUS (Drmexternals. h)
ms.assetid: 76748fb3-340e-47e2-969d-5e857bb4e4d8
keywords:
- Formato de mídia do Windows de enumeração de DRM_INDIVIDUALIZATION_STATUS
- Formato de mídia do Windows de enumeração
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d59a19c58c775ee22d78e17bc09add2825948e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104370903"
---
# <a name="drm_individualization_status-enumeration-drmexternalsh"></a><span data-ttu-id="4a2b1-106">Enumeração de DRM_INDIVIDUALIZATION_STATUS (Drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="4a2b1-106">DRM_INDIVIDUALIZATION_STATUS enumeration (Drmexternals.h)</span></span>

<span data-ttu-id="4a2b1-107">O tipo de enumeração **\_ \_ status de individualização de DRM** define os Estados válidos para [*individualização*](wmformat-glossary.md)de DRM.</span><span class="sxs-lookup"><span data-stu-id="4a2b1-107">The **DRM\_INDIVIDUALIZATION\_STATUS** enumeration type defines the valid states for DRM [*individualization*](wmformat-glossary.md).</span></span> <span data-ttu-id="4a2b1-108">Quando um aplicativo inicia a individualização com uma chamada para [**IWMDRMReader:: individualize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize), o progresso da solicitação de individualização é transmitido para o aplicativo por meio de chamadas para o método [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) .</span><span class="sxs-lookup"><span data-stu-id="4a2b1-108">When an application initiates individualization with a call to [**IWMDRMReader::Individualize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize), the progress of the individualization request is conveyed to the application through calls to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method.</span></span> <span data-ttu-id="4a2b1-109">As mensagens de status de individualização usarão o \_ membro WMT individualize do tipo de enumeração [**\_ status WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) como o parâmetro *status* .</span><span class="sxs-lookup"><span data-stu-id="4a2b1-109">Individualization status messages will all use the WMT\_INDIVIDUALIZE member of the [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) enumeration type as the *Status* parameter.</span></span> <span data-ttu-id="4a2b1-110">O status da individualização é passado para **OnStatus** *no parâmetro de* física.</span><span class="sxs-lookup"><span data-stu-id="4a2b1-110">The status of the individualization is passed to **OnStatus** in the *pValue* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a2b1-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a2b1-111">Syntax</span></span>


```C++
typedef enum DRM_INDIVIDUALIZATION_STATUS { 
  INDI_UNDEFINED  = 0x0000,
  INDI_BEGIN      = 0x0001,
  INDI_SUCCEED    = 0x0002,
  INDI_FAIL       = 0x0004,
  INDI_CANCEL     = 0x0008,
  INDI_DOWNLOAD   = 0x0010,
  INDI_INSTALL    = 0x0020
} ;
```



## <a name="constants"></a><span data-ttu-id="4a2b1-112">Constantes</span><span class="sxs-lookup"><span data-stu-id="4a2b1-112">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4a2b1-113"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**i \_ INdefinido**</span><span class="sxs-lookup"><span data-stu-id="4a2b1-113"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="4a2b1-114">Este valor está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="4a2b1-114">This value is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="4a2b1-115"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**início do i \_**</span><span class="sxs-lookup"><span data-stu-id="4a2b1-115"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI\_BEGIN**</span></span>
</dt> <dd>

<span data-ttu-id="4a2b1-116">Indica o início do processo de individualização.</span><span class="sxs-lookup"><span data-stu-id="4a2b1-116">Indicates the start of the individualization process.</span></span>

</dd> <dt>

<span data-ttu-id="4a2b1-117"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**i com \_ sucesso**</span><span class="sxs-lookup"><span data-stu-id="4a2b1-117"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI\_SUCCEED**</span></span>
</dt> <dd>

<span data-ttu-id="4a2b1-118">Indica que o processo de individualização foi concluído.</span><span class="sxs-lookup"><span data-stu-id="4a2b1-118">Indicates that the individualization process has been completed.</span></span>

</dd> <dt>

<span data-ttu-id="4a2b1-119"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**falha de i \_**</span><span class="sxs-lookup"><span data-stu-id="4a2b1-119"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**INDI\_FAIL**</span></span>
</dt> <dd>

<span data-ttu-id="4a2b1-120">Indica que o processo de individualização falhou.</span><span class="sxs-lookup"><span data-stu-id="4a2b1-120">Indicates that the individualization process failed.</span></span>

</dd> <dt>

<span data-ttu-id="4a2b1-121"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**i \_ cancelar**</span><span class="sxs-lookup"><span data-stu-id="4a2b1-121"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI\_CANCEL**</span></span>
</dt> <dd>

<span data-ttu-id="4a2b1-122">Indica que o processo de individualização foi cancelado como resultado de uma chamada para [**IWMDRMReader:: CancelIndividualization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization).</span><span class="sxs-lookup"><span data-stu-id="4a2b1-122">Indicates that the individualization process was canceled as the result of a call to [**IWMDRMReader::CancelIndividualization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization).</span></span>

</dd> <dt>

<span data-ttu-id="4a2b1-123"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**Download do i \_**</span><span class="sxs-lookup"><span data-stu-id="4a2b1-123"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**INDI\_DOWNLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="4a2b1-124">Indica que a atualização de segurança está sendo baixada.</span><span class="sxs-lookup"><span data-stu-id="4a2b1-124">Indicates that the security upgrade is being downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="4a2b1-125"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**i \_ instalar**</span><span class="sxs-lookup"><span data-stu-id="4a2b1-125"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**INDI\_INSTALL**</span></span>
</dt> <dd>

<span data-ttu-id="4a2b1-126">Indica que a atualização de segurança está sendo instalada.</span><span class="sxs-lookup"><span data-stu-id="4a2b1-126">Indicates that the security upgrade is being installed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a2b1-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a2b1-127">Remarks</span></span>

<span data-ttu-id="4a2b1-128">Essa enumeração é usada pela estrutura [**de \_ \_ status individual do WM**](wm-individualize-status.md) .</span><span class="sxs-lookup"><span data-stu-id="4a2b1-128">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](wm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a2b1-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a2b1-129">Requirements</span></span>



| <span data-ttu-id="4a2b1-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a2b1-130">Requirement</span></span> | <span data-ttu-id="4a2b1-131">Valor</span><span class="sxs-lookup"><span data-stu-id="4a2b1-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a2b1-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a2b1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4a2b1-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4a2b1-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4a2b1-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a2b1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4a2b1-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4a2b1-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4a2b1-136">Versão</span><span class="sxs-lookup"><span data-stu-id="4a2b1-136">Version</span></span><br/>                  | <span data-ttu-id="4a2b1-137">SDK do Windows Media Format 7 ou versões posteriores do SDK</span><span class="sxs-lookup"><span data-stu-id="4a2b1-137">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="4a2b1-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4a2b1-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a2b1-139"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a2b1-139"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a2b1-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a2b1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a2b1-141">**\_status do http DRM \_**</span><span class="sxs-lookup"><span data-stu-id="4a2b1-141">**DRM\_HTTP\_STATUS**</span></span>](drm-http-status.md)
</dt> <dt>

[<span data-ttu-id="4a2b1-142">**Tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="4a2b1-142">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





