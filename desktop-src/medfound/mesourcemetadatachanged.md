---
description: Gerado por uma origem de mídia quando ele atualiza seus metadados.
ms.assetid: 6818b0c9-9628-41e6-8dc6-dff26f4fcfd2
title: Evento MESourceMetadataChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b72463d145d7b4b4b14ac3c321f19a7f9a4c2178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921033"
---
# <a name="mesourcemetadatachanged-event"></a>Evento MESourceMetadataChanged

Gerado por uma origem de mídia quando ele atualiza seus metadados.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="remarks"></a>Comentários

Se a origem da mídia não puder fornecer todos os metadados quando a origem for criada pela primeira vez, ele deverá gerar esse evento depois que os metadados estiverem disponíveis.

A origem da mídia deve criar um novo descritor de apresentação e copiar todos os atributos do descritor de apresentação (PD) para o objeto de evento. O aplicativo pode usar o objeto de evento para enumerar os novos atributos de PD. Em particular, os valores para [a \_ \_ duração do MF PD](mf-pd-duration-attribute.md) e o [ \_ \_ \_ \_ Tamanho total do arquivo MF PD](mf-pd-total-file-size-attribute.md) podem ser desconhecidos até que o arquivo seja completamente baixado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Atributos do descritor de apresentação](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




