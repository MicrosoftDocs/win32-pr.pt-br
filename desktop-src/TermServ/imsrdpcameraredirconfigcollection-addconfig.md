---
title: Método IMsRdpCameraRedirConfigCollection AddConfig
description: Adiciona um objeto IMsRdpCameraRedirConfig à coleção (a câmera correspondente não precisa estar conectada).
ms.tgt_platform: multiple
keywords:
- Método AddConfig Serviços de Área de Trabalho Remota
- Interface addConfig Serviços de Área de Trabalho Remota, IMsRdpCameraRedirConfigCollection
- Interface IMsRdpCameraRedirConfigCollection Serviços de Área de Trabalho Remota, método AddConfig
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.AddConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 88d4f7952497ca0afd970a979441f98864b2855ed3f36f3e556dc4241ed52769
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033646"
---
# <a name="imsrdpcameraredirconfigcollectionaddconfig-method"></a>Método IMsRdpCameraRedirConfigCollection::AddConfig

Adiciona um [objeto IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) à coleção (a câmera correspondente não precisa estar conectada).

## <a name="syntax"></a>Sintaxe

```C++
HRESULT AddConfig(
    [in] BSTR symbolicLink,
    [in] VARIANT_BOOL fRedirected
);
```

## <a name="parameters"></a>Parâmetros

*symbolicLink* \[ Em\]

O link simbólico para o novo [objeto IMsRdpCameraRedirConfig.](imsrdpcameraredirconfig.md)

*fRedirected* \[ Em\]

Especifica se a nova câmera é redirecionada ou não por padrão.

## <a name="return-value"></a>Valor retornado

Retornar **S \_ OK se** for bem-sucedido.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|---------------------------------------|
| Cliente mínimo com suporte| Windows 10, versão 1803 (build 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfigCollection é definido como AE45252B-AAAB-4504-B681-649D6073A37A          |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>