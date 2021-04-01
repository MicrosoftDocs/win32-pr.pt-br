---
description: Contém os nomes amigáveis dos estilos de intercâmbio de mídia acessível (SAMI) sincronizados definidos no arquivo SAMI.
ms.assetid: bc679f0e-17f6-455c-8a00-1d435538ef86
title: Atributo MF_PD_SAMI_STYLELIST (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb07dd1713faa81fd02bfe7a32c81398cddb736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837153"
---
# <a name="mf_pd_sami_stylelist-attribute"></a>Atributo de estilo ' MF \_ PD \_ samilist \_

Contém os nomes amigáveis dos estilos de intercâmbio de mídia acessível (SAMI) sincronizados definidos no arquivo SAMI.

A [fonte de mídia Sami](sami-media-source.md) define esse atributo no descritor de apresentação que ele cria.

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="remarks"></a>Comentários

O blob de atributo tem a seguinte estrutura:



Tipo de Dados

Descrição

Tamanho (bytes)

**DWORD**

Número de cadeias de caracteres de estilo.

4

Para cada cadeia de estilo:

**DWORD**

Tamanho da cadeia de caracteres em bytes, incluindo o caractere **nulo** .

4

**LPWSTR**

Cadeia de caracteres largo terminada em nulo que contém o nome do estilo.

Varia



 

Para definir o estilo ou recuperar o estilo atual, use a interface [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) .

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="examples"></a>Exemplos


```C++
HRESULT DisplaySAMIStyleNames(IMFPresentationDescriptor *pPD)
{
    UINT8 *pBuf = NULL;
    UINT32 cbBuf = 0;

    HRESULT hr = pPD->GetAllocatedBlob(MF_PD_SAMI_STYLELIST, &pBuf, &cbBuf);

    if (SUCCEEDED(hr))
    {

        DWORD cStyles = ((DWORD*)pBuf)[0];
        UINT8 *pStrings = pBuf + sizeof(DWORD);

        for (DWORD i = 0; i < cStyles; i++)
        {
            DWORD cbString = ((DWORD*)pStrings)[0];
            pStrings += sizeof(DWORD);

            wprintf_s(L"%s\n", (WCHAR*)pStrings);

            pStrings += cbString;
        }
    }
    CoTaskMemFree(pBuf);
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos do descritor de apresentação](presentation-descriptor-attributes.md)
</dt> <dt>

[Fonte de mídia SAMI](sami-media-source.md)
</dt> </dl>

 

 




