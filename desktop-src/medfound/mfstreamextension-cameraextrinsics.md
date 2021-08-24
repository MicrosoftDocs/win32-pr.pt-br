---
description: Contém as extrínsecos da câmera para o fluxo.
ms.assetid: 2236C135-BA3D-4C1B-8A39-5E23EF67425A
title: Atributo MFStreamExtension_CameraExtrinsics (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acf76c829383d229df8039bfff5d75234d31e2625f758d1bca254217b6e138c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713536"
---
# <a name="mfstreamextension_cameraextrinsics-attribute"></a>\_Atributo MFStreamExtension CameraExtrinsics

Contém as extrínsecos da câmera para o fluxo.

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFMediaSourceEx:: Getstreamattributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes).

## <a name="remarks"></a>Comentários

O valor do atributo é um [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




