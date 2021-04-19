---
description: Especifica se as topologias têm uma hora de início e de término global.
ms.assetid: 6810a22c-f091-423c-97dd-c04fdabdb9bb
title: Atributo MF_SESSION_GLOBAL_TIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b930ed47c5f314b12aba0075cdc9120d2179325
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814496"
---
# <a name="mf_session_global_time-attribute"></a>\_Atributo de \_ tempo global de sessão MF \_

Especifica se as topologias têm uma hora de início e de término global.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Tratar como um valor booliano.

## <a name="remarks"></a>Comentários

Você pode definir esse atributo ao criar a mídia sesison usando o parâmetro *pConfiguration* da função [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) ou [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

Se esse atributo estiver presente e for diferente de zero, todas as topologias passadas para a sessão de mídia devem ter os atributos [**\_ \_ PROJECTSTART de topologia MF**](mf-topology-projectstart-attribute.md) e [**MF \_ Topology \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) . Esses atributos especificam os horários de início e de parada da topologia em relação à apresentação inteira.

Se esse atributo estiver ausente ou **false**, as topologias não deverão ter o atributo [**MF \_ Topology \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) ou [**MF \_ Topology \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) .

Use este atributo para criar sequências de edição. Para obter mais informações, consulte [tempos de apresentação da sequência](sequence-presentation-times.md).

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de sessão de mídia](media-session-attributes.md)
</dt> <dt>

[Tempos de apresentação da sequência](sequence-presentation-times.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**\_PROJECTSTART de topologia MF \_**](mf-topology-projectstart-attribute.md)
</dt> <dt>

[**\_PROJECTSTOP de topologia MF \_**](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




