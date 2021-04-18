---
description: Recupera informações de compartilhamento de DDE. Isso geralmente é feito para edição.
ms.assetid: a2e48a4d-2b72-40a3-b827-474da1db0910
title: Função NDdeShareGetInfo (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareGetInfo
- NDdeShareGetInfoA
- NDdeShareGetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 72dc9ae12b174555debfa21afac15e5bfbed993e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760421"
---
# <a name="nddesharegetinfo-function"></a>Função NDdeShareGetInfo

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]

Recupera informações de compartilhamento de DDE. Isso geralmente é feito para edição.

## <a name="syntax"></a>Sintaxe


```C++
UINT NDdeShareGetInfo(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnTotalAvailable,
  _In_  LPWORD  lpnItems
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszServer* \[ no\]
</dt> <dd>

O nome do servidor no qual o DSDM reside.

</dd> <dt>

*lpszShareName* \[ no\]
</dt> <dd>

O nome do compartilhamento cujas informações serão recuperadas do DSDM. Esse parâmetro não deve ser **nulo**.

</dd> <dt>

*nLevel* \[ no\]
</dt> <dd>

O nível de informações. Esse parâmetro deve ser 2.

</dd> <dt>

*lpBuffer* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe a estrutura [**NDDESHAREINFO**](nddeshareinfo-str.md) e os dados associados apontados por seus membros. Este parâmetro pode ser **NULL**. Se *lpBuffer* for **NULL**, o DSDM calculará o número de bytes necessários para armazenar as informações de compartilhamento solicitadas e retornará esse valor no campo *LPNTOTALAVAILABLE* junto com o \_ erro NDDE \_ buf muito \_ pequeno.

</dd> <dt>

*cBufSize* \[ no\]
</dt> <dd>

O tamanho do buffer *lpBuffer* , em bytes. Se *lpBuffer* for **NULL**, *cBufSize* deverá ser zero.

</dd> <dt>

*lpnTotalAvailable* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número total de bytes necessários para armazenar as informações de compartilhamento solicitadas. Este parâmetro não pode ser **nulo**.

</dd> <dt>

*lpnItems* \[ no\]
</dt> <dd>

Um ponteiro para uma máscara de seleção de item para recuperação de informações de compartilhamento parcial.

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
| Nomes Unicode e ANSI<br/>   | **NDdeShareGetInfoW** (Unicode) e **NDdeShareGetInfoA** (ANSI)<br/>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de troca dinâmica de dados de rede](network-dynamic-data-exchange.md)
</dt> <dt>

[Funções DDE de rede](network-dde-functions.md)
</dt> <dt>

[**NDDESHAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeShareSetInfo**](nddesharesetinfo.md)
</dt> </dl>

 

 




