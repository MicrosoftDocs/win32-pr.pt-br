---
title: Estrutura de DRM_OPL_OUTPUT_IDS (wmdrmsdk. h)
description: A estrutura de IDs de saída do DRM \_ OPL \_ \_ contém um número de identificadores de saída de OPL (nível de proteção de saída).
ms.assetid: 3627f2a7-1cea-400b-82e7-678898ccc386
keywords:
- Formato de mídia do Windows de estrutura de DRM_OPL_OUTPUT_IDS
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_OPL_OUTPUT_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 265e1015dd31281043d388debc802b390e7dd2d534f426ecbe24402efffd13df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658856"
---
# <a name="drm_opl_output_ids-structure"></a>\_Estrutura de \_ IDs de saída do DRM OPL \_

A estrutura de **\_ IDs de \_ saída \_ do DRM OPL** contém um número de identificadores de saída de OPL (nível de proteção de saída).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct DRM_OPL_OUTPUT_IDS {
  WORD cIds;
  GUID *rgIds;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**cIds**
</dt> <dd>

Número de identificadores na matriz referenciados por **rgIds**.

</dd> <dt>

**rgIds**
</dt> <dd>

Endereço de uma matriz de GUIDs. Cada membro da matriz contém um identificador de saída OPL.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada como membro da [**\_ \_ OPL de cópia DRM**](drmdrm-copy-opl.md) e das estruturas [**\_ \_ OPL de reprodução DRM**](drmdrm-play-opl.md) para identificar grupos de identificadores de saída.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





