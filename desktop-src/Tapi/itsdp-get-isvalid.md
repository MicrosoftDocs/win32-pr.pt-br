---
description: O método get IsValid valida o \_ blob SDP (Protocolo de Descritor de Sessão; consulte RFC 2327) para obter valores de estrutura e campo.
ms.assetid: a3f849ac-bda9-4937-bf3b-bce8df20cbf0
title: Método ITSdp::get_IsValid (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1674b51c605354a021948a63a0e993578a3d0114e625acec2cb9e24238423c56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140289"
---
# <a name="itsdpget_isvalid-method"></a>Método ITSdp::get \_ IsValid

\[As interfaces e controles de Conferência de Telefonia IP de reunião não estão disponíveis para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método \_ get IsValid** valida o blob SDP (Protocolo de Descritor de Sessão; consulte RFC 2327) para obter valores de estrutura e campo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_IsValid(
  [out] VARIANT_BOOL *pfIsValid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pfIsValid* \[ out\]
</dt> <dd>

Indica se a estrutura de blob é válida.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O *parâmetro pfIsValid* não é válido.<br/>              |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | O *parâmetro pfIsValid* não é um ponteiro válido.<br/>    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Erro não especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




