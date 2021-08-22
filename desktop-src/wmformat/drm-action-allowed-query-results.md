---
title: DRM_ACTION_ALLOWED_QUERY_RESULTS enumeração (Wmdrmsdk.h)
description: O tipo de enumeração DRM ACTION ALLOWED QUERY RESULTS é usado pela \_ \_ interface \_ IWMDRMLicenseQuery QueryActionAllowed para especificar o motivo pelo qual uma ação \_ não é permitida.
ms.assetid: dc784cdf-6efe-415b-ba72-eb8fc50bef10
keywords:
- DRM_ACTION_ALLOWED_QUERY_RESULTS formato de mídia das janelas de enumeração
- formato de mídia das janelas de enumeração
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
ms.openlocfilehash: d66973838bb6d9cf745ae30b885acccf7b4b311834bbe827d96ccbeea501bd17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547806"
---
# <a name="drm_action_allowed_query_results-enumeration"></a>ENUMERAÇÃO DE \_ RESULTADOS DA CONSULTA PERMITIDA \_ \_ DA \_ AÇÃO DRM

O tipo de enumeração **DRM \_ ACTION ALLOWED \_ \_ QUERY \_ RESULTS** é usado pela interface [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) para especificar o motivo pelo qual uma ação não é permitida.

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

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**CONSULTA PERMITIDA \_ DA \_ AÇÃO DRM NÃO \_ \_ \_ HABILITADA**
</dt> <dd>

Especifica que a ação de consultas não é permitida. Para ações que não são permitidas, o valor retornado é esse valor combinado usando um OR bit a bit com um ou mais dos outros valores nesta enumeração.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**A AÇÃO \_ DRM \_ PERMITIU QUE A CONSULTA NÃO \_ \_ \_ HABILITADA \_ NÃO PERMITIA NENHUMA \_ LICENÇA**
</dt> <dd>

Especifica que não existe uma licença para o conteúdo solicitado.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**A AÇÃO \_ DRM \_ PERMITIU QUE A CONSULTA NÃO ESTAVA \_ \_ \_ HABILITADA \_ SEM \_ DIREITO**
</dt> <dd>

Especifica que existe uma licença para o conteúdo, mas que o direito consultado não é permitido.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**A AÇÃO \_ DRM \_ PERMITIU QUE A CONSULTA NÃO ESTÁ \_ \_ \_ HABILITADA \_ ESGOTADA**
</dt> <dd>

Especifica que o direito consultado é restrito por uma contagem e que não mais usos permanecem.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**A AÇÃO \_ DRM \_ PERMITIU QUE A CONSULTA NÃO \_ \_ \_ \_ EXPIRADA**
</dt> <dd>

Especifica que o direito consultado é restrito com uma data de validade anterior à data atual.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**CONSULTA PERMITIDA \_ DA \_ AÇÃO DRM NÃO \_ \_ \_ HABILITADA \_ NÃO \_ INICIADA**
</dt> <dd>

Especifica que o direito consultado é restrito com uma data de início posterior à data atual.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**A AÇÃO \_ DRM \_ PERMITIU QUE A CONSULTA NÃO \_ \_ \_ HABILITADA \_ APPSEC MUITO \_ \_ BAIXA**
</dt> <dd>

Especifica que existe uma licença para o conteúdo e que a licença permite o direito consultado, mas que o nível de segurança do aplicativo de chamada não é alto o suficiente.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**AÇÃO DRM \_ \_ PERMITIDO CONSULTA NÃO \_ \_ \_ \_ HABILITADA REQ \_ INDIV**
</dt> <dd>

Especifica que existe uma licença para o conteúdo e que a licença permite o direito consultado, mas que o subsistema DRM deve ser individualizado.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**A AÇÃO \_ DRM \_ PERMITIU QUE A CONSULTA NÃO \_ \_ \_ HABILITADA \_ COPIA \_ OPL MUITO \_ \_ BAIXA**
</dt> <dd>

Especifica que o nível de proteção de saída do cliente é muito baixo.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**A AÇÃO DRM \_ PERMITIU QUE A CONSULTA NÃO \_ \_ \_ \_ HABILITADA \_ COPIA \_ OPL EXCLUÍDA \_**
</dt> <dd>

Especifica que o nível de proteção de saída do cliente está na lista de exclusão.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**A AÇÃO \_ DRM \_ PERMITIU QUE A CONSULTA \_ NÃO \_ \_ HABILITADA \_ NÃO PERMITIA SUPORTE A \_ \_ RELÓGIO**
</dt> <dd>

Especifica que a licença requer suporte de relógio seguro e que o cliente não a fornece.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**A AÇÃO \_ DRM \_ PERMITIU QUE A CONSULTA NÃO \_ \_ \_ HABILITADA \_ NÃO PERMITIA SUPORTE À \_ \_ MEDIÇÃO**
</dt> <dd>

Especifica que a ação consultada é permitida por uma licença, mas essa medição é necessária e o cliente não dá suporte à medição.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**A AÇÃO DRM \_ PERMITIU QUE A CONSULTA NÃO \_ \_ \_ \_ HABILITADA PROFUNDIDADE \_ DA CADEIA MUITO \_ \_ \_ ALTA**
</dt> <dd>

Especifica que os direitos da ação consultada não podem ser determinados porque o conteúdo é coberto por uma licença encadeada e a licença folha está ausente.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os valores desse tipo de enumeração indicam que uma ação não é permitida. Um valor de zero indica que a ação é permitida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de enumeração**](drm-enumeration-types.md)
</dt> </dl>

 

 





