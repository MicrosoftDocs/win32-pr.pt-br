---
description: Os GUIDs a seguir definem os tipos para o objeto de exclusão mútua para fluxos ASF (Advanced Systems Format).
ms.assetid: 3db8eebd-2e26-4c77-8f66-7d08436c9e42
title: GUIDs de tipo de exclusão mútua do ASF (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fc035248610c8f58928347093dad4470f58f9818dc99fee1d88ac3fc0d13d88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035534"
---
# <a name="asf-mutual-exclusion-type-guids"></a>GUIDs de tipo de exclusão mútua do ASF

Os GUIDs a seguir definem os tipos para o objeto de exclusão mútua para fluxos ASF (Advanced Systems Format).



| Constante                                                                                                                                                                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFMutexType_Language"></span><span id="mfasfmutextype_language"></span><span id="MFASFMUTEXTYPE_LANGUAGE"></span><dl> <dt>**Linguagem MFASFMutexType \_**</dt> </dl>                 | Os fluxos são mutuamente exclusivos por idioma. Esse tipo de exclusão mútua é semelhante às faixas de áudio em um DVD.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="MFASFMutexType_Bitrate"></span><span id="mfasfmutextype_bitrate"></span><span id="MFASFMUTEXTYPE_BITRATE"></span><dl> <dt>**Taxa de bits MFASFMutexType \_**</dt> </dl>                     | Os fluxos são mutuamente exclusivos por taxa de bits. Esse tipo de exclusão mútua também é chamado de exclusão de MBR (taxa de bits múltipla).<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MFASFMutexType_Presentation"></span><span id="mfasfmutextype_presentation"></span><span id="MFASFMUTEXTYPE_PRESENTATION"></span><dl> <dt>**Apresentação MFASFMutexType \_**</dt> </dl> | Os fluxos são mutuamente exclusivos por apresentação. Esse tipo pode ser usado para muitos cenários, mas só deve ser usado quando o conteúdo é o mesmo, mas assume um formato diferente. Por exemplo, dois fluxos que contêm o mesmo vídeo, um formatado para preencher a tela e o outro mantendo a taxa de proporção de widescreen original, devem ser mutuamente exclusivos usando esse tipo. Outro exemplo são os fluxos que contêm vídeo da mesma cena de ângulos diferentes.<br/> |
| <span id="MFASFMutexType_Unknown"></span><span id="mfasfmutextype_unknown"></span><span id="MFASFMUTEXTYPE_UNKNOWN"></span><dl> <dt>**MFASFMutexType \_ Desconhecido**</dt> </dl>                     | Os fluxos são mutuamente exclusivos com base em critérios personalizados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFASFMutualExclusion::GetType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-gettype)
</dt> <dt>

[**IMFASFMutualExclusion::SetType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype)
</dt> <dt>

[Media Foundation constantes](media-foundation-constants.md)
</dt> </dl>

 

 




