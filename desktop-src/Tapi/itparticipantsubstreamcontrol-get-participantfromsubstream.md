---
description: O \_ método Get ParticipantFromSubStream permite que um aplicativo descubra quais participantes estão associados a um determinado substream.
ms.assetid: 0e42b4f0-d5b6-4b33-b7e5-dc525524ece7
title: 'Método ITParticipantSubStreamControl:: get_ParticipantFromSubStream (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a507665e7f81339ce10961d69e08e76f60bb2be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753543"
---
# <a name="itparticipantsubstreamcontrolget_participantfromsubstream-method"></a>Método ITParticipantSubStreamControl:: get \_ ParticipantFromSubStream

\[**obter \_ O ParticipantFromSubStream** não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ ParticipantFromSubStream** permite que um aplicativo descubra quais participantes estão associados a um determinado substream.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ParticipantFromSubStream(
  [in]  ITSubStream   *pITSubStream,
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pITSubStream* \[ no\]
</dt> <dd>

Ponteiro para a interface [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .

</dd> <dt>

*ppParticipant* \[ fora\]
</dt> <dd>

Ponteiro para matriz de ponteiros de interface [**ITParticipant**](itparticipant.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                     | Descrição                                                                        |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | O método foi bem-sucedido.<br/>                                                       |
| <dl> <dt>**\_ponteiro E**</dt> </dl>       | O parâmetro *pITSubStream* ou *ppParticipant* não é um ponteiro válido.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>    | O parâmetro *pITSubStream* não aponta para uma interface válida.<br/>         |
| <dl> <dt>**TAPI \_ E \_ noitems**</dt> </dl> | Não há participantes associados ao Subfluxo.<br/>                |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>   | Há memória insuficiente para executar a operação.<br/>                    |



 

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

 

