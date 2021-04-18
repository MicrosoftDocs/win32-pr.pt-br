---
title: Enumeração de DRM_ACTION_ALLOWED_QUERY_RESULTS (wmdrmsdk. h)
description: O \_ tipo de enumeração de resultados de consulta permitidos da ação DRM \_ \_ \_ é usado pela interface IWMDRMLicenseQuery QueryActionAllowed para especificar o motivo pelo qual uma ação não é permitida.
ms.assetid: dc784cdf-6efe-415b-ba72-eb8fc50bef10
keywords:
- Formato de mídia do Windows de enumeração de DRM_ACTION_ALLOWED_QUERY_RESULTS
- Formato de mídia do Windows de enumeração
topic_type:
- apiref
api_name:
- DRM_ACTION_ALLOWED_QUERY_RESULTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d1e328acb915bd32547f3455e8556e4caba2360
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778785"
---
# <a name="drm_action_allowed_query_results-enumeration"></a><span data-ttu-id="8cef6-105">\_Enumeração de \_ resultados de \_ consulta permitidos \_ da ação DRM</span><span class="sxs-lookup"><span data-stu-id="8cef6-105">DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS enumeration</span></span>

<span data-ttu-id="8cef6-106">O tipo de enumeração de **\_ \_ \_ \_ resultados de consulta permitidos da ação DRM** é usado pela interface [**IWMDRMLicenseQuery:: QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) para especificar o motivo pelo qual uma ação não é permitida.</span><span class="sxs-lookup"><span data-stu-id="8cef6-106">The **DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS** enumeration type is used by the [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) interface to specify the reason an action is not allowed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cef6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cef6-107">Syntax</span></span>


```C++
typedef enum DRM_ACTION_ALLOWED_QUERY_RESULTS { 
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED                       = 0x00000001,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE            = 0x00000002,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT              = 0x00000004,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED             = 0x00000008,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED               = 0x00000010,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED           = 0x00000020,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW        = 0x00000040,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV             = 0x00000080,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW      = 0x00000100,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED     = 0x00000200,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT      = 0x00000400,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT   = 0x00000800,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH  = 0x00001000
} ;
```



## <a name="constants"></a><span data-ttu-id="8cef6-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="8cef6-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8cef6-109"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**consulta de ação de DRM \_ \_ permitida \_ \_ não \_ habilitada**</span><span class="sxs-lookup"><span data-stu-id="8cef6-109"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED**</span></span>
</dt> <dd>

<span data-ttu-id="8cef6-110">Especifica que a ação de consultas não é permitida.</span><span class="sxs-lookup"><span data-stu-id="8cef6-110">Specifies that the queries action is not allowed.</span></span> <span data-ttu-id="8cef6-111">Para ações que não são permitidas, o valor retornado é esse valor combinado por meio de um bit de bits ou com um ou mais dos outros valores nesta enumeração.</span><span class="sxs-lookup"><span data-stu-id="8cef6-111">For actions that are not allowed, the returned value is this value combined by using a bitwise OR with one or more of the other values in this enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="8cef6-112"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**\_consulta permitida ação de DRM \_ \_ \_ não \_ habilitada \_ sem \_ licença**</span><span class="sxs-lookup"><span data-stu-id="8cef6-112"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_LICENSE**</span></span>
</dt> <dd>

<span data-ttu-id="8cef6-113">Especifica que uma licença não existe para o conteúdo solicitado.</span><span class="sxs-lookup"><span data-stu-id="8cef6-113">Specifies that a license does not exist for the requested content.</span></span>

</dd> <dt>

<span data-ttu-id="8cef6-114"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**consulta de DRM \_ \_ permitida \_ \_ não \_ habilitada \_ no \_ direito**</span><span class="sxs-lookup"><span data-stu-id="8cef6-114"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_RIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="8cef6-115">Especifica que existe uma licença para o conteúdo, mas que o direito consultado não é permitido.</span><span class="sxs-lookup"><span data-stu-id="8cef6-115">Specifies that a license exists for the content, but that the queried right is not allowed.</span></span>

</dd> <dt>

<span data-ttu-id="8cef6-116"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**\_consulta permitida ação de DRM \_ \_ \_ não \_ habilitada \_ esgotada**</span><span class="sxs-lookup"><span data-stu-id="8cef6-116"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_EXHAUSTED**</span></span>
</dt> <dd>

<span data-ttu-id="8cef6-117">Especifica que o direito consultado é restrito por uma contagem e que nenhum uso restante permanece.</span><span class="sxs-lookup"><span data-stu-id="8cef6-117">Specifies that the queried right is restricted by a count, and that no more uses remain.</span></span>

</dd> <dt>

<span data-ttu-id="8cef6-118"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**\_consulta permitida ação de DRM \_ \_ \_ não \_ habilitada \_ expirada**</span><span class="sxs-lookup"><span data-stu-id="8cef6-118"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_EXPIRED**</span></span>
</dt> <dd>

<span data-ttu-id="8cef6-119">Especifica que o direito consultado é restrito com uma data de expiração anterior à data atual.</span><span class="sxs-lookup"><span data-stu-id="8cef6-119">Specifies that the queried right is restricted with an expiration date that is earlier than the current date.</span></span>

</dd> <dt>

<span data-ttu-id="8cef6-120"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**\_consulta permitida ação de DRM \_ \_ \_ não \_ habilitada \_ não \_ iniciada**</span><span class="sxs-lookup"><span data-stu-id="8cef6-120"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NOT\_STARTED**</span></span>
</dt> <dd>

<span data-ttu-id="8cef6-121">Especifica que o direito consultado é restrito com uma data de início posterior à data atual.</span><span class="sxs-lookup"><span data-stu-id="8cef6-121">Specifies that the queried right is restricted with a start date that is later than the current date.</span></span>

</dd> <dt>

<span data-ttu-id="8cef6-122"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**a \_ ação DRM com \_ permissão de \_ consulta \_ não \_ habilitada \_ APPSEC \_ muito \_ baixa**</span><span class="sxs-lookup"><span data-stu-id="8cef6-122"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_APPSEC\_TOO\_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="8cef6-123">Especifica que existe uma licença para o conteúdo e que a licença permite o direito consultado, mas que o nível de segurança do aplicativo de chamada não é alto o suficiente.</span><span class="sxs-lookup"><span data-stu-id="8cef6-123">Specifies that a license exists for the content and that the license allows the queried right, but that the security level of the calling application is not high enough.</span></span>

</dd> <dt>

<span data-ttu-id="8cef6-124"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**solicitação de DRM \_ \_ permitida \_ consulta \_ não \_ habilitada \_ \_ indiv req.**</span><span class="sxs-lookup"><span data-stu-id="8cef6-124"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_REQ\_INDIV**</span></span>
</dt> <dd>

<span data-ttu-id="8cef6-125">Especifica que existe uma licença para o conteúdo e que a licença permite o direito consultado, mas que o subsistema DRM deve ser individualizado.</span><span class="sxs-lookup"><span data-stu-id="8cef6-125">Specifies that a license exists for the content and that the license allows the queried right, but that the DRM subsystem must be individualized.</span></span>

</dd> <dt>

<span data-ttu-id="8cef6-126"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**\_operação DRM \_ permitida \_ consulta \_ não \_ habilitada \_ cópia \_ OPL \_ muito \_ baixa**</span><span class="sxs-lookup"><span data-stu-id="8cef6-126"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_COPY\_OPL\_TOO\_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="8cef6-127">Especifica que o nível de proteção de saída do cliente é muito baixo.</span><span class="sxs-lookup"><span data-stu-id="8cef6-127">Specifies that the output protection level of the client is too low.</span></span>

</dd> <dt>

<span data-ttu-id="8cef6-128"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**\_ação DRM \_ permitida \_ consulta \_ não \_ habilitada \_ cópia \_ OPL \_ excluída**</span><span class="sxs-lookup"><span data-stu-id="8cef6-128"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_COPY\_OPL\_EXCLUDED**</span></span>
</dt> <dd>

<span data-ttu-id="8cef6-129">Especifica que o nível de proteção de saída do cliente está na lista de exclusões.</span><span class="sxs-lookup"><span data-stu-id="8cef6-129">Specifies that the output protection level of the client is on the exclusion list.</span></span>

</dd> <dt>

<span data-ttu-id="8cef6-130"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**consulta de ação de DRM \_ \_ permitida \_ \_ não \_ habilitada \_ sem \_ suporte de relógio \_**</span><span class="sxs-lookup"><span data-stu-id="8cef6-130"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_CLOCK\_SUPPORT**</span></span>
</dt> <dd>

<span data-ttu-id="8cef6-131">Especifica que a licença requer suporte ao Clock seguro e que o cliente não a fornece.</span><span class="sxs-lookup"><span data-stu-id="8cef6-131">Specifies that the license requires secure clock support and that the client does not provide it.</span></span>

</dd> <dt>

<span data-ttu-id="8cef6-132"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**\_consulta permitida ação de DRM \_ \_ \_ não \_ habilitada \_ sem \_ \_ suporte para medição**</span><span class="sxs-lookup"><span data-stu-id="8cef6-132"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_METERING\_SUPPORT**</span></span>
</dt> <dd>

<span data-ttu-id="8cef6-133">Especifica que a ação consultada é permitida por uma licença, mas essa medição é necessária e o cliente não dá suporte à medição.</span><span class="sxs-lookup"><span data-stu-id="8cef6-133">Specifies that the queried action is allowed by a license, but that metering is required and the client does not support metering.</span></span>

</dd> <dt>

<span data-ttu-id="8cef6-134"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**a \_ ação de DRM \_ permitiu a profundidade de \_ \_ \_ cadeia não habilitada \_ \_ \_ muito \_ alta**</span><span class="sxs-lookup"><span data-stu-id="8cef6-134"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_CHAIN\_DEPTH\_TOO\_HIGH**</span></span>
</dt> <dd>

<span data-ttu-id="8cef6-135">Especifica que os direitos da ação consultada não podem ser determinados porque o conteúdo é coberto por uma licença encadeada e a licença de folha está ausente.</span><span class="sxs-lookup"><span data-stu-id="8cef6-135">Specifies that the rights for the queried action cannot be determined because the content is covered by a chained license and the leaf license is missing.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8cef6-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cef6-136">Remarks</span></span>

<span data-ttu-id="8cef6-137">Os valores desse tipo de enumeração indicam que uma ação não é permitida.</span><span class="sxs-lookup"><span data-stu-id="8cef6-137">The values of this enumeration type indicate that an action is not allowed.</span></span> <span data-ttu-id="8cef6-138">Um valor de zero indica que a ação é permitida.</span><span class="sxs-lookup"><span data-stu-id="8cef6-138">A value of zero indicates that the action is allowed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cef6-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cef6-139">Requirements</span></span>



| <span data-ttu-id="8cef6-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cef6-140">Requirement</span></span> | <span data-ttu-id="8cef6-141">Valor</span><span class="sxs-lookup"><span data-stu-id="8cef6-141">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8cef6-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8cef6-142">Header</span></span><br/> | <dl> <span data-ttu-id="8cef6-143"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cef6-143"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cef6-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cef6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cef6-145">**Tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="8cef6-145">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





