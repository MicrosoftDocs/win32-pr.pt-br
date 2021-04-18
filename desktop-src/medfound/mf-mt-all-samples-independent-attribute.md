---
description: Especifica para um tipo de mídia se cada amostra é independente dos outros exemplos no fluxo.
ms.assetid: 40434f63-e191-45e1-b788-5f80fe7f49ae
title: Atributo MF_MT_ALL_SAMPLES_INDEPENDENT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82173e99a30e033b3d90f6cfec0dc2aa8b3af97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748083"
---
# <a name="mf_mt_all_samples_independent-attribute"></a>\_ \_ Atributo independente de todos os \_ exemplos \_ do MF MT

Especifica para um tipo de mídia se cada amostra é independente dos outros exemplos no fluxo.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Tratar como um valor booliano.

## <a name="remarks"></a>Comentários

Se esse atributo for **false**, alguns exemplos não poderão ser usados sem fazer referência a outros exemplos no fluxo. Por exemplo, se um formato de vídeo contiver quadros Delta, esse atributo deverá ser **false**.

Esse atributo corresponde ao campo **bTemporalCompression** na estrutura do [**tipo de \_ mídia \_**](/windows/win32/api/strmif/ns-strmif-am_media_type) do DirectShow am.

Defina esse atributo como **true** para todos os tipos de mídia descompactados.

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

 

 
