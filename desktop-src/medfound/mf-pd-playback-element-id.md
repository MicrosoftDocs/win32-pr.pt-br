---
description: Contém o identificador do elemento playlist na apresentação.
ms.assetid: 355818cf-1e00-46ad-9ce1-ab3a178164f9
title: Atributo MF_PD_PLAYBACK_ELEMENT_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 744a1d164c71cbd7eb8bb47ef12be68d47b8351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754422"
---
# <a name="mf_pd_playback_element_id-attribute"></a>\_Atributo de \_ ID do elemento de reprodução de PD MF \_ \_

Contém o identificador do elemento playlist na apresentação.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Comentários

As fontes de mídia que entregam listas de reprodução podem, opcionalmente, definir esse atributo nos descritores de apresentação.

Quando uma fonte de mídia fornece uma lista de reprodução, ela envia um evento [MENewPresentation](menewpresentation.md) para cada elemento da playlist após o primeiro. Esse evento contém um descritor de apresentação para o novo elemento playlist. A origem da mídia pode atribuir identificadores aos elementos, definindo o \_ atributo de ID do elemento de reprodução de PD MF \_ \_ \_ em cada descritor de apresentação, incluindo aquele criado por [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).

Uma origem de mídia também pode enviar o evento [MENewPresentation](menewpresentation.md) devido a um comutador de fluxo dinâmico ou uma alteração no número de fluxos. Nessa situação, o valor da ID do \_ elemento MF PD \_ playback \_ \_ deve permanecer o mesmo em ambas as apresentações, para indicar que as duas apresentações representam o mesmo elemento de playlist. Se duas apresentações consecutivas tiverem o mesmo valor para esse atributo, o pipeline de Microsoft Media Foundation espera que os carimbos de data/hora permaneçam contínuos na transição. Portanto, a origem da mídia não deve usar o atributo de [ \_ \_ \_ \_ início real da origem do evento MF](mf-event-source-actual-start-attribute.md) quando ela faz a transição para a próxima apresentação.

As fontes de mídia que implementam [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) devem usar o atributo [ \_ \_ \_ ElementID da sequência MF TOPONODE](mf-toponode-sequence-elementid-attribute.md) em vez do atributo de ID do elemento de reprodução de PD do MF \_ \_ \_ \_ .

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                     |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do descritor de apresentação](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




