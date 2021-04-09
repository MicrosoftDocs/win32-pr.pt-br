---
description: Especifica o idioma de um fluxo.
ms.assetid: b64a9554-a560-4212-8964-b68ebbadc046
title: Atributo MF_SD_LANGUAGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad13ec4d7d17e715bd2583e499c686de26c7b9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171028"
---
# <a name="mf_sd_language-attribute"></a>\_Atributo de \_ linguagem SD MF

Especifica o idioma de um fluxo.

## <a name="data-type"></a>Tipo de dados

Cadeia de caracteres largos

## <a name="remarks"></a>Comentários

O valor desse atributo é uma marca de linguagem compatível com RFC 1766. Esse atributo se aplica a descritores de fluxo.

Uma origem de mídia (ou qualquer objeto que cria um descritor de fluxo) pode definir esse atributo se o fluxo tiver um idioma especificado. Os aplicativos podem consultar esse atributo para obter o idioma. Se o atributo não estiver definido, o fluxo não terá um idioma especificado.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]<br/>                              |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Atributos do descritor de fluxo](stream-descriptor-attributes.md)
</dt> </dl>

 

 




