---
description: TSPIMessage é um tipo de enumeração que define o conjunto de funções LINEEVENT e PHONEEVENT adicionais que aparecem em TSPI que não aparecem na TAPI.
ms.assetid: b3c4ce68-033f-42f1-8c37-66326d21bf32
title: TSPIMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f74b412d131fc40a13f9da13dc86ba4f31a3becf6bb747e95131bc3bb0e2bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739156"
---
# <a name="tspimessage"></a>TSPIMessage

**TSPIMessage** é um tipo de enumeração que define o conjunto de funções [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) e [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) adicionais que aparecem em TSPI que não aparecem na TAPI.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>\_base da mensagem TSPI \_
</dt> <dd>

O número mais baixo no intervalo de valores de mensagem específicos de TSPI. Esse valor não tem nenhum significado, mas serve como base para definir os outros valores.

</dd> <dt>

<span id="LINE_NEWCALL"></span><span id="line_newcall"></span>NewCall de linha \_
</dt> <dd>

Especifica que uma chamada nova recebida chegou e a apresenta à TAPI. Essa deve ser a primeira mensagem enviada à TAPI para uma nova chamada de entrada. A TAPI retorna seu identificador opaco para a chamada como parte de seu tratamento dessa mensagem.

</dd> <dt>

<span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>CALLDEVSPECIFIC de linha \_
</dt> <dd>

Especifica que um evento específico do dispositivo ocorreu em um dispositivo de chamada.

</dd> <dt>

<span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>CALLDEVSPECIFICFEATURE de linha \_
</dt> <dd>

Especifica que um evento de recurso específico do dispositivo ocorreu em um dispositivo de chamada.

</dd> </dl>

 

 
