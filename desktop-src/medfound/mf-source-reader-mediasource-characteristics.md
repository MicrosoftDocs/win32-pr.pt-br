---
description: Obtém as características da origem da mídia do leitor de origem.
ms.assetid: 4cd48b69-6f7b-4b13-86f3-b38969025f70
title: Atributo MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de4d1ed026f7b74f290446af74a6cf9947612617
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297991"
---
# <a name="mf_source_reader_mediasource_characteristics-attribute"></a>\_Atributo de \_ \_ \_ características Media Source do leitor de origem MF

Obtém as características da origem da mídia do [leitor de origem](source-reader.md).

## <a name="data-type"></a>Tipo de dados

**UINT32**

O valor é um or **bit a** bit de sinalizadores da enumeração de [**\_ características do MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .

## <a name="remarks"></a>Comentários

Para obter esse atributo, chame o método [**IMFSourceReader:: Getpresentationattribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) no leitor de origem. Defina o parâmetro *dwStreamIndex* como **\_ \_ \_ mediaprovider do leitor de origem MF** e o parâmetro *GuidAttribute* como \_ características do leitor de origem MF \_ \_ \_ .

O tipo **PROPVARIANT** para esse atributo é **VT \_ UI4**.

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
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Leitor de origem](source-reader.md)
</dt> </dl>

 

 




