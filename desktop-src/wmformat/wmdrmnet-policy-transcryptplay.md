---
title: Estrutura de WMDRMNET_POLICY_TRANSCRYPTPLAY (wmdrmsdk. h)
description: a \_ estrutura TRANSCRYPTPLAY da política WMDRMNET \_ contém as informações de política para reproduzir conteúdo usando Windows mídia DRM para dispositivos de rede.
ms.assetid: 95671c58-a593-40bb-856e-28ad1cba340e
keywords:
- Formato de mídia do Windows de estrutura de WMDRMNET_POLICY_TRANSCRYPTPLAY
- estruturar formato de mídia do Windows
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
# <a name="wmdrmnet_policy_transcryptplay-structure"></a>\_Estrutura TRANSCRYPTPLAY da política de WMDRMNET \_

a **estrutura \_ \_ TRANSCRYPTPLAY da política WMDRMNET** contém as informações de política para reproduzir conteúdo usando Windows mídia DRM para dispositivos de rede.

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

Níveis de proteção de saída para reprodução. **WMDRMNET \_ A \_ reprodução \_ de política OPL** é um tipo definido como [**DRM \_ Play \_ OPL \_ ex**](drm-play-opl-ex.md).

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

 

 





