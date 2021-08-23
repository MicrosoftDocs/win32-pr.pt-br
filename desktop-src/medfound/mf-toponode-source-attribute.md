---
description: Contém um ponteiro para a fonte de mídia associada a um nó de topologia.
ms.assetid: 73b84ab6-bdc2-4b22-9ce4-b79b954476e5
title: MF_TOPONODE_SOURCE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce77b001cdfb5bad982de09c3d58cf1a717a5e841cc148d98967e82a60b088a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600096"
---
# <a name="mf_toponode_source-attribute"></a>Atributo MF \_ TOPONODE \_ SOURCE

Contém um ponteiro para a fonte de mídia associada a um nó de topologia.

## <a name="data-type"></a>Tipo de dados

**IUnknown\***

## <a name="remarks"></a>Comentários

Esse atributo se aplica aos nós de origem **(NÓ SOURCESTREAM DA \_ \_ TOPOLOGIA \_ do MF).**

O valor do atributo é um ponteiro para a interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) da fonte de mídia. Esse atributo é necessário.

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> </dl>

 

 




