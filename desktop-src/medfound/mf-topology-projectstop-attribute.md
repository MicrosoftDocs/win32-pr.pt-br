---
description: Especifica a hora de início de uma topologia em relação ao início da primeira topologia na sequência.
ms.assetid: 1ca3709e-88ea-40ca-8da4-c2259365122b
title: MF_TOPOLOGY_PROJECTSTOP atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ab227f1fdcda99148be3106b2ea724578f30bd9fd83756cd3b9d16f46ef993
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875393"
---
# <a name="mf_topology_projectstop-attribute"></a>Atributo MF \_ TOPOLOGY \_ PROJECTSTOP

Especifica a hora de início de uma topologia em relação ao início da primeira topologia na sequência.

## <a name="data-type"></a>Tipo de dados

**UINT64**

Trate como um **valor LONGLONG.**

## <a name="remarks"></a>Comentários

O valor é dado em unidades de 100 nanossegundos.

Se a Sessão de Mídia tiver sido criada com o atributo [**MF \_ SESSION GLOBAL \_ \_ TIME**](mf-session-global-time-attribute.md) igual a **TRUE**, todas as topologias deverão conter o atributo **MF \_ TOPOLOGY \_ PROJECTSTOP.** Caso contrário, as topologias não devem conter o **atributo MF \_ TOPOLOGY \_ PROJECTSTOP.** Para obter mais informações, consulte [Tempos de apresentação de sequência.](sequence-presentation-times.md)

Esse atributo é um valor assinado, embora seja armazenado como **um UINT64.**

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

[Tempos de apresentação de sequência](sequence-presentation-times.md)
</dt> <dt>

[Atributos de topologia](topology-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**INÍCIO DO PROJETO \_ DE \_ TOPOLOGIA DO MF**](mf-topology-projectstart-attribute.md)
</dt> </dl>

 

 




