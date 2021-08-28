---
description: Especifica o tempo necessário para reproduzir um arquivo ASF (Advanced Systems Format), em unidades de 100 nanossegundos.
ms.assetid: 3d36808b-aa13-4205-ad92-97e951ee827e
title: MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc0e4609f70fa96a0e08339e496b1d7ed6ac7004108ec56ff870ed6f4e7fcb6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104342"
---
# <a name="mf_pd_asf_fileproperties_play_duration-attribute"></a>Atributo MF \_ PD \_ ASF \_ FILEPROPERTIES \_ PLAY \_ DURATION

Especifica o tempo necessário para reproduzir um arquivo ASF (Advanced Systems Format), em unidades de 100 nanossegundos.

Esse valor inclui o tempo de pré-roll. Para recuperar a duração real da reprodução, obter o valor do [**atributo MF \_ PD \_ DURATION.**](mf-pd-duration-attribute.md) No entanto, se o valor de pré-roll for maior que a duração da reprodução, o valor de **MF \_ PD \_ DURATION** será zero.

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="remarks"></a>Comentários

Esse atributo se aplica a descritores de apresentação para conteúdo ASF.

O [**método IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.

## <a name="examples"></a>Exemplos


```C++
HRESULT GetPlayDuration(
    IMFASFContentInfo *pContentInfo,  // An initialized ContentInfo object. 
    UINT64 *pcbPlayDuration           // Receives the play duration.
    )
{
    IMFPresentationDescriptor* pPD = NULL;

    HRESULT hr = pContentInfo->GeneratePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION, pcbPlayDuration);
        pPD->Release();
    }
    return hr;
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos do descritor de apresentação](presentation-descriptor-attributes.md)
</dt> <dt>

[Objeto de header ASF](asf-file-structure.md)
</dt> <dt>

[Descritores de apresentação](presentation-descriptors.md)
</dt> </dl>

 

 




