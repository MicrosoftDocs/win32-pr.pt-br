---
description: Indica que Moov será gravado antes da caixa mdat no arquivo gerado.
ms.assetid: 97B68B0A-8266-4FCF-8CD9-35890E1AC774
title: Atributo MF_MPEG4SINK_MOOV_BEFORE_MDAT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e98614484beee5187364570e3c5517ba0f61e0d77161484b59af93a9f5a6512c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104732"
---
# <a name="mf_mpeg4sink_moov_before_mdat-attribute"></a>MF \_ MPEG4SINK \_ Moov \_ antes do \_ atributo MDAT

Indica que ' Moov ' será gravado antes da caixa ' mdat ' no arquivo gerado.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

O comportamento padrão do coletor de mídia do MPEG4 é gravar ' Moov ' após a caixa ' mdat '. A configuração desse atributo faz com que o arquivo gerado grave ' Moov ' antes da caixa ' mdat '.

Para que o coletor MPEG4 Use esse atributo, o fluxo de bytes transmitido não deve ser de busca lenta ou remoto para.

Esse recurso envolve uma cópia de arquivo adicional/remuxing.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




