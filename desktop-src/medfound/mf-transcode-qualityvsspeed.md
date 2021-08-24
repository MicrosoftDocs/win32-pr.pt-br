---
description: Especifica um número entre 0 e 100 que indica a compensação entre a qualidade de codificação e a velocidade de codificação.
ms.assetid: 872140e8-fd39-446c-a84f-1e04ea95076e
title: Atributo MF_TRANSCODE_QUALITYVSSPEED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7498cd319f347d8509f42e1713e1b2e267b32406eceb073ea9ca1e4cb4ea8d80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604665"
---
# <a name="mf_transcode_qualityvsspeed-attribute"></a>\_Atributo QUALITYVSSPEED de rescodificação MF \_

Especifica um número entre 0 e 100 que indica a compensação entre a qualidade de codificação e a velocidade de codificação.

## <a name="data-type"></a>Tipo de dados

**UINT32**

O valor dessa propriedade tem o seguinte intervalo.



| Valor                                                                          | Significado                                     |
|--------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>0</dt> </dl>   | Menor qualidade e codificação mais rápida.<br/>  |
| <dl> <dt>100</dt> </dl> | Maior qualidade, codificação mais lenta.<br/> |



 

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Esse atributo tem o mesmo valor de GUID que a propriedade [AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) definida para [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)e tem a mesma interpretação.

o aplicativo pode definir esse atributo no perfil transcodificar antes de criar a topologia de transcodificação para Windows codecs de mídia. O valor deve estar no intervalo de 0 a 100. Para fluxo de vídeo, o construtor de topologia transcodificar mapeia um valor para o valor especificado pelo aplicativo e fornece o valor mapeado para a propriedade **MFPKEY \_ COMPLEXITYEX** do codificador. Valores mais baixos permitem que o codificador use algoritmos de codificação menos complicados. O uso de algoritmos mais simples produz uma saída de baixa qualidade, mas o processo de codificação é mais rápido e requer menos capacidade de processamento.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[API de transcodificação](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile:: setvideoattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
