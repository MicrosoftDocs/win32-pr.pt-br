---
title: Interface do IMsRdpCameraRedirConfig
description: Representa as configurações de uma câmera que está disponível para redirecionamento.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpCameraRedirConfig
- Serviços de Área de Trabalho Remota da interface IMsRdpCameraRedirConfig, descrita
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: fbb0f3344e0653ea4a87c876bb8ca7b8a67e7d21
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104500114"
---
# <a name="imsrdpcameraredirconfig-interface"></a>Interface do IMsRdpCameraRedirConfig

Representa as configurações de uma câmera que está disponível para redirecionamento.

## <a name="members"></a>Membros

A interface **IMsRdpCameraRedirConfig** herda de **IUnknown**. **IMsRdpCameraRedirConfig** também tem estes tipos de membros:

- [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsRdpCameraRedirConfig** tem essas propriedades.

| Propriedade         | Tipo de acesso           | Descrição            |
|:-----------------|:----------------------|:-----------------------|
| [**DeviceExists**](imsrdpcameraredirconfig-deviceexists.md)      | Somente leitura | Especifica se o dispositivo de câmera existe ou não no momento (ou seja, a câmera está conectada).   |
| [**FriendlyName**](imsrdpcameraredirconfig-friendlyname.md)                       | Somente leitura |    Obtém o nome amigável da câmera.    |
| [**InstanceId**](imsrdpcameraredirconfig-instanceid.md)      | Somente leitura |  Obtém a ID da instância da câmera.  |
| [**ParentInstanceId**](imsrdpcameraredirconfig-parentinstanceid.md)                       | Somente leitura |    Obtém a ID da instância do dispositivo pai da câmera.   |
| [**Redirected**](imsrdpcameraredirconfig-redirected.md)      | Leitura/Gravação |  Especifica se a câmera é redirecionada ou não.  |
| [**SymbolicLink**](imsrdpcameraredirconfig-symboliclink.md)                       | Somente leitura |   Obtém o link simbólico da interface de **KSCATEGORY_VIDEO_CAMERA** para a câmera.   |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|---------------------------------------|
| Cliente mínimo com suporte| Windows 10, versão 1803 (build 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfig é definido como 09750604-D625-47C1-9FCD-F09F735705D7            |

## <a name="see-also"></a>Confira também

- [**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
- [**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)