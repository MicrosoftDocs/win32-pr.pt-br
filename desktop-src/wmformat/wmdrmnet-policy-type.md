---
title: WMDRMNET_POLICY_TYPE enumeração (Wmdrmsdk.h)
description: O tipo de enumeração WMDRMNET POLICY TYPE lista os tipos de políticas que estão disponíveis para Windows DRM de \_ Mídia para operações de \_ Dispositivos de Rede.
ms.assetid: 83e9e247-3bd8-4857-97b6-95b3cd5ad25c
keywords:
- WMDRMNET_POLICY_TYPE formato de mídia das janelas de enumeração
- formato de mídia das janelas de enumeração
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
# <a name="wmdrmnet_policy_type-enumeration"></a>Enumeração DE TIPO DE POLÍTICA WMDRMNET \_ \_

O tipo de enumeração **WMDRMNET \_ POLICY \_ TYPE** lista os tipos de políticas que estão disponíveis para operações Windows DRM de Mídia para Dispositivos de Rede.

## <a name="syntax"></a>Sintaxe


```C++
typedef enum WMDRMNET_POLICY_TYPE { 
  WMDRMNET_POLICY_TYPE_UNDEFINED       = 0x0000,
  WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY  = 0x0001
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**TIPO DE POLÍTICA WMDRMNET \_ \_ \_ INDEFINIDO**
</dt> <dd>

Não há suporte para tipos de política indefinido.

</dd> <dt>

<span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**TIPO DE POLÍTICA WMDRMNET \_ \_ \_ TRANSCRYPTPLAY**
</dt> <dd>

A política rege a capacidade de converter o conteúdo protegido pelo DRM de mídia Windows em um DRM de mídia Windows protegido para dados de Dispositivos de Rede e reproduzi-lo em um dispositivo em rede.

</dd> </dl>

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de enumeração**](drm-enumeration-types.md)
</dt> <dt>

[**POLÍTICA \_ WMDRMNET**](wmdrmnet-policy.md)
</dt> </dl>

 

 





