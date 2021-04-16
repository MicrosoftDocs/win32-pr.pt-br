---
description: Contém a marca de formato WAVE original para um fluxo de áudio.
ms.assetid: 2b30a1c2-4a42-4b09-acb6-b76267cc7ed0
title: Atributo MF_MT_ORIGINAL_WAVE_FORMAT_TAG (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba89171f9ae2bf3ab99df05bd3ae64b7d52be6d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786951"
---
# <a name="mf_mt_original_wave_format_tag-attribute"></a>\_Atributo de \_ \_ marca de \_ formato wave original MF \_ MT

Contém a marca de formato WAVE original para um fluxo de áudio.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Comentários

Dependendo do arquivo de origem, a origem da mídia AVI pode definir esse atributo nos tipos de mídia que ele oferece.

Um arquivo AVI contém um cabeçalho de fluxo para cada fluxo no arquivo. A fonte de mídia AVI converte o cabeçalho do fluxo em um tipo de mídia. Para fluxos de áudio, o cabeçalho de fluxo contém uma marca de formato que identifica o formato de áudio. (A marca de formato está contida no membro **wFormatTag** da estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .) Na maioria dos casos, a origem de mídia AVI converte a marca de formato diretamente em um GUID de subtipo, conforme descrito no tópico [**GUIDs de subtipo de áudio**](audio-subtype-guids.md). Em alguns casos, no entanto, ele mapeia a marca de formato original para outra marca de formato equivalente. Nesse caso, a origem da mídia armazena a marca de formato original no tipo de mídia, usando \_ o \_ atributo de marca de formato wave original MF MT \_ \_ \_ .

Os mapeamentos de formato são armazenados no registro sob a seguinte chave:

**HKEY \_ CLASSES \_ raiz** \\ **MediaFoundation** \\ **MapAudioFormatTag**

Cada entrada é um valor **DWORD** . O nome da entrada é a representação decimal da marca de formato. O valor da entrada é a marca de formato equivalente.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 
