---
description: Especifica se o sink de captura de amostra usa o relógio de apresentação para agendar exemplos.
ms.assetid: 780ec4a6-8e14-4b81-9d50-82b2850c70ae
title: MF_SAMPLEGRABBERSINK_IGNORE_CLOCK atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d757b02a060b4e598ff42d3bd8b9ad7f38af41143c807647aa6f2b8528677cf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474419"
---
# <a name="mf_samplegrabbersink_ignore_clock-attribute"></a>Atributo MF \_ SAMPLEGRABBERSINK \_ \_ IGNORE CLOCK

Especifica se o sink de captura de amostra usa o relógio de apresentação para agendar exemplos.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Você pode definir esse atributo no objeto de ativação criado pela [**função MFCreateSampleGrabberSinkActivate.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) De definir o atributo antes de chamar [**o método IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) no objeto de ativação.

Por padrão, quando o sink-grabber de exemplo recebe um exemplo, ele aguarda até o tempo de apresentação do exemplo para invocar o retorno de chamada do aplicativo. Se o atributo MF SAMPLEGRABBERSINK IGNORE CLOCK for não zero, o \_ \_ sink-grabber de exemplo ignorará o relógio de apresentação e invocará o retorno de chamada assim que receber \_ cada amostra.

Uso recomendado:

-   Se você quiser processar amostras o mais rápido possível, de definir esse atributo como **TRUE.**
-   Se você quiser que as chamadas para o método de retorno de chamada sejam sincronizadas com o relógio, não de definir esse atributo ou defini-lo como **FALSE.** Você pode obter exemplos um pouco antes do relógio, enquanto ainda permanece sincronizado, definindo o atributo [**MF \_ SAMPLEGRABBERSINK \_ SAMPLE TIME \_ \_ OFFSET.**](mf-samplegrabbersink-sample-time-offset-attribute.md)

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> </dl>

 

 




