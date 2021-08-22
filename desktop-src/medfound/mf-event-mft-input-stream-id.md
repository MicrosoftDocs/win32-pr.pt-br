---
description: Especifica um fluxo de entrada em uma Media Foundation transformação (MFT).
ms.assetid: 2922af62-3fcc-4153-a26a-aba3c4121a0b
title: Atributo MF_EVENT_MFT_INPUT_STREAM_ID (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d211eb30280e6b7390df8509795d49567c7f8a8c9016b2825786858fe888b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973805"
---
# <a name="mf_event_mft_input_stream_id-attribute"></a>\_Atributo de \_ \_ ID do fluxo de entrada do MFT do \_ evento MF \_

Especifica um fluxo de entrada em uma Media Foundation transformação (MFT).

## <a name="data-type"></a>Tipo de dados

**UINT32**

O valor é um identificador de fluxo de entrada.

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a>Comentários

Esse atributo é usado com os seguintes eventos:

-   [METransformDrainComplete](metransformdraincomplete.md)
-   [METransformNeedInput](metransformneedinput.md)

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[aplicativos UWP para aplicativos de área de trabalho Windows 7 \|\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Aplicativos de aplicativos de área de trabalho do servidor 2008 R2 \[ \| UWP\]<br/>                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs assíncrona](asynchronous-mfts.md)
</dt> <dt>

[Atributos do evento](event-attributes.md)
</dt> </dl>

 

 




