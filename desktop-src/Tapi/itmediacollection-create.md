---
description: O método Create cria uma nova mídia com propriedades padrão, adiciona-a à coleção no índice especificado e retorna um ponteiro para a interface ITMedia.
ms.assetid: f0036556-d2e7-4589-8bb4-e2c5559902fe
title: 'Método ITMediaCollection:: Create (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8033fb2f541f5451f918845858df756b32361f54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761821"
---
# <a name="itmediacollectioncreate-method"></a>Método ITMediaCollection:: Create

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Create** cria uma nova mídia com propriedades padrão, adiciona-a à coleção no índice especificado e retorna um ponteiro para a interface [**ITMedia**](itmedia.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Create(
  [in]  LONG    Index,
  [out] ITMedia **ppMedia
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Índice* \[ do no\]
</dt> <dd>

Índice do novo item. O valor mínimo para o índice é 1 e o valor máximo para o índice é o número atual de itens + 1.

</dd> <dt>

*ppMedia* \[ fora\]
</dt> <dd>

Ponteiro para a interface [**ITMedia**](itmedia.md) criada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                         | Significado                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *ppMedia* não é um ponteiro válido.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro de *índice* não é válido.<br/>                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                  |



 

## <a name="remarks"></a>Comentários

A maioria das listas de C e C++ é baseada em 0, mas esse índice é baseado em 1 para Visual Basic compatibilidade, o que significa que o primeiro item tem um número de índice de 1.

A TAPI chama o método **AddRef** na interface [**ITMedia**](itmedia.md) retornada por **ITMediaCollection:: Create**. O aplicativo deve chamar **Release** na interface [**ITMedia**](itmedia.md) para liberar recursos associados a ela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




