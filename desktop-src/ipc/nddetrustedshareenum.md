---
description: Recupera os nomes de todos os compartilhamentos de DDE de rede que são confiáveis no contexto do processo de chamada.
ms.assetid: 8e2323a4-0c27-44e6-9598-08a3c1a88bd3
title: Função NDdeTrustedShareEnum (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeTrustedShareEnum
- NDdeTrustedShareEnumA
- NDdeTrustedShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: caa3f7c20b95243e03c0c6025d1ff32d60443ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297298"
---
# <a name="nddetrustedshareenum-function"></a>Função NDdeTrustedShareEnum

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]

Recupera os nomes de todos os compartilhamentos de DDE de rede que são confiáveis no contexto do processo de chamada.

## <a name="syntax"></a>Sintaxe


```C++
UINT NDdeTrustedShareEnum(
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

Um ponteiro para um buffer que recebe a lista de compartilhamentos DDE confiáveis. A lista de compartilhamentos DDE confiáveis é retornada como uma sequência de cadeias de caracteres separadas por nulo terminando com um caractere nulo duplo no final. Este parâmetro pode ser **NULL**. Se o *lpBuffer* for **nulo**, o DSDM retornará o tamanho do buffer necessário para manter a lista de compartilhamentos no campo *lpcbTotalAvailable* .

</dd> <dt>

*cBufSize* \[ no\]
</dt> <dd>

O tamanho do buffer *lpBuffer* , em bytes. Esse parâmetro deve ser zero se *lpBuffer* for **nulo**.

</dd> <dt>

*lpnEntriesRead* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número total de compartilhamentos confiáveis sendo enumerados. Este parâmetro não pode ser **nulo**.

</dd> <dt>

*lpcbTotalAvailable* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número total de bytes necessários para armazenar a lista de compartilhamentos DDE confiáveis. Este parâmetro não pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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
| Nomes Unicode e ANSI<br/>   | **NDdeTrustedShareEnumW** (Unicode) e **NDdeTrustedShareEnumA** (ANSI)<br/>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de troca dinâmica de dados de rede](network-dynamic-data-exchange.md)
</dt> <dt>

[Funções DDE de rede](network-dde-functions.md)
</dt> </dl>

 

 




