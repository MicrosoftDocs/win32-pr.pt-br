---
description: Contém a hora de início em que uma fonte de mídia é reiniciada de sua posição atual.
ms.assetid: b598b4d1-40e1-4282-b312-5aa6ca3a6733
title: Atributo MF_EVENT_SOURCE_ACTUAL_START (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0132fd8fc50f4e71a3b5bb334bc528d86c04e50c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370669"
---
# <a name="mf_event_source_actual_start-attribute"></a>\_Atributo de \_ \_ início real de origem do evento MF \_

Contém a hora de início em que uma fonte de mídia é reiniciada de sua posição atual.

## <a name="data-type"></a>Tipo de dados

**UINT64**

Tratar como um valor de **LONGLONG** .

## <a name="remarks"></a>Comentários

Esse atributo é usado com o evento [MESourceStarted](mesourcestarted.md) . O atributo é relevante quando os dados do evento estão vazios (**VT \_ vazio**), o que indica que a origem da mídia foi iniciada a partir da posição de reprodução atual. Nesse caso, o atributo **de \_ \_ \_ \_ início real da origem do evento MF** especifica a hora de início real. Se os dados do evento forem **VT \_ vazio** e esse atributo não estiver definido, o tempo de início será considerado como zero.

Quando os dados de evento [MESourceStarted](mesourcestarted.md) contêm a hora de início (**VT \_ i8**), esse atributo não deve ser definido.

Esse atributo é um valor assinado, embora seja armazenado como um **UINT64**.

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

[**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes:: setuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




