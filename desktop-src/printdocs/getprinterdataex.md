---
description: A função GetPrinterDataEx recupera dados de configuração para a impressora ou o servidor de impressão especificado.
ms.assetid: 5d9183a7-97cc-46de-848e-e37ce51396eb
title: Função GetPrinterDataEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDataEx
- GetPrinterDataExA
- GetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 146c4f650b646e5b2be9e0ec809221beebe9f596fcb591fe148be615417faa04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034174"
---
# <a name="getprinterdataex-function"></a>Função GetPrinterDataEx

A função **GetPrinterDataEx** recupera dados de configuração para a impressora ou o servidor de impressão especificado. **GetPrinterDataEx** pode recuperar valores armazenados pela função [**SetPrinterData**](setprinterdata.md) . Além disso, o **GetPrinterDataEx** pode recuperar valores que a função [**SetPrinterDataEx**](setprinterdataex.md) armazenada sob uma chave especificada.

## <a name="syntax"></a>Sintaxe


```C++
DWORD GetPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _In_  LPCTSTR pValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   nSize,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para a impressora ou o servidor de impressão para o qual a função recupera dados de configuração. Use a função [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)ou [**AddPrinter**](addprinter.md) para recuperar um identificador de impressora.

</dd> <dt>

*pKeyName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a chave que contém o valor a ser recuperado. Use o caractere de barra invertida ( \\ ) como um delimitador para especificar um caminho que tenha uma ou mais subchaves.

Se *hPrinter* for um identificador para uma impressora e *pKeyName* for **nulo** ou uma cadeia de caracteres vazia, **GetPrinterDataEx** retornará um **\_ \_ parâmetro inválido de erro**.

Se *hPrinter* for um identificador para um servidor de impressão, *pKeyName* será ignorado.

</dd> <dt>

*valores principais* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que identifica os dados a serem recuperados.

Para impressoras, essa cadeia de caracteres especifica o nome de um valor na chave *pKeyName* .

Para servidores de impressão, essa cadeia é uma das cadeias de caracteres predefinidas listadas na seção comentários a seguir.

</dd> <dt>

*pType* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o tipo de dados armazenados no valor. A função retorna o tipo especificado na chamada [**SetPrinterDataEx**](setprinterdataex.md) quando os dados foram armazenados. Esse parâmetro poderá ser **nulo** se você não precisar das informações. **GetPrinterDataEx** passa *pType* como o parâmetro *lpdwType* de uma chamada de função [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) .

</dd> <dt>

*pData* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe os dados de configuração.

</dd> <dt>

*nSize* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer apontado por *pData*.

</dd> <dt>

*pcbNeeded* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados de configuração. Se o tamanho do buffer especificado por *nSize* for muito pequeno, a função retornará um **erro com \_ mais \_ dados** e *pcbNeeded* indicará o tamanho do buffer necessário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno **será \_ êxito no erro**.

Se a função falhar, o valor de retorno será um valor de erro.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

**GetPrinterDataEx** recupera os dados de configuração de impressora que foram definidos pelas funções [**SetPrinterDataEx**](setprinterdataex.md) e [**SetPrinterData**](setprinterdata.md) .

Chamar **GetPrinterDataEx** com o parâmetro *pKeyName* definido como "PrinterDriverData" é equivalente a chamar a função [**GetPrinterData**](getprinterdata.md) .

Se *hPrinter* for um identificador para um *servidor de impressão, o* especifiquename poderá especificar um dos valores predefinidos a seguir.



| Valor                                                               | Comentários                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG \_ permitir que o \_ usuário \_ MANAGEFORMS**                                | Windows XP com Service Pack 2 (SP2) e posterior<br/> Windows Server 2003 com Service Pack 1 (SP1) e posterior<br/>                                                                                                    |
| **arquitetura do SPLREG \_**                                            |                                                                                                                                                                                                                                 |
| **aviso de SPLREG \_ \_ habilitado**                                           |                                                                                                                                                                                                                                 |
| **SPLREG \_ o \_ diretório de spool padrão \_**                               |                                                                                                                                                                                                                                 |
| **SPLREG \_ \_ nome do computador DNS \_**                                      |                                                                                                                                                                                                                                 |
| **SPLREG \_ DS \_ presente**                                             | Após o retorno bem-sucedido, *pData* conterá 0x0001 se o computador estiver em um domínio DS; caso contrário, 0.<br/>                                                                                                                         |
| **SPLREG \_ DS \_ presente \_ para o \_ usuário**                                  | Após o retorno bem-sucedido, o *pData* conterá 0x0001 se o usuário estiver conectado a um domínio DS; caso contrário, 0.<br/>                                                                                                                   |
| **\_log de eventos do SPLREG \_**                                              |                                                                                                                                                                                                                                 |
| **\_versão principal do SPLREG \_**                                          |                                                                                                                                                                                                                                 |
| **SPLREG \_ \_ versão secundária**                                          |                                                                                                                                                                                                                                 |
| **\_ \_ pop-up do SPLREG net**                                              | sem suporte no Windows Server 2003 e posterior<br/>                                                                                                                                                                       |
| **\_ \_ pop-up do SPLREG net para o \_ \_ computador**                                | Após o retorno bem-sucedido, o *pData* conterá 1 se as notificações de trabalho devem ser enviadas para o computador cliente ou 0 se as notificações de trabalho forem enviadas ao usuário.<br/> sem suporte no Windows Server 2003 e posterior<br/> |
| **\_versão do so SPLREG \_**                                             | Windows XP e posterior<br/>                                                                                                                                                                                                 |
| **SPLREG \_ os \_ VERSIONEX**                                           |                                                                                                                                                                                                                                 |
| **\_padrão de \_ prioridade de thread de porta SPLREG \_ \_**                         |                                                                                                                                                                                                                                 |
| **\_prioridade de \_ thread de porta SPLREG \_**                                  |                                                                                                                                                                                                                                 |
| **\_grupos de \_ isolamento do driver de impressão SPLREG \_ \_**                        | Windows 7 e posterior<br/>                                                                                                                                                                                                  |
| **\_tempo de isolamento do driver de impressão SPLREG \_ antes da \_ \_ \_ \_ reciclagem**         | Windows 7 e posterior<br/>                                                                                                                                                                                                  |
| **\_isolamento do driver de impressão SPLREG máximo de \_ \_ \_ \_ objetos antes da \_ \_ reciclagem** | Windows 7 e posterior<br/>                                                                                                                                                                                                  |
| **\_ \_ \_ \_ tempo limite de ociosidade do isolamento do driver de impressão SPLREG \_**                 | Windows 7 e posterior<br/>                                                                                                                                                                                                  |
| **\_política de \_ execução de isolamento do driver de impressão SPLREG \_ \_ \_**             | Windows 7 e posterior<br/>                                                                                                                                                                                                  |
| **\_política de \_ substituição de isolamento do driver de impressão SPLREG \_ \_ \_**              | Windows 7 e posterior<br/>                                                                                                                                                                                                  |
| **\_fax remoto do SPLREG \_**                                             | Após o retorno bem-sucedido, o *pData* conterá 0x0001 se o serviço de fax der suporte a clientes remotos. caso contrário, 0.<br/>                                                                                                               |
| **\_ \_ pop-up de repetição do SPLREG**                                            | Após o retorno bem-sucedido, o *pData* conterá 1 se o servidor estiver definido para repetir janelas pop-up para todos os trabalhos ou 0 se o servidor não tentar novamente janelas pop-up para todos os trabalhos.<br/> sem suporte no Windows Server 2003 e posterior<br/> |
| **\_prioridade de thread do Agendador SPLREG \_ \_**                             |                                                                                                                                                                                                                                 |
| **\_padrão de prioridade de thread do Agendador SPLREG \_ \_ \_**                    |                                                                                                                                                                                                                                 |
| **SPLREG \_ WEBSHAREMGMT**                                            | Windows Server 2003 e posterior<br/>                                                                                                                                                                                        |



 

Os valores a seguir de valueName indicam o *comportamento de impressão* do pool quando ocorre um erro.



| Valor                                       | Comentários                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_erro de reinicialização \_ de SPLREG \_ no \_ pool \_**   | O valor de *pData* indica o tempo, em segundos, quando um trabalho é reiniciado em outra porta após a ocorrência de um erro. Essa configuração é usada com **o \_ trabalho de reinicialização SPLREG \_ \_ no \_ pool \_ habilitado**.<br/> |
| **\_trabalho de reinicialização \_ de SPLREG \_ no \_ pool \_ habilitado** | Um valor diferente de zero em *pData* indica que o **\_ erro SPLREG reiniciar o \_ trabalho \_ no \_ pool \_** está habilitado.<br/>                                                                                            |



 

O tempo especificado em **SPLREG \_ reiniciar o \_ trabalho \_ no \_ pool \_** é um tempo mínimo. O tempo real pode ser maior, dependendo das seguintes configurações do monitor de porta, que são valores de registro nessa chave do registro:

**HKLM \\ sistema \\ CurrentControlSet \\ controle \\ Imprimir \\ monitores \\ <  > \\ portas monitor**

Chame a [**função RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) para consultar esses valores.



| Configuração do monitor de porta     | Tipo de dados      | Significado                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **StatusUpdateEnabled**  | **REG \_ DWORD** | Se um valor não zero, habilita o monitor de porta a atualizar o spooler com o status da porta.<br/>            |
| **StatusUpdateInterval** | **REG \_ DWORD** | Especifica o intervalo, em minutos, quando o monitor de porta atualiza o spooler com o status da porta.<br/> |



 

Se *pKeyName* for uma das chaves do DS (Serviço de Diretório) predefinida (consulte [**SetPrinter**](setprinter.md)) e *pValueName* contiver uma vírgula (','), a parte de *pValueName* antes da vírgula será o nome do valor e a parte de *pValueName* à direita da vírgula será o OID da propriedade DS. Uma sub-chave chamada OID é criada e um novo valor que consiste no nome do valor e OID é inserido sob a chave OID. [**SetPrinterDataEx**](setprinterdataex.md) também adiciona o nome do valor e os dados sob a chave DS.

No Windows 7 e versões posteriores do Windows, os trabalhos de impressão enviados a um servidor de impressão são renderizados no cliente por padrão. A configuração da renderização do lado do cliente para uma impressora pode ser lida definindo *pKeyName* como "PrinterDriverData" e *pValueName* como o valor de configuração na tabela a seguir.



| Configuração                      | Tipo de dados      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **REG \_ DWORD** | Um valor de 0 ou se esse valor não estiver presente no Registro, habilita a renderização padrão do lado do cliente de trabalhos de impressão.<br/> Um valor de 1 desabilita a renderização do lado do cliente de trabalhos de impressão.<br/>                                                                                                                                                                                                          |
| **ForceClientSideRendering** | **REG \_ DWORD** | Um valor de 0 ou se esse valor não estiver presente no Registro fará com que os trabalhos de impressão sejam renderizados no cliente. Se um trabalho de impressão não puder ser renderizado no cliente, ele será renderizado no servidor. Se um trabalho de impressão não puder ser renderizado no servidor, ele falhará.<br/> Um valor de 1 renderizará trabalhos de impressão no cliente. Se um trabalho de impressão não puder ser renderizado no cliente, ele falhará.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **GetPrinterDataExW** (Unicode) e **GetPrinterDataExA** (ANSI)<br/>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

