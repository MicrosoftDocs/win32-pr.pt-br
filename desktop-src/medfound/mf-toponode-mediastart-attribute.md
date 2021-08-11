---
description: Especifica a hora de início da apresentação.
ms.assetid: a2a64cac-0dc1-41b0-b59c-a477c7304ba1
title: MF_TOPONODE_MEDIASTART atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7efeed2bd34745ffda4e756c8b43894bd51fc287ded5cba0ecf0ffb323713754
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244417"
---
# <a name="mf_toponode_mediastart-attribute"></a>Atributo MF \_ TOPONODE \_ MEDIASTART

Especifica a hora de início da apresentação.

## <a name="data-type"></a>Tipo de dados

**UINT64**

Trate como um **valor LONGLONG.**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Para definir esse atributo, chame [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Aplica-se a

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a>Comentários

Esse atributo especifica a posição na origem em que a reprodução é iniciada, em unidades de 100 nanossegundos, em relação ao início da origem. Se o atributo não estiver definido, a reprodução será iniciada em zero (o início do arquivo). Por exemplo, para iniciar a reprodução na marca de 5 segundos, de definir esse atributo como 50000000. De definir o atributo nos nós de origem na topologia (nós com o tipo igual a **MF \_ \_ TOPOLOGY SOURCESTREAM \_ NODE**). De definir o atributo antes [**de chamar IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

> [!Note]  
> Se você inserir manualmente um decodificador na topologia, também deverá definir os atributos [MF \_ TOPNODE \_ MARKIN \_ HERE](mf-toponode-markin-here-attribute.md) e [MF \_ TOPONODE \_ MARKOUT \_ HERE](mf-toponode-markout-here-attribute.md) no nó do decodificador.

 

Esse atributo é um valor assinado, embora seja armazenado como **um UINT64.** No entanto, valores negativos não são significativos.

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Tempos de apresentação de sequência](sequence-presentation-times.md)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> <dt>

[**MF \_ TOPNODE \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md)
</dt> </dl>

 

 




