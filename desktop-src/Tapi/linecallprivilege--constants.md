---
description: As constantes de sinalizador de bits LINECALLPRIVILEGE descrevem os tipos de direitos de acesso ou privilégios que um aplicativo com um handle de chamada pode ter para \_ a chamada correspondente.
ms.assetid: a58b7e9e-696e-4421-9b31-1ba8afe6e03b
title: LINECALLPRIVILEGE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c00dd43442345c545bb5e0b1718131b6815fd236f9c7d770c0f3b47b10b47a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660046"
---
# <a name="linecallprivilege_-constants"></a>Constantes LINECALLPRIVILEGE \_

As constantes de sinalizador de bits **LINECALLPRIVILEGE \_** descrevem os tipos de direitos de acesso ou privilégios que um aplicativo com um handle de chamada pode ter para a chamada correspondente.

<dl> <dt>

<span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**LINECALLPRIVILEGE \_ MONITOR**
</dt> <dd> <dl> <dt>



O aplicativo tem privilégios de monitor para a chamada. Esses privilégios permitem que o aplicativo monitore alterações de estado e consulte informações e status sobre a chamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**LINECALLPRIVILEGE \_ NONE**
</dt> <dd> <dl> <dt>



O aplicativo não tem privilégios para a chamada. O handle do aplicativo é nulo e não deve ser usado.


</dt> </dl> </dd> <dt>

<span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**PROPRIETÁRIO DE LINECALLPRIVILEGE \_**
</dt> <dd> <dl> <dt>



O aplicativo tem privilégios de proprietário para a chamada. Esses privilégios permitem que o aplicativo manipule a chamada de maneiras que afetam o estado da chamada.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Nenhuma extensibilidade. Todos os 32 bits são reservados.

Quando um alça de chamada é fornecido pela primeira vez a um aplicativo ou sempre que os privilégios de chamada desse aplicativo são modificados, a mensagem [**LINE \_ CALLSTATE**](line-callstate.md) é enviada ao aplicativo. Quando um aplicativo entrega uma chamada e se o aplicativo receptor ainda não tiver um alçamento com privilégios de proprietário, essa mensagem informará o aplicativo sobre seus novos privilégios para a chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




