---
description: As GUIDs a seguir definem os tipos para o objeto de exclusão mútua para fluxos ASF (Advanced Systems Format).
ms.assetid: 3db8eebd-2e26-4c77-8f66-7d08436c9e42
title: GUIDs do tipo de exclusão mútua do ASF (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a6fedc766e26c35bb967054a704b732ca03e8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164222"
---
# <a name="asf-mutual-exclusion-type-guids"></a>GUIDs do tipo de exclusão mútua do ASF

As GUIDs a seguir definem os tipos para o objeto de exclusão mútua para fluxos ASF (Advanced Systems Format).



| Constante                                                                                                                                                                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFMutexType_Language"></span><span id="mfasfmutextype_language"></span><span id="MFASFMUTEXTYPE_LANGUAGE"></span><dl> <dt>**\_Linguagem MFASFMutexType**</dt> </dl>                 | Os fluxos são mutuamente exclusivos por idioma. Esse tipo de exclusão mútua é semelhante às faixas de áudio em um DVD.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="MFASFMutexType_Bitrate"></span><span id="mfasfmutextype_bitrate"></span><span id="MFASFMUTEXTYPE_BITRATE"></span><dl> <dt>**\_Taxa de bits MFASFMutexType**</dt> </dl>                     | Os fluxos são mutuamente exclusivos por taxa de bits. Esse tipo de exclusão mútua também é chamado de exclusão de taxa de bits múltipla (MBR).<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MFASFMutexType_Presentation"></span><span id="mfasfmutextype_presentation"></span><span id="MFASFMUTEXTYPE_PRESENTATION"></span><dl> <dt>**Apresentação do MFASFMutexType \_**</dt> </dl> | Os fluxos são mutuamente exclusivos por apresentação. Esse tipo pode ser usado para muitos cenários, mas só deve ser usado quando o conteúdo é o mesmo, mas usa um formulário diferente. Por exemplo, dois fluxos contendo o mesmo vídeo, um formatado para preencher a tela e o outro, mantendo a proporção de proporção widescreen original, devem ser mutuamente exclusivos com o uso desse tipo. Outro exemplo são os fluxos que contêm vídeo da mesma captura de cena de diferentes ângulos.<br/> |
| <span id="MFASFMutexType_Unknown"></span><span id="mfasfmutextype_unknown"></span><span id="MFASFMUTEXTYPE_UNKNOWN"></span><dl> <dt>**MFASFMutexType \_ desconhecido**</dt> </dl>                     | Os fluxos são mutuamente exclusivos com base em critérios personalizados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFASFMutualExclusion:: GetType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-gettype)
</dt> <dt>

[**IMFASFMutualExclusion:: SetType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype)
</dt> <dt>

[Media Foundation constantes](media-foundation-constants.md)
</dt> </dl>

 

 




