---
title: WMDRMNET_POLICY_GLOBAL_REQUIREMENTS estrutura (Wmdrmsdk.h)
description: A estrutura DE REQUISITOS GLOBAIS DA POLÍTICA WMDRMNET \_ \_ contém \_ requisitos globais para Windows DRM de Mídia para Dispositivos de Rede.
ms.assetid: 140b3a6f-ccba-4735-b48a-2e990f5ec570
keywords:
- WMDRMNET_POLICY_GLOBAL_REQUIREMENTS formato de mídia do Windows da estrutura
- formato de mídia de janelas de estrutura
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_GLOBAL_REQUIREMENTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e2a8dc7be95638e171126eb4a55c50744ee3e5126d3e0b49eb8f229ec0257e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843966"
---
# <a name="wmdrmnet_policy_global_requirements-structure"></a>Estrutura DE REQUISITOS GLOBAIS DA POLÍTICA WMDRMNET \_ \_ \_

A **estrutura DE REQUISITOS GLOBAIS DA POLÍTICA WMDRMNET \_ \_ \_** contém requisitos globais para Windows DRM de Mídia para Dispositivos de Rede.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct WMDRMNET_POLICY_GLOBAL_REQUIREMENTS {
  WMDRMNET_POLICY_MINIMUM_ENVIRONMENT MinimumEnvironment;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**MinimumEnvironment**
</dt> <dd>

[**WMDRMNET \_ ESTRUTURA \_ DE \_ AMBIENTE MÍNIMO**](wmdrmnet-policy-minimum-environment.md) DE POLÍTICA que contém os requisitos mínimos de segurança para Windows DRM de Mídia para Dispositivos de Rede.

</dd> </dl>

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](drm-structures.md)
</dt> <dt>

[**POLÍTICA \_ WMDRMNET**](wmdrmnet-policy.md)
</dt> </dl>

 

 





