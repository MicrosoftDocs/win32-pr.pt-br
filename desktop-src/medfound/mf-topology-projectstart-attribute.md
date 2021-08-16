---
description: Especifica o tempo de parada de uma topologia, em relação ao início da primeira topologia na sequência.
ms.assetid: 7669f97e-87ad-4a64-a2a5-62b8ce450d80
title: MF_TOPOLOGY_PROJECTSTART atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f295f68b3ac94bf29fa4607eb2b5ba00ea8eab19774bcaa0af150ef6d3fbe1f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875403"
---
# <a name="mf_topology_projectstart-attribute"></a>Atributo MF \_ TOPOLOGY \_ PROJECTSTART

Especifica o tempo de parada de uma topologia, em relação ao início da primeira topologia na sequência.

## <a name="data-type"></a>Tipo de dados

**UINT64**

Trate como um **valor LONGLONG.**

## <a name="remarks"></a>Comentários

O valor é dado em unidades de 100 nanossegundos.

Se a Sessão de Mídia tiver sido criada com o atributo [**MF \_ SESSION GLOBAL \_ \_ TIME**](mf-session-global-time-attribute.md) igual a **TRUE**, todas as topologias deverão conter o atributo **\_ \_ PROJECTSTART da TOPOLOGIA do MF.** Caso contrário, as topologias não devem conter o **atributo MF \_ TOPOLOGY \_ PROJECTSTART.** Para obter mais informações, consulte [Tempos de apresentação de sequência.](sequence-presentation-times.md)

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

[**PROJETOS DE \_ TOPOLOGIA DO MFTOP \_**](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




