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
# <a name="drm_action_allowed_query_results-enumeration"></a>\_Enumeração de \_ resultados de \_ consulta permitidos \_ da ação DRM

O tipo de enumeração de **\_ \_ \_ \_ resultados de consulta permitidos da ação DRM** é usado pela interface [**IWMDRMLicenseQuery:: QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) para especificar o motivo pelo qual uma ação não é permitida.

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**consulta de ação de DRM \_ \_ permitida \_ \_ não \_ habilitada**
</dt> <dd>

Especifica que a ação de consultas não é permitida. Para ações que não são permitidas, o valor retornado é esse valor combinado por meio de um bit de bits ou com um ou mais dos outros valores nesta enumeração.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**\_consulta permitida ação de DRM \_ \_ \_ não \_ habilitada \_ sem \_ licença**
</dt> <dd>

Especifica que uma licença não existe para o conteúdo solicitado.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**consulta de DRM \_ \_ permitida \_ \_ não \_ habilitada \_ no \_ direito**
</dt> <dd>

Especifica que existe uma licença para o conteúdo, mas que o direito consultado não é permitido.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**\_consulta permitida ação de DRM \_ \_ \_ não \_ habilitada \_ esgotada**
</dt> <dd>

Especifica que o direito consultado é restrito por uma contagem e que nenhum uso restante permanece.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**\_consulta permitida ação de DRM \_ \_ \_ não \_ habilitada \_ expirada**
</dt> <dd>

Especifica que o direito consultado é restrito com uma data de expiração anterior à data atual.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**\_consulta permitida ação de DRM \_ \_ \_ não \_ habilitada \_ não \_ iniciada**
</dt> <dd>

Especifica que o direito consultado é restrito com uma data de início posterior à data atual.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**a \_ ação DRM com \_ permissão de \_ consulta \_ não \_ habilitada \_ APPSEC \_ muito \_ baixa**
</dt> <dd>

Especifica que existe uma licença para o conteúdo e que a licença permite o direito consultado, mas que o nível de segurança do aplicativo de chamada não é alto o suficiente.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**solicitação de DRM \_ \_ permitida \_ consulta \_ não \_ habilitada \_ \_ indiv req.**
</dt> <dd>

Especifica que existe uma licença para o conteúdo e que a licença permite o direito consultado, mas que o subsistema DRM deve ser individualizado.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**\_operação DRM \_ permitida \_ consulta \_ não \_ habilitada \_ cópia \_ OPL \_ muito \_ baixa**
</dt> <dd>

Especifica que o nível de proteção de saída do cliente é muito baixo.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**\_ação DRM \_ permitida \_ consulta \_ não \_ habilitada \_ cópia \_ OPL \_ excluída**
</dt> <dd>

Especifica que o nível de proteção de saída do cliente está na lista de exclusões.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**consulta de ação de DRM \_ \_ permitida \_ \_ não \_ habilitada \_ sem \_ suporte de relógio \_**
</dt> <dd>

Especifica que a licença requer suporte ao Clock seguro e que o cliente não a fornece.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**\_consulta permitida ação de DRM \_ \_ \_ não \_ habilitada \_ sem \_ \_ suporte para medição**
</dt> <dd>

Especifica que a ação consultada é permitida por uma licença, mas essa medição é necessária e o cliente não dá suporte à medição.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**a \_ ação de DRM \_ permitiu a profundidade de \_ \_ \_ cadeia não habilitada \_ \_ \_ muito \_ alta**
</dt> <dd>

Especifica que os direitos da ação consultada não podem ser determinados porque o conteúdo é coberto por uma licença encadeada e a licença de folha está ausente.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os valores desse tipo de enumeração indicam que uma ação não é permitida. Um valor de zero indica que a ação é permitida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de enumeração**](drm-enumeration-types.md)
</dt> </dl>

 

 





