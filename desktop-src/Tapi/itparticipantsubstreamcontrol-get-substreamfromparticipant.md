---
description: O método get SubStreamFromParticipant permite que um aplicativo descubra \_ quais substreams estão associados a um determinado participante.
ms.assetid: d45cdd1d-13cf-433a-9b19-193d5c0cba11
title: Método ITParticipantSubStreamControl::get_SubStreamFromParticipant (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae40487bbef7e678722a2710d99bce9ed1ebe2f5192705f0a7dc03f86e10e421
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621526"
---
# <a name="itparticipantsubstreamcontrolget_substreamfromparticipant-method"></a>Método ITParticipantSubStreamControl::get \_ SubStreamFromParticipant

\[**get \_ SubStreamFromParticipant** não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método \_ get SubStreamFromParticipant** permite que um aplicativo descubra quais substreams estão associados a um determinado participante.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_SubStreamFromParticipant(
  [in]  ITParticipant *pParticipant,
  [out] ITSubStream   **ppITSubStream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pParticipant* \[ Em\]
</dt> <dd>

Ponteiro para a interface [**ITParticipant.**](itparticipant.md)

</dd> <dt>

*ppITSubStream* \[ out\]
</dt> <dd>

Ponteiro para a matriz de ponteiros de interface [**ITParticipant.**](itparticipant.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                                  |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                                 |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | O *parâmetro ppITSubStream* não é um ponteiro válido.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O *parâmetro pParticipant* não aponta para uma interface válida.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>  | Não foi possível acessar as informações de participante do fluxo.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/>              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITParticipantSubStreamControl**](itparticipantsubstreamcontrol.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

