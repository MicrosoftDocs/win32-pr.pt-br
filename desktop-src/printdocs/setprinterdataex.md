---
description: A função SetPrinterDataEx define os dados de configuração para um servidor de impressão ou impressora. A função armazena os dados de configuração na chave do registro de impressoras.
ms.assetid: b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1
title: Função SetPrinterDataEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterDataEx
- SetPrinterDataExA
- SetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 9f384c9c9d6f0d956264b45ec8b52043ad20e897
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171327"
---
# <a name="setprinterdataex-function"></a>Função SetPrinterDataEx

A função **SetPrinterDataEx** define os dados de configuração para um servidor de impressão ou impressora. A função armazena os dados de configuração na chave do registro da impressora.

## <a name="syntax"></a>Sintaxe


```C++
DWORD SetPrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName,
  _In_ DWORD   Type,
  _In_ LPBYTE  pData,
  _In_ DWORD   cbData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para a impressora ou o servidor de impressão para o qual a função define os dados de configuração. Use a função [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)ou [**AddPrinter**](addprinter.md) para recuperar um identificador de impressora.

</dd> <dt>

*pKeyName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a chave que contém o valor a ser definido. Se a chave ou subchaves especificadas não existirem, a função as criará.

Para armazenar os dados de configuração que podem ser publicados no serviço de diretório (DS), especifique uma das seguintes chaves de registro predefinidas.



| Valor                                                                                                                                                                      | Significado                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="SPLDS_DRIVER_KEY"></span><span id="splds_driver_key"></span><dl> <dt>**SPLDS_DRIVER_KEY**</dt> </dl>    | Os drivers de impressora usam essa chave para armazenar as propriedades do driver.<br/>                             |
| <span id="SPLDS_SPOOLER_KEY"></span><span id="splds_spooler_key"></span><dl> <dt>**SPLDS_SPOOLER_KEY**</dt> </dl> | Reservado. Usado somente pelo spooler de impressão para armazenar propriedades internas do spooler.<br/>       |
| <span id="SPLDS_USER_KEY"></span><span id="splds_user_key"></span><dl> <dt>**SPLDS_USER_KEY**</dt> </dl>          | Os aplicativos usam essa chave para armazenar propriedades de impressora, como números de ativos de impressora.<br/> |



 

Os valores armazenados na chave de SPLDS_USER_KEY serão publicados no serviço de diretório somente se houver uma propriedade correspondente no esquema. Um administrador de domínio deve criar a propriedade se ela ainda não existir. Para publicar uma propriedade definida pelo usuário depois de usar **SetPrinterDataEx** para adicionar ou alterar um valor, chame [**setprinter**](setprinter.md) com *Level* = 7 e com o membro **dwAction** de [**PRINTER_INFO_7**](printer-info-7.md) definido como **DSPRINT_UPDATE**.

Você pode especificar outras chaves para armazenar dados de configuração não DS. Use o caractere de barra invertida ( \\ ) como um delimitador para especificar um caminho que tenha uma ou mais subchaves.

Se *hPrinter* for um identificador para uma impressora e *pKeyName* for **nulo** ou uma cadeia de caracteres vazia, **SetPrinterDataEx** retornará **ERROR_INVALID_PARAMETER**.

Se *hPrinter* for um identificador para um servidor de impressão, *pKeyName* será ignorado.

Não use **SPLDS_SPOOLER_KEY**. Para alterar as propriedades da impressora do spooler, use [**Setprinter**](setprinter.md) com o *nível* = 2.

</dd> <dt>

*valores principais* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que identifica os dados a serem definidos.

Para impressoras, essa cadeia de caracteres especifica o nome de um valor na chave *pKeyName* .

Para servidores de impressão, essa cadeia é uma das cadeias de caracteres predefinidas listadas na seção comentários a seguir.

</dd> <dt>

*Tipo* \[ de no\]
</dt> <dd>

Um código que indica o tipo de dados apontado pelo parâmetro *pData* . Para obter uma lista dos possíveis códigos de tipo, consulte [tipos de valor do registro](/windows/desktop/SysInfo/registry-value-types).

Se *pKeyName* especificar uma das chaves de serviço de diretório predefinidas, o *tipo* deverá ser **REG_SZ**, **REG_MULTI_SZ**, **REG_DWORD** ou **REG_BINARY**. Se **REG_BINARY** for usado, *cbData* deverá ser igual a 1 e o serviço de diretório tratará os dados como um valor booliano.

</dd> <dt>

*pData* \[ no\]
</dt> <dd>

Um ponteiro para um buffer que contém os dados de configuração da impressora.

</dd> <dt>

*cbData* \[ no\]
</dt> <dd>

O tamanho, em bytes, da matriz.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será **ERROR_SUCCESS**.

Se a função falhar, o valor de retorno será um valor de erro.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Para recuperar dados de configuração existentes para uma impressora ou spooler de impressão, chame a função [**GetPrinterDataEx**](getprinterdataex.md) .

Chamar **SetPrinterDataEx** com o parâmetro *pKeyName* definido como "PrinterDriverData" é equivalente a chamar a função [**SetPrinterData**](setprinterdata.md) .

Se *hPrinter* for um identificador para um *servidor de impressão, o* especifiquename poderá especificar um dos valores predefinidos a seguir.



| Valor                                                               | Comentários                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG_ALLOW_USER_MANAGEFORMS**                                | Windows XP com Service Pack 2 (SP2) e posterior<br/> Windows Server 2003 com Service Pack 1 (SP1) e posterior<br/>                                                                                                    |
| **SPLREG_BEEP_ENABLED**                                           |                                                                                                                                                                                                                                 |
| **SPLREG_DEFAULT_SPOOL_DIRECTORY**                               |                                                                                                                                                                                                                                 |
| **SPLREG_EVENT_LOG**                                              |                                                                                                                                                                                                                                 |
| **SPLREG_NET_POPUP**                                              | Sem suporte no Windows Server 2003 e posterior<br/>                                                                                                                                                                       |
| **SPLREG_PORT_THREAD_PRIORITY_DEFAULT**                         |                                                                                                                                                                                                                                 |
| **SPLREG_PORT_THREAD_PRIORITY**                                  |                                                                                                                                                                                                                                 |
| **SPLREG_PRINT_DRIVER_ISOLATION_GROUPS**                        | Windows 7 e posterior<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_TIME_BEFORE_RECYCLE**         | Windows 7 e posterior<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_MAX_OBJECTS_BEFORE_RECYCLE** | Windows 7 e posterior<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_IDLE_TIMEOUT**                 | Windows 7 e posterior<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_EXECUTION_POLICY**             | Windows 7 e posterior<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_OVERRIDE_POLICY**              | Windows 7 e posterior<br/>                                                                                                                                                                                                  |
| **SPLREG_RETRY_POPUP**                                            | Após o retorno bem-sucedido, o *pData* conterá 1 se o servidor estiver definido para repetir janelas pop-up para todos os trabalhos ou 0 se o servidor não tentar novamente janelas pop-up para todos os trabalhos.<br/> Sem suporte no Windows Server 2003 e posterior<br/> |
| **SPLREG_SCHEDULER_THREAD_PRIORITY**                             |                                                                                                                                                                                                                                 |
| **SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT**                    |                                                                                                                                                                                                                                 |
| **SPLREG_WEBSHAREMGMT**                                            | Windows Server 2003 e posterior<br/>                                                                                                                                                                                        |



 

A passagem de um dos valores predefinidos a *seguir, como o valor de* valueName, define o comportamento de impressão do pool quando ocorre um erro.



| Valor                                       | Comentários                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG_RESTART_JOB_ON_POOL_ERROR**   | O valor de *pData* indica o tempo, em segundos, quando um trabalho é reiniciado em outra porta após a ocorrência de um erro. Essa configuração é usada com **SPLREG_RESTART_JOB_ON_POOL_ENABLED**.<br/> |
| **SPLREG_RESTART_JOB_ON_POOL_ENABLED** | Um valor diferente de zero em *pData* indica que **SPLREG_RESTART_JOB_ON_POOL_ERROR** está habilitado.<br/>                                                                                            |



 

O tempo especificado em **SPLREG_RESTART_JOB_ON_POOL_ERROR** é um tempo mínimo. O tempo real pode ser maior, dependendo das seguintes configurações do monitor de porta, que são valores de registro nessa chave do registro:

**HKLM \\ sistema \\ CurrentControlSet \\ controle \\ Imprimir \\ monitores \\ <  > \\ portas monitor**

Chame a função [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) para definir esses valores.



| Configuração do monitor de porta     | Tipo de dados      | Significado                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **StatusUpdateEnabled**  | **REG_DWORD** | Se um valor diferente de zero, permite que o monitor de porta atualize o spooler com o status da porta.<br/>            |
| **StatusUpdateInterval** | **REG_DWORD** | Especifica o intervalo, em minutos, quando o monitor de porta atualiza o spooler com o status da porta.<br/> |



 

Para garantir que o spooler redirecione trabalhos para a próxima impressora disponível no pool (quando o trabalho de impressão não é impresso dentro do tempo definido), o monitor de porta deve dar suporte a SNMP e as portas de rede no pool devem ser configuradas como "status SNMP habilitado". O monitor de porta que dá suporte a SNMP é o monitor de porta TCP/IP padrão.

No Windows 7 e versões posteriores do Windows, os trabalhos de impressão enviados a um servidor de impressão são renderizados no cliente por padrão. O processamento do lado do cliente de trabalhos de impressão pode ser configurado definindo *pKeyName* como "PrinterDriverData" e *valores* de configuração na tabela a seguir.



| Configuração                      | Tipo de dados      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **REG_DWORD** | Um valor de 0, ou se esse valor não estiver presente no registro, habilitará a renderização padrão do lado do cliente de trabalhos de impressão.<br/> Um valor de 1 desabilita a renderização do lado do cliente de trabalhos de impressão.<br/>                                                                                                                                                                                                          |
| **ForceClientSideRendering** | **REG_DWORD** | Um valor de 0 ou, se esse valor não estiver presente no registro, fará com que os trabalhos de impressão sejam renderizados no cliente. Se um trabalho de impressão não puder ser processado no cliente, ele será renderizado no servidor. Se não for possível renderizar um trabalho de impressão no servidor, ele falhará.<br/> Um valor de 1 processará trabalhos de impressão no cliente. Se não for possível renderizar um trabalho de impressão no cliente, ele falhará.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **SetPrinterDataExW** (Unicode) e **SetPrinterDataExA** (ANSI)<br/>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> <dt>

[**PRINTER_INFO_7**](printer-info-7.md)
</dt> </dl>

 

