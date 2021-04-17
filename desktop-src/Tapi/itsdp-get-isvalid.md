---
description: O \_ método Get IsValid valida o protocolo SDP (Session Descriptor Protocol), consulte o blob RFC 2327) para a estrutura e os valores de campo.
ms.assetid: a3f849ac-bda9-4937-bf3b-bce8df20cbf0
title: 'Método ITSdp:: get_IsValid (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88ca3cfdc1061e0a2830010ec39b2e6667c9341c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756994"
---
# <a name="itsdpget_isvalid-method"></a>Método IsValid de ITSdp:: get \_

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ IsValid** valida o protocolo SDP (Session Descriptor Protocol), consulte o blob RFC 2327) para a estrutura e os valores de campo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_IsValid(
  [out] VARIANT_BOOL *pfIsValid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pfIsValid* \[ fora\]
</dt> <dd>

Indica se a estrutura do blob é válida.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *pfIsValid* não é válido.<br/>              |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *pfIsValid* não é um ponteiro válido.<br/>    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




