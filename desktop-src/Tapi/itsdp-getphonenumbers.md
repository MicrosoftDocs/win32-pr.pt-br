---
description: O método GetPhoneNumbers Obtém uma matriz de números de telefone associados a um blob de conferência.
ms.assetid: c4ad6c5a-e15c-45ae-94de-763a843554bb
title: 'Método ITSdp:: GetPhoneNumbers (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 465bc6b2d2167ca17d25b8f50466f111724ea3b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783365"
---
# <a name="itsdpgetphonenumbers-method"></a>Método ITSdp:: GetPhoneNumbers

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **GetPhoneNumbers** Obtém uma matriz de números de telefone associados a um blob de conferência.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPhoneNumbers(
  [out] VARIANT *pNumbers,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNumbers* \[ fora\]
</dt> <dd>

Ponteiro de **variante** para um SafeArray dos números de telefone de listagem de **BSTRs**.

</dd> <dt>

*pNames* \[ fora\]
</dt> <dd>

Ponteiro de **variante** para um SafeArray de nomes de listagem **BSTR** s.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                             |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                            |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *pNumbers* ou *pNames* não é um ponteiro válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/>         |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                           |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                          |



 

## <a name="remarks"></a>Comentários

As listas das quais *pNumbers* e *pNames* apontam têm o mesmo comprimento.

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

 

 




