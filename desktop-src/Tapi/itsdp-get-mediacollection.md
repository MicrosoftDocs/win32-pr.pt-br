---
description: O método \_ get MediaCollection obtém um ponteiro para a interface ITMediaCollection da conferência.
ms.assetid: 8109582a-74f0-47e8-91d1-0d89c3d3c331
title: Método ITSdp::get_MediaCollection (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cf358089a394775c753adc0642897021e91df5bfcd5f23418e638df82db03a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774506"
---
# <a name="itsdpget_mediacollection-method"></a>Método ITSdp::get \_ MediaCollection

\[As interfaces e controles de Conferência de Telefonia IP de reunião não estão disponíveis para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método \_ get MediaCollection** obtém um ponteiro para a interface [**ITMediaCollection**](itmediacollection.md) da conferência.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_MediaCollection(
  [out] ITMediaCollection **ppMediaCollection
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppMediaCollection* \[ out\]
</dt> <dd>

Ponteiro para [**ITMediaCollection.**](itmediacollection.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor                                                                                                                           | Significado                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                            | O método foi bem-sucedido.<br/>                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                    | O *parâmetro ppMediaCollection* não é um ponteiro válido.<br/>                        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                                   | Há memória insuficiente para executar a operação.<br/>                             |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                                          | Erro não especificado.<br/>                                                               |
| <dl> <dt>**HRESULT \_ FROM ERROR CODE \_ \_ (ERROR INVALID \_ \_ DATA)**</dt> </dl> | Ocorreu um erro interno, geralmente devido à falha de um método anterior.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                                       | Este método ainda não foi implementado.<br/>                                              |



 

## <a name="remarks"></a>Comentários

Um [**ponteiro ITMediaCollection**](itmediacollection.md) também pode ser obtido usando **QueryInterface**.

TAPI chama o **método AddRef** na interface [**ITMediaCollection**](itmediacollection.md) retornada por **ITSdp::get \_ MediaCollection**. O aplicativo deve chamar **Release** na interface **ITMediaCollection** para liberar recursos associados a ele.

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
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




