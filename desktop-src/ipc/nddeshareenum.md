---
description: Recupera a lista de compartilhamentos DDE disponíveis.
ms.assetid: ce5aeddd-d9d1-40a2-a807-1a9c9f98f171
title: Função NDdeShareEnum (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareEnum
- NDdeShareEnumA
- NDdeShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: e6b101a7ba45e28175a8d6ee0730e704a6f519142f94e4fc2273d1d76dcfe1cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014736"
---
# <a name="nddeshareenum-function"></a>Função NDdeShareEnum

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]

Recupera a lista de compartilhamentos DDE disponíveis.

## <a name="syntax"></a>Sintaxe


```C++
UINT NDdeShareEnum(
  _In_  LPTSTR  lpszServer,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnEntriesRead,
  _Out_ LPDWORD lpcbTotalAvailable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszServer* \[ no\]
</dt> <dd>

O nome do servidor no qual o DSDM reside.

</dd> <dt>

*nLevel* \[ no\]
</dt> <dd>

Reservado. Esse parâmetro deve ser zero.

</dd> <dt>

*lpBuffer* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe a lista de compartilhamentos de DDE. A lista de compartilhamentos DDE é armazenada como uma sequência de cadeias de caracteres separadas por nulo terminando com um caractere nulo duplo no final. Este parâmetro pode ser **NULL**. Se *lpBuffer* for **NULL**, o DSDM retornará o tamanho do buffer necessário para manter a lista de compartilhamentos no parâmetro *lpcbTotalAvailable* .

</dd> <dt>

*cBufSize* \[ no\]
</dt> <dd>

O tamanho do buffer *lpBuffer* , em bytes. Esse parâmetro deve ser zero se *lpBuffer* for **nulo**.

</dd> <dt>

*lpnEntriesRead* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número total de compartilhamentos sendo enumerados. Este parâmetro não pode ser **nulo**.

</dd> <dt>

*lpcbTotalAvailable* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número total de bytes necessários no buffer para armazenar a lista de compartilhamentos de DDE. Este parâmetro não pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, o valor de retorno será NDDE \_ nenhum \_ erro.

Se a função falhar, o valor de retorno será um código de erro, que pode ser convertido em uma mensagem de erro de texto chamando [**NDdeGetErrorString**](nddegeterrorstring.md). Se o parâmetro *lpBuffer* for **NULL**, ele retornará NDDE \_ buf \_ muito \_ pequeno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **NDdeShareEnumW** (Unicode) e **NDdeShareEnumA** (ANSI)<br/>                  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[visão geral de troca dinâmica de dados de rede](network-dynamic-data-exchange.md)
</dt> <dt>

[Funções DDE de rede](network-dde-functions.md)
</dt> </dl>

 

 




