---
title: Estrutura de DRM_OUTPUT_PROTECTION (wmdrmsdk. h)
description: A estrutura de proteção de saída do DRM \_ \_ contém informações sobre uma tecnologia de proteção de saída.
ms.assetid: e458013d-b77e-4e03-bff9-e3ecfc72ebdb
keywords:
- Formato de mídia do Windows de estrutura de DRM_OUTPUT_PROTECTION
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a10428d86503e952dc82a7d45bddc11f5dd1286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810814"
---
# <a name="drm_output_protection-structure"></a>Estrutura de proteção de \_ saída DRM \_

A estrutura de **\_ \_ proteção de saída do DRM** contém informações sobre uma tecnologia de proteção de saída.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct DRM_OUTPUT_PROTECTION {
  GUID guidId;
  BYTE bConfigData;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**guidId**
</dt> <dd>

GUID que identifica a tecnologia de proteção de saída.

</dd> <dt>

**bConfigData**
</dt> <dd>

Dados de configuração para a tecnologia.

</dd> </dl>

## <a name="remarks"></a>Comentários

**DRM \_ A proteção de \_ saída de \_ áudio** e a **proteção de \_ \_ saída \_ de vídeo DRM** são definidas como **\_ \_ proteção de saída DRM** em instruções **typedef** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_proteção de saída DRM \_ \_ ex**](drm-output-protection-ex.md)
</dt> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





