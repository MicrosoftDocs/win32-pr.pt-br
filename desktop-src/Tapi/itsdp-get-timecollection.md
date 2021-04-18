---
description: O \_ método Get timecollection Obtém um ponteiro para uma interface ITTimeCollection para a conferência.
ms.assetid: 1cfe3f5a-dcf7-480b-9b23-e17259d8ee9c
title: 'Método ITSdp:: get_TimeCollection (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1bac0f38f8c96762d4e36d8d3dfdff2136bdb86
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796323"
---
# <a name="itsdpget_timecollection-method"></a>Método ITSdp:: get \_ timecollection

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ timecollection** Obtém um ponteiro para uma interface [**ITTimeCollection**](ittimecollection.md) para a conferência.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_TimeCollection(
  [out] ITTimeCollection **ppTimeCollection
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppTimeCollection* \[ fora\]
</dt> <dd>

Ponteiro para [**ITTimeCollection**](ittimecollection.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                                                           | Significado                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                            | O método foi bem-sucedido.<br/>                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                    | O parâmetro *ppTimeCollection* não é um ponteiro válido.<br/>                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                                   | Há memória insuficiente para executar a operação.<br/>                             |
| <dl> <dt>**E \_ falha**</dt> </dl>                                          | Erro não especificado.<br/>                                                               |
| <dl> <dt>**HRESULT \_ do \_ código de erro \_ ( \_ dados inválidos do erro \_ )**</dt> </dl> | Ocorreu um erro interno, geralmente devido à falha de um método anterior.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                                       | Este método ainda não foi implementado.<br/>                                              |



 

## <a name="remarks"></a>Comentários

Um ponteiro [**ITTimeCollection**](ittimecollection.md) também pode ser obtido usando **QueryInterface**.

A TAPI chama o método **AddRef** na interface [**ITTimeCollection**](ittimecollection.md) retornada por **ITSdp:: get \_ timecollection**. O aplicativo deve chamar **Release** na interface **ITTimeCollection** para liberar recursos associados a ela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITTimeCollection**](ittimecollection.md)
</dt> </dl>

 

 




