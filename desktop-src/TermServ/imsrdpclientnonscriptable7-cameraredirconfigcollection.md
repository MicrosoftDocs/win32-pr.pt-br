---
title: Propriedade IMsRdpClientNonScriptable7 CameraRedirConfigCollection
description: Obtém a coleção de câmeras (e as configurações associadas) que estão disponíveis para redirecionamento.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade CameraRedirConfigCollection
- Propriedade CameraRedirConfigCollection Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable7, Propriedade CameraRedirConfigCollection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.CameraRedirConfigCollection
- IMsRdpClientNonScriptable7.get_CameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 817d3d73b4abbf8aa8b4126fd99ed7d11c3fff51
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104295928"
---
# <a name="imsrdpclientnonscriptable7cameraredirconfigcollection-property"></a>Propriedade IMsRdpClientNonScriptable7:: CameraRedirConfigCollection

Obtém a coleção de câmeras (e as configurações associadas) que estão disponíveis para redirecionamento.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_CameraRedirConfigCollection(
  [out, retval] IMsRdpCameraRedirConfigCollection** ppCameraCollection
);
```

## <a name="property-value"></a>Valor da propriedade

Um [IMsRdpCameraRedirConfigCollection](imsrdpcameraredirconfigcollection.md) que representa a coleção de câmeras (e as configurações associadas) que estão disponíveis para redirecionamento.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|---------------------------------------|
| Cliente mínimo com suporte| Windows 10, versão 1803 (build 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClientNonScriptable7 é definido como 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC          |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientNonScriptable7**](imsrdpclientnonscriptable7.md)
</dt> </dl>