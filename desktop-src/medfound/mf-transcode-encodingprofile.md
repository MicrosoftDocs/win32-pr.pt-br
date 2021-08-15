---
description: Especifica o perfil de conformidade do dispositivo para codificar arquivos ASF (Advanced Streaming Format).
ms.assetid: 9a6b6402-ff53-4399-8616-06b7768a8737
title: MF_TRANSCODE_ENCODINGPROFILE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58b44a923abc563a84f3536fd6353ac2a3dd2352e472344edf7053d647674908
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244227"
---
# <a name="mf_transcode_encodingprofile-attribute"></a>Atributo MF \_ TRANSCODE \_ ENCODINGPROFILE

Especifica o perfil de conformidade do dispositivo para codificar arquivos ASF (Advanced Streaming Format).

## <a name="data-type"></a>Tipo de dados

**Lpwstr**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetAllocatedString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).

Para definir esse atributo, chame [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Comentários

Use esse atributo ao transcodificar para um dispositivo que dá suporte Windows Mídia. Se esse atributo for definido, o codificador usará o perfil de conformidade do dispositivo ou o modelo para codecs Windows Mídia. De definir o atributo no perfil de transcodificar antes de criar a topologia de transcodificar.

O valor desse atributo pode ser qualquer uma das cadeias de caracteres de modelo de conformidade listadas nos tópicos a seguir:

-   [Modelos de conformidade do dispositivo de áudio](../wmformat/audio-device-conformance-templates.md)
-   [Modelos de conformidade do dispositivo de vídeo](../wmformat/video-device-conformance-templates.md)

Para Windows de vídeo de mídia, o construtor de topologia usa esse atributo para definir a propriedade [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) no codificador. O codificador tentará usar o modelo especificado para codificar o conteúdo. Para obter o modelo real, percorra os nós da topologia de transcódigo para obter um ponteiro para o nó do codificador. Em seguida, obter o valor da [**propriedade \_ MFPKEY DECODERCOMPLEXITYPROFILE**](mfpkey-decodercomplexityprofileproperty.md) do codificador.

O construtor de topologia também usa o valor desse atributo para definir a propriedade "DeviceConformanceTemplate" no sink de mídia do ASF.

Se esse atributo for definido, o objeto de metadados do arquivo ASF sempre será gerado independentemente do valor especificado pelo aplicativo do atributo [MF \_ TRANSCODE \_ SKIP \_ METADATA \_ TRANSFER.](mf-transcode-skip-metadata-transfer.md)

Os valores típicos para esse atributo incluem o seguinte:



| Valor   | Descrição                      |
|---------|----------------------------------|
| "AP"    | Vídeo de perfil avançado           |
| "MP"    | Vídeo de perfil principal               |
| "SP"    | Vídeo de perfil simples             |
| "MP@LL" | Perfil principal, vídeo de nível médio |
| "L2"    | Perfil de áudio, <= 160 Kbps    |



 

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[API de transcodificar](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile::GetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getaudioattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getvideoattributes)
</dt> <dt>

[**IMFTranscodeProfile::GetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
