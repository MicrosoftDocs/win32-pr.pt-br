---
description: A função GetCaptureCommentFromFilename extrai o comentário de captura de um arquivo de captura.
ms.assetid: d3665cb0-d54d-45f7-aef9-c2e603d6f773
title: Função GetCaptureCommentFromFilename (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureCommentFromFilename
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1b92b81fa00834c3a4038a6a6bb9f295246a7c0b217c99779a5d2c569dbbf982
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366807"
---
# <a name="getcapturecommentfromfilename-function"></a>Função GetCaptureCommentFromFilename

A **função GetCaptureCommentFromFilename** extrai o comentário de captura de um [*arquivo de captura*](c.md).

## <a name="syntax"></a>Sintaxe


```C++
DWORD  WINAPI GetCaptureCommentFromFilename(
  _In_ LPSTR lpFilename,
  _In_ LPSTR lpComment,
  _In_ DWORD BufferSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpFilename* \[ Em\]
</dt> <dd>

Ponteiro para o nome do arquivo de captura.

</dd> <dt>

*lpComment* \[ Em\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres pré-alocada para o comentário.

</dd> <dt>

*BufferSize* \[ Em\]
</dt> <dd>

Tamanho da cadeia de caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida (ou seja, se o comentário for encontrado e copiado ou não houver nenhum comentário no arquivo de captura), o valor de retorno será NMERR \_ SUCCESS.

Se a função não for bem-sucedida, o valor de retorno será um código de erro.



| Código de retorno                                                                                                 | Descrição                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**ERRO DE LEITURA DO ARQUIVO NMERR \_ \_ \_**</dt> </dl>     | O comentário de captura não pode ser lido.<br/>                               |
| <dl> <dt>**FORMATO DE ARQUIVO INVÁLIDO NMERR \_ \_ \_**</dt> </dl> | O quadro Comentário não é um formato de arquivo válido.<br/>                     |
| <dl> <dt>**ARQUIVO NMERR \_ \_ NÃO \_ ENCONTRADO**</dt> </dl>      | O arquivo especificado pelo parâmetro *lpFilename* não pode ser encontrado.<br/> |
| <dl> <dt>**PARÂMETRO INVÁLIDO \_ NMERR \_**</dt> </dl>    | Um dos parâmetros é especificado incorretamente.<br/>                   |



 

## <a name="remarks"></a>Comentários

[*Especialistas*](e.md) e [*analisadores podem*](p.md) chamar a **função GetCaptureCommentFromFilename.**

Para recuperar o comentário de uma captura em tempo real, chame a [função GetCaptureComment.](getcapturecomment.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[GetCaptureComment](getcapturecomment.md)
</dt> </dl>

 

 




