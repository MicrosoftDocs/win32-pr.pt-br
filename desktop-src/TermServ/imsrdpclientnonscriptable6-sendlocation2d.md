---
title: Método IMsRdpClientNonScriptable6 SendLocation2D
description: Envia um valor de latitude e longitude para o servidor para que a localização geográfica do cliente possa ser refletida na sessão remota.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SendLocation2D
- Método SendLocation2D Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable6, método SendLocation2D
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation2D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: b706fdb35ba8360b294d25021c0c1a18bbe90188
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "103645610"
---
# <a name="imsrdpclientnonscriptable6sendlocation2d-method"></a>Método IMsRdpClientNonScriptable6:: SendLocation2D

Envia um valor de latitude e longitude para o servidor para que a localização geográfica do cliente possa ser refletida na sessão remota.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT SendLocation2D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude
);
```

## <a name="parameters"></a>Parâmetros

*latitude* \[ no\]

A latitude de uma localização geográfica. O intervalo válido de valores de latitude é de-90,0 a 90,0 graus.

*longitude* \[ no\]

A longitude de uma localização geográfica. O intervalo válido de valores de latitude é de-180,0 a 180,0 graus.

## <a name="return-value"></a>Retornar valor

Retornar **S \_ OK** se for bem-sucedido.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|---------------------------------------|
| Cliente mínimo com suporte| Windows 10, versão 1709 (build 16299)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClientNonScriptable6 é definido como 05293249-B28B-4DB8-BE64-1B2F496B910E            |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md)
</dt> </dl>
