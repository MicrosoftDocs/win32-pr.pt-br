---
description: Habilita o processamento de baixa latência no pipeline de Microsoft Media Foundation.
ms.assetid: 4D11B4D6-8CFF-4850-BF8F-9019A1F79153
title: Atributo MF_LOW_LATENCY (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d1b0a89452256f01fc893ced7dc191fd064bbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662610"
---
# <a name="mf_low_latency-attribute"></a>\_Atributo de baixa \_ latência MF

Habilita o processamento de baixa latência no pipeline de Microsoft Media Foundation.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

A baixa latência é definida como o menor atraso possível de quando os dados de mídia são gerados (ou recebidos) quando são renderizados. Baixa latência é desejável para cenários de comunicação em tempo real. Para outros cenários, como reprodução ou transcodificação local, você normalmente não deve habilitar o modo de baixa latência, pois ele pode afetar a qualidade.

> [!Note]  
> O valor de GUID desse atributo é idêntico à propriedade [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md) definida para a interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .

 

Defina esse atributo em componentes de pipeline da seguinte maneira:

-   Origem da mídia: Use o método [**IMFMediaSourceEx:: Getsourceattributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes) .
-   Media Foundation transformar (MFT): Use o método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Para os codificadores, o codificador pode dar suporte à baixa latência por meio da interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .
-   Coletor de mídia: consulte o coletor de mídia para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

Normalmente, os aplicativos não definem esse atributo diretamente nos componentes do pipeline, mas, em vez disso, definem o atributo em um dos seguintes objetos:

-   [Sessão de mídia](media-session.md): Use o parâmetro *PConfiguation* da função [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) ou [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) , ou então defina o atributo na topologia.
-   [Leitor de origem](source-reader.md): defina o atributo com as propriedades de configuração ao criar o leitor de origem. Para obter mais informações, consulte [atributos do leitor de origem](source-reader-attributes.md).
-   [Gravador de coletor](sink-writer.md): defina o atributo com as propriedades de configuração ao criar o gravador de coletor. Para obter mais informações, consulte [atributos do gravador do coletor](sink-writer-attributes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do gravador de coletor](sink-writer-attributes.md)
</dt> <dt>

[Atributos do leitor de origem](source-reader-attributes.md)
</dt> <dt>

[Atributos de transformação](transform-attributes.md)
</dt> </dl>

 

 
