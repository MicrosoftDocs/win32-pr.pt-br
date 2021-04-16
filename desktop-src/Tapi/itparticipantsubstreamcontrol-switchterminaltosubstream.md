---
description: O método SwitchTerminalToSubStream define um terminal para o Subfluxo de participante.
ms.assetid: 39e1d4b9-2e39-4b36-9a6a-89e41cd59153
title: 'Método ITParticipantSubStreamControl:: SwitchTerminalToSubStream (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f10401b2cf1598c76537ebd3a7049d67bf0657
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759469"
---
# <a name="itparticipantsubstreamcontrolswitchterminaltosubstream-method"></a>Método ITParticipantSubStreamControl:: SwitchTerminalToSubStream

\[O **SwitchTerminalToSubStream** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **SwitchTerminalToSubStream** define um terminal para o Subfluxo de participante.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SwitchTerminalToSubStream(
  [in] ITTerminal  *pITTerminal,
  [in] ITSubStream *pITSubStream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pITTerminal* \[ no\]
</dt> <dd>

Ponteiro para a interface [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .

</dd> <dt>

*pITSubStream* \[ no\]
</dt> <dd>

Ponteiro para a interface [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                     | Descrição                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | O método foi bem-sucedido.<br/>                                                                       |
| <dl> <dt>**E \_ inesperado**</dt> </dl>    | Não foi possível acessar as informações do participante para o fluxo.<br/>                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>    | O parâmetro *pParticipant* ou *pITSubStream* não aponta para uma interface válida.<br/> |
| <dl> <dt>**TAPI \_ E \_ noitems**</dt> </dl> | O Subfluxo não está pronto.<br/>                                                             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>   | Há memória insuficiente para executar a operação.<br/>                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITParticipantSubStreamControl**](itparticipantsubstreamcontrol.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)
</dt> </dl>

 

