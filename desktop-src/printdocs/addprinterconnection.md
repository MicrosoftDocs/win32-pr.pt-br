---
description: A função AddPrinterConnection adiciona uma conexão à impressora especificada para o usuário atual.
ms.assetid: 6decf89a-1411-4e7e-aa20-60e7068658c2
title: Função AddPrinterConnection (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection
- AddPrinterConnectionA
- AddPrinterConnectionW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 83c4d348266e0d596deccb03b39e98ec41f8f23837727520d55b9baff82fec4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869028"
---
# <a name="addprinterconnection-function"></a>Função AddPrinterConnection

A **função AddPrinterConnection** adiciona uma conexão à impressora especificada para o usuário atual.

## <a name="syntax"></a>Sintaxe


```C++
BOOL AddPrinterConnection(
  _In_ LPTSTR pName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pName* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome de uma impressora à qual o usuário atual deseja estabelecer uma conexão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um valor não zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração do servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Quando Windows faz uma conexão com uma impressora, pode ser necessário copiar arquivos de driver de impressora para o servidor ao qual a impressora está anexada. Se o usuário não tiver permissão para copiar arquivos para o local apropriado, a função **AddPrinterConnection** falhará e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará ERROR \_ ACCESS \_ DENIED.

Uma conexão de impressora estabelecida chamando **AddPrinterConnection** será enumerada quando [**EnumPrinters**](enumprinters.md) for chamado com *dwType* definido como PRINTER \_ ENUM \_ CONNECTION.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **AddPrinterConnectionW** (Unicode) e **AddPrinterConnectionA** (ANSI)<br/>                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ConnectToPrinterDlg**](connecttoprinterdlg.md)
</dt> <dt>

[**DeletePrinterConnection**](deleteprinterconnection.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> </dl>

 

