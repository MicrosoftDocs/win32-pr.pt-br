---
description: A função OpenPrinter recupera um identificador para a impressora ou o servidor de impressão especificado ou outros tipos de identificadores no subsistema de impressão.
ms.assetid: 96763220-d851-46f0-8be8-403f3356edb9
title: Função OpenPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter
- OpenPrinterA
- OpenPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 48f25f9c8aec314b997a4600335e22bea2f0bbd8eefa78235ddbb25192f556f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868591"
---
# <a name="openprinter-function"></a>Função OpenPrinter

A função **OpenPrinter** recupera um identificador para a impressora ou o servidor de impressão especificado ou outros tipos de identificadores no subsistema de impressão.

## <a name="syntax"></a>Sintaxe


```C++
BOOL OpenPrinter(
  _In_  LPTSTR             pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPrinterName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da impressora ou do servidor de impressão, o objeto de impressora, o XcvMonitor ou o XcvPort.

Para um objeto de impressora, use: PrinterName, trabalho xxxx. Para um XcvMonitor, use: nomedoservidor, XcvMonitor Monitorname. Para um XcvPort, use: nomedoservidor, XcvPort PortName.

Se for **NULL**, indicará o servidor de impressora local.

</dd> <dt>

*phPrinter* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe um identificador (não seguro para thread) para o objeto de impressora aberta ou de servidor de impressão.

O parâmetro *phPrinter* pode retornar um identificador Xcv para uso com a função XcvData. Para obter mais informações sobre XcvData, consulte o DDK.

</dd> <dt>

*pDefault* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ padrões de impressora**](printer-defaults.md) . Esse valor pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

Não chame esse método em [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Um identificador obtido para uma impressora remota por uma chamada para **OpenPrinter** para uma impressora remota acessa a impressora por meio de um cache local no serviço spooler de impressão. Esse cache não é preciso em tempo real. Para obter dados precisos, substitua a chamada OpenPrinter por [**OpenPrinter2**](openprinter2.md) por POptions. dwFlags definido como \_ opção de impressora \_ sem \_ cache. Observe que apenas OpenPrinter2W é funcional. A função retorna um identificador de impressora que usa outras chamadas à API de impressão e ignora o cache local. Esse método é bloqueado enquanto aguarda a comunicação de rede com a impressora remota, portanto, ele pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação da interface do usuário pode fazer com que o aplicativo pareça sem resposta.

 

> [!Note]  
> Um identificador obtido por uma chamada para **OpenPrinter** para uma impressora remota acessará a impressora por meio de um cache local no serviço spooler de impressão. Esse cache é, por design, não é preciso em tempo real. Se você precisar obter dados precisos, substitua a chamada **OpenPrinter** por [**OpenPrinter2**](openprinter2.md) por *pOptions. dwFlags* definido como [**opção de impressora \_ \_ sem \_ cache**](printer-options.md). Observe que apenas **OpenPrinter2W** é funcional. Ao fazer isso, a função retorna um identificador de impressora que faz com que outras chamadas à API de impressão ignorem o cache local. Observe que essa abordagem será bloqueada enquanto aguarda a comunicação de rede de ida e volta para a impressora remota, para que ela possa não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Portanto, chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

O identificador apontado por *phPrinter* não é thread-safe. Se os chamadores precisarem usá-lo simultaneamente em vários threads, eles deverão fornecer acesso de sincronização personalizado ao identificador da impressora usando as [funções de sincronização](/windows/desktop/Sync/synchronization-functions). Para evitar escrever código personalizado, o aplicativo pode abrir um identificador de impressora em cada thread, conforme necessário.

O parâmetro *pDefault* permite que você especifique o tipo de dados e os valores do modo de dispositivo que são usados para imprimir documentos enviados pela função [**StartDocPrinter**](startdocprinter.md) . No entanto, você pode substituir esses valores usando a função [**SetJob**](setjob.md) depois que um documento for iniciado.

As configurações [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) definidas na estrutura [**\_ padrões da impressora**](printer-defaults.md) do parâmetro *pDefault* não são usadas quando o valor do membro *pDatatype* da estrutura [**info do documento \_ \_ 1**](doc-info-1.md) que foi passada no parâmetro *pDocInfo* da chamada [**StartDocPrinter**](startdocprinter.md) é "RAW". quando um documento de alto nível (como um arquivo Adobe PDF ou Microsoft Word) ou outros dados de impressora (como PCL, PS ou HPGL) são enviados diretamente para uma impressora com *pDatatype* definido como "RAW", o documento deve descrever totalmente as configurações do trabalho de impressão estilo **DEVMODE** no idioma compreendido pelo hardware.

Você pode chamar a função **OpenPrinter** para abrir um identificador para um servidor de impressão ou para determinar os direitos de acesso que um cliente tem a um servidor de impressão. Para fazer isso, especifique o nome do servidor de impressão no parâmetro *pPrinterName* , defina os membros **pDatatype** e **PDevMode** da estrutura [**\_ padrões da impressora**](printer-defaults.md) como **NULL** e defina o membro **desiredAccess** para especificar um valor de máscara de acesso do servidor, como servidor \_ todo \_ acesso. Quando você terminar com a alça, passe-a para a função [**ClosePrinter**](closeprinter.md) para fechá-la.

Use o membro **desiredAccess** da estrutura [**\_ padrões da impressora**](printer-defaults.md) para especificar os direitos de acesso necessários para a impressora. Os direitos de acesso podem ser um dos seguintes. (Se *pDefault* for **nulo**, os direitos de acesso serão impressora \_ uso de acesso \_ .)



| Valor de acesso desejado                        | Significado                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| acesso de impressora \_ \_ administrar                 | Para executar tarefas administrativas, como as fornecidas pelo [**Setprinter**](setprinter.md).                                                                                                 |
| \_uso de acesso à impressora \_                        | Para executar operações básicas de impressão.                                                                                                                                                        |
| \_todos os \_ acessos à impressora                        | Para executar todas as tarefas administrativas e operações básicas de impressão, exceto para sincronizar (consulte [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights).                                     |
| \_Gerenciamento de acesso à impressora \_ \_ limitado            | Para executar tarefas administrativas, como as fornecidas por [**Setprinter**](setprinter.md) e [**SetPrinterData**](setprinterdata.md). Esse valor está disponível a partir de Windows 8.1. |
| valores de segurança genéricos, como gravar \_ DAC | Para permitir direitos de acesso de controle específico. Consulte [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights).                                                                                      |



 

Se um usuário não tiver permissão para abrir uma impressora ou um servidor de impressão especificado com o acesso desejado, a chamada **OpenPrinter** falhará com um valor de retorno zero e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o valor de erro \_ acesso \_ negado.

## <a name="examples"></a>Exemplos

Para obter um programa de exemplo que usa essa função, consulte [como imprimir usando a API de impressão GDI](how-to--print-using-the-gdi-print-api.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **OpenPrinterW** (Unicode) e **OpenPrinterA** (ANSI)<br/>                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**padrões de impressora \_**](printer-defaults.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 

