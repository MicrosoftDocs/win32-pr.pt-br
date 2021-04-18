---
description: A função CloseSpoolFileHandle fecha um identificador para um arquivo de spool associado ao trabalho de impressão atualmente enviado pelo aplicativo.
ms.assetid: e2c0e68f-b72e-4a97-ba18-8943bc5789c1
title: Função CloseSpoolFileHandle (winspool. h)
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
ms.openlocfilehash: c808bddde5b9b4e4a87a8608c1efb3999ce1f391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758497"
---
# <a name="closespoolfilehandle-function"></a>Função CloseSpoolFileHandle

A função **CloseSpoolFileHandle** fecha um identificador para um arquivo de spool associado ao trabalho de impressão atualmente enviado pelo aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
BOOL CloseSpoolFileHandle(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para a impressora para a qual o trabalho foi enviado. Deve ser o mesmo identificador que foi usado para obter *hSpoolFile* com [**GetSpoolFileHandle**](getspoolfilehandle.md).

</dd> <dt>

*hSpoolFile* \[ no\]
</dt> <dd>

Um identificador para o arquivo de spool que está sendo fechado. Se [**CommitSpoolData**](commitspooldata.md) não tiver sido chamado desde que [**GetSpoolFileHandle**](getspoolfilehandle.md) foi chamado, ele deverá ser o mesmo identificador retornado por **GetSpoolFileHandle**. Caso contrário, ele deve ser o identificador que foi retornado pela chamada mais recente para **CommitSpoolData**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**True**, se tiver sucesso; caso contrário, **false** .

## <a name="remarks"></a>Comentários

Seu aplicativo não deve chamar [**ClosePrinter**](closeprinter.md) em *hPrinter* até depois de ter acessado o arquivo de spool pela última vez. Em seguida, ele deve chamar **CloseSpoolFileHandle** seguido por **ClosePrinter**. As tentativas de acessar o identificador de arquivo de spool depois que o *hPrinter* original foi fechado falharão mesmo que o próprio identificador de arquivo não tenha sido fechado. **CloseSpoolFileHandle** falhará se **ClosePrinter** for chamado primeiro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool. drv</dt> </dl>                   |



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

 

 




