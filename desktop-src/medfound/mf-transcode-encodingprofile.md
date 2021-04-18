---
description: Especifica o perfil de conformidade do dispositivo para codificar arquivos ASF (Advanced Streaming Format).
ms.assetid: 9a6b6402-ff53-4399-8616-06b7768a8737
title: Atributo MF_TRANSCODE_ENCODINGPROFILE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020344cb2c2f6fc4a539c7cdbc8df0dc69d80d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502107"
---
# <a name="mf_transcode_encodingprofile-attribute"></a>\_Atributo ENCODINGPROFILE de rescodificação MF \_

Especifica o perfil de conformidade do dispositivo para codificar arquivos ASF (Advanced Streaming Format).

## <a name="data-type"></a>Tipo de dados

**LPWSTR**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: Getallocatestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).

Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Comentários

Use esse atributo ao transcodificar para um dispositivo que dá suporte à mídia do Windows. Se esse atributo for definido, o codificador usará o perfil de conformidade do dispositivo, ou modelo, para os codecs de mídia do Windows. Defina o atributo no perfil transcodificar antes de criar a topologia de transcodificação.

O valor desse atributo pode ser qualquer uma das cadeias de caracteres do modelo de conformidade listadas nos seguintes tópicos:

-   [Modelos de conformidade do dispositivo de áudio](../wmformat/audio-device-conformance-templates.md)
-   [Modelos de conformidade de dispositivo de vídeo](../wmformat/video-device-conformance-templates.md)

Para a codificação de vídeo do Windows Media, o construtor de topologias usa esse atributo para definir a propriedade [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) no codificador. O codificador tentará usar o modelo especificado para codificar o conteúdo. Para obter o modelo real, percorra os nós da topologia de transcodificação para obter um ponteiro para o nó do codificador. Em seguida, obtenha o valor da propriedade [**MFPKEY \_ DECODERCOMPLEXITYPROFILE**](mfpkey-decodercomplexityprofileproperty.md) do codificador.

O construtor de topologias também usa o valor desse atributo para definir a propriedade "DeviceConformanceTemplate" no coletor de mídia ASF.

Se esse atributo for definido, o objeto de metadados do arquivo ASF será sempre gerado, independentemente do valor especificado pelo aplicativo do atributo [de \_ \_ transferência de \_ metadados \_ MF de ignorar](mf-transcode-skip-metadata-transfer.md) .

Os valores típicos para esse atributo incluem o seguinte:



| Valor   | Descrição                      |
|---------|----------------------------------|
| PONTOS    | Vídeo de perfil avançado           |
| MP    | Vídeo do perfil principal               |
| SP3    | Vídeo de perfil simples             |
| "MP@LL" | Perfil principal, vídeo de nível médio |
| Cache    | Perfil de áudio, <= 160 kbps    |



 

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[API de transcodificação](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile:: getaudioattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getaudioattributes)
</dt> <dt>

[**IMFTranscodeProfile:: setaudioattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)
</dt> <dt>

[**IMFTranscodeProfile:: setvideoattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getvideoattributes)
</dt> <dt>

[**IMFTranscodeProfile:: getvideoattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
