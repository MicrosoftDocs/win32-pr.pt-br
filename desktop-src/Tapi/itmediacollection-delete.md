---
description: O método Delete exclui a mídia correspondente ao índice especificado.
ms.assetid: 5fcbd026-75a8-4db2-a701-e080dc222537
title: 'ITMediaCollection: método de:D xcluir (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ffabee84bd7d04f517ef26ad5259f642cfed48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754738"
---
# <a name="itmediacollectiondelete-method"></a>ITMediaCollection: método de:D xcluir

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **delete** exclui a mídia correspondente ao índice especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Índice* \[ do no\]
</dt> <dd>

Índice da mídia a ser excluída.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                                                              | Descrição                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                                     | O método foi bem-sucedido.<br/>                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                             | O parâmetro de *índice* tem um valor menor que 1 ou maior que o número atual de elementos.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                                            | Há memória insuficiente para executar a operação.<br/>                                          |
| <dl> <dt>**E \_ falha**</dt> </dl>                                                   | Erro interno (deve ocorrer apenas se uma chamada anterior retornou um erro).<br/>                      |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                                                | Este método ainda não foi implementado.<br/>                                                           |
| <dl> <dt>**HRESULT \_ do \_ código de erro \_ (SDPBLB \_ conf \_ blob \_ destruído)**</dt> </dl> | O blob SDP não existe.<br/>                                                                   |



 

## <a name="remarks"></a>Comentários

A maioria das listas de C e C++ é baseada em 0, mas esse índice é baseado em 1 para Visual Basic compatibilidade, o que significa que o primeiro item tem um número de índice de 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




