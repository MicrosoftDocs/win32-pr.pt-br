---
description: O método getemailnames Obtém uma matriz de nomes de email associados ao blob de conferência.
ms.assetid: e51f25d7-41e5-408e-930b-396c7ac24437
title: 'Método ITSdp:: getemailnames (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f74ea369210a6ca32e47bb3359000195c544374b7352da96570f6d0f58f2af4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140259"
---
# <a name="itsdpgetemailnames-method"></a>Método ITSdp:: getemailnames

\[os controles e as interfaces de conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Getemailnames** Obtém uma matriz de nomes de email associados ao blob de conferência.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetEmailNames(
  [out] VARIANT *pAddresses,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAddresses* \[ fora\]
</dt> <dd>

Ponteiro de **variante** para um SafeArray de **BSTR** s listando endereços de email.

</dd> <dt>

*pNames* \[ fora\]
</dt> <dd>

Ponteiro de **variante** para um SafeArray de nomes de listagem **BSTR** s.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                              |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *pAddresses* ou *pNames* não é um ponteiro válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/>           |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                             |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                            |



 

## <a name="remarks"></a>Comentários

As listas das quais *pAddresses* e *pNames* apontam têm o mesmo comprimento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




