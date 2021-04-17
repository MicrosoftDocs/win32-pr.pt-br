---
title: Estrutura de DRM_COPY_OPL (wmdrmsdk. h)
description: A \_ estrutura OPL de cópia do DRM \_ contém informações sobre os níveis de proteção de saída (OPLs) especificados em uma licença para ações de cópia.
ms.assetid: 439cbd56-05c1-46f8-86b9-ac1341902a40
keywords:
- Formato de mídia do Windows de estrutura de DRM_COPY_OPL
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_COPY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28655e220588bb704567de033e1117dd569d3ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782690"
---
# <a name="drm_copy_opl-structure"></a>\_Estrutura OPL de cópia DRM \_

A **estrutura \_ \_ OPL de cópia do DRM** contém informações sobre os níveis de proteção de saída (OPLs) especificados em uma licença para ações de cópia.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct DRM_COPY_OPL {
  WORD               wMinimumCopyLevel;
  DRM_OPL_OUTPUT_IDS oplIdIncludes;
  DRM_OPL_OUTPUT_IDS oplIdExcludes;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**wMinimumCopyLevel**
</dt> <dd>

OPL mínimo para ações de cópia.

</dd> <dt>

**oplIdIncludes**
</dt> <dd>

[**DRM \_ OPL \_ \_**](drmdrm-opl-output-ids.md) a estrutura de IDs de saída que contém os identificadores de tecnologias a permitir. Esse membro é usado para tecnologias de saída atribuídas OPLs menor do que o nível de cópia mínimo, mas para o qual o conteúdo pode ser copiado.

</dd> <dt>

**oplIdExcludes**
</dt> <dd>

[**DRM \_ OPL \_ \_**](drmdrm-opl-output-ids.md) a estrutura de IDs de saída que contém os identificadores de saída de tecnologias para restringir. Esse membro é usado para tecnologias de saída que recebem OPLs que excedem o nível de cópia mínimo, mas que o emissor da licença não concede direitos para copiar para o.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_OPL de reprodução DRM \_**](drmdrm-play-opl.md)
</dt> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





