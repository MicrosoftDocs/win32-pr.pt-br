---
description: Especifica o modo estéreo downmix para um decodificador de áudio Dolby Digital.
ms.assetid: 270893C6-8B44-4A4D-AE2B-2E58E260F649
title: Propriedade CODECAPI_AVDecDDStereoDownMixMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7caaed1af804e22b3ec6085241746bdf01eb7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370542"
---
# <a name="codecapi_avdecddstereodownmixmode-property"></a>\_Propriedade CODECAPI AVDecDDStereoDownMixMode

Especifica o modo estéreo downmix para um decodificador de áudio Dolby Digital.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecDDStereoDownMixMode**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade é um membro da enumeração [**eAVDecDDStereoDownMixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecddstereodownmixmode) .

## <a name="remarks"></a>Comentários

Esse atributo se aplica quando a entrada para o decodificador é áudio PCM multicanal e a saída é áudio estéreo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

