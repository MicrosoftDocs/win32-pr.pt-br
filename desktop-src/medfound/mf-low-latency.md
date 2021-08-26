---
description: Habilita o processamento de baixa latência no pipeline Microsoft Media Foundation dados.
ms.assetid: 4D11B4D6-8CFF-4850-BF8F-9019A1F79153
title: MF_LOW_LATENCY atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51421b68e23ab3f29c15b0b360a7d189befb45cd9046176e6dcb99f1b0748f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956446"
---
# <a name="mf_low_latency-attribute"></a>Atributo MF \_ LOW \_ LATENCY

Habilita o processamento de baixa latência no pipeline Microsoft Media Foundation dados.

## <a name="data-type"></a>Tipo de dados

**BOOL** armazenado como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

A baixa latência é definida como o menor atraso possível de quando os dados de mídia são gerados (ou recebidos) até quando são renderizados. A baixa latência é desejável para cenários de comunicação em tempo real. Para outros cenários, como reprodução local ou transcodificação, normalmente você não deve habilitar o modo de baixa latência, pois isso pode afetar a qualidade.

> [!Note]  
> O valor guid desse atributo é idêntico à propriedade [ \_ CODECAPI AVLowLatencyMode](codecapi-avlowlatencymode.md) definida para a interface [**ICodecAPI.**](/windows/win32/api/strmif/nn-strmif-icodecapi)

 

De definir esse atributo em componentes de pipeline da seguinte forma:

-   Fonte de mídia: use [**o método IMFMediaSourceEx::GetSourceAttributes.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes)
-   Media Foundation transformação (MFT): use o [**método IMFTransform::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) Para codificadores, o codificador pode dar suporte à baixa latência por meio da interface [**ICodecAPI.**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   Sink de mídia: consulte o sink de mídia para a interface [**IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

Os aplicativos normalmente não configuram esse atributo diretamente nos componentes do pipeline, mas, em vez disso, configuram o atributo em um dos seguintes objetos:

-   Sessão de [Mídia:](media-session.md)use o parâmetro *pConfiguation* da função [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) ou [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) ou delimita o atributo na topologia.
-   [Leitor de Origem:](source-reader.md)de definido o atributo com as propriedades de configuração ao criar o Leitor de Origem. Para obter mais informações, consulte [Atributos de leitor de origem](source-reader-attributes.md).
-   [Sink Writer:](sink-writer.md)de definir o atributo com as propriedades de configuração ao criar o Sink Writer. Para obter mais informações, consulte [Sink Writer Attributes](sink-writer-attributes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do Sink Writer](sink-writer-attributes.md)
</dt> <dt>

[Atributos de leitor de origem](source-reader-attributes.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 
