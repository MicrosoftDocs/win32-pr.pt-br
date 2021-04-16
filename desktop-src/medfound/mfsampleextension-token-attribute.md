---
description: 'Contém um ponteiro para o token que foi fornecido ao método IMFMediaStream:: RequestSample.'
ms.assetid: 9403bb15-e912-4aa3-9af1-fef4a4f9b242
title: Atributo MFSampleExtension_Token (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17331ad098f80c2676e9d057e1688a776cee305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808351"
---
# <a name="mfsampleextension_token-attribute"></a>\_Atributo de token MFSampleExtension

Contém um ponteiro para o token que foi fornecido ao método [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .

## <a name="data-type"></a>Tipo de dados

**IUnknown \** _

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [_ *IMFAttributes:: getunknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="applies-to"></a>Aplica-se a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Comentários

Esse atributo se aplica a exemplos de mídia. O valor do atributo é o ponteiro **IUnknown** que é passado para o parâmetro *PToken* do método [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) . O chamador usa esse atributo para acompanhar o status da solicitação.

Se você estiver escrevendo uma fonte de mídia personalizada, defina esse atributo no exemplo quando o fluxo de mídia fornecer um exemplo em resposta ao método [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) , a menos que o valor de *pToken* seja **nulo**.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]<br/>                              |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de exemplo](sample-attributes.md)
</dt> <dt>

[Amostras de mídia](media-samples.md)
</dt> </dl>

 

 




