---
description: Número de amostras de áudio contidas em um bloco compactado de dados de áudio. Esse atributo pode ser usado em formatos de áudio compactados que têm um número fixo de amostras dentro de cada bloco.
ms.assetid: 6ae31548-4d78-4e38-9cfc-01b611a6022d
title: Atributo MF_MT_AUDIO_SAMPLES_PER_BLOCK (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c453fa4daeaa310b5e41add44b63b0fb45372d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780435"
---
# <a name="mf_mt_audio_samples_per_block-attribute"></a>\_Exemplos de áudio MF MT \_ \_ \_ por atributo de \_ bloco

Número de amostras de áudio contidas em um bloco compactado de dados de áudio. Esse atributo pode ser usado em formatos de áudio compactados que têm um número fixo de amostras dentro de cada bloco.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo corresponde ao membro **wSamplesPerBlock** da estrutura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]<br/>                              |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 
