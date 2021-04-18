---
description: Retorna um ponteiro para o comentário de uma captura.
ms.assetid: 3ef5c5b3-5586-469f-8975-049713715403
title: Função GetCaptureComment (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureComment
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ca2d3dd3fdc91c54c49b12119a56180396df5ec5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766848"
---
# <a name="getcapturecomment-function"></a>Função GetCaptureComment

A função **GetCaptureComment** retorna um ponteiro para o comentário de uma captura.

## <a name="syntax"></a>Sintaxe


```C++
LPSTR WINAPI GetCaptureComment(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hCapture* \[ no\]
</dt> <dd>

Um identificador para a captura. Para obter mais informações sobre como obter o identificador de captura, consulte a seção comentários.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida (ou seja, se a captura contiver um comentário), o valor de retorno será um ponteiro para a cadeia de caracteres de comentário.

Se a função não for bem-sucedida, o valor de retorno será **nulo**.

## <a name="remarks"></a>Comentários

Não altere a cadeia de caracteres de comentário retornada, que é a cadeia de caracteres de comentário real que está na captura carregada. As alterações podem corromper a captura. Tentativas de modificar o resultado da cadeia de caracteres em uma violação de acesso.

O identificador da captura pode ser obtido de várias maneiras, dependendo se a chamada é feita por um especialista ou analisador. Para especialistas, o identificador é especificado no membro **hCapture** da estrutura [EXPERTSTARTUPINFO](expertstartupinfo.md) . Para analisadores, o identificador de captura pode ser obtido chamando a função [GetFrameCaptureHandle](getframecapturehandle.md) .

Para recuperar o comentário de uma captura de seu arquivo de captura, chame a função [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md) .

Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetCaptureComment** .

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

[EXPERTSTARTUPINFO](expertstartupinfo.md)
</dt> <dt>

[GetCaptureCommentFromFilename](getcapturecommentfromfilename.md)
</dt> <dt>

[GetFrameCaptureHandle](getframecapturehandle.md)
</dt> </dl>

 

 




