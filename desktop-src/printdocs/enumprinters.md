---
description: A função EnumPrinters enumera impressoras, servidores de impressão, domínios ou provedores de impressão disponíveis.
ms.assetid: 0d0cc726-c515-4146-9273-cdf1db3c76b7
title: Função EnumPrinters (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinters
- EnumPrintersA
- EnumPrintersW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: fb88cef081010f1319fb194904933ba2366d6593f0d2517c696bb6d6490ace20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119353836"
---
# <a name="enumprinters-function"></a>Função EnumPrinters

A **função EnumPrinters** enumera impressoras, servidores de impressão, domínios ou provedores de impressão disponíveis.

## <a name="syntax"></a>Sintaxe


```C++
BOOL EnumPrinters(
  _In_  DWORD   Flags,
  _In_  LPTSTR  Name,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinterEnum,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Sinalizadores* \[ Em\]
</dt> <dd>

Os tipos de objetos de impressão que a função deve enumerar. Esse valor pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_ENUM_LOCAL"></span><span id="printer_enum_local"></span><dl> <dt>**PRINTER \_ ENUM \_ LOCAL**</dt> </dl>                       | Se o sinalizador PRINTER ENUM NAME também não for passado, a função ignorará o parâmetro Name e enumera as \_ \_ impressoras instaladas localmente.  Se PRINTER \_ ENUM \_ NAME também for passado, a função enumera as impressoras locais em *Nome*. <br/> |
| <span id="PRINTER_ENUM_NAME"></span><span id="printer_enum_name"></span><dl> <dt>**NOME \_ DE ENUM DA \_ IMPRESSORA**</dt> </dl>                          | A função enumera a impressora identificada pelo *Nome*. Pode ser um servidor, um domínio ou um provedor de impressão. Se *Name* for **NULL**, a função enumera os provedores de impressão disponíveis.<br/>                                                    |
| <span id="PRINTER_ENUM_SHARED"></span><span id="printer_enum_shared"></span><dl> <dt>**PRINTER \_ ENUM \_ SHARED**</dt> </dl>                    | A função enumera impressoras que têm o atributo compartilhado. Não pode ser usado isoladamente; use uma operação OR para combinar com outro tipo \_ PRINTER ENUM.<br/>                                                                               |
| <span id="PRINTER_ENUM_CONNECTIONS"></span><span id="printer_enum_connections"></span><dl> <dt>**CONEXÕES \_ ENUM DA \_ IMPRESSORA**</dt> </dl>     | A função enumera a lista de impressoras às quais o usuário fez conexões anteriores.<br/>                                                                                                                                               |
| <span id="PRINTER_ENUM_NETWORK"></span><span id="printer_enum_network"></span><dl> <dt>**REDE \_ ENUM \_ DA IMPRESSORA**</dt> </dl>                 | A função enumera impressoras de rede no domínio do computador. Esse valor só será válido se *Level* for 1.<br/>                                                                                                                                |
| <span id="PRINTER_ENUM_REMOTE"></span><span id="printer_enum_remote"></span><dl> <dt>**PRINTER \_ ENUM \_ REMOTE**</dt> </dl>                    | A função enumera impressoras de rede e servidores de impressão no domínio do computador. Esse valor só será válido se *Level* for 1.<br/>                                                                                                              |
| <span id="PRINTER_ENUM_CATEGORY_3D"></span><span id="printer_enum_category_3d"></span><dl> <dt>**CATEGORIA \_ DE ENUM \_ DA IMPRESSORA \_ 3D**</dt> </dl>    | A função enumera apenas impressoras 3D.<br/>                                                                                                                                                                                                   |
| <span id="PRINTER_ENUM_CATEGORY_ALL"></span><span id="printer_enum_category_all"></span><dl> <dt>**PRINTER \_ ENUM \_ CATEGORY \_ ALL**</dt> </dl> | A função enumera todos os dispositivos de impressão, incluindo impressoras 3D.<br/>                                                                                                                                                                           |



 

Se *Level* for 4, você só poderá usar as constantes PRINTER ENUM CONNECTIONS e \_ PRINTER \_ \_ ENUM \_ LOCAL.

> [!Note]  
> Dispositivos de impressão 3D não são enumerados por padrão. Você deve incluir **PRINTER \_ ENUM \_ CATEGORY \_ 3D** e **PRINTER \_ ENUM \_ LOCAL** para enumerar apenas impressoras 3D. Para incluir impressoras 3D, juntamente com todas as outras impressoras locais, use **PRINTER \_ ENUM \_ CATEGORY \_ ALL** e **PRINTER \_ ENUM \_ LOCAL.**

 

</dd> <dt>

*Nome* \[ Em\]
</dt> <dd>

Se *Level* for 1, Flags contiver PRINTER ENUM NAME e Name for não NULL, Name será um ponteiro para uma cadeia de *caracteres* terminada em nulo que especifica o nome do objeto \_ a ser \_ enumerado.    Essa cadeia de caracteres pode ser o nome de um servidor, um domínio ou um provedor de impressão.

Se *Level* for 1, *Flags* contiver PRINTER ENUM NAME e Name for NULL, a função enumera os \_ \_ provedores de impressão  disponíveis. 

Se *Level* for 1, *Flags* contiver PRINTER \_ ENUM REMOTE e \_ *Name* for **NULL,** a função enumera as impressoras no domínio do usuário.

Se *Level* for 2 ou 5,*Name* será um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome de um servidor cujas impressoras devem ser enumeradas. Se essa cadeia de caracteres **for NULL,** a função enumera as impressoras instaladas no computador local.

Se *Level* for 4, *Name* deverá ser **NULL.** A função sempre consulta no computador local.

Quando *Nome* é **NULL,** a definição *de Sinalizadores* como PRINTER \_ ENUM LOCAL PRINTER \_ \| \_ ENUM \_ ENUM CONNECTIONS enumera impressoras instaladas no computador local. Essas impressoras incluem aquelas que estão fisicamente anexadas ao computador local, bem como impressoras remotas às quais ele tem uma conexão de rede.

Quando *Name* não for **NULL,** definir *Sinalizadores* como PRINTER ENUM LOCAL PRINTER ENUM NAME enumera as impressoras locais instaladas no \_ nome do \_ \| \_ \_ *servidor.*

</dd> <dt>

*Nível* \[ Em\]
</dt> <dd>

O tipo de estruturas de dados apontadas *por pPrinterEnum*. Os valores válidos são 1, 2, 4 e 5, que correspondem às estruturas de dados [**PRINTER \_ INFO \_ 1,**](printer-info-1.md) [**PRINTER INFO \_ \_ 2,**](printer-info-2.md) [**PRINTER INFO \_ \_ 4**](printer-info-4.md)e [**PRINTER INFO \_ \_ 5.**](printer-info-5.md)

Esse valor pode ser 1, 2, 4 ou 5.

</dd> <dt>

*pPrinterEnum* \[ out\]
</dt> <dd>

Um ponteiro para um buffer que recebe uma matriz de estruturas [**PRINTER \_ INFO \_ 1,**](printer-info-1.md) [**PRINTER INFO \_ \_ 2,**](printer-info-2.md) [**PRINTER INFO \_ \_ 4**](printer-info-4.md)ou [**PRINTER INFO \_ \_ 5.**](printer-info-5.md) Cada estrutura contém dados que descrevem um objeto de impressão disponível.

Se *Level* for 1, a matriz conterá estruturas [**PRINTER INFO \_ \_ 1.**](printer-info-1.md) Se *Level* for 2, a matriz conterá estruturas [**PRINTER INFO \_ \_ 2.**](printer-info-2.md) Se *Level* for 4, a matriz conterá estruturas [**PRINTER INFO \_ \_ 4.**](printer-info-4.md) Se *Level* for 5, a matriz conterá estruturas [**PRINTER INFO \_ \_ 5.**](printer-info-5.md)

O buffer deve ser grande o suficiente para receber a matriz de estruturas de dados e quaisquer cadeias de caracteres ou outros dados para os quais os membros da estrutura apontam. Se o buffer for muito pequeno, o *parâmetro pcbNeeded* retornará o tamanho do buffer necessário.

</dd> <dt>

*cbBuf* \[ Em\]
</dt> <dd>

O tamanho, em bytes, do buffer apontado por *pPrinterEnum.*

</dd> <dt>

*pcbNeeded* \[ out\]
</dt> <dd>

Um ponteiro para um valor que recebe o número de bytes copiados se a função for bem-sucedida ou o número de bytes necessários se *cbBuf* for muito pequeno.

</dd> <dt>

*pcReturned* \[ out\]
</dt> <dd>

Um ponteiro para um valor que recebe o número de estruturas [**PRINTER \_ INFO \_ 1**](printer-info-1.md), [**PRINTER INFO \_ \_ 2,**](printer-info-2.md) [**PRINTER INFO \_ \_ 4**](printer-info-4.md)ou [**PRINTER INFO \_ \_ 5**](printer-info-5.md) que a função retorna na matriz à qual *pPrinterEnum* aponta.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um valor não zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

Não chame esse método em [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração do servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Se **EnumPrinters retornar** uma estrutura [**PRINTER INFO \_ \_ 1**](printer-info-1.md) na qual PRINTER ENUM CONTAINER for especificado, isso indicará que há uma hierarquia de objetos \_ de \_ impressora. Um aplicativo pode enumerar a hierarquia chamando **EnumPrinters** novamente, definindo Nome como o valor do membro **pName** da estrutura **PRINTER INFO \_ \_ 1.** 

A **função EnumPrinters** não recupera informações de segurança. Se [**as estruturas PRINTER \_ INFO \_ 2**](printer-info-2.md) são retornadas na matriz apontada por *pPrinterEnum*, seus *membros pSecurityDescriptor* serão definidos como **NULL.**

Para obter informações sobre a impressora padrão, chame [**GetDefaultPrinter**](getdefaultprinter.md).

A estrutura [**PRINTER \_ INFO \_ 4**](printer-info-4.md) fornece uma maneira fácil e extremamente rápida de recuperar os nomes das impressoras instaladas em um computador local, bem como as conexões remotas que um usuário estabeleceu. Quando **EnumPrinters** é chamado com uma estrutura de dados **PRINTER INFO \_ \_ 4,** essa função consulta o Registro para obter as informações especificadas e retorna imediatamente. Isso difere do comportamento de **EnumPrinters** quando chamado com outros níveis de **INFORMAÇÕES DE IMPRESSORA _ \_ \_ \* *estruturas de dados. Em particular, quando _* EnumPrinters** é chamado com uma estrutura de dados nível 2 ([**PRINTER INFO \_ \_ 2**](printer-info-2.md)), ele executa uma chamada [**openPrinter**](openprinter.md) em cada conexão remota. Se uma conexão remota estiver inocedenciada ou o servidor remoto não existir mais ou a impressora remota não existir mais, a função deverá aguardar o RPC passar do tempo e, consequentemente, falhar na **chamada do OpenPrinter.** Isso pode levar algum tempo. Passar uma estrutura **PRINTER \_ INFO \_ 4** permite que um aplicativo recupere um mínimo de informações necessárias; se informações mais detalhadas são desejadas, uma chamada subsequente de **EnumPrinters** nível 2 pode ser feita.

**Windows Vista:** Os dados da impressora retornados **por EnumPrinters** são recuperados de um cache local quando o valor *de Level* é 4.

A tabela a seguir mostra a **saída EnumPrinters** para vários *valores flags* quando o *parâmetro Level* é definido como 1.

Na coluna *parâmetro Name* da tabela, você deve substituir um nome apropriado para Provedor de Impressão, Domínio e Computador. Por exemplo, para "Provedor de Impressão", você pode usar o nome do provedor de impressão de rede ou o nome do provedor de impressão local. Para recuperar nomes de provedor de impressão, **chame EnumPrinters** com *Nome* definido como **NULL.**



| *Parâmetro Flags*                                  | *Parâmetro name*                            | Resultado                                                                                            |
|----------------------------------------------------|---------------------------------------------|---------------------------------------------------------------------------------------------------|
| PRINTER \_ ENUM \_ LOCAL (e não PRINTER \_ ENUM \_ NAME) | O *parâmetro* Name é ignorado.<br/> | Todas as impressoras locais.<br/>                                                                    |
| NOME \_ DE ENUM DA \_ IMPRESSORA                                | "Provedor de Impressão"<br/>                 | Todos os nomes de domínio<br/>                                                                       |
| NOME \_ DE ENUM DA \_ IMPRESSORA                                | "Provedor de Impressão! Domínio"<br/>          | Todas as impressoras e servidores de impressão no domínio do computador<br/>                                |
| NOME \_ DE ENUM DA \_ IMPRESSORA                                | "Provedor de Impressão!! \\ \\ Computador"<br/>    | Todas as impressoras compartilhadas no \\ \\ computador<br/>                                                     |
| NOME \_ DE ENUM DA \_ IMPRESSORA                                | Uma cadeia de caracteres vazia, ""<br/>              | Todas as impressoras locais.<br/>                                                                    |
| NOME \_ DE ENUM DA \_ IMPRESSORA                                | **NULL**<br/>                         | Todos os provedores de impressão no domínio do computador<br/>                                           |
| CONEXÕES \_ ENUM DA \_ IMPRESSORA                         | O *parâmetro* Name é ignorado.<br/> | Todas as impressoras remotas conectadas<br/>                                                          |
| REDE \_ ENUM \_ DA IMPRESSORA                             | O *parâmetro* Name é ignorado.<br/> | Todas as impressoras no domínio do computador<br/>                                                  |
| PRINTER \_ ENUM \_ REMOTE                              | Uma cadeia de caracteres vazia, ""<br/>              | Todas as impressoras e servidores de impressão no domínio do computador<br/>                                |
| PRINTER \_ ENUM \_ REMOTE                              | "Provedor de Impressão"<br/>                 | O mesmo que O NOME \_ ENUM DA \_ IMPRESSORA<br/>                                                            |
| PRINTER \_ ENUM \_ REMOTE                              | "Provedor de Impressão! Domínio"<br/>          | Todas as impressoras e servidores de impressão no domínio do computador, independentemente *do domínio* especificado.<br/> |
| CATEGORIA \_ DE ENUM \_ DA IMPRESSORA \_ 3D                        | O *parâmetro* Name é ignorado.<br/> | Somente impressoras 3D são enumeradas.<br/>                                                       |
| PRINTER \_ ENUM \_ CATEGORY \_ ALL                       | O *parâmetro* Name é ignorado.<br/> | Impressoras 3D são enumeradas, juntamente com todas as outras impressoras.<br/>                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **EnumPrintersW** (Unicode) **e EnumPrintersA** (ANSI)<br/>                                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA \_ IMPRESSORA 1**](printer-info-1.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA IMPRESSORA \_ 2**](printer-info-2.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA IMPRESSORA \_ 4**](printer-info-4.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA IMPRESSORA \_ 5**](printer-info-5.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

