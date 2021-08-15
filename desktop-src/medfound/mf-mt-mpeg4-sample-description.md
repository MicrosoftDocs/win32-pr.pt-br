---
description: Contém a caixa de descrição de exemplo para um arquivo MP4 ou 3GP.
ms.assetid: ea157988-bd15-465c-bd6a-6d33cc1a0323
title: Atributo MF_MT_MPEG4_SAMPLE_DESCRIPTION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c59827fa5d2ba6c6621c7e251cf319478fd621d24639e105dcd44863495b364
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741757"
---
# <a name="mf_mt_mpeg4_sample_description-attribute"></a>Atributo de descrição de exemplo do MF \_ MT \_ MPEG4 \_ \_

Contém a caixa de descrição de exemplo para um arquivo MP4 ou 3GP.

## <a name="data-type"></a>Tipo de dados

**MINUCIOSA\[\]**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Para definir esse atributo, chame [**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="applies-to"></a>Aplica-se a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Comentários

A caixa Descrição de exemplo descreve a codificação usada para um fluxo no arquivo.

A fonte de arquivos MPEG-4 define esse atributo no tipo de mídia para cada fluxo. O valor do atributo são os dados brutos na caixa Descrição de exemplo. Se a origem do arquivo MPEG-4 puder analisar a descrição do exemplo, ela também adicionará os detalhes do formato ao tipo de mídia. Caso contrário, o aplicativo ou o decodificador deve analisar a descrição de exemplo do atributo de descrição de exemplo do MF \_ MT \_ MPEG4 \_ \_ .

Ao definir esse atributo no coletor MPEG-4 através do método [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) , os dados do atributo exemplo de descrição de MPEG4 do MF \_ MT \_ \_ \_ não devem ser alterados depois que um ou mais exemplos forem enviados para o coletor na interface [**IMFStreamSink::P rocesssample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) do fluxo correspondente.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[aplicativos UWP para aplicativos de área de trabalho Windows 7 \|\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Aplicativos de aplicativos de área de trabalho do servidor 2008 R2 \[ \| UWP\]<br/>                     |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




