---
description: A interface ITLocalParticipant é exposta no objeto Stream quando o IPConf MSP dá suporte à chamada.
ms.assetid: 64965ae2-e30b-4353-a502-f96018da71a5
title: Interface ITLocalParticipant (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4017837a0b970cb791cdf454437fe2d48720028
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788061"
---
# <a name="itlocalparticipant-interface"></a>Interface ITLocalParticipant

A interface **ITLocalParticipant** é exposta no objeto Stream quando o IPConf MSP dá suporte à chamada. O MSP implementa métodos que permitem que um aplicativo obtenha e defina informações do participante. A interface **ITLocalParticipant** é criada chamando **QueryInterface** no [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).

## <a name="members"></a>Membros

A interface **ITLocalParticipant** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITLocalParticipant** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITLocalParticipant** tem esses métodos.



| Método                                                                                     | Descrição                                                                            |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**obter \_ LocalParticipantTypedInfo**](itlocalparticipant-get-localparticipanttypedinfo.md) | Obtém informações do participante, como nome de email ou localização geográfica.<br/> |
| [**colocar \_ LocalParticipantTypedInfo**](itlocalparticipant-put-localparticipanttypedinfo.md) | Define informações do participante.<br/>                                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

