---
description: Recupera informações de compartilhamento de DDE. Isso geralmente é feito para edição.
ms.assetid: a2e48a4d-2b72-40a3-b827-474da1db0910
title: Função NDdeShareGetInfo (Nddeapi.h)
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
ms.openlocfilehash: 2c622a611b3d917dcf67de2ec6b96070ec0e54e9e53b0cef04c3c9e35b859e40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014746"
---
# <a name="nddesharegetinfo-function"></a>Função NDdeShareGetInfo

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ NOT \_ IMPLEMENTED.\]

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

*lpszServer* \[ Em\]
</dt> <dd>

O nome do servidor no qual o DSDM reside.

</dd> <dt>

*lpszShareName* \[ Em\]
</dt> <dd>

O nome do compartilhamento cujas informações devem ser recuperadas do DSDM. Esse parâmetro não deve ser **NULL.**

</dd> <dt>

*nLevel* \[ Em\]
</dt> <dd>

O nível de informações. Esse parâmetro deve ser 2.

</dd> <dt>

*lpBuffer* \[ out\]
</dt> <dd>

Um ponteiro para um buffer que recebe a estrutura [**NDINFOAREINFO**](nddeshareinfo-str.md) e os dados associados apontados por seus membros. Este parâmetro pode ser **NULL**. Se *lpBuffer* for **NULL,** o DSDM calculará o número de bytes necessários para armazenar as informações de compartilhamento solicitadas e retornará esse valor no campo *lpnTotalAvailable* junto com o erro NDDE \_ BUF \_ TOO \_ SMALL.

</dd> <dt>

*cBufSize* \[ Em\]
</dt> <dd>

O tamanho do *buffer lpBuffer,* em bytes. Se *lpBuffer* for **NULL,** *cBufSize* deverá ser zero.

</dd> <dt>

*lpnTotalAvailable* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número total de bytes necessários para armazenar as informações de compartilhamento solicitadas. Esse parâmetro não pode ser **NULL.**

</dd> <dt>

*lpnItems* \[ Em\]
</dt> <dd>

Um ponteiro para uma máscara de seleção de item para recuperação parcial de informações de compartilhamento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será NDDE \_ NO \_ ERROR.

Se a função falhar, o valor de retorno será um código de erro, que pode ser convertido em uma mensagem de erro de texto chamando [**NDdeGetErrorString**](nddegeterrorstring.md). Se o *parâmetro lpBuffer* for **NULL**, ele retornará NDDE \_ BUF \_ MUITO \_ PEQUENO.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **NDdeShareGetInfoW** (Unicode) e **NDdeShareGetInfoA** (ANSI)<br/>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral Dados Dinâmicos Exchange rede](network-dynamic-data-exchange.md)
</dt> <dt>

[Funções DDE de rede](network-dde-functions.md)
</dt> <dt>

[**NDINFOAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeShareSetInfo**](nddesharesetinfo.md)
</dt> </dl>

 

 




