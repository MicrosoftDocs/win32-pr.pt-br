---
description: O \_ método Put status define o status de um participante.
ms.assetid: 8478fcf4-00b3-4b77-9859-e5a80ce24be1
title: 'ITParticipant: método de ut_Status de:p (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82eadc9832105ecb0cf440b070dbff8b3fe658d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760159"
---
# <a name="itparticipantput_status-method"></a>ITParticipant::p \_ método de status UT

\[**Put \_ O status** não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Put \_ status** define o status de um participante.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Status(
  [in] ITStream     *pITStream,
  [in] VARIANT_BOOL fEnable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pITStream* \[ no\]
</dt> <dd>

Ponteiro para a interface [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .

</dd> <dt>

*fEnable* \[ no\]
</dt> <dd>

VARIANT \_ true se o participante estiver habilitado no fluxo, Variant \_ false se for para ser desabilitado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                              |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Método não implementado.<br/>                                        |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *pITStream* não é um ponteiro válido.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *pITStream* não aponta para uma interface válida.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/>           |



 

## <a name="remarks"></a>Comentários

Habilitar ou desabilitar o status de um participante em um fluxo permite que um aplicativo simplifique o mudo de um determinado participante.

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

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[**obter \_ status**](itparticipant-get-status.md)
</dt> </dl>

 

