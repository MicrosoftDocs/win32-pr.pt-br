---
title: WMDRMNET_POLICY_TRANSCRYPTPLAY estrutura (Wmdrmsdk.h)
description: A estrutura WMDRMNET POLICY TRANSCRYPTPLAY contém as informações de política para reprodução de conteúdo usando Windows DRM de \_ Mídia para \_ Dispositivos de Rede.
ms.assetid: 95671c58-a593-40bb-856e-28ad1cba340e
keywords:
- WMDRMNET_POLICY_TRANSCRYPTPLAY formato de mídia windows da estrutura
- formato de mídia de janelas de estrutura
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TRANSCRYPTPLAY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fe64c796a1f2f15e4733e7dd3d82e918306fb95d78c61fb85ad2d813d946d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118195501"
---
# <a name="wmdrmnet_policy_transcryptplay-structure"></a>Estrutura WMDRMNET \_ POLICY \_ TRANSCRYPTPLAY

A **estrutura WMDRMNET \_ POLICY \_ TRANSCRYPTPLAY** contém as informações de política para reprodução de conteúdo usando Windows DRM de Mídia para Dispositivos de Rede.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct WMDRMNET_POLICY_TRANSCRYPTPLAY {
  WMDRMNET_POLICY_GLOBAL_REQUIREMENTS globals;
  WMDRMNET_POLICY_PLAY_OPL            playOPLs;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**Globals**
</dt> <dd>

Estrutura de política global.

</dd> <dt>

**playOPLs**
</dt> <dd>

Níveis de proteção de saída para reprodução. **WMDRMNET \_ POLICY \_ PLAY \_ OPL** é um tipo definido como [**DRM PLAY \_ \_ OPL \_ EX.**](drm-play-opl-ex.md)

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

 

 





