---
description: O próximo método obtém o próximo número especificado de elementos na sequência de enumeração. Esse método é ocultado das linguagens de Visual Basic e script.
ms.assetid: bd94f592-ac6f-48b7-8190-352a5e18f224
title: 'Método IEnumParticipant:: Next (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89586370d01aaac54f05242e0eb3c53eb938c47b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779312"
---
# <a name="ienumparticipantnext-method"></a>Método IEnumParticipant:: Next

\[A **seguir** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O **próximo** método obtém o próximo número especificado de elementos na sequência de enumeração. Esse método é ocultado das linguagens de Visual Basic e script.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Next(
  [in]  ULONG         celt,
  [out] ITParticipant **ppElements,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*celt* \[ no\]
</dt> <dd>

Número de elementos solicitados.

</dd> <dt>

*ppElements* \[ fora\]
</dt> <dd>

Ponteiro para interfaces [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) .

</dd> <dt>

*pceltFetched* \[ fora\]
</dt> <dd>

Ponteiro para o número de elementos realmente fornecidos. Poderá ser **NULL** se *celt* for um.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método retornou *celt* número de elementos.<br/>           |
| <dl> <dt>**\_falso**</dt> </dl>       | O número de elementos restantes era menor que *celt*.<br/>   |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *ppElements* não é um ponteiro válido.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

A TAPI chama o método [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) na interface [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) retornada por **IEnumParticipant:: Next**. O aplicativo deve chamar [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) na interface **ITAgentHandler** para liberar recursos associados a ela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

