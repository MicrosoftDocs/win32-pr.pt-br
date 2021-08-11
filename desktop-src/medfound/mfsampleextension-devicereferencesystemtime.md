---
description: Especifica o data/hora do dispositivo original no exemplo.
ms.assetid: 93BB6E41-308E-4527-A04B-C685C818FEC4
title: MFSampleExtension_DeviceReferenceSystemTime atributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0458c1a2b0f5b204483cba0e6f571a2a5ace34b7b39463cc20ded664eecaaa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241131"
---
# <a name="mfsampleextension_devicereferencesystemtime-attribute"></a>Atributo MFSampleExtension \_ DeviceReferenceSystemTime

Especifica o data/hora do dispositivo original no exemplo.

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="remarks"></a>Comentários

Esse é o carimbo de data/hora de referência do dispositivo de exemplos de mídia em resolução de 100ns. Esse carimbo de data/hora pode ou não carregar o valor real do QPC (contador de desempenho de consulta), dependendo da fonte que produz os exemplos. Esse valor pode ser modificado por outros componentes no pipeline de mídia. Esse valor não está disponível para MFTs inseridos no pipeline de captura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Mfcaptureengine.idl</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




