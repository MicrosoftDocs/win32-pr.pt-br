---
description: Quando uma fonte de mídia solicita uma nova taxa de reprodução, esse atributo especifica se a origem também solicita a fina. Para obter uma definição de estreitamento, consulte sobre o controle de taxa.
ms.assetid: 42b6d0b3-e5af-4a48-969c-53628d1b7c31
title: Atributo MF_EVENT_DO_THINNING (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08807413881a13789c50dbf2d063693e7e4539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921029"
---
# <a name="mf_event_do_thinning-attribute"></a>O \_ evento MF \_ faz o atributo de \_ finamento

Quando uma fonte de mídia solicita uma nova taxa de reprodução, esse atributo especifica se a origem também solicita a fina. Para obter uma definição de estreitamento, consulte [sobre o controle de taxa](about-rate-control.md).

## <a name="data-type"></a>Tipo de dados

**UINT32**

Tratar como um valor booliano.

## <a name="remarks"></a>Comentários

Esse atributo é usado com o evento [MESourceRateChangeRequested](mesourceratechangerequested.md) . Se o valor for **true**, a origem da mídia estará solicitando um comutador para reprodução fina.

O valor padrão é **false**.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do evento](event-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




