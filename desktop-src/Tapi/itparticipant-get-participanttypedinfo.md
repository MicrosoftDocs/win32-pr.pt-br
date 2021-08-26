---
description: O método \_ get ParticipantTypedInfo obtém uma representação BSTR do tipo de informação necessária, como PTI \_ EMAILADDRESS.
ms.assetid: 8dcc6182-ad3c-47f2-b4a0-e18a3c9f6888
title: Método ITParticipant::get_ParticipantTypedInfo (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43afb80b0f1161cf0060c8492576ade4f682af44cb4b2dbb13ab49d2c65aab66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867146"
---
# <a name="itparticipantget_participanttypedinfo-method"></a>Método ITParticipant::get \_ ParticipantTypedInfo

\[**get \_ ParticipantTypedInfo** não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método \_ get ParticipantTypedInfo** obtém uma representação **BSTR** do tipo de informação necessária, como PTI \_ EMAILADDRESS.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*InfoType* \[ Em\]
</dt> <dd>

[**PARTICIPANTE \_ Descritor \_ TYPED INFO**](participant-typed-info.md) do tipo de informação necessária.

</dd> <dt>

*ppInfo* \[ out\]
</dt> <dd>

Ponteiro para **a representação BSTR** das informações necessárias.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                    | Descrição                                                     |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ FAIL**</dt> </dl>         | Armazenamento informações em *ppInfo* falharam.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | O *parâmetro InfoType* não é válido.<br/>               |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>      | O *parâmetro ppInfo* não é um ponteiro válido.<br/>       |
| <dl> <dt>**TAPI \_ E \_ NOITEM**</dt> </dl> | TAPI não tem informações sobre o tipo especificado.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Há memória insuficiente para executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o *parâmetro ppInfo.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                |
| Cabeçalho<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**INFORMAÇÕES \_ DIGITADOS DO \_ PARTICIPANTE**](participant-typed-info.md)
</dt> <dt>

[**tipos de mídia**](tapimediatype--constants.md)
</dt> </dl>

 

