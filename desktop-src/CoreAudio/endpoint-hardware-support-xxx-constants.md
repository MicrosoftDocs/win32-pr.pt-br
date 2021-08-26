---
description: As constantes do suporte de hardware do ENDPOINT \_ \_ \_ xxx são sinalizadores de suporte de hardware para um dispositivo de ponto de extremidade de áudio.
ms.assetid: 54032f75-2287-4589-bda5-e005ee077c41
title: Constantes de ENDPOINT_HARDWARE_SUPPORT_XXX (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c975a7bc00229943bb943035bf1fc84609414d83015ce4ae7d84d175b2e18a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053716"
---
# <a name="endpoint_hardware_support_xxx-constants"></a>Constantes de suporte de hardware de ponto de extremidade \_ \_ \_ xxx

As constantes do suporte de hardware do ENDPOINT \_ \_ \_ xxx são sinalizadores de suporte de hardware para um dispositivo de ponto de extremidade de áudio.



| Constante/valor                                                                                                                                                                                                                                                                           | Descrição                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="ENDPOINT_HARDWARE_SUPPORT_VOLUME"></span><span id="endpoint_hardware_support_volume"></span><dl> <dt>**Ponto de extremidade \_ \_ \_ Volume de suporte de hardware**</dt> <dt>0x00000001</dt> </dl> | O dispositivo de ponto de extremidade de áudio dá suporte a um controle de volume de hardware.<br/> |
| <span id="ENDPOINT_HARDWARE_SUPPORT_MUTE"></span><span id="endpoint_hardware_support_mute"></span><dl> <dt>**Ponto de extremidade \_ \_Ativar/ \_ desativar suporte de hardware**</dt> <dt>0x00000002</dt> </dl>       | O dispositivo de ponto de extremidade de áudio dá suporte a um controle de mudo de hardware.<br/>   |
| <span id="ENDPOINT_HARDWARE_SUPPORT_METER"></span><span id="endpoint_hardware_support_meter"></span><dl> <dt>**Ponto de extremidade \_ \_ \_ Medidor de suporte de hardware**</dt> <dt>0x00000004</dt> </dl>    | O dispositivo de ponto de extremidade de áudio dá suporte a um medidor de pico de hardware.<br/>     |



## <a name="remarks"></a>Comentários

Os métodos [**IAudioEndpointVolume:: QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport) e [**IAudioMeterInformation:: QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport) usam as constantes de suporte de hardware de ponto de extremidade \_ \_ \_ xxx.

Uma máscara de suporte de hardware indica quais funções um dispositivo de ponto de extremidade de áudio implementa no hardware. A máscara pode ser 0 ou a combinação bit-a-OR de uma ou mais constantes de suporte de hardware de ponto de extremidade \_ \_ \_ xxx. Se um bit que corresponde a uma constante de suporte de hardware de ponto de extremidade em particular \_ \_ \_ for definido na máscara, o significado é que a função representada por essa constante é implementada no hardware pelo dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Principais constantes de áudio](core-audio-constants.md)
</dt> <dt>

[**IAudioEndpointVolume::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport)
</dt> <dt>

[**IAudioMeterInformation::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport)
</dt> </dl>

 

 




