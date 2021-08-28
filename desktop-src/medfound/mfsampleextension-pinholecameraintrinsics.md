---
description: Contém os intrínsecos da câmera de pino para o exemplo.
ms.assetid: AF7EA6A0-90C5-49A8-AD68-776BF770A448
title: MFSampleExtension_PinholeCameraIntrinsics atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb26cd7931b1dfe2e17dcd1b8dfff8ee7f972f6dad066bee6879f0de12b3609
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113076"
---
# <a name="mfsampleextension_pinholecameraintrinsics-attribute"></a>Atributo MFSampleExtension \_ PinholeCameraIntrinsics

Contém os intrínsecos da câmera de pino para o exemplo.

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetBlob.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)

Para definir esse atributo, chame [**IMFAttributes::SetBlob.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)

## <a name="applies-to"></a>Aplica-se a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Comentários

O valor do atributo é [**um MF VouleCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).

Esse atributo é opcional para dar suporte a câmeras que não estão calibradas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




