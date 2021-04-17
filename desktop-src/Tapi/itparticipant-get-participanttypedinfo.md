---
description: O \_ método Get ParticipantTypedInfo Obtém uma representação BSTR do tipo de informações necessárias, como PTI \_ EmailAddress.
ms.assetid: 8dcc6182-ad3c-47f2-b4a0-e18a3c9f6888
title: 'Método ITParticipant:: get_ParticipantTypedInfo (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9936f49e6daa05702699487e4313a918c545a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766223"
---
# <a name="itparticipantget_participanttypedinfo-method"></a>Método ITParticipant:: get \_ ParticipantTypedInfo

\[**obter \_ O ParticipantTypedInfo** não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ ParticipantTypedInfo** Obtém uma representação **BSTR** do tipo de informações necessárias, como PTI \_ EmailAddress.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*InfoType* \[ no\]
</dt> <dd>

[**Participante \_ do Descritor de \_ informações digitados**](participant-typed-info.md) do tipo de informação necessário.

</dd> <dt>

*ppInfo* \[ fora\]
</dt> <dd>

Ponteiro para representação **BSTR** das informações necessárias.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                    | Descrição                                                     |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ falha**</dt> </dl>         | O armazenamento de informações em *ppInfo* falhou.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | O parâmetro *InfoType* não é válido.<br/>               |
| <dl> <dt>**\_ponteiro E**</dt> </dl>      | O parâmetro *ppInfo* não é um ponteiro válido.<br/>       |
| <dl> <dt>**TAPI \_ E \_ noitem**</dt> </dl> | A TAPI não tem informações sobre o tipo especificado.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Há memória insuficiente para executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o parâmetro *ppInfo* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                |
| parâmetro<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**\_informações de tipo de participante \_**](participant-typed-info.md)
</dt> <dt>

[**tipos de mídia**](tapimediatype--constants.md)
</dt> </dl>

 

