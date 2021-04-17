---
title: Estrutura de DRM_OUTPUT_PROTECTION_EX (wmdrmsdk. h)
description: A \_ estrutura ex de proteção de saída DRM \_ \_ contém informações sobre uma tecnologia de proteção de saída. Essa estrutura estende \_ a proteção de saída DRM \_ adicionando um número de versão.
ms.assetid: eeebf5da-172b-4781-8c44-00504a6961bf
keywords:
- Formato de mídia do Windows de estrutura de DRM_OUTPUT_PROTECTION_EX
- estruturar formato de mídia do Windows
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
ms.openlocfilehash: aeadbb845dc115b1faff858fe3a6ba0064eb425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797636"
---
# <a name="drm_output_protection_ex-structure"></a>\_ \_ Estrutura ex de proteção de saída DRM \_

A **estrutura \_ \_ \_ ex de proteção de saída DRM** contém informações sobre uma tecnologia de proteção de saída. Essa estrutura estende **a \_ \_ proteção de saída DRM** adicionando um número de versão.

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

**DW**
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

**DRM \_ Proteção de saída de áudio \_ \_ \_ ex** e **proteção de saída de vídeo DRM, por \_ \_ \_ \_ exemplo** , são definidas como **\_ \_ proteção de saída DRM** em instruções **typedef** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_proteção de saída DRM \_**](drm-output-protection.md)
</dt> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





