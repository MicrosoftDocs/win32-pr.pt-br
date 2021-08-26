---
description: A função CloseSpoolFileHandle fecha um handle para um arquivo de spool associado ao trabalho de impressão enviado atualmente pelo aplicativo.
ms.assetid: e2c0e68f-b72e-4a97-ba18-8943bc5789c1
title: Função CloseSpoolFileHandle (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CloseSpoolFileHandle
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: f62173747472820f1642578778b67f3cdc3403523d6ae28453888dae3d6d1a23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950526"
---
# <a name="closespoolfilehandle-function"></a>Função CloseSpoolFileHandle

A **função CloseSpoolFileHandle** fecha um handle para um arquivo de spool associado ao trabalho de impressão enviado atualmente pelo aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
BOOL CloseSpoolFileHandle(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ Em\]
</dt> <dd>

Um alça para a impressora para a qual o trabalho foi enviado. Esse deve ser o mesmo handle que foi usado para obter *hSpoolFile* com [**GetSpoolFileHandle**](getspoolfilehandle.md).

</dd> <dt>

*hSpoolFile* \[ Em\]
</dt> <dd>

Um alça para o arquivo de spool que está sendo fechado. Se [**CommitSpoolData**](commitspooldata.md) não tiver sido chamado desde [**que GetSpoolFileHandle**](getspoolfilehandle.md) foi chamado, esse deverá ser o mesmo handle retornado por **GetSpoolFileHandle.** Caso contrário, ele deverá ser o alça que foi retornado pela chamada mais recente para **CommitSpoolData.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**TRUE**, se for bem-sucedido, **false caso** contrário.

## <a name="remarks"></a>Comentários

Seu aplicativo não deve chamar [**ClosePrinter**](closeprinter.md) no *hPrinter* até que ele tenha acessado o arquivo spool pela última vez. Em seguida, ele deve **chamar CloseSpoolFileHandle** seguido **por ClosePrinter**. As tentativas de acessar o alça do arquivo spool depois que o *hPrinter* original tiver sido fechado falharão mesmo que o próprio controle de arquivo não tenha sido fechado. **CloseSpoolFileHandle** falhará se **ClosePrinter** for chamado primeiro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool.drv</dt> </dl>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**GetSpoolFileHandle**](getspoolfilehandle.md)
</dt> </dl>

 

 




