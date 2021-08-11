---
description: A função SetPrinterData define os dados de configuração para um servidor de impressão ou impressora.
ms.assetid: 16072de9-98fb-4ada-8216-180b64cf44c8
title: Função SetPrinterData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterData
- SetPrinterDataA
- SetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 7b28c61030271b9de2e946fd59cddf5253a80cd4faec40ee66ceb2ae6cefdce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118233945"
---
# <a name="setprinterdata-function"></a>Função SetPrinterData

A função **SetPrinterData** define os dados de configuração para um servidor de impressão ou impressora.

Para especificar a chave do registro sob a qual armazenar os dados, chame a função [**SetPrinterDataEx**](setprinterdataex.md) . Chamar **SetPrinterData** é equivalente a chamar a função **SetPrinterDataEx** com o parâmetro *pKeyName* definido como "PrinterDriverData".

## <a name="syntax"></a>Sintaxe


```C++
DWORD SetPrinterData(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pValueName,
  _In_ DWORD  Type,
  _In_ LPBYTE pData,
  _In_ DWORD  cbData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para a impressora ou o servidor de impressão para o qual a função define os dados de configuração. Use a função [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)ou [**AddPrinter**](addprinter.md) para recuperar um identificador de impressora.

</dd> <dt>

*valores principais* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que identifica os dados a serem definidos.

Para impressoras, essa cadeia de caracteres é o nome de um valor de registro na chave "PrinterDriverData" da impressora no registro.

Para servidores de impressão, essa cadeia é uma das cadeias de caracteres predefinidas listadas na seção comentários a seguir.

</dd> <dt>

*Tipo* \[ de no\]
</dt> <dd>

Um código que indica o tipo de dados para o qual o parâmetro *pData* aponta. Para obter uma lista dos possíveis códigos de tipo, consulte [tipos de valor do registro](/windows/desktop/SysInfo/registry-value-types).

</dd> <dt>

*pData* \[ no\]
</dt> <dd>

Um ponteiro para uma matriz de bytes que contém os dados de configuração da impressora.

</dd> <dt>

*cbData* \[ no\]
</dt> <dd>

O tamanho, em bytes, da matriz.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno **será \_ êxito no erro**.

Se a função falhar, o valor de retorno será um valor de erro.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Para recuperar os dados de configuração existentes de uma impressora, chame a função [**GetPrinterDataEx**](getprinterdataex.md) ou [**GetPrinterData**](getprinterdata.md) .

Se *hPrinter* for um identificador para um *servidor de impressão, o* especifiquename poderá especificar um dos valores predefinidos a seguir.



| Valor                                                               | Comentários                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG \_ permitir que o \_ usuário \_ MANAGEFORMS**                                | Windows XP com Service Pack 2 (SP2) e posterior<br/> Windows Server 2003 com Service Pack 1 (SP1) e posterior<br/>                                                                                                    |
| **aviso de SPLREG \_ \_ habilitado**                                           |                                                                                                                                                                                                                                 |
| **SPLREG \_ o \_ diretório de spool padrão \_**                               |                                                                                                                                                                                                                                 |
| **\_log de eventos do SPLREG \_**                                              |                                                                                                                                                                                                                                 |
| **\_ \_ pop-up do SPLREG net**                                              | sem suporte no Windows Server 2003 e posterior<br/>                                                                                                                                                                       |
| **\_padrão de \_ prioridade de thread de porta SPLREG \_ \_**                         |                                                                                                                                                                                                                                 |
| **\_prioridade de \_ thread de porta SPLREG \_**                                  |                                                                                                                                                                                                                                 |
| **\_grupos de \_ isolamento do driver de impressão SPLREG \_ \_**                        | Windows 7 e posterior<br/>                                                                                                                                                                                                  |
| **\_tempo de isolamento do driver de impressão SPLREG \_ antes da \_ \_ \_ \_ reciclagem**         | Windows 7 e posterior<br/>                                                                                                                                                                                                  |
| **\_isolamento do driver de impressão SPLREG máximo de \_ \_ \_ \_ objetos antes da \_ \_ reciclagem** | Windows 7 e posterior<br/>                                                                                                                                                                                                  |
| **\_ \_ \_ \_ tempo limite de ociosidade do isolamento do driver de impressão SPLREG \_**                 | Windows 7 e posterior<br/>                                                                                                                                                                                                  |
| **\_política de \_ execução de isolamento do driver de impressão SPLREG \_ \_ \_**             | Windows 7 e posterior<br/>                                                                                                                                                                                                  |
| **\_política de \_ substituição de isolamento do driver de impressão SPLREG \_ \_ \_**              | Windows 7 e posterior<br/>                                                                                                                                                                                                  |
| **\_ \_ pop-up de repetição do SPLREG**                                            | Após o retorno bem-sucedido, o *pData* conterá 1 se o servidor estiver definido para repetir janelas pop-up para todos os trabalhos ou 0 se o servidor não tentar novamente janelas pop-up para todos os trabalhos.<br/> sem suporte no Windows Server 2003 e posterior<br/> |
| **\_prioridade de thread do Agendador SPLREG \_ \_**                             |                                                                                                                                                                                                                                 |
| **\_padrão de prioridade de thread do Agendador SPLREG \_ \_ \_**                    |                                                                                                                                                                                                                                 |
| **SPLREG \_ WEBSHAREMGMT**                                            | Windows Server 2003 e posterior<br/>                                                                                                                                                                                        |



 

Os valores a seguir de valueName determinam o *comportamento de impressão* do pool quando ocorre um erro.



| Valor                                       | Comentários                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_erro de reinicialização \_ de SPLREG \_ no \_ pool \_**   | O valor de *pData* indica o tempo, em segundos, quando um trabalho é reiniciado em outra porta após a ocorrência de um erro. Essa configuração é usada com **o \_ trabalho de reinicialização SPLREG \_ \_ no \_ pool \_ habilitado**.<br/> |
| **\_trabalho de reinicialização \_ de SPLREG \_ no \_ pool \_ habilitado** | Um valor diferente de zero em *pData* indica que o **\_ erro SPLREG reiniciar o \_ trabalho \_ no \_ pool \_** está habilitado.<br/>                                                                                            |



 

O tempo especificado em **SPLREG \_ reiniciar o \_ trabalho \_ no \_ pool \_** é um tempo mínimo. O tempo real pode ser maior, dependendo das seguintes configurações do monitor de porta, que são valores de registro nessa chave do registro:

**HKLM \\ sistema \\ CurrentControlSet \\ controle \\ Imprimir \\ monitores \\ <  > \\ portas monitor**

Chame a função [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) para definir esses valores.



| Configuração do monitor de porta     | Tipo de dados      | Significado                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **StatusUpdateEnabled**  | **REG \_ DWORD** | Se um valor diferente de zero, permite que o monitor de porta atualize o spooler com o status da porta.<br/>            |
| **StatusUpdateInterval** | **REG \_ DWORD** | Especifica o intervalo, em minutos, quando o monitor de porta atualiza o spooler com o status da porta.<br/> |



 

no Windows 7 e versões posteriores do Windows, os trabalhos de impressão enviados a um servidor de impressão são renderizados no cliente por padrão. A renderização do lado do cliente de trabalhos de impressão pode ser configurada para cada impressora definindo os valores a *seguir em valores* de valor.



| Configuração                      | Tipo de dados      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **REG \_ DWORD** | Um valor de 0, ou se esse valor não estiver presente no registro, habilitará a renderização padrão do lado do cliente de trabalhos de impressão.<br/> Um valor de 1 desabilita a renderização do lado do cliente de trabalhos de impressão.<br/>                                                                                                                                                                                                      |
| **ForceClientSideRendering** | **REG \_ DWORD** | Um valor de 0 ou, se esse valor não estiver presente no registro, fará com que os trabalhos de impressão sejam renderizados no cliente. Se um trabalho de impressão não puder ser processado no cliente, ele será renderizado no servidor. Se não for possível renderizar um trabalho de impressão no servidor, ele falhará.<br/> Um valor de 1 processará trabalhos de impressão no cliente. Se não for possível renderizar um trabalho de impressão no cliente, ele falhará.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **SetPrinterDataW** (Unicode) e **SetPrinterDataA** (ANSI)<br/>                                   |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Getprinter**](getprinter.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

