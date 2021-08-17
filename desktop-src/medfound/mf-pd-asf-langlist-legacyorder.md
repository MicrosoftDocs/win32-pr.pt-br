---
description: Contém uma lista de idiomas RFC 1766 usados na apresentação atual.
ms.assetid: 8853bd88-d51a-478c-8c78-cf69a260e295
title: Atributo MF_PD_ASF_LANGLIST_LEGACYORDER (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32693550ecbe48d14d6e26b9c509f3b90cfd1c327fd945583f1cdff729db7bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102926"
---
# <a name="mf_pd_asf_langlist_legacyorder-attribute"></a>\_Atributo MF PD \_ ASF \_ langlist \_ LEGACYORDER

Contém uma lista de idiomas RFC 1766 usados na apresentação atual.

## <a name="data-type"></a>Tipo de dados

**MINUCIOSA \[\]**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Para definir esse atributo, chame [**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="applies-to"></a>Aplica-se a

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Comentários

Esse atributo se aplica a descritores de apresentação que foram gerados do [objeto ASF ContentInfo](asf-contentinfo-object.md) por uma chamada para [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor). O formato da matriz de bytes é o seguinte:



| Campo de objeto de lista de idiomas | Tipo de dados    | Tamanho    | Descrição                            |
|----------------------------|--------------|---------|----------------------------------------|
| Contagem de registros de ID de idioma  | **DWORD**    | 4 bytes | Número de idiomas                    |
| Registros de ID de idioma        | **MINUCIOSA**\[\] | Varia  | Matriz de cadeias de caracteres de linguagem (veja abaixo). |



 

O primeiro **DWORD** é o número de idiomas, seguido por uma matriz de cadeias de caracteres de identificador de linguagem. Cada cadeia de caracteres tem o seguinte formato:



| Campo de objeto de lista de idiomas | Tipo de dados     | Tamanho    | Descrição                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| Comprimento da ID de idioma         | **DWORD**     | 4 bytes | O comprimento da cadeia de caracteres em bytes, incluindo o tamanho do caractere **nulo** à direita. |
| ID do idioma                | **WCHAR**\[\] | Varia  | Uma cadeia de caracteres terminada em nulo que contém o nome do idioma RFC 1766.                           |



 

Cada cadeia de caracteres é uma marca de idioma compatível com RFC 1766.

Use esse atributo somente para compatibilidade com versões anteriores com a ordem de enumeração da interface [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) no SDK do formato de mídia Windows. As cadeias de caracteres de idioma são armazenadas em uma ordem diferente no atributo [**MF \_ PD \_ ASF \_ langlist**](mf-pd-asf-langlist-attribute.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do descritor de apresentação](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
