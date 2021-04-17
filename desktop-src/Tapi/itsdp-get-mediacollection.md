---
description: O \_ método Get mediacollection Obtém um ponteiro para a interface ITMediaCollection da conferência.
ms.assetid: 8109582a-74f0-47e8-91d1-0d89c3d3c331
title: 'Método ITSdp:: get_MediaCollection (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f8812debf8c04fe022f24061660d6ea3bb5f162
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780598"
---
# <a name="itsdpget_mediacollection-method"></a>Método ITSdp:: obter \_ mediacollection

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ mediacollection** Obtém um ponteiro para a interface [**ITMediaCollection**](itmediacollection.md) da conferência.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_MediaCollection(
  [out] ITMediaCollection **ppMediaCollection
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppMediaCollection* \[ fora\]
</dt> <dd>

Ponteiro para [**ITMediaCollection**](itmediacollection.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                                                           | Significado                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                            | O método foi bem-sucedido.<br/>                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                    | O parâmetro *ppMediaCollection* não é um ponteiro válido.<br/>                        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                                   | Há memória insuficiente para executar a operação.<br/>                             |
| <dl> <dt>**E \_ falha**</dt> </dl>                                          | Erro não especificado.<br/>                                                               |
| <dl> <dt>**HRESULT \_ do \_ código de erro \_ ( \_ dados inválidos do erro \_ )**</dt> </dl> | Ocorreu um erro interno, geralmente devido à falha de um método anterior.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                                       | Este método ainda não foi implementado.<br/>                                              |



 

## <a name="remarks"></a>Comentários

Um ponteiro [**ITMediaCollection**](itmediacollection.md) também pode ser obtido usando **QueryInterface**.

A TAPI chama o método **AddRef** na interface [**ITMediaCollection**](itmediacollection.md) retornada por **ITSdp:: get \_ mediacollection**. O aplicativo deve chamar **Release** na interface **ITMediaCollection** para liberar recursos associados a ela.

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

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




