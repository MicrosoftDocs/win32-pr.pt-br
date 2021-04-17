---
description: A tabela a seguir contém códigos de erro específicos para o Microsoft DirectX Media Objects (DMOs). Esses códigos de erro são definidos no arquivo de cabeçalho Mediaerr. h.
ms.assetid: 1ded5656-084d-4315-a414-aebf4a1820dc
title: Códigos de erro DMO (Mediaerr. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76c8cd5e7001751cd2cf9eb7da4d88b2dc100bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747573"
---
# <a name="dmo-error-codes"></a>Códigos de erro do DMO

A tabela a seguir contém códigos de erro específicos para o Microsoft DirectX Media Objects (DMOs). Esses códigos de erro são definidos no arquivo de cabeçalho Mediaerr. h.



| Constante/valor                                                                                                                                                                                                                                                  | Descrição                                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMO_E_INVALIDSTREAMINDEX"></span><span id="dmo_e_invalidstreamindex"></span><dl> <dt>**DMO \_ E \_ INVALIDSTREAMINDEX**</dt> <dt>0x80040201</dt> </dl> | Índice de fluxo inválido.<br/>                                                                                                                                    |
| <span id="DMO_E_INVALIDTYPE"></span><span id="dmo_e_invalidtype"></span><dl> <dt>**DMO \_ E \_ INvalidatype**</dt> <dt>0x80040202</dt> </dl>                      | Tipo de mídia inválido.<br/>                                                                                                                                      |
| <span id="DMO_E_TYPE_NOT_SET"></span><span id="dmo_e_type_not_set"></span><dl> <dt>**DMO \_ \_Tipo E \_ não \_ definido**</dt> <dt>0x80040203</dt> </dl>                 | O tipo de mídia não foi definido. Um ou mais fluxos exigem um tipo de mídia para que essa operação possa ser executada.<br/>                                                 |
| <span id="DMO_E_NOTACCEPTING"></span><span id="dmo_e_notaccepting"></span><dl> <dt>**DMO \_ E não \_ aceitar**</dt> <dt>0x80040204</dt> </dl>                   | Os dados não podem ser aceitos neste fluxo. Talvez seja necessário processar mais dados de saída; consulte [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput).<br/> |
| <span id="DMO_E_TYPE_NOT_ACCEPTED"></span><span id="dmo_e_type_not_accepted"></span><dl> <dt>**DMO \_ \_Tipo E \_ não \_ aceito**</dt> <dt>0x80040205</dt> </dl>  | O tipo de mídia não foi aceito.<br/>                                                                                                                             |
| <span id="DMO_E_NO_MORE_ITEMS"></span><span id="dmo_e_no_more_items"></span><dl> <dt>**DMO \_ E \_ não há \_ mais \_ itens**</dt> <dt>0x80040206</dt> </dl>              | O índice do tipo de mídia está fora do intervalo.<br/>                                                                                                                        |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Mediaerr. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes do DMO](dmo-constants.md)
</dt> </dl>

 

 




