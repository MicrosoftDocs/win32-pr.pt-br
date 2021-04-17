---
title: Enumeração de MSDRM_STATUS (wmdrmsdk. h)
description: O \_ tipo de enumeração status Msdrm define as condições de status para o subsistema DRM.
ms.assetid: b26600ea-2603-4fca-9408-2d5c88091dcc
keywords:
- Formato de mídia do Windows de enumeração de MSDRM_STATUS
- Formato de mídia do Windows de enumeração
topic_type:
- apiref
api_name:
- MSDRM_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2a73de9e33216e22a01966be8f2ed6a3185fdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762199"
---
# <a name="msdrm_status-enumeration"></a><span data-ttu-id="a4941-105">\_Enumeração de status Msdrm</span><span class="sxs-lookup"><span data-stu-id="a4941-105">MSDRM\_STATUS enumeration</span></span>

<span data-ttu-id="a4941-106">O tipo de enumeração **\_ status Msdrm** define as condições de status para o subsistema DRM.</span><span class="sxs-lookup"><span data-stu-id="a4941-106">The **MSDRM\_STATUS** enumeration type defines status conditions for the DRM subsystem.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4941-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4941-107">Syntax</span></span>


```C++
typedef enum MSDRM_STATUS { 
  DRM_ERROR                        = 0,
  DRM_INFORMATION                  = 1,
  DRM_BACKUPRESTORE_BEGIN          = 2,
  DRM_BACKUPRESTORE_END            = 3,
  DRM_BACKUPRESTORE_CONNECTING     = 4,
  DRM_BACKUPRESTORE_DISCONNECTING  = 5,
  DRM_ERROR_WITHURL                = 6,
  DRM_RESTRICTED_LICENSE           = 7,
  DRM_NEEDS_INDIVIDUALIZATION      = 8,
  DRM_PLAY_OPL_NOTIFICATION        = 9,
  DRM_COPY_OPL_NOTIFICATION        = 10,
  DRM_REFRESHCRL_COMPLETE          = 11
} ;
```



## <a name="constants"></a><span data-ttu-id="a4941-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="a4941-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a4941-109"><span id="DRM_ERROR"></span><span id="drm_error"></span>**erro de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="a4941-109"><span id="DRM_ERROR"></span><span id="drm_error"></span>**DRM\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="a4941-110">Especifica que ocorreu um erro.</span><span class="sxs-lookup"><span data-stu-id="a4941-110">Specifies that an error has occurred.</span></span>

</dd> <dt>

<span data-ttu-id="a4941-111"><span id="DRM_INFORMATION"></span><span id="drm_information"></span>**informações de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="a4941-111"><span id="DRM_INFORMATION"></span><span id="drm_information"></span>**DRM\_INFORMATION**</span></span>
</dt> <dd>

<span data-ttu-id="a4941-112">Especifica que há informações de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="a4941-112">Specifies that there is additional status information.</span></span>

</dd> <dt>

<span data-ttu-id="a4941-113"><span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**\_início de BACKUPRESTORE DRM \_**</span><span class="sxs-lookup"><span data-stu-id="a4941-113"><span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**DRM\_BACKUPRESTORE\_BEGIN**</span></span>
</dt> <dd>

<span data-ttu-id="a4941-114">Especifica que uma operação de backup ou restauração de licença foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="a4941-114">Specifies that a license backup or restore operation has begun.</span></span>

</dd> <dt>

<span data-ttu-id="a4941-115"><span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**fim do DRM \_ BACKUPRESTORE \_**</span><span class="sxs-lookup"><span data-stu-id="a4941-115"><span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**DRM\_BACKUPRESTORE\_END**</span></span>
</dt> <dd>

<span data-ttu-id="a4941-116">Especifica que uma operação de backup ou restauração de licença terminou.</span><span class="sxs-lookup"><span data-stu-id="a4941-116">Specifies that a license backup or restore operation has ended.</span></span>

</dd> <dt>

<span data-ttu-id="a4941-117"><span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**\_conexão BACKUPRESTORE \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="a4941-117"><span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**DRM\_BACKUPRESTORE\_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="a4941-118">Especifica que uma operação de backup ou restauração de licença está em andamento e que o computador cliente está se conectando ao servidor de backup.</span><span class="sxs-lookup"><span data-stu-id="a4941-118">Specifies that a license backup or restore operation is in progress and that the client computer is connecting with the backup server.</span></span>

</dd> <dt>

<span data-ttu-id="a4941-119"><span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**desconexão de \_ BACKUPRESTORE DRM \_**</span><span class="sxs-lookup"><span data-stu-id="a4941-119"><span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**DRM\_BACKUPRESTORE\_DISCONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="a4941-120">Especifica que uma operação de backup ou restauração de licença está em andamento e que o computador cliente está desconectando do servidor de backup.</span><span class="sxs-lookup"><span data-stu-id="a4941-120">Specifies that a license backup or restore operation is in progress and that the client computer is disconnecting from the backup server.</span></span>

</dd> <dt>

<span data-ttu-id="a4941-121"><span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**erro de DRM \_ \_ WITHURL**</span><span class="sxs-lookup"><span data-stu-id="a4941-121"><span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**DRM\_ERROR\_WITHURL**</span></span>
</dt> <dd>

<span data-ttu-id="a4941-122">Especifica que a operação de DRM encontrou uma URL inadequada.</span><span class="sxs-lookup"><span data-stu-id="a4941-122">Specifies that the DRM operation has encountered a bad URL.</span></span>

</dd> <dt>

<span data-ttu-id="a4941-123"><span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**\_licença restrita de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="a4941-123"><span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**DRM\_RESTRICTED\_LICENSE**</span></span>
</dt> <dd>

<span data-ttu-id="a4941-124">Especifica que a operação DRM não pode continuar porque nenhuma licença que concede o direito necessário existe no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="a4941-124">Specifies that the DRM operation cannot continue because no license granting the required right exists on the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="a4941-125"><span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM \_ precisa de \_ individualização**</span><span class="sxs-lookup"><span data-stu-id="a4941-125"><span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM\_NEEDS\_INDIVIDUALIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="a4941-126">Especifica que a operação DRM não pode continuar porque o subsistema DRM precisa ser individualizado.</span><span class="sxs-lookup"><span data-stu-id="a4941-126">Specifies that the DRM operation cannot continue because the DRM subsystem needs to be individualized.</span></span>

</dd> <dt>

<span data-ttu-id="a4941-127"><span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**\_notificação de \_ OPL de reprodução de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="a4941-127"><span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**DRM\_PLAY\_OPL\_NOTIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="a4941-128">Especifica que uma operação de reprodução não pode ser concluída porque um requisito de nível de proteção de saída não foi atendido.</span><span class="sxs-lookup"><span data-stu-id="a4941-128">Specifies that a playback operation cannot be completed because an output protection level requirement has not been met.</span></span>

</dd> <dt>

<span data-ttu-id="a4941-129"><span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**\_notificação de \_ OPL de cópia de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="a4941-129"><span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**DRM\_COPY\_OPL\_NOTIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="a4941-130">Especifica que uma operação de cópia não pode ser concluída porque um requisito de nível de proteção de saída não foi atendido.</span><span class="sxs-lookup"><span data-stu-id="a4941-130">Specifies that a copy operation cannot be completed because an output protection level requirement has not been met.</span></span>

</dd> <dt>

<span data-ttu-id="a4941-131"><span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**\_REFRESHCRL DRM \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="a4941-131"><span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**DRM\_REFRESHCRL\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="a4941-132">Especifica que uma chamada para [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) concluiu a atualização de uma lista de revogação.</span><span class="sxs-lookup"><span data-stu-id="a4941-132">Specifies that a call to [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) has completed refreshing a revocation list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4941-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4941-133">Remarks</span></span>

<span data-ttu-id="a4941-134">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a4941-134">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4941-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4941-135">Requirements</span></span>



| <span data-ttu-id="a4941-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4941-136">Requirement</span></span> | <span data-ttu-id="a4941-137">Valor</span><span class="sxs-lookup"><span data-stu-id="a4941-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a4941-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4941-138">Header</span></span><br/> | <dl> <span data-ttu-id="a4941-139"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4941-139"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4941-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4941-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4941-141">**Tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="a4941-141">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





