---
description: O método get \_ Status retorna um BOOL VARIANT que indica \_ o status do participante.
ms.assetid: 03ad763b-5223-41b5-b0cf-1f13c761f5c2
title: Método ITParticipant::get_Status (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1585c9605447e7b515885ecf9e30d060afb7a57d14c5b29a66025f2df9da05a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060844"
---
# <a name="itparticipantget_status-method"></a>Método de Status ITParticipant::get \_

\[**get \_ O status** não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método get \_ Status** retorna um BOOL VARIANT \_ que indica o status do participante.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Status(
  [in]  ITStream     *pITStream,
  [out] VARIANT_BOOL *pStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pITStream* \[ Em\]
</dt> <dd>

Ponteiro para a interface [**ITStream.**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)

</dd> <dt>

*pStatus* \[ out\]
</dt> <dd>

VARIANT \_ TRUE se o participante estiver habilitado no fluxo, VARIANT FALSE se ele estiver \_ desabilitado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                              |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Método não implementado.<br/>                                        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/>           |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | O *parâmetro pITStream* não é um ponteiro válido.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O *parâmetro pITStream* não aponta para uma interface válida.<br/> |



 

## <a name="remarks"></a>Comentários

Habilenciar ou desabilitar o status de um participante em um fluxo permite que um aplicativo basicamente mute um determinado participante.

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

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[**put \_ Status**](itparticipant-put-status.md)
</dt> </dl>

 

