---
description: Adiciona uma conexão à impressora especificada para o usuário atual e especifica os detalhes da conexão.
ms.assetid: 5ae98157-5978-449e-beb1-4787110925fa
title: Função AddPrinterConnection2 (winspool. h)
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
ms.openlocfilehash: b24d5ddb25a43fae8576a042c4be6da8fd7cfef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782213"
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

*HWND* \[ no\]
</dt> <dd>

Um identificador para a janela pai no qual a caixa de diálogo será exibida se o sistema de impressão precisar baixar um driver de impressora do servidor de impressão para essa conexão.

</dd> <dt>

*pszName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres de constante terminada em nulo especificando o nome da impressora à qual o usuário atual deseja se conectar.

</dd> <dt>

*dwLevel* 
</dt> <dd>

A versão da estrutura apontada por *pConnectionInfo*. Atualmente, somente o nível 1 é definido, portanto, o valor de *dwLevel* deve ser 1.

</dd> <dt>

*pConnectionInfo* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**informações de conexão de impressora \_ \_ \_ 1**](printer-connection-info-1.md) . Consulte a seção comentários para obter mais informações sobre esse parâmetro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Quando o Windows Vista faz uma conexão com uma impressora, pode ser necessário copiar arquivos de driver de impressora do servidor ao qual a impressora está conectada. Se o usuário não tiver permissão para copiar arquivos para o local apropriado, a função **AddPrinterConnection2** falhará e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o \_ acesso ao erro \_ negado.

Se os arquivos de driver de impressora precisarem ser copiados do servidor de impressão, mas não puderem ser copiados silenciosamente devido às políticas de grupo que estão em vigor e \_ \_ a conexão de impressora sem \_ interface do usuário estiver definida em *pConnectionInfo->dwFlags*, nenhuma caixa de diálogo será exibida e a chamada falhará.

Se o driver de impressora local pode ser usado para renderizar trabalhos de impressão para esta impressora e a versão do driver local não deve corresponder à versão do driver de impressora no servidor, defina \_ incompatibilidade de conexão de impressora \_ em *PConnectionInfo->dwFlags* e atribua o ponteiro a uma variável de cadeia de caracteres que contenha o caminho para o driver de impressora local para *pConnectionInfo->pszDriverName*.

Uma conexão de impressora estabelecida pela chamada de **AddPrinterConnection2** será enumerada quando [**EnumPrinters**](enumprinters.md) for chamado com *dwType* definido como conexão de \_ enumeração de impressora \_ .

Não há suporte para a versão ANSI dessa função, **AddPrinterConnection2A**, e **\_ não \_ há suporte para** retorno de erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
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

 

