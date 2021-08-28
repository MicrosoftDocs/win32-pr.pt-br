---
description: O \_ método Get EnumerationIf Obtém um ponteiro para uma interface de enumeração de mídia.
ms.assetid: d5f1e10f-e5ad-45e6-a5ec-024905603012
title: 'Método ITMediaCollection:: get_EnumerationIf (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe14475e216b5143b599aab50d12d1d0c548b5f64dd8e44edd2e6aab249905c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060854"
---
# <a name="itmediacollectionget_enumerationif-method"></a>Método ITMediaCollection:: get \_ EnumerationIf

\[os controles e as interfaces de conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ EnumerationIf** Obtém um ponteiro para uma interface de enumeração de mídia.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_EnumerationIf(
  [out] IEnumMedia **pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PVal* \[ fora\]
</dt> <dd>

Ponteiro para a interface [**IEnumMedia**](ienummedia.md) para o item desejado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor                                                                                         | Significado                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *PVal* não é um ponteiro válido.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                  |



 

## <a name="remarks"></a>Comentários

Esse método é intercambiável com [**Get \_ \_ NewEnum**](itmediacollection-get--newenum.md) , exceto pelo fato de que ele retorna [**IEnumMedia**](ienummedia.md) em vez de **IUnknown**.

A TAPI chama o método **AddRef** na interface [**IEnumMedia**](ienummedia.md) retornada por **ITMediaCollection:: get \_ Enumerationlf**. O aplicativo deve chamar **Release** na interface **IEnumMedia** para liberar recursos associados a ela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




