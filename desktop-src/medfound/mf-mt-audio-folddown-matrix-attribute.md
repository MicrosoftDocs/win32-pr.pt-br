---
description: Especifica como um decodificador de áudio deve transformar áudio de multicanal em saída de estéreo. Esse processo também é chamado de dobra.
ms.assetid: 6dfe2b97-1ebc-4954-b478-85b3bbba89e3
title: Atributo MF_MT_AUDIO_FOLDDOWN_MATRIX (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10bb8aa00835ab31f6c05eaa9a1d0e5d9d126b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760364"
---
# <a name="mf_mt_audio_folddown_matrix-attribute"></a>\_Atributo de \_ \_ matriz FOLDDOWN de áudio MF MT \_

Especifica como um decodificador de áudio deve transformar áudio de multicanal em saída de estéreo. Esse processo também é chamado *de dobra*.

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="remarks"></a>Comentários

Esse atributo se aplica a tipos de mídia de áudio.

O valor desse atributo é uma estrutura [**de \_ matriz MFFOLDDOWN**](/windows/desktop/api/mfapi/ns-mfapi-mffolddown_matrix) .

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

[**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




