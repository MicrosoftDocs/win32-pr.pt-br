---
title: Estrutura de WMDRMNET_POLICY_MINIMUM_ENVIRONMENT (wmdrmsdk. h)
description: a \_ estrutura de \_ ambiente mínima da política WMDRMNET \_ contém os requisitos mínimos de segurança para Windows Media DRM para dispositivos de rede.
ms.assetid: b1bc9a8d-197e-45fe-a152-0b81add977eb
keywords:
- Formato de mídia do Windows de estrutura de WMDRMNET_POLICY_MINIMUM_ENVIRONMENT
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26c11cf02d7cfcd2e3ab62c4e6b110e2c20b77cf6f79251a23f642b38d4df553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118027457"
---
# <a name="wmdrmnet_policy_minimum_environment-structure"></a>\_Estrutura de \_ ambiente mínima da política de WMDRMNET \_

a estrutura de **\_ \_ \_ ambiente mínima da política WMDRMNET** contém os requisitos mínimos de segurança para Windows Media DRM para dispositivos de rede.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct WMDRMNET_POLICY_MINIMUM_ENVIRONMENT {
  WORD  wMinimumSecurityLevel;
  DWORD dwMinimumAppRevocationListVersion;
  DWORD dwMinimumDeviceRevocationListVersion;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**wMinimumSecurityLevel**
</dt> <dd>

Nível mínimo de segurança do aplicativo necessário.

</dd> <dt>

**dwMinimumAppRevocationListVersion**
</dt> <dd>

A versão mínima da lista de certificados revogados do aplicativo é necessária.

</dd> <dt>

**dwMinimumDeviceRevocationListVersion**
</dt> <dd>

Lista mínima de revogação de certificados de dispositivo necessária.

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

 

 





