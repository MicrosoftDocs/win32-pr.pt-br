---
title: Interface do IMsRdpCameraRedirConfigCollection
description: Representa a coleção de câmeras (e as configurações associadas) que estão disponíveis para redirecionamento.
ms.tgt_platform: multiple
keywords:
- Interface IMsRdpCameraRedirConfigCollection Serviços de Área de Trabalho Remota
- Interface IMsRdpCameraRedirConfigCollection Serviços de Área de Trabalho Remota , descrita
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 43758b4f129b6f689e857755001324e76d8d735d3e78f2a5ce7444e604e3d920
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119400616"
---
# <a name="imsrdpcameraredirconfigcollection-interface"></a>Interface do IMsRdpCameraRedirConfigCollection

 Representa a coleção de câmeras (e as configurações associadas) que estão disponíveis para redirecionamento.

## <a name="members"></a>Membros

A interface **IMsRdpCameraRedirConfigCollection** herda **de IUnknown.** **IMsRdpCameraRedirConfigCollection** também tem estes tipos de membros:

- [Métodos](#methods)
- [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IMsRdpCameraRedirConfigCollection** tem esses métodos.

| Método            | Descrição              |
|:------------------|:-------------------------|
| [**AddConfig**](imsrdpcameraredirconfigcollection-addconfig.md)       |  Adiciona um [objeto IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) à coleção (a câmera correspondente não precisa estar conectada).                   |
| [**Rescan**](imsrdpcameraredirconfigcollection-rescan.md)       |  Enumera dispositivos de câmera conectados.                   |

### <a name="properties"></a>Propriedades

A interface **IMsRdpCameraRedirConfigCollection** tem essas propriedades.

| Propriedade         | Tipo de acesso           | Description            |
|:-----------------|:----------------------|:-----------------------|
| [**ByIndex**](imsrdpcameraredirconfigcollection-byindex.md)      | Somente leitura |  Retorna um [objeto IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) por seu índice na coleção.   |
| [**ByInstanceId**](imsrdpcameraredirconfigcollection-byinstanceid.md)                       | Somente leitura |    Retorna um [objeto IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) da coleção que corresponde à ID de instância especificada.    |
| [**BySymbolicLink**](imsrdpcameraredirconfigcollection-bysymboliclink.md)      | Somente leitura |  Retorna um [objeto IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) da coleção que corresponde ao link simbólico determinado da interface **KSCATEGORY_VIDEO_CAMERA** para a câmera.  |
| [**Contagem**](imsrdpcameraredirconfigcollection-count.md)                       | Somente leitura |    Retorna o número de [objetos IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) na coleção.   |
| [**EncodeVideo**](imsrdpcameraredirconfigcollection-encodevideo.md)      | Leitura/Gravação |  Especifica se o fluxo de vídeo é codificado em H.264 ou não.  |
| [**Igualdade de codificação**](imsrdpcameraredirconfigcollection-encodingquality.md)                       | Leitura/Gravação |    Especifica a qualidade da codificação (taxa de bits).   |
| [**RedirectByDefault**](imsrdpcameraredirconfigcollection-redirectbydefault.md)                       | Leitura/Gravação |   Especifica se uma nova câmera é redirecionada ou não por padrão.    |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|---------------------------------------|
| Cliente mínimo com suporte| Windows 10, versão 1803 (build 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfigCollection é definido como AE45252B-AAAB-4504-B681-649D6073A37A            |

## <a name="see-also"></a>Confira também

- [**IMsRdpCameraRedirConfig**](imsrdpcameraredirconfig.md)
- [**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)
