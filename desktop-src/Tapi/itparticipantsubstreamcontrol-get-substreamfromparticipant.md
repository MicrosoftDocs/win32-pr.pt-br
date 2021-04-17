---
description: O \_ método Get SubStreamFromParticipant permite que um aplicativo descubra quais subfluxos estão associados a um determinado participante.
ms.assetid: d45cdd1d-13cf-433a-9b19-193d5c0cba11
title: 'Método ITParticipantSubStreamControl:: get_SubStreamFromParticipant (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0eae68cd62c38348e1a576f114a9e93ac52f9cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766220"
---
# <a name="itparticipantsubstreamcontrolget_substreamfromparticipant-method"></a>Método ITParticipantSubStreamControl:: get \_ SubStreamFromParticipant

\[**obter \_ O SubStreamFromParticipant** não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ SubStreamFromParticipant** permite que um aplicativo descubra quais subfluxos estão associados a um determinado participante.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_SubStreamFromParticipant(
  [in]  ITParticipant *pParticipant,
  [out] ITSubStream   **ppITSubStream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pParticipant* \[ no\]
</dt> <dd>

Ponteiro para a interface [**ITParticipant**](itparticipant.md) .

</dd> <dt>

*ppITSubStream* \[ fora\]
</dt> <dd>

Ponteiro para matriz de ponteiros de interface [**ITParticipant**](itparticipant.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                                  |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                                 |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *ppITSubStream* não é um ponteiro válido.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *pParticipant* não aponta para uma interface válida.<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl>  | Não foi possível acessar as informações do participante do fluxo.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/>              |



 

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
</dt> </dl>

 

