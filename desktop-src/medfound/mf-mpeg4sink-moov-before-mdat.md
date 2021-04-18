---
description: Indica que Moov será gravado antes da caixa mdat no arquivo gerado.
ms.assetid: 97B68B0A-8266-4FCF-8CD9-35890E1AC774
title: Atributo MF_MPEG4SINK_MOOV_BEFORE_MDAT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b5d345dc027c457ceb6123ce3854fff4b74f987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105773041"
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
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




