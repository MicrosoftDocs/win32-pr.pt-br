---
title: Método IMsRdpClientNonScriptable6 SendLocation3D
description: Envia um valor de latitude, longitude e altitude para o servidor para que o local geográfico do cliente possa ser refletido na sessão remota.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SendLocation3D
- Método SendLocation3D Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable6, método SendLocation3D
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation3D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: c63e779b6d6d090544af40a7ee6d9c05f8c49494
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104456325"
---
# <a name="imsrdpclientnonscriptable6sendlocation3d-method"></a>Método IMsRdpClientNonScriptable6:: SendLocation3D

Envia um valor de latitude, longitude e altitude para o servidor para que o local geográfico do cliente possa ser refletido na sessão remota.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT SendLocation3D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude,
  [in] INT32 altitude
);
```

## <a name="parameters"></a>Parâmetros

*latitude* \[ no\]

A latitude de uma localização geográfica. O intervalo válido de valores de latitude é de-90,0 a 90,0 graus.

*longitude* \[ no\]

A longitude de uma localização geográfica. O intervalo válido de valores de latitude é de-180,0 a 180,0 graus.

*altitude* \[ no\]

A altitude de uma localização geográfica em metros.

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
