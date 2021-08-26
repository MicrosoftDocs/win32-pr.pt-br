---
title: Estrutura de WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX (wmdrmsdk. h)
description: A \_ estrutura ex de restrições de vídeo analógica do WMDRM \_ \_ \_ contém informações estendidas sobre uma restrição para reproduzir conteúdo como vídeo analógico.
ms.assetid: fe9092fe-a717-4377-9653-1cc07795319f
keywords:
- Formato de mídia do Windows de estrutura de WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e9cbacff2d330c869c35eb7a3d1ca46ae6c80a030495ffec42eabc3726436c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006536"
---
# <a name="wmdrm_analog_video_restrictions_ex-structure"></a>\_ \_ \_ Estrutura ex de restrições de vídeo analógico WMDRM \_

A **estrutura \_ \_ ex de \_ restrições \_ de vídeo analógica do WMDRM** contém informações estendidas sobre uma restrição para reproduzir conteúdo como vídeo analógico.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX {
  DWORD dwVersion;
  GUID  guidRestrictionID;
  DWORD cbRestrictionData;
  BYTE  *pbRestrictionData;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**DW**
</dt> <dd>

Número da versão.

</dd> <dt>

**guidRestrictionID**
</dt> <dd>

ID da restrição.

</dd> <dt>

**cbRestrictionData**
</dt> <dd>

Tamanho dos dados de restrição em bytes.

</dd> <dt>

**pbRestrictionData**
</dt> <dd>

Dados de restrição.

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

[**\_restrições de \_ vídeo \_ analógico WMDRM**](wmdrm-analog-video-restrictions.md)
</dt> </dl>

 

 





