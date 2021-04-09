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
ms.openlocfilehash: 9ac4dd4b0db9a59cc0140872ff04f89adaf8b6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011732"
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

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, ela retornará um identificador para o arquivo de spool.

Se a função falhar, ela retornará **um \_ \_ valor de identificador inválido**.

## <a name="remarks"></a>Comentários

Com o identificador para o arquivo de spool, seu aplicativo pode gravar no arquivo de spool com chamadas para [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) seguido por [**CommitSpoolData**](commitspooldata.md).

Seu aplicativo não deve chamar [**ClosePrinter**](closeprinter.md) em *hPrinter* até depois de ter acessado o arquivo de spool pela última vez. Em seguida, ele deve chamar [**CloseSpoolFileHandle**](closespoolfilehandle.md) seguido por **ClosePrinter**. As tentativas de acessar o identificador de arquivo de spool depois que o *hPrinter* original foi fechado falharão mesmo que o próprio identificador de arquivo não tenha sido fechado. O **CloseSpoolFileHandle** , por si só, falhará se **ClosePrinter** for chamado primeiro.

Essa função falhará se for chamada antes que o trabalho de impressão tenha terminado o spool.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
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

 

