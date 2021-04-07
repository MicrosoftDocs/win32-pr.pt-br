---
description: Especifica o carimbo de data/hora do dispositivo original no exemplo.
ms.assetid: 93BB6E41-308E-4527-A04B-C685C818FEC4
title: Atributo MFSampleExtension_DeviceReferenceSystemTime (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00af99e3d2c34d0e4cf72af519497ea04f13e62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827543"
---
# <a name="mfsampleextension_devicereferencesystemtime-attribute"></a>\_Atributo MFSampleExtension DeviceReferenceSystemTime

Especifica o carimbo de data/hora do dispositivo original no exemplo.

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="remarks"></a>Comentários

Este é um carimbo de data/hora de referência de dispositivo de amostras de mídia em resolução de 100ns. Esse carimbo de data/hora pode ou não transportar o valor real do contador de desempenho de consulta (QPC), dependendo da origem que produz os exemplos. Esse valor pode ser modificado por outros componentes no pipeline de mídia. Esse valor não está disponível para MFTs inserido no pipeline de captura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                   |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Mfcaptureengine. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




