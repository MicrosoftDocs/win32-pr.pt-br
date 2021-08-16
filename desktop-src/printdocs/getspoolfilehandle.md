---
description: A função GetSpoolFileHandle recupera um identificador para o arquivo de spool associado ao trabalho enviado no momento pelo aplicativo.
ms.assetid: df6f28b3-66a6-4fb7-bdde-40cd7d934c5f
title: Função GetSpoolFileHandle (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSpoolFileHandle
- GetSpoolFileHandleA
- GetSpoolFileHandleW
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 10b0b36333e51dfb5c831f6c74e00c6930ccbb9d1ce31646fed0d689abc7f639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117686689"
---
# <a name="getspoolfilehandle-function"></a>Função GetSpoolFileHandle

A função **GetSpoolFileHandle** recupera um identificador para o arquivo de spool associado ao trabalho enviado no momento pelo aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
HANDLE GetSpoolFileHandle(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para a impressora para a qual o trabalho foi enviado. Deve ser o mesmo identificador que foi usado para enviar o trabalho. (Use a função [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) para recuperar um identificador de impressora.)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, ela retornará um identificador para o arquivo de spool.

Se a função falhar, ela retornará **um \_ \_ valor de identificador inválido**.

## <a name="remarks"></a>Comentários

Com o identificador para o arquivo de spool, seu aplicativo pode gravar no arquivo de spool com chamadas para [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) seguido por [**CommitSpoolData**](commitspooldata.md).

Seu aplicativo não deve chamar [**ClosePrinter**](closeprinter.md) em *hPrinter* até depois de ter acessado o arquivo de spool pela última vez. Em seguida, ele deve chamar [**CloseSpoolFileHandle**](closespoolfilehandle.md) seguido por **ClosePrinter**. As tentativas de acessar o identificador de arquivo de spool depois que o *hPrinter* original foi fechado falharão mesmo que o próprio identificador de arquivo não tenha sido fechado. O **CloseSpoolFileHandle** , por si só, falhará se **ClosePrinter** for chamado primeiro.

Essa função falhará se for chamada antes que o trabalho de impressão tenha terminado o spool.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **GetSpoolFileHandleW** (Unicode) e **GetSpoolFileHandleA** (ANSI)<br/>                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**CloseSpoolFileHandle**](closespoolfilehandle.md)
</dt> <dt>

[**CommitSpoolData**](commitspooldata.md)
</dt> </dl>

 

