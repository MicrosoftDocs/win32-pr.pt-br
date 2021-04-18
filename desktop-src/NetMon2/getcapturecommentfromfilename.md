---
description: A função GetCaptureCommentFromFilename extrai o comentário de captura de um arquivo de captura.
ms.assetid: d3665cb0-d54d-45f7-aef9-c2e603d6f773
title: Função GetCaptureCommentFromFilename (Netmon. h)
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
ms.openlocfilehash: 9dbfb086ccc27ad2f4c35018c3384a4b81ef0528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810297"
---
# <a name="getcapturecommentfromfilename-function"></a>Função GetCaptureCommentFromFilename

A função **GetCaptureCommentFromFilename** extrai o comentário de captura de um [*arquivo de captura*](c.md).

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

*lpFileName* \[ no\]
</dt> <dd>

Ponteiro para o nome do arquivo de captura.

</dd> <dt>

*lpComment* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres alocada previamente para o comentário.

</dd> <dt>

*BufferSize* \[ no\]
</dt> <dd>

Tamanho da cadeia de caracteres.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida (ou seja, se o comentário for encontrado e copiado, ou não houver nenhum comentário no arquivo de captura), o valor de retorno será NMERR com \_ êxito.

Se a função não for bem-sucedida, o valor de retorno será um código de erro.



| Código de retorno                                                                                                 | Descrição                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**\_erro de \_ leitura do arquivo NMERR \_**</dt> </dl>     | Não é possível ler o comentário de captura.<br/>                               |
| <dl> <dt>**NMERR \_ \_ formato de arquivo inválido \_**</dt> </dl> | O quadro de comentário não é um formato de arquivo válido.<br/>                     |
| <dl> <dt>**\_arquivo NMERR \_ não \_ encontrado**</dt> </dl>      | O arquivo especificado pelo parâmetro *lpFileName* não pode ser encontrado.<br/> |
| <dl> <dt>**NMERR \_ \_ parâmetro inválido**</dt> </dl>    | Um dos parâmetros foi especificado incorretamente.<br/>                   |



 

## <a name="remarks"></a>Comentários

Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetCaptureCommentFromFilename** .

Para recuperar o comentário de uma captura em tempo real, chame a função [GetCaptureComment](getcapturecomment.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[GetCaptureComment](getcapturecomment.md)
</dt> </dl>

 

 




