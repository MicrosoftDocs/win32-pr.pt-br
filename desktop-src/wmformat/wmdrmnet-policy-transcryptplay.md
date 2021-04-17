---
title: Estrutura de WMDRMNET_POLICY_TRANSCRYPTPLAY (wmdrmsdk. h)
description: A \_ estrutura TRANSCRYPTPLAY da política WMDRMNET \_ contém as informações de política para reproduzir conteúdo usando o Windows Media DRM para dispositivos de rede.
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
ms.openlocfilehash: 0681251428b87b323c9ad3e73277ec8cdd2b95f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747225"
---
# <a name="wmdrmnet_policy_transcryptplay-structure"></a>\_Estrutura TRANSCRYPTPLAY da política de WMDRMNET \_

A **estrutura \_ \_ TRANSCRYPTPLAY da política WMDRMNET** contém as informações de política para reproduzir conteúdo usando o Windows Media DRM para dispositivos de rede.

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

 

 





