---
title: Estrutura de WMDRMNET_POLICY (wmdrmsdk. h)
description: A \_ estrutura da política WMDRMNET contém a política a ser usada para operações do Windows Media DRM para dispositivos de rede.
ms.assetid: 11eaaeb2-3470-4f58-ae1c-53ee0f60bdce
keywords:
- Formato de mídia do Windows de estrutura de WMDRMNET_POLICY
- estruturar formato de mídia do Windows
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
ms.openlocfilehash: 574e37a8c5ee7f68291012b86cda3a89e25949ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747274"
---
# <a name="wmdrmnet_policy-structure"></a>Estrutura de política do WMDRMNET \_

A estrutura da **\_ política WMDRMNET** contém a política a ser usada para operações do Windows Media DRM para dispositivos de rede.

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

Membro da enumeração [**de \_ \_ tipo de política WMDRMNET**](wmdrmnet-policy-type.md) que especifica o tipo de política.

</dd> <dt>

**pbPolicy**
</dt> <dd>

Buffer que contém a política. O único tipo de política com suporte no momento é o **\_ tipo de política WMDRMNET \_ \_ TRANSCRYPTPLAY**. Este membro é um ponteiro para uma **estrutura \_ \_ TRANSCRYPTPLAY da política WMDRMNET** .

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada como um parâmetro para o método [**IWMDRMNetTransmitter:: GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](drm-structures.md)
</dt> <dt>

[**\_ \_ requisitos globais da política de WMDRMNET \_**](wmdrmnet-policy-global-requirements.md)
</dt> <dt>

[**\_ \_ ambiente mínimo da política de WMDRMNET \_**](wmdrmnet-policy-minimum-environment.md)
</dt> <dt>

[**política de WMDRMNET \_ \_ TRANSCRYPTPLAY**](wmdrmnet-policy-transcryptplay.md)
</dt> <dt>

[**\_tipo de política WMDRMNET \_**](wmdrmnet-policy-type.md)
</dt> </dl>

 

 





