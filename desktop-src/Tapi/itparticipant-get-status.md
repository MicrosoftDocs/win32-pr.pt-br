---
description: O \_ método Get status retorna uma variante \_ booliana que indica o status do participante.
ms.assetid: 03ad763b-5223-41b5-b0cf-1f13c761f5c2
title: 'Método ITParticipant:: get_Status (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de39ac0833f856e35cc120b4f4e5b00bcd617de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754189"
---
# <a name="itparticipantget_status-method"></a>Método de status ITParticipant:: get \_

\[**obter \_ O status** não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ status** retorna uma variante \_ booliana que indica o status do participante.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Status(
  [in]  ITStream     *pITStream,
  [out] VARIANT_BOOL *pStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pITStream* \[ no\]
</dt> <dd>

Ponteiro para a interface [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .

</dd> <dt>

*pStatus* \[ fora\]
</dt> <dd>

VARIANT \_ true se o participante estiver habilitado no fluxo, Variant \_ false se ele estiver desabilitado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                              |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Método não implementado.<br/>                                        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/>           |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *pITStream* não é um ponteiro válido.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *pITStream* não aponta para uma interface válida.<br/> |



 

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

[**Status de Put \_**](itparticipant-put-status.md)
</dt> </dl>

 

