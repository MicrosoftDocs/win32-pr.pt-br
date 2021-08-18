---
description: A função GetPrinterDriver recupera dados de driver para a impressora especificada. Se o driver não estiver instalado no computador local, GetPrinterDriver o instalará.
ms.assetid: 93f859b4-1005-4359-8029-9536d6eeb7e7
title: Função GetPrinterDriver (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver
- GetPrinterDriverA
- GetPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 0a20cd1dedb515714565c1e94f7847fdfc5c7969429686f17682b76cfef070e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971375"
---
# <a name="getprinterdriver-function"></a>Função GetPrinterDriver

A **função GetPrinterDriver** recupera dados de driver para a impressora especificada. Se o driver não estiver instalado no computador local, **GetPrinterDriver** o instalará.

## <a name="syntax"></a>Sintaxe


```C++
BOOL GetPrinterDriver(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ Em\]
</dt> <dd>

Um alça para a impressora para a qual os dados do driver devem ser recuperados. Use a [**função OpenPrinter**](openprinter.md) [**ou AddPrinter**](addprinter.md) para recuperar um alça de impressora.

</dd> <dt>

*pEnvironment* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente (por exemplo, Windows x86, Windows IA64 ou Windows x64). Se esse parâmetro for **NULL,** o ambiente atual do aplicativo de chamada e do computador cliente (não do aplicativo de destino e do servidor de impressão) será usado.

</dd> <dt>

*Nível* \[ Em\]
</dt> <dd>

A estrutura do driver de impressora retornada no buffer *pDriverInfo.* Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                | Significado                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | [**INFORMAÇÕES \_ DO DRIVER \_ 1**](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**INFORMAÇÕES \_ DO DRIVER \_ 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**INFORMAÇÕES \_ DO DRIVER \_ 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**INFORMAÇÕES \_ DO DRIVER \_ 4**](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | [**INFORMAÇÕES \_ DO DRIVER \_ 5**](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**INFORMAÇÕES \_ DO DRIVER \_ 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**INFORMAÇÕES \_ DO DRIVER \_ 8**](driver-info-8.md)<br/> |



 

</dd> <dt>

*pDriverInfo* \[ out\]
</dt> <dd>

Um ponteiro para um buffer que recebe uma estrutura que contém informações sobre o driver, conforme especificado por Level. O buffer deve ser grande o suficiente para armazenar as cadeias de caracteres apontadas pelos membros da estrutura.

Para determinar o tamanho do buffer necessário, chame **GetPrinterDriver** com *cbBuf* definido como zero. **GetPrinterDriver** falha, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna ERROR INSUFFICIENT BUFFER e o parâmetro \_ \_ *pcbNeeded* retorna o tamanho, em bytes, do buffer necessário para manter a matriz de estruturas e seus dados.

</dd> <dt>

*cbBuf* \[ Em\]
</dt> <dd>

O tamanho, em bytes, da matriz na qual *pDriverInfo aponta.*

</dd> <dt>

*pcbNeeded* \[ out\]
</dt> <dd>

Um ponteiro para um valor que recebe o número de bytes copiados se a função for bem-sucedida ou o número de bytes necessários se *cbBuf* for muito pequeno.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um valor não zero.

Se a função falhar, o valor retornado será zero.

Para um driver inexistente, a função retorna ERROR \_ UNKNOWN \_ PRINTER \_ DRIVER.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração do servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

As [**estruturas DRIVER \_ INFO \_ 2,**](driver-info-2.md) [**DRIVER INFO \_ \_ 3,**](driver-info-3.md) [**DRIVER INFO \_ \_ 4,**](driver-info-4.md) [**DRIVER INFO \_ \_ 5**](driver-info-5.md)e [**DRIVER INFO \_ \_ 6**](driver-info-6.md) contêm o nome do arquivo ou o caminho completo e o nome do arquivo do driver de impressora no membro **pDriverPath.** Um aplicativo pode usar o caminho e o nome do arquivo para carregar um driver de impressora chamando a [**função LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e fornecendo o caminho e o nome do arquivo como o único argumento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **GetPrinterDriverW** (Unicode) e **GetPrinterDriverA** (ANSI)<br/>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**INFORMAÇÕES \_ DO DRIVER \_ 1**](driver-info-1.md)
</dt> <dt>

[**INFORMAÇÕES \_ DO DRIVER \_ 2**](driver-info-2.md)
</dt> <dt>

[**INFORMAÇÕES \_ DO DRIVER \_ 3**](driver-info-3.md)
</dt> <dt>

[**INFORMAÇÕES \_ DO DRIVER \_ 4**](driver-info-4.md)
</dt> <dt>

[**INFORMAÇÕES \_ DO DRIVER \_ 5**](driver-info-5.md)
</dt> <dt>

[**INFORMAÇÕES \_ DO DRIVER \_ 6**](driver-info-6.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

