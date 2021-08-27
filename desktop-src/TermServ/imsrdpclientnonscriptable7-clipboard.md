---
title: Propriedade IMsRdpClientNonScriptable7 Clipboard
description: Obtém o controlador de área de transferência usado para sincronizar as áreas de transferência locais e remotas se a sincronização manual da área de transferência estiver habilitada.
ms.tgt_platform: multiple
keywords:
- Propriedades da área de transferência Serviços de Área de Trabalho Remota
- A propriedade clipboard Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable7
- Interface IMsRdpClientNonScriptable7 Serviços de Área de Trabalho Remota , propriedade Clipboard
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
ms.openlocfilehash: 236666cbef369c4f2353ff524ceb7544e62f50d4a7e4a7ac59f3882057a92f48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009636"
---
# <a name="imsrdpclientnonscriptable7clipboard-property"></a>Propriedade IMsRdpClientNonScriptable7::Clipboard

Obtém o controlador de área de transferência usado para sincronizar as áreas de transferência locais e remotas se a sincronização manual da área de transferência estiver habilitada.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT get_Clipboard(
  [out, retval] IMsRdpClipboard** ppClipboard
);
```

## <a name="property-value"></a>Valor da propriedade

Uma [IMsRdpClipboard](imsrdpclipboard.md) que representa o controlador de área de transferência usado para sincronizar as áreas de transferência locais e remotas se a sincronização manual da área de transferência estiver habilitada (ou seja, o valor da propriedade [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) está definido como **True).**

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