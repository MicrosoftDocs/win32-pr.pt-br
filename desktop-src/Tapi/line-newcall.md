---
description: A mensagem de NewCall da linha TSPI \_ é enviada para a função de retorno de chamada LINEEVENT sempre que uma nova chamada que a TAPI não originou chega em uma linha aberta pela TAPI.
ms.assetid: 36122dfb-1ed6-459d-aa2b-69c86daaddd8
title: Mensagem de LINE_NEWCALL (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed3e7380b2f328283e5f5cad9e84f5a1d0c450dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796319"
---
# <a name="line_newcall-message"></a>Mensagem de NewCall de linha \_

A mensagem **de \_ NewCall da linha** TSPI é enviada para a função de retorno de chamada [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) sempre que uma nova chamada que a TAPI não originou chega em uma linha aberta pela TAPI. Essa deve ser a primeira mensagem enviada referente a essa chamada. A TAPI grava o identificador opaco *htCall* no local passado pelo provedor de serviços como *dwParam2*. Isso fornece ao provedor de serviços o valor de *htCall* a ser usado nas mensagens subsequentes.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*htLine* 
</dt> <dd>

O identificador de objeto TAPI opaco para o dispositivo de linha.

</dd> <dt>

*htCall* 
</dt> <dd>

Não utilizado.

</dd> <dt>

*dwMsg* 
</dt> <dd>

A linha de valor \_ NewCall.

</dd> <dt>

*dwParam1* 
</dt> <dd>

O identificador opaco do provedor de serviço para a chamada, do tipo [**HDRVCALL**](hdrvline.md). A TAPI passa esse valor como o parâmetro *hdCall* para identificar a chamada nos procedimentos subsequentes que ele invoca para operar na chamada.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Um ponteiro do tipo LPHTAPICALL apontando para um [**HTAPICALL**](htapicall.md). A TAPI grava o identificador opaco TAPI para a chamada para o local indicado. O provedor de serviços deve salvar esse valor e passá-lo como o parâmetro *htCall* para identificar a chamada em eventos subsequentes que ele relata para a chamada.

Esse parâmetro também pode adquirir um valor de **NULL** (consulte a seção de comentários a seguir).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O provedor de serviços deve enviar a mensagem [**\_ callstate de linha**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) como a próxima mensagem para essa chamada. O evento **line \_ NewCall** é incomum, pois ele também passa um valor de volta para o provedor de serviços.

Essa função relata quaisquer novas chamadas originadas no provedor de serviços (entrada, saída, iniciadas no telefone e assim por diante) para as quais a TAPI e o provedor de serviços ainda não alteraram os identificadores opacos. Os identificadores são trocados para que a TAPI e o provedor de serviços possam, subsequentemente, fazer solicitações e relatar eventos que envolvam a chamada. Como essas novas chamadas não são necessariamente de entrada, as chamadas podem inicialmente estar em qualquer Estado, não necessariamente no estado de *oferta* . Se o provedor de serviços for iniciado e descobre que uma ou mais chamadas já estão ativas na linha, ela informará a TAPI delas com mensagens de **\_ NewCall de linha** seguidas por mensagens [**\_ callstate de linha**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) que indicam o estado atual. Uma nova chamada de saída, iniciada no telefone pelo usuário, seria relatada com uma **mensagem \_ NewCall de linha** e a mensagem **\_ callstate de linha** inicial indicaria que a chamada estava no estado de **sinal** de discagem (e continuando a partir daí).

Se o provedor de serviços passar um grande número de chamadas para a TAPI em um período muito curto (durante o mesmo ciclo de interrupção), a TAPI poderá ficar registrada no processamento dessas chamadas. Quando isso acontece, a TAPI sinaliza ao provedor de serviços para aguardar um pouco de tempo antes de enviar mais chamadas. Ele sinaliza isso escrevendo um valor de **NULL**, em vez de um [**HTAPICALL**](htapicall.md)válido, no local apontado pelo parâmetro *dwParam2* da **linha \_ NewCall**. Isso indica que a tentativa de processar o identificador de chamada recém oferecido não foi bem-sucedida, provavelmente devido a uma incapacidade temporária de alocar memória. O provedor de serviços pode responder descartando a chamada ou reenviando a mensagem **\_ NewCall de linha** após um atraso de agendamento (durante o qual o provedor de serviços deve produzir o processador para permitir que a TAPI processe outras ações pendentes). Em qualquer caso, nenhuma mensagem adicional sobre a nova chamada pode ser passada para a TAPI até que a troca de identificador seja realizada com êxito. Quando o local apontado por *dwParam2* adquire um valor não **nulo** , o provedor de serviços sabe que esse valor é um identificador [**HTAPICALL**](htapicall.md) válido para a chamada.

Não há nenhuma mensagem diretamente correspondente no nível de TAPI. Essa mensagem é usada no nível de TSPI para introduzir de forma exclusiva e não ambígua uma nova chamada de entrada para a TAPI e recuperar o identificador opaco da TAPI para a chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**chamada de LINHAstate \_**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))
</dt> <dt>

[**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> </dl>

 

