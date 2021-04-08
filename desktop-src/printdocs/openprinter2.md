---
description: Recupera um identificador para a impressora especificada, o servidor de impressão ou outros tipos de identificadores no subsistema de impressão, enquanto define algumas das opções de impressora.
ms.assetid: e2370ae4-4475-4ccc-a6f9-3d33d1370054
title: Função OpenPrinter2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter2
- OpenPrinter2A
- OpenPrinter2W
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 46788d7ad810ef623cd77793a72ab6c046b73590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828764"
---
# <a name="openprinter2-function"></a>Função OpenPrinter2

Recupera um identificador para a impressora especificada, o servidor de impressão ou outros tipos de identificadores no subsistema de impressão, enquanto define algumas das opções de impressora.

## <a name="syntax"></a>Sintaxe


```C++
BOOL OpenPrinter2(
  _In_  LPCTSTR            pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault,
  _In_  PPRINTER_OPTIONS   pOptions
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPrinterName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres constante terminada em nulo que especifica o nome da impressora ou do servidor de impressão, o objeto de impressora, o XcvMonitor ou o XcvPort.

Para um objeto de impressora, use: PrinterName, trabalho xxxx. Para um XcvMonitor, use: nomedoservidor, XcvMonitor Monitorname. Para um XcvPort, use: nomedoservidor, XcvPort PortName.

**Windows Vista:** Se for **NULL**, indicará o servidor de impressão local.

</dd> <dt>

*phPrinter* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe um identificador para o objeto de impressora aberta ou de servidor de impressão.

</dd> <dt>

*pDefault* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ padrões de impressora**](printer-defaults.md) . Esse valor pode ser **nulo**.

</dd> <dt>

*pOptions* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ Opções de impressora**](printer-options.md) . Esse valor pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

Não chame esse método em [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

A versão ANSI dessa função não foi implementada e \_ não \_ há suporte para o erro.

O parâmetro *pDefault* permite que você especifique o tipo de dados e os valores do modo de dispositivo que são usados para imprimir documentos enviados pela função [**StartDocPrinter**](startdocprinter.md) . No entanto, você pode substituir esses valores usando a função [**SetJob**](setjob.md) depois que um documento for iniciado.

Você pode chamar a função **OpenPrinter2** para abrir um identificador para um servidor de impressão ou para determinar os direitos de acesso do cliente a um servidor de impressão. Para fazer isso, especifique o nome do servidor de impressão no parâmetro *pPrinterName* , defina os membros **pDatatype** e **PDevMode** da estrutura [**\_ padrões da impressora**](printer-defaults.md) como **NULL** e defina o membro **desiredAccess** para especificar um valor de máscara de acesso do servidor, como servidor \_ todo \_ acesso. Quando você terminar com o identificador, passe-o para a função [**ClosePrinter**](closeprinter.md) para fechá-lo.

Use o membro **desiredAccess** da estrutura [**\_ padrões da impressora**](printer-defaults.md) para especificar os direitos de acesso necessários. Os direitos de acesso podem ser um dos seguintes.



| Valor de acesso desejado                        | Significado                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| acesso de impressora \_ \_ administrar                 | Para executar tarefas administrativas, como as fornecidas pelo [**Setprinter**](setprinter.md).                                                                                                 |
| \_uso de acesso à impressora \_                        | Para executar operações básicas de impressão.                                                                                                                                                        |
| \_todos os \_ acessos à impressora                        | Para executar todas as tarefas administrativas e operações básicas de impressão, exceto sincronizar. Consulte [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights).                                         |
| \_Gerenciamento de acesso à impressora \_ \_ limitado            | Para executar tarefas administrativas, como as fornecidas por [**Setprinter**](setprinter.md) e [**SetPrinterData**](setprinterdata.md). Esse valor está disponível a partir de Windows 8.1. |
| valores de segurança genéricos, como gravar \_ DAC | Para permitir direitos de acesso de controle específico. Consulte [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights).                                                                                      |



 

Se um usuário não tiver permissão para abrir uma impressora ou servidor de impressão especificado com o acesso desejado, a chamada **OpenPrinter2** falhará e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o valor erro \_ acesso \_ negado.

Quando *pPrinterName* é uma impressora local, o **OpenPrinter2** ignora todos os valores do **dwFlags** que a estrutura [**de \_ Opções de impressora**](printer-options.md) apontou para usar o *pOptions*, exceto a opção de impressora do \_ \_ cliente \_ mudar. Se o último for passado, **OpenPrinter2** retornará um erro de \_ acesso \_ negado. Da mesma forma, ao abrir uma impressora local, o **OpenPrinter2** não oferece nenhuma vantagem sobre [**OpenPrinter**](openprinter.md).

**Windows Vista:** Os dados de impressora retornados por **OpenPrinter2** são recuperados de um cache local, a menos que a **opção de impressora sem sinalizador de \_ \_ \_ cache** esteja definida no campo **dwFlags** da estrutura de [**\_ Opções de impressora**](printer-options.md) referenciada por *pOptions*.

## <a name="examples"></a>Exemplos

Neste exemplo, **OpenPrinter2** falha quando o \_ acesso à impressora \_ Gerenciar \_ limitado é passado para a estrutura de [**\_ padrões de impressora**](printer-defaults.md) e o usuário não tem a permissão apropriada.


```C++
// Specify the limited management permission.
PRINTER_DEFAULTS defaults = {};
defaults.DesiredAccess = PRINTER_ACCESS_MANAGE_LIMITED;

// Open a printer to which the user has no administrative rights.
HANDLE printer = nullptr;
assert(!OpenPrinter2(L QueueWithNoAdminRights , // Queue name
                     &printer,                  // Printer handle
                     &defaults,                 // Printer defaults
                     nullptr));                 // Printer options

assert(GetLastError() == ERROR_ACCESS_DENIED);

if (printer)
{
    ClosePrinter(printer);
}
```



Para um programa de exemplo que mostra como usar essa função, consulte [como imprimir usando a API de impressão GDI](how-to--print-using-the-gdi-print-api.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nomes Unicode e ANSI<br/>   | **OpenPrinter2W** (Unicode) e **OpenPrinter2A** (ANSI)<br/>                                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**padrões de impressora \_**](printer-defaults.md)
</dt> <dt>

[**opções de impressora \_**](printer-options.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

