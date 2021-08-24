---
description: O \_ método Get NetworkType Obtém o tipo de rede.
ms.assetid: 5597284a-9cc6-422b-a064-cda25aa5964b
title: 'Método ITConnection:: get_NetworkType (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d323d7465563d0a0d400c930585c2c0df002cedfae252d205d53aea8040f337
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660326"
---
# <a name="itconnectionget_networktype-method"></a>Método ITConnection:: get \_ NetworkType

\[os controles e as interfaces de conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ NetworkType** Obtém o tipo de rede.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_NetworkType(
  [out] BSTR *ppNetworkType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppNetworkType* \[ fora\]
</dt> <dd>

Ponteiro para um **BSTR** que contém o tipo de rede.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                     |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *ppNetworkType* não é um ponteiro válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/>  |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                   |



 

## <a name="remarks"></a>Comentários

O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o parâmetro *ppNetworkType* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> <dt>

[**ITConnection::p UT \_ NetworkType**](itconnection-put-networktype.md)
</dt> </dl>

 

