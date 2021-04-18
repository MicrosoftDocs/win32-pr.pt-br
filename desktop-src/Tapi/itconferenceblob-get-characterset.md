---
description: O \_ método Get CharacterSet Obtém um \_ \_ descritor de conjunto de caracteres de blob do conjunto de caracteres usado no blob de conferência atual.
ms.assetid: 9783d18c-79f6-4faa-b12d-9504c13d54e3
title: 'Método ITConferenceBlob:: get_CharacterSet (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681085672f49c75a8434c4b0311e75d2b9cea270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810138"
---
# <a name="itconferenceblobget_characterset-method"></a>Método ITConferenceBlob:: get \_ CharacterSet

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ CharacterSet** Obtém um descritor de [**\_ \_ conjunto de caracteres de blob**](blob-character-set.md) do conjunto de caracteres usado no blob de conferência atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_CharacterSet(
  [out] BLOB_CHARACTER_SET *pCharacterSet
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCharacterSet* \[ fora\]
</dt> <dd>

Ponteiro para um descritor de [**\_ \_ conjunto de caracteres de blob**](blob-character-set.md) do conjunto de caracteres.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                                   | Descrição                                                      |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | O método foi bem-sucedido.<br/>                                     |
| <dl> <dt>**\_ponteiro E**</dt> </dl>                     | O parâmetro *pCharacterSet* não é um ponteiro válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                 | Há memória insuficiente para executar a operação.<br/>  |
| <dl> <dt>**E \_ falha**</dt> </dl>                        | Erro não especificado.<br/>                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                     | Este método ainda não foi implementado.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                  | *pCharacterSet* é **nulo**.<br/>                          |
| <dl> <dt>**RESULTADO ERRO de \_ dados inválidos \_**</dt> </dl> | O conjunto de caracteres atual é inválido ou não está disponível.<br/>  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITConferenceBlob**](itconferenceblob.md)
</dt> <dt>

[**\_conjunto de caracteres de blob \_**](blob-character-set.md)
</dt> </dl>

 

 




