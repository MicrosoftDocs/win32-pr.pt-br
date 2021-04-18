---
description: As \_ constantes de sinalizador de bit LINECALLPRIVILEGE descrevem os tipos de direitos de acesso ou privilégios que um aplicativo com um identificador de chamada pode ter para a chamada correspondente.
ms.assetid: a58b7e9e-696e-4421-9b31-1ba8afe6e03b
title: Constantes de LINECALLPRIVILEGE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2569ec255d2da3ad384292eb87afaa285f54b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759048"
---
# <a name="linecallprivilege_-constants"></a>\_Constantes LINECALLPRIVILEGE

As constantes de sinalizador de bit **LINECALLPRIVILEGE \_** descrevem os tipos de direitos de acesso ou privilégios que um aplicativo com um identificador de chamada pode ter para a chamada correspondente.

<dl> <dt>

<span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**MONITOR de LINECALLPRIVILEGE \_**
</dt> <dd> <dl> <dt>



O aplicativo tem privilégios de monitor para a chamada. Esses privilégios permitem que o aplicativo monitore as alterações de estado e as informações de consulta e o status sobre a chamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**LINECALLPRIVILEGE \_ nenhum**
</dt> <dd> <dl> <dt>



O aplicativo não tem privilégios para a chamada. O identificador do aplicativo é void e não deve ser usado.


</dt> </dl> </dd> <dt>

<span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**proprietário do LINECALLPRIVILEGE \_**
</dt> <dd> <dl> <dt>



O aplicativo tem privilégios de proprietário para a chamada. Esses privilégios permitem que o aplicativo manipule a chamada de maneira que afete o estado da chamada.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

Quando um identificador de chamada é fornecido pela primeira vez a um aplicativo ou sempre que os privilégios de chamada desse aplicativo são modificados, a mensagem [**\_ callstate de linha**](line-callstate.md) é enviada ao aplicativo. Quando um aplicativo passa por uma chamada e, se o aplicativo de recebimento ainda não tiver um identificador com privilégios de proprietário, essa mensagem informará ao aplicativo sobre seus novos privilégios para a chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




