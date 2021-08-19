---
description: Adiciona uma conexão à impressora especificada para o usuário atual e especifica os detalhes da conexão.
ms.assetid: 5ae98157-5978-449e-beb1-4787110925fa
title: Função AddPrinterConnection2 (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection2
- AddPrinterConnection2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: f54cdafc2bc5c957f21ed4f9a14355d6a70f7df817e975c1fe701e2b20af35a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868964"
---
# <a name="addprinterconnection2-function"></a>Função AddPrinterConnection2

Adiciona uma conexão à impressora especificada para o usuário atual e especifica os detalhes da conexão.

## <a name="syntax"></a>Sintaxe


```C++
BOOL AddPrinterConnection2(
  _In_ HWND    hWnd,
  _In_ LPCTSTR pszName,
       DWORD   dwLevel,
  _In_ PVOID   pConnectionInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hWnd* \[ Em\]
</dt> <dd>

Um alça para a janela pai na qual a caixa de diálogo será exibida se o sistema de impressão tiver que baixar um driver de impressora do servidor de impressão para essa conexão.

</dd> <dt>

*pszName* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres com terminação nula constante que especifica o nome da impressora à qual o usuário atual deseja se conectar.

</dd> <dt>

*dwLevel* 
</dt> <dd>

A versão da estrutura apontada por *pConnectionInfo*. Atualmente, apenas o nível 1 é definido, portanto, o valor *de dwLevel* deve ser 1.

</dd> <dt>

*pConnectionInfo* \[ Em\]
</dt> <dd>

Um ponteiro para uma estrutura [**PRINTER \_ CONNECTION INFO \_ \_ 1.**](printer-connection-info-1.md) Consulte a seção Comentários para obter mais informações sobre esse parâmetro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um valor não zero.

Se a função falhar, o valor retornado será zero. Para obter informações de erro estendidas, [**chame GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração do servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Quando Windows Vista faz uma conexão com uma impressora, talvez seja necessário copiar arquivos de driver de impressora do servidor ao qual a impressora está anexada. Se o usuário não tiver permissão para copiar arquivos para o local apropriado, a função **AddPrinterConnection2** falhará e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará ERROR \_ ACCESS \_ DENIED.

Se os arquivos do driver de impressora devem ser copiados do servidor de impressão, mas não podem ser copiados silenciosamente devido às políticas de grupo que estão em vigor e PRINTER CONNECTION NO UI está definida em \_ \_ \_ *pConnectionInfo->dwFlags*, nenhuma caixa de diálogo será exibida e a chamada falhará.

Se o driver de impressora local puder ser usado para renderizar trabalhos de impressão para essa impressora e a versão do driver local não corresponder à versão do driver de impressora no servidor, defina PRINTER \_ CONNECTION \_ MISMATCH em *pConnectionInfo->dwFlags* e atribua o ponteiro a uma variável de cadeia de caracteres que contém o caminho para o driver de impressora local para *pConnectionInfo->pszDriverName*.

Uma conexão de impressora estabelecida chamando **AddPrinterConnection2** será enumerada quando [**EnumPrinters**](enumprinters.md) for chamado com *dwType* definido como PRINTER \_ ENUM \_ CONNECTION.

A versão ANSI dessa função, **AddPrinterConnection2A,** não tem suporte e retorna **ERROR NOT \_ \_ SUPPORTED**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **AddPrinterConnection2W** (Unicode)<br/>                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ConnectToPrinterDlg**](connecttoprinterdlg.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**DeletePrinterConnection**](deleteprinterconnection.md)
</dt> </dl>

 

