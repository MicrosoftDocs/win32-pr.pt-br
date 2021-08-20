---
title: DRM_OUTPUT_PROTECTION_EX estrutura (Wmdrmsdk.h)
description: A estrutura EX \_ DA PROTEÇÃO DE SAÍDA \_ \_ DRM contém informações sobre uma tecnologia de proteção de saída. Essa estrutura estende a PROTEÇÃO DE \_ SAÍDA DRM \_ adicionando um número de versão.
ms.assetid: eeebf5da-172b-4781-8c44-00504a6961bf
keywords:
- DRM_OUTPUT_PROTECTION_EX formato de mídia do Windows
- formato de mídia de janelas de estrutura
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac3033482dc84ad8a25e2e18c359cd621228fef37cc97673f9a5eeae9a57b1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118029580"
---
# <a name="drm_output_protection_ex-structure"></a>Estrutura EX \_ DA PROTEÇÃO DE SAÍDA \_ \_ DRM

A **estrutura EX DA PROTEÇÃO DE SAÍDA \_ \_ \_ DRM** contém informações sobre uma tecnologia de proteção de saída. Essa estrutura estende a **PROTEÇÃO DE \_ SAÍDA DRM \_** adicionando um número de versão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct DRM_OUTPUT_PROTECTION_EX {
  DWORD dwVersion;
  GUID  guidId;
  DWORD dwConfigData;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**Dwversion**
</dt> <dd>

Número da versão.

</dd> <dt>

**guidId**
</dt> <dd>

GUID que identifica a tecnologia de proteção de saída.

</dd> <dt>

**dwConfigData**
</dt> <dd>

Dados de configuração para a tecnologia.

</dd> </dl>

## <a name="remarks"></a>Comentários

**DRM \_ AUDIO \_ OUTPUT PROTECTION EX \_ \_ e** **DRM VIDEO OUTPUT PROTECTION \_ \_ \_ \_ EX** são definidos como PROTEÇÃO DE SAÍDA **DRM \_ \_** em **instruções typedef.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PROTEÇÃO DE \_ SAÍDA DRM \_**](drm-output-protection.md)
</dt> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





