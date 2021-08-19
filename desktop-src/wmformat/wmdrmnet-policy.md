---
title: WMDRMNET_POLICY estrutura (Wmdrmsdk.h)
description: A estrutura WMDRMNET POLICY contém a política a ser usada para Windows DRM de \_ Mídia para operações de Dispositivos de Rede.
ms.assetid: 11eaaeb2-3470-4f58-ae1c-53ee0f60bdce
keywords:
- WMDRMNET_POLICY formato de mídia do Windows da estrutura
- formato de mídia de janelas de estrutura
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf648ef5e300fa9fef1cf12fd4698f4ec196f62130bf75a02f263cd96931f0bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653419"
---
# <a name="wmdrmnet_policy-structure"></a>Estrutura WMDRMNET \_ POLICY

A **estrutura WMDRMNET \_ POLICY** contém a política a ser usada para Windows DRM de Mídia para operações de Dispositivos de Rede.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct WMDRMNET_POLICY {
  WMDRMNET_POLICY_TYPE ePolicyType;
  BYTE                 *pbPolicy;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**ePolicyType**
</dt> <dd>

Membro da [**enumeração WMDRMNET \_ POLICY \_ TYPE**](wmdrmnet-policy-type.md) que especifica o tipo de política.

</dd> <dt>

**pbPolicy**
</dt> <dd>

Buffer que contém a política. O único tipo de política atualmente com suporte é **WMDRMNET \_ POLICY \_ TYPE \_ TRANSCRYPTPLAY**. Esse membro é um ponteiro para uma estrutura **WMDRMNET \_ POLICY \_ TRANSCRYPTPLAY.**

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada como um parâmetro para o [**método IWMDRMNetTransmitter::GetLeafLicenseResponse.**](iwmdrmnettransmitter-getleaflicenseresponse.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](drm-structures.md)
</dt> <dt>

[**REQUISITOS GLOBAIS DA POLÍTICA WMDRMNET \_ \_ \_**](wmdrmnet-policy-global-requirements.md)
</dt> <dt>

[**AMBIENTE MÍNIMO DA POLÍTICA WMDRMNET \_ \_ \_**](wmdrmnet-policy-minimum-environment.md)
</dt> <dt>

[**WMDRMNET \_ POLICY \_ TRANSCRYPTPLAY**](wmdrmnet-policy-transcryptplay.md)
</dt> <dt>

[**TIPO DE POLÍTICA WMDRMNET \_ \_**](wmdrmnet-policy-type.md)
</dt> </dl>

 

 





