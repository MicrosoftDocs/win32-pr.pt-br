---
description: Armazena o tempo (em unidades de 100 a nanossegundos) em que a apresentação deve começar, em relação ao início da origem da mídia.
ms.assetid: 7a3dddad-067b-46af-9ed9-4ccc65f9d772
title: Atributo MF_PD_PLAYBACK_BOUNDARY_TIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22abadb4e0148a2079a9a7387e43599f4f79b8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011740"
---
# <a name="mf_pd_playback_boundary_time-attribute"></a>\_Atributo de \_ \_ tempo limite de reprodução de PD MF \_

Armazena o tempo (em unidades de 100 a nanossegundos) em que a apresentação deve começar, em relação ao início da origem da mídia.

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Para definir esse atributo, chame [**IMFAttributes:: setuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Aplica-se a

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Comentários

O \_ atributo de \_ tempo limite de reprodução de PD MF \_ \_ é opcional para fontes de mídia em uma lista de reprodução. Esse valor indica a hora de início real da apresentação. Considere uma lista de reprodução que inclui fontes de mídia *Element1*, *Element2* e *Element3* em uma sequência. 15 segundos depois que o *Element1* começa a ser reproduzido, ocorre uma alteração dinâmica de fluxo. O novo fluxo deve começar a reproduzir 15 segundos na apresentação. No entanto, o quadro-chave mais próximo do tempo de apresentação de 15 segundos é de 12 segundos para o novo fluxo. Para iniciar a nova apresentação em 15 segundos, uma marca é necessária para que as amostras decodificadas sejam removidas de 12 segundos para 15 segundos.

Antes da transição, o evento [MENewPresentation](menewpresentation.md) é gerado pela fonte de mídia. Isso retorna o descritor de apresentação que contém o atributo de [ID do elemento de reprodução de PD do MF \_ \_ \_ \_](mf-pd-playback-element-id.md) para *Element1*. Além disso, ele contém o \_ atributo de tempo limite de reprodução de PD MF \_ \_ \_ que é definido como 15 segundos para indicar a hora em que a transição ocorreu. A origem da mídia executa a marca de 15 segundos após a decodificação, o que impede que os quadros de 12 segundos a 15 segundos sejam exibidos.

Esse valor afeta apenas o tempo de marcação e não afeta como a sessão de mídia ajusta carimbos de data/hora. Esse atributo é ignorado, a menos que a origem de mídia indique por meio do atributo de ID do elemento de reprodução de PD do MF que esta apresentação é o mesmo elemento de reprodução que o anterior. [ \_ \_ \_ \_ ](mf-pd-playback-element-id.md)

O \_ atributo de \_ tempo limite de reprodução de PD MF \_ \_ é semelhante ao atributo [MF \_ TOPONODE \_ MEDIASTART](mf-toponode-mediastart-attribute.md) que é definido no nó de topologia. Para aplicativos em execução no Windows Vista, as fontes de mídia que implementam [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) devem usar **MF \_ TOPONODE \_ MEDIASTART** em vez de \_ \_ tempo limite de reprodução do MF PD \_ \_ .

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

 

 




