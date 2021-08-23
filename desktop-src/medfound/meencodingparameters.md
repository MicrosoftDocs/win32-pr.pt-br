---
description: Enviado pelo pipeline para codificar MFTs serialmente com exemplos de mídia por meio de IMFTransform::P rocessEvent.
ms.assetid: D5D4544B-CD8D-4C94-B050-7BA1944800CC
title: Evento MEEncodingParameters (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2230640adf1f92111569a39558f2959271a23ea2b5dbe5d0d915b6a2b989d371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723826"
---
# <a name="meencodingparameters-event"></a>Evento MEEncodingParameters

Enviado pelo pipeline para codificar MFTs serialmente com amostras de mídia por meio [**de IMFTransform::P rocessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ VAZIO<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Os atributos a seguir são definidos para esse evento.



| Atributo                                         | Descrição                                                                                                                    |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)<br/> | Contém as novas configurações baseadas em ICodecAPI que o codificador deve aplicar em exemplos de entrada subsequentes.<br/> <br/> |



## <a name="remarks"></a>Comentários

O conteúdo do evento é um armazenamento de atributos (ponteiro IMFAttributes) que contém as novas configurações baseadas em ICodecAPI /// que o codificador deve aplicar em amostras de entrada subsequentes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                                  |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects.h (inclua Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




