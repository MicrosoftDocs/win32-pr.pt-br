---
title: Enumeração de WMDRMNET_POLICY_TYPE (wmdrmsdk. h)
description: o \_ tipo de \_ enumeração tipo de política WMDRMNET lista os tipos de políticas que estão disponíveis para Windows mídia DRM para operações de dispositivos de rede.
ms.assetid: 83e9e247-3bd8-4857-97b6-95b3cd5ad25c
keywords:
- Formato de mídia do Windows de enumeração de WMDRMNET_POLICY_TYPE
- Formato de mídia do Windows de enumeração
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aec574717abb51117b142b8450ad7548d84766b4138f76a4296982422462fbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697808"
---
# <a name="wmdrmnet_policy_type-enumeration"></a>Enumeração de tipo de \_ política WMDRMNET \_

o tipo de enumeração **\_ \_ tipo de política WMDRMNET** lista os tipos de políticas que estão disponíveis para Windows mídia DRM para operações de dispositivos de rede.

## <a name="syntax"></a>Syntax


```C++
typedef enum WMDRMNET_POLICY_TYPE { 
  WMDRMNET_POLICY_TYPE_UNDEFINED       = 0x0000,
  WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY  = 0x0001
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**\_tipo de política WMDRMNET \_ \_ indefinido**
</dt> <dd>

Não há suporte para tipos de política indefinidos.

</dd> <dt>

<span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**\_tipo de política WMDRMNET \_ \_ TRANSCRYPTPLAY**
</dt> <dd>

a política rege a capacidade de converter conteúdo protegido por Windows drm de mídia em proteção Windows drm de mídia para dispositivos de rede e reproduzi-lo em um dispositivo em redes.

</dd> </dl>

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de enumeração**](drm-enumeration-types.md)
</dt> <dt>

[**política de WMDRMNET \_**](wmdrmnet-policy.md)
</dt> </dl>

 

 





