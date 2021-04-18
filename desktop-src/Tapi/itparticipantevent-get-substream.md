---
description: O \_ Subfluxo Get Obtém um ponteiro para uma matriz de interfaces ITSubStream que representam os subfluxos envolvidos no evento.
ms.assetid: 0af9097a-2481-4543-bb3d-35ccd352e992
title: 'Método ITParticipantEvent:: get_SubStream (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8c2944004af31adfb7256376992506eef59b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782910"
---
# <a name="itparticipanteventget_substream-method"></a>Método ITParticipantEvent:: Get de \_ substream

\[**obter \_ O substream** não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O **\_ Subfluxo Get** Obtém um ponteiro para uma matriz de interfaces [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) que representam os subfluxos envolvidos no evento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_SubStream(
  [out] ITSubStream **ppSubStream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppSubStream* \[ fora\]
</dt> <dd>

Ponteiro para matriz de ponteiros [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                           | Significado                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**TAPI \_ E \_ noitems**</dt> </dl> | Não há subfluxos associados ao evento.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>   | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**\_ponteiro E**</dt> </dl>       | O parâmetro *ppSubStream* não é um ponteiro válido.<br/>  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITParticipantEvent**](itparticipantevent.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

