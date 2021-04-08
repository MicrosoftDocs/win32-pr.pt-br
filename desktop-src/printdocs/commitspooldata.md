---
description: A função CommitSpoolData notifica o spooler de impressão que uma quantidade especificada de dados foi gravada em um arquivo de spool especificado e está pronta para ser renderizada.
ms.assetid: cb8899e0-2fdf-4928-adff-17ef5af39f63
title: Função CommitSpoolData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommitSpoolData
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: fa90cb1344e7c087a601a74991598e509daed226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828210"
---
# <a name="commitspooldata-function"></a>Função CommitSpoolData

A função **CommitSpoolData** notifica o spooler de impressão que uma quantidade especificada de dados foi gravada em um arquivo de spool especificado e está pronta para ser renderizada.

## <a name="syntax"></a>Sintaxe


```C++
HANDLE CommitSpoolData(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile,
       DWORD  cbCommit
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

Um identificador para o arquivo de spool que está sendo alterado. Na primeira chamada de **CommitSpoolData**, deve ser o mesmo identificador retornado por [**GetSpoolFileHandle**](getspoolfilehandle.md). As chamadas subsequentes para **CommitSpoolData** devem passar o identificador retornado pela chamada anterior. Consulte Observações.

</dd> <dt>

*cbCommit* 
</dt> <dd>

O número de bytes confirmados para o spooler de impressão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, ela retornará um identificador para o arquivo de spool.

Se a função falhar, ela retornará um \_ valor de identificador inválido \_ .

## <a name="remarks"></a>Comentários

Os aplicativos que enviam um trabalho de impressão do spooler podem chamar [**GetSpoolFileHandle**](getspoolfilehandle.md) e, em seguida, gravar dados diretamente no identificador do arquivo de spool chamando [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile). Para notificar o spooler de impressão de que o arquivo contém dados que estão prontos para serem renderizados, o aplicativo deve chamar **CommitSpoolData** e fornecer o número de bytes disponíveis.

Se **CommitSpoolData** for chamado várias vezes, cada chamada deverá usar o identificador de arquivo de spool retornado pela chamada anterior. Quando não forem gravados mais dados no arquivo de spool, [**CloseSpoolFileHandle**](closespoolfilehandle.md) deverá ser chamado para o identificador de arquivo retornado pela última chamada para **CommitSpoolData**.

Antes de chamar **CommitSpoolData**, os aplicativos devem definir o ponteiro do arquivo para a posição que ele tinha antes de gravar dados no arquivo. No processo de renderização dos dados no arquivo de spooler, o spooler de impressão moverá o ponteiro do arquivo de spool *cbCommit* bytes do valor atual do ponteiro do arquivo.

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

[**GetSpoolFileHandle**](getspoolfilehandle.md)
</dt> <dt>

[**CloseSpoolFileHandle**](closespoolfilehandle.md)
</dt> </dl>

 

