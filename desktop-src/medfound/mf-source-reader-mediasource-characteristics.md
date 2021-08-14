---
description: Obtém as características da fonte de mídia do Leitor de Origem.
ms.assetid: 4cd48b69-6f7b-4b13-86f3-b38969025f70
title: MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS atributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5ec5461bc289517490ae11bdd507895cd1ad434c53b1665ac5c6394907f15a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739959"
---
# <a name="mf_source_reader_mediasource_characteristics-attribute"></a>Atributo MF \_ SOURCE \_ READER \_ MEDIASOURCE \_ CHARACTERISTICS

Obtém as características da fonte de mídia do [Leitor de Origem.](source-reader.md)

## <a name="data-type"></a>Tipo de dados

**UINT32**

O valor é um **OR bit** a bit de sinalizadores da [**enumeração MFMEDIASOURCE \_ CHARACTERISTICS.**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics)

## <a name="remarks"></a>Comentários

Para obter esse atributo, chame o [**método IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) no leitor de origem. De definir o *parâmetro dwStreamIndex* como **MF \_ SOURCE READER \_ \_ MEDIASOURCE** e *o parâmetro guidAttribute* como MF \_ SOURCE READER \_ \_ MEDIASOURCE \_ CHARACTERISTICS.

O **tipo PROPVARIANT** para esse atributo é **VT \_ UI4.**

## <a name="examples"></a>Exemplos


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows aplicativos UWP de 7 \[ \| áreas de trabalho\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP de aplicativos da área de trabalho do Server 2008 R2 \|\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Leitor de Origem](source-reader.md)
</dt> </dl>

 

 




