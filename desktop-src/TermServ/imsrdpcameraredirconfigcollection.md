---
title: Interface do IMsRdpCameraRedirConfigCollection
description: Representa a coleção de câmeras (e as configurações associadas) que estão disponíveis para redirecionamento.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpCameraRedirConfigCollection
- Serviços de Área de Trabalho Remota da interface IMsRdpCameraRedirConfigCollection, descrita
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
ms.openlocfilehash: 3d97249a7485ec024ee3611809c87c5b6ed41143
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104087193"
---
# <a name="imsrdpcameraredirconfigcollection-interface"></a>Interface do IMsRdpCameraRedirConfigCollection

 Representa a coleção de câmeras (e as configurações associadas) que estão disponíveis para redirecionamento.

## <a name="members"></a>Membros

A interface **IMsRdpCameraRedirConfigCollection** herda de **IUnknown**. **IMsRdpCameraRedirConfigCollection** também tem estes tipos de membros:

- [Métodos](#methods)
- [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IMsRdpCameraRedirConfigCollection** tem esses métodos.

| Método            | Descrição              |
|:------------------|:-------------------------|
| [**Addconfig**](imsrdpcameraredirconfigcollection-addconfig.md)       |  Adiciona um objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) à coleção (a câmera correspondente não precisa estar conectada).                   |
| [**Examinar novamente**](imsrdpcameraredirconfigcollection-rescan.md)       |  Enumera os dispositivos de câmera conectados.                   |

### <a name="properties"></a>Propriedades

A interface **IMsRdpCameraRedirConfigCollection** tem essas propriedades.

| Propriedade         | Tipo de acesso           | Descrição            |
|:-----------------|:----------------------|:-----------------------|
| [**ByIndex**](imsrdpcameraredirconfigcollection-byindex.md)      | Somente leitura |  Retorna um objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) por seu índice na coleção.   |
| [**ByInstanceId**](imsrdpcameraredirconfigcollection-byinstanceid.md)                       | Somente leitura |    Retorna um objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) da coleção que corresponde à ID de instância especificada.    |
| [**BySymbolicLink**](imsrdpcameraredirconfigcollection-bysymboliclink.md)      | Somente leitura |  Retorna um objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) da coleção que corresponde ao link simbólico fornecido da interface de **KSCATEGORY_VIDEO_CAMERA** para a câmera.  |
| [**Contar**](imsrdpcameraredirconfigcollection-count.md)                       | Somente leitura |    Retorna o número de objetos [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) na coleção.   |
| [**EncodeVideo**](imsrdpcameraredirconfigcollection-encodevideo.md)      | Leitura/Gravação |  Especifica se o fluxo de vídeo é ou não codificado em H. 264.  |
| [**EncodingQuality**](imsrdpcameraredirconfigcollection-encodingquality.md)                       | Leitura/Gravação |    Especifica a qualidade de codificação (taxa de bits).   |
| [**RedirectByDefault**](imsrdpcameraredirconfigcollection-redirectbydefault.md)                       | Leitura/Gravação |   Especifica se uma nova câmera será redirecionada por padrão.    |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|---------------------------------------|
| Cliente mínimo com suporte| Windows 10, versão 1803 (build 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfigCollection é definido como AE45252B-aaab-4504-B681-649D6073A37A            |

## <a name="see-also"></a>Confira também

- [**IMsRdpCameraRedirConfig**](imsrdpcameraredirconfig.md)
- [**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)
