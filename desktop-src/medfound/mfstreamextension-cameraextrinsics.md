---
description: Contém as extrínsecos da câmera para o fluxo.
ms.assetid: 2236C135-BA3D-4C1B-8A39-5E23EF67425A
title: Atributo MFStreamExtension_CameraExtrinsics (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a551aaaef48100d6104804e54f7e0ddfac3f5cb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091055"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




