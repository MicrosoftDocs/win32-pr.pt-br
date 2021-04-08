---
title: Propriedade IMsRdpClientNonScriptable7 Clipboard
description: Obtém o controlador da área de transferência usado para sincronizar as áreas de transferência local e remota se a sincronização da área de transferência manual estiver habilitada.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade da área de transferência
- Propriedade da área de transferência Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable7, Propriedade Clipboard
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.Clipboard
- IMsRdpClientNonScriptable7.get_Clipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 770930eb780b3ce8684608ffcdc0c13c1630cab0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "103919670"
---
# <a name="imsrdpclientnonscriptable7clipboard-property"></a>Propriedade IMsRdpClientNonScriptable7:: Clipboard

Obtém o controlador da área de transferência usado para sincronizar as áreas de transferência local e remota se a sincronização da área de transferência manual estiver habilitada.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT get_Clipboard(
  [out, retval] IMsRdpClipboard** ppClipboard
);
```

## <a name="property-value"></a>Valor da propriedade

Um [IMsRdpClipboard](imsrdpclipboard.md) que representa o controlador da área de transferência usado para sincronizar as áreas de transferência local e remota se a sincronização da área de transferência manual estiver habilitada (ou seja, o valor da propriedade [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) for definido como **true**).

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