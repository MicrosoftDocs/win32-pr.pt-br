---
description: As GUIDs a seguir definem extensões de carga para fluxos ASF (Advanced Systems Format).
ms.assetid: db973b41-1e5c-4bc8-921d-5e9312eb21cb
title: GUIDs de extensão de carga ASF (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6478c024d3e79b0f8035f03b6e893e2e5d0308037242f9ac3013450b57f83242
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959566"
---
# <a name="asf-payload-extension-guids"></a>GUIDs de extensão de carga ASF

As GUIDs a seguir definem extensões de carga para fluxos ASF (Advanced Systems Format).



| Constante                                                                                                                                                                                                                                                                                      | Descrição                                                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFSampleExtension_SampleDuration"></span><span id="mfasfsampleextension_sampleduration"></span><span id="MFASFSAMPLEEXTENSION_SAMPLEDURATION"></span><dl> <dt>**MFASFSampleExtension \_ SampleDuration**</dt> </dl>         | Os dados indicam a duração, em milissegundos, do exemplo contido no objeto de buffer.<br/>                                                                       |
| <span id="MFASFSampleExtension_OutputCleanPoint"></span><span id="mfasfsampleextension_outputcleanpoint"></span><span id="MFASFSAMPLEEXTENSION_OUTPUTCLEANPOINT"></span><dl> <dt>**MFASFSampleExtension \_ OutputCleanPoint**</dt> </dl> | Os dados indicam se o exemplo é um quadro-chave. Um valor de zero indica que o exemplo não é um quadro-chave. Um valor diferente de zero indica que se trata de um quadro-chave.<br/> |
| <span id="MFASFSampleExtension_SMPTE"></span><span id="mfasfsampleextension_smpte"></span><span id="MFASFSAMPLEEXTENSION_SMPTE"></span><dl> <dt>**MFASFSampleExtension \_ SMPTE**</dt> </dl>                                             | Os dados são um código de tempo SMPTE.<br/>                                                                                                                                        |
| <span id="MFASFSampleExtension_FileName"></span><span id="mfasfsampleextension_filename"></span><span id="MFASFSAMPLEEXTENSION_FILENAME"></span><dl> <dt>**\_Nome de arquivo MFASFSampleExtension**</dt> </dl>                                 | Os dados na extensão de exemplo especificam o nome do arquivo do qual o conteúdo no exemplo foi tirado.<br/>                                                       |
| <span id="MFASFSampleExtension_ContentType"></span><span id="mfasfsampleextension_contenttype"></span><span id="MFASFSAMPLEEXTENSION_CONTENTTYPE"></span><dl> <dt>**\_ContentType MFASFSampleExtension**</dt> </dl>                     | Os dados identificam o tipo de conteúdo que o exemplo contém.<br/>                                                                                                     |
| <span id="MFASFSampleExtension_PixelAspectRatio"></span><span id="mfasfsampleextension_pixelaspectratio"></span><span id="MFASFSAMPLEEXTENSION_PIXELASPECTRATIO"></span><dl> <dt>**MFASFSampleExtension \_ PixelAspectRatio**</dt> </dl> | Os dados indicam a taxa de proporção de pixel do conteúdo no exemplo.<br/>                                                                                               |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFASFStreamConfig::AddPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension)
</dt> <dt>

[**IMFASFStreamConfig::GetPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension)
</dt> <dt>

[Media Foundation constantes](media-foundation-constants.md)
</dt> </dl>

 

 




