---
description: Contém os intrínsecos da câmera de pino para o fluxo.
ms.assetid: 7E5E7C60-9C3F-406B-A7DD-A953181CD314
title: MFStreamExtension_PinholeCameraIntrinsics atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0a77f7d49770e084dfe258169863a713311be02f1711c6f637c7bfc16b4e55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973175"
---
# <a name="mfstreamextension_pinholecameraintrinsics-attribute"></a>Atributo MFStreamExtension \_ PinholeCameraIntrinsics

Contém os intrínsecos da câmera de pino para o fluxo.

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFMediaSourceEx::GetStreamAttributes.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes)

## <a name="remarks"></a>Comentários

O valor do atributo é [**um MF VouleCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




