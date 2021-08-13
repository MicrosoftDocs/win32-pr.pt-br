---
description: Contém a marca de formato WAVE original para um fluxo de áudio.
ms.assetid: 2b30a1c2-4a42-4b09-acb6-b76267cc7ed0
title: MF_MT_ORIGINAL_WAVE_FORMAT_TAG atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89f05086858f54c619e3896f5978cf81005e9b1e80e858bc89c71e951ab48b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741661"
---
# <a name="mf_mt_original_wave_format_tag-attribute"></a>Atributo \_ MF MT \_ ORIGINAL \_ WAVE FORMAT \_ \_ TAG

Contém a marca de formato WAVE original para um fluxo de áudio.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Comentários

Dependendo do arquivo de origem, a fonte de mídia AVI pode definir esse atributo nos tipos de mídia que oferece.

Um arquivo AVI contém um header de fluxo para cada fluxo no arquivo. A fonte de mídia AVI converte o header de fluxo em um tipo de mídia. Para fluxos de áudio, o título do fluxo contém uma marca de formato que identifica o formato de áudio. (A marca de formato está contida no **membro wFormatTag** da [**estrutura WAVEFORMATEX.)**](/previous-versions/dd757713(v=vs.85)) Na maioria dos casos, a fonte de mídia AVI converte a marca de formato diretamente em um GUID de subtipo, conforme descrito no tópico [**GUIDs de subtipo de áudio**](audio-subtype-guids.md). Em alguns casos, no entanto, ele mapeia a marca de formato original para outra marca de formato equivalente. Nesse caso, a fonte de mídia armazena a marca de formato original no tipo de mídia, usando o atributo \_ MF MT \_ ORIGINAL WAVE FORMAT \_ \_ \_ TAG.

Os mapeamentos de formato são armazenados no Registro sob a seguinte chave:

**HKEY \_ CLASSES \_ ROOT** \\ **MediaFoundation** \\ **MapAudioFormatTag**

Cada entrada é um **valor DWORD.** O nome da entrada é a representação decimal da marca de formato. O valor da entrada é a marca de formato equivalente.

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 
