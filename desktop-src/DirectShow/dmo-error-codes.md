---
description: A tabela a seguir contém códigos de erro específicos para DMOs (Objetos de Mídia) do Microsoft DirectX. Esses códigos de erro são definidos no arquivo de headerr.h.
ms.assetid: 1ded5656-084d-4315-a414-aebf4a1820dc
title: DMO Códigos de erro (Mediaerr.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aa8f45b8f9f61185adbcd79a354df8ab3e41471067b66179193b825a5e40651
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653290"
---
# <a name="dmo-error-codes"></a>DMO Códigos de erro

A tabela a seguir contém códigos de erro específicos para DMOs (Objetos de Mídia) do Microsoft DirectX. Esses códigos de erro são definidos no arquivo de headerr.h.



| Constante/valor                                                                                                                                                                                                                                                  | Descrição                                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMO_E_INVALIDSTREAMINDEX"></span><span id="dmo_e_invalidstreamindex"></span><dl> <dt>**DMO \_ E \_ INVALIDSTREAMINDEX**</dt> <dt>0x80040201</dt> </dl> | Índice de fluxo inválido.<br/>                                                                                                                                    |
| <span id="DMO_E_INVALIDTYPE"></span><span id="dmo_e_invalidtype"></span><dl> <dt>**DMO \_ E \_ INVALIDTYPE**</dt> <dt>0x80040202</dt> </dl>                      | Tipo de mídia inválido.<br/>                                                                                                                                      |
| <span id="DMO_E_TYPE_NOT_SET"></span><span id="dmo_e_type_not_set"></span><dl> <dt>**DMO \_ E \_ TYPE \_ NOT \_ SET**</dt> <dt>0X80040203</dt> </dl>                 | O tipo de mídia não foi definido. Um ou mais fluxos exigem um tipo de mídia antes que essa operação possa ser executada.<br/>                                                 |
| <span id="DMO_E_NOTACCEPTING"></span><span id="dmo_e_notaccepting"></span><dl> <dt>**DMO \_ E \_ NOTACCEPTING**</dt> <dt>0x80040204</dt> </dl>                   | Os dados não podem ser aceitos neste fluxo. Talvez seja necessário processar mais dados de saída; consulte [**IMediaObject::P rocessInput.**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput)<br/> |
| <span id="DMO_E_TYPE_NOT_ACCEPTED"></span><span id="dmo_e_type_not_accepted"></span><dl> <dt>**DMO \_ E \_ TYPE \_ NOT \_ ACCEPTED**</dt> <dt>0X80040205</dt> </dl>  | O tipo de mídia não foi aceito.<br/>                                                                                                                             |
| <span id="DMO_E_NO_MORE_ITEMS"></span><span id="dmo_e_no_more_items"></span><dl> <dt>**DMO \_ E \_ NÃO HÁ MAIS ITENS \_ \_ 0X80040206**</dt> <dt></dt> </dl>              | O índice de tipo de mídia está fora do intervalo.<br/>                                                                                                                        |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Mediaerr.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DMO Constantes](dmo-constants.md)
</dt> </dl>

 

 




