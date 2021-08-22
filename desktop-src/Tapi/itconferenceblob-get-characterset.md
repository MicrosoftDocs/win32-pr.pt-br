---
description: O método \_ get CharacterSet obtém um descritor CHARACTER SET de BLOB do conjunto de \_ \_ caracteres usado no blob de conferência atual.
ms.assetid: 9783d18c-79f6-4faa-b12d-9504c13d54e3
title: Método ITConferenceBlob::get_CharacterSet (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20a9dd719d2ae9742a6ec4b3295e3e22ffe871b4a38c55d07e07a3421271553d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060994"
---
# <a name="itconferenceblobget_characterset-method"></a>Método ITConferenceBlob::get \_ CharacterSet

\[As interfaces e controles de conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método \_ get CharacterSet** obtém um descritor [**CHARACTER SET \_ \_ de BLOB**](blob-character-set.md) do conjunto de caracteres usado no blob de conferência atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_CharacterSet(
  [out] BLOB_CHARACTER_SET *pCharacterSet
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCharacterSet* \[ out\]
</dt> <dd>

Ponteiro para um [**descritor \_ CHARACTER SET \_ de BLOB**](blob-character-set.md) do conjunto de caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                                   | Descrição                                                      |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | O método foi bem-sucedido.<br/>                                     |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>                     | O *parâmetro pCharacterSet* não é um ponteiro válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                 | Há memória insuficiente para executar a operação.<br/>  |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                        | Erro não especificado.<br/>                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                     | Este método ainda não foi implementado.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                  | *pCharacterSet* é **NULL.**<br/>                          |
| <dl> <dt>**(HRESULT) ERRO \_ DADOS \_ INVÁLIDOS**</dt> </dl> | O conjunto de caracteres atual é inválido ou não está disponível.<br/>  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITConferenceBlob**](itconferenceblob.md)
</dt> <dt>

[**CONJUNTO DE \_ CARACTERES DE \_ BLOB**](blob-character-set.md)
</dt> </dl>

 

 




