---
title: Estrutura de WMDRMNET_POLICY_GLOBAL_REQUIREMENTS (wmdrmsdk. h)
description: A \_ estrutura de \_ requisitos globais da política WMDRMNET \_ contém requisitos globais para o Windows Media DRM para dispositivos de rede.
ms.assetid: 140b3a6f-ccba-4735-b48a-2e990f5ec570
keywords:
- Formato de mídia do Windows de estrutura de WMDRMNET_POLICY_GLOBAL_REQUIREMENTS
- estruturar formato de mídia do Windows
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
ms.openlocfilehash: 0ccf13c881c9696d970a00ac902f3f8d08f13c58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760492"
---
# <a name="wmdrmnet_policy_global_requirements-structure"></a>\_Estrutura de \_ requisitos globais da política de WMDRMNET \_

A estrutura de **\_ \_ \_ requisitos globais da política WMDRMNET** contém requisitos globais para o Windows Media DRM para dispositivos de rede.

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

[**WMDRMNET \_ Estrutura \_ de \_ ambiente mínima de política**](wmdrmnet-policy-minimum-environment.md) que contém os requisitos mínimos de segurança para o Windows Media DRM para dispositivos de rede.

</dd> </dl>

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](drm-structures.md)
</dt> <dt>

[**política de WMDRMNET \_**](wmdrmnet-policy.md)
</dt> </dl>

 

 





