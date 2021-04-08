---
description: A função EnumPrinters enumera impressoras disponíveis, servidores de impressão, domínios ou provedores de impressão.
ms.assetid: 0d0cc726-c515-4146-9273-cdf1db3c76b7
title: Função EnumPrinters (winspool. h)
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
ms.openlocfilehash: 6d82e8e6ff4f56a3c67fa29c48e982ebe0fd4599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828315"
---
# <a name="enumprinters-function"></a>Função EnumPrinters

A função **EnumPrinters** enumera impressoras disponíveis, servidores de impressão, domínios ou provedores de impressão.

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

*Flags* \[in\]
</dt> <dd>

Os tipos de objetos de impressão que a função deve enumerar. Esse valor pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_ENUM_LOCAL"></span><span id="printer_enum_local"></span><dl> <dt>**\_local de enumeração de impressora \_**</dt> </dl>                       | Se o sinalizador de nome de enumeração da impressora \_ \_ também não for passado, a função ignora o parâmetro de *nome* e enumera as impressoras instaladas localmente. Se \_ \_ o nome de enumeração da impressora também for passado, a função enumerará as impressoras locais no *nome*. <br/> |
| <span id="PRINTER_ENUM_NAME"></span><span id="printer_enum_name"></span><dl> <dt>**\_nome da enumeração da impressora \_**</dt> </dl>                          | A função enumera a impressora identificada pelo *nome*. Pode ser um servidor, um domínio ou um provedor de impressão. Se *Name* for **NULL**, a função enumerará os provedores de impressão disponíveis.<br/>                                                    |
| <span id="PRINTER_ENUM_SHARED"></span><span id="printer_enum_shared"></span><dl> <dt>**ENUM de impressora \_ \_ compartilhado**</dt> </dl>                    | A função enumera impressoras que têm o atributo compartilhado. Não pode ser usado isoladamente; Use uma operação ou para combinar com outro tipo de enumeração de impressora \_ .<br/>                                                                               |
| <span id="PRINTER_ENUM_CONNECTIONS"></span><span id="printer_enum_connections"></span><dl> <dt>**\_conexões de enum de impressora \_**</dt> </dl>     | A função enumera a lista de impressoras para as quais o usuário fez conexões anteriores.<br/>                                                                                                                                               |
| <span id="PRINTER_ENUM_NETWORK"></span><span id="printer_enum_network"></span><dl> <dt>**\_rede de enumeração de impressora \_**</dt> </dl>                 | A função enumera impressoras de rede no domínio do computador. Esse valor será válido somente se o *nível* for 1.<br/>                                                                                                                                |
| <span id="PRINTER_ENUM_REMOTE"></span><span id="printer_enum_remote"></span><dl> <dt>**\_remoto de enumeração de impressora \_**</dt> </dl>                    | A função enumera impressoras de rede e servidores de impressão no domínio do computador. Esse valor será válido somente se o *nível* for 1.<br/>                                                                                                              |
| <span id="PRINTER_ENUM_CATEGORY_3D"></span><span id="printer_enum_category_3d"></span><dl> <dt>**Categoria de enumeração de impressora \_ \_ \_ 3D**</dt> </dl>    | A função enumera somente as impressoras 3D.<br/>                                                                                                                                                                                                   |
| <span id="PRINTER_ENUM_CATEGORY_ALL"></span><span id="printer_enum_category_all"></span><dl> <dt>**Categoria de enumeração de impressora \_ \_ \_ todos**</dt> </dl> | A função enumera todos os dispositivos de impressão, incluindo impressoras 3D.<br/>                                                                                                                                                                           |



 

Se o *nível* for 4, você só poderá usar as constantes de enum de impressora e de enumeração de impressoras da impressora \_ \_ \_ \_ .

> [!Note]  
> os dispositivos de impressão 3D não são enumerados por padrão. Você deve incluir a **categoria de enumeração de impressora \_ \_ \_ 3D** e a **enumeração de impressora \_ \_ local** para enumerar somente impressoras 3D. Para incluir impressoras 3D, juntamente com todas as outras impressoras locais, use a **categoria de enumeração de impressora \_ \_ \_ todos** e a **enumeração de impressora \_ \_ local**.

 

</dd> <dt>

*Nome* \[ do no\]
</dt> <dd>

Se o *nível* for 1, os *sinalizadores* contiverem o nome de enumeração da impressora \_ e o \_ *nome* não for **nulo**, o *nome* será um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do objeto a ser enumerado. Essa cadeia de caracteres pode ser o nome de um servidor, um domínio ou um provedor de impressão.

Se o *nível* for 1, os *sinalizadores* contiverem \_ \_ o nome de enumeração da impressora e o *nome* for **nulo**, a função enumerará os provedores de impressão disponíveis.

Se *Level* for 1, *flags* contém \_ Remote enum de impressora \_ e *Name* é **NULL**, então a função enumera as impressoras no domínio do usuário.

Se *Level* for 2 ou 5,*Name* será um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome de um servidor cujas impressoras devem ser enumeradas. Se essa cadeia de caracteres for **nula**, a função enumerará as impressoras instaladas no computador local.

Se o *nível* for 4, o *nome* deverá ser **nulo**. A função sempre consulta no computador local.

Quando o *nome* é **nulo**, a definição de *sinalizadores* para impressora \_ enum \_ impressora local enum \| \_ \_ Connections enumera as impressoras instaladas no computador local. Essas impressoras incluem aquelas que estão fisicamente anexadas ao computador local, bem como impressoras remotas às quais ele tem uma conexão de rede.

Quando o *nome* não for **nulo**, definir *sinalizadores* para impressora \_ enum \_ impressora local \| \_ \_ nome de enumeração enumerará as impressoras locais que estão instaladas no *nome* do servidor.

</dd> <dt>

*Nível* \[ do no\]
</dt> <dd>

O tipo de estruturas de dados apontado por *pPrinterEnum*. Os valores válidos são 1, 2, 4 e 5, que correspondem às estruturas de dados informações da impressora [**\_ \_ 1**](printer-info-1.md), [**informações da impressora \_ \_ 2**](printer-info-2.md) , [**\_ informações \_ 4**](printer-info-4.md)da impressora e [**\_ informações \_ 5**](printer-info-5.md) da impressora.

Esse valor pode ser 1, 2, 4 ou 5.

</dd> <dt>

*pPrinterEnum* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe uma matriz de [**informações de impressora \_ \_ 1**](printer-info-1.md), [**informações da impressora \_ \_ 2**](printer-info-2.md), [**informações da impressora \_ \_ 4**](printer-info-4.md)ou estruturas de [**informações da impressora \_ \_ 5**](printer-info-5.md) . Cada estrutura contém dados que descrevem um objeto de impressão disponível.

Se o *nível* for 1, a matriz conterá estruturas de [**informações de impressora \_ \_ 1**](printer-info-1.md) . Se o *nível* for 2, a matriz conterá estruturas de [**informações da impressora \_ \_ 2**](printer-info-2.md) . Se o *nível* for 4, a matriz conterá as estruturas de [**informações da impressora \_ \_ 4**](printer-info-4.md) . Se o *nível* for 5, a matriz conterá estruturas de [**informações da impressora \_ \_ 5**](printer-info-5.md) .

O buffer deve ser grande o suficiente para receber a matriz de estruturas de dados e quaisquer cadeias de caracteres ou outros dados aos quais os membros da estrutura apontam. Se o buffer for muito pequeno, o parâmetro *pcbNeeded* retornará o tamanho de buffer necessário.

</dd> <dt>

*cbBuf* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer apontado por *pPrinterEnum*.

</dd> <dt>

*pcbNeeded* \[ fora\]
</dt> <dd>

Um ponteiro para um valor que recebe o número de bytes copiados se a função for bem sucedido ou o número de bytes necessários se *cbBuf* for muito pequeno.

</dd> <dt>

*pcReturned* \[ fora\]
</dt> <dd>

Um ponteiro para um valor que recebe o número de estruturas informações da impressora [**\_ \_ 1**](printer-info-1.md), [**informações da impressora \_ \_ 2**](printer-info-2.md) , [**informações da impressora \_ \_ 4**](printer-info-4.md)ou [**informações da impressora \_ \_ 5**](printer-info-5.md) que a função retorna na matriz para a qual *pPrinterEnum* aponta.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

Não chame esse método em [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Se **EnumPrinters** retornar uma estrutura de [**informações de impressora \_ \_ 1**](printer-info-1.md) na \_ qual \_ o contêiner de enumeração de impressora é especificado, isso indica que há uma hierarquia de objetos de impressora. Um aplicativo pode enumerar a hierarquia chamando **EnumPrinters** novamente, definindo o *nome* como o valor do membro **pname** da estrutura **\_ info \_ -Printer** .

A função **EnumPrinters** não recupera informações de segurança. Se as estruturas de [**informações da impressora \_ \_ 2**](printer-info-2.md) forem retornadas na matriz apontada por *pPrinterEnum*, seus membros *pSecurityDescriptor* serão definidos como **NULL**.

Para obter informações sobre a impressora padrão, chame [**GetDefaultPrinter**](getdefaultprinter.md).

A [**estrutura \_ informações \_ da impressora 4**](printer-info-4.md) fornece uma maneira fácil e rápida de recuperar os nomes das impressoras instaladas em um computador local, bem como as conexões remotas que um usuário estabeleceu. Quando **EnumPrinters** é chamado com uma estrutura de dados de **informações de impressora \_ \_ 4** , essa função consulta o registro para obter as informações especificadas e retorna imediatamente. Isso difere do comportamento de **EnumPrinters** quando chamado com outros níveis de **informações de \_ impressora \_ \* *_ estruturas de dados. Em particular, quando _* EnumPrinters** é chamado com uma estrutura de dados de nível 2 ([**informações da impressora \_ \_ 2**](printer-info-2.md)), ele executa uma chamada [**OpenPrinter**](openprinter.md) em cada conexão remota. Se uma conexão remota estiver inativa, ou o servidor remoto não existir mais, ou se a impressora remota não existir mais, a função deverá aguardar até que o RPC expire e, consequentemente, falhar na chamada **OpenPrinter** . Isso pode levar algum tempo. Passar uma estrutura de **\_ informações sobre a impressora \_ 4** permite que um aplicativo recupere um mínimo de informações necessárias. se forem desejadas informações mais detalhadas, uma chamada subsequente de **EnumPrinters** nível 2 poderá ser feita.

**Windows Vista:** Os dados de impressora retornados por **EnumPrinters** são recuperados de um cache local quando o valor de *Level* é 4.

A tabela a seguir mostra a saída **EnumPrinters** para vários valores de *sinalizadores* quando o parâmetro *Level* é definido como 1.

Na coluna parâmetro de *nome* da tabela, você deve substituir um nome apropriado para o provedor de impressão, o domínio e a máquina. Por exemplo, para "provedor de impressão", você pode usar o nome do provedor de impressão de rede ou o nome do provedor de impressão local. Para recuperar nomes de provedor de impressão, chame **EnumPrinters** com o *nome* definido como **NULL**.



| Parâmetro *flags*                                  | Parâmetro de *nome*                            | Resultado                                                                                            |
|----------------------------------------------------|---------------------------------------------|---------------------------------------------------------------------------------------------------|
| \_ \_ Local de enumeração de impressora (e não nome de enumeração de impressora \_ \_ ) | O parâmetro *Name* é ignorado.<br/> | Todas as impressoras locais.<br/>                                                                    |
| \_nome da enumeração da impressora \_                                | "Provedor de impressão"<br/>                 | Todos os nomes de domínio<br/>                                                                       |
| \_nome da enumeração da impressora \_                                | "Provedor de impressão! Controlador<br/>          | Todas as impressoras e servidores de impressão no domínio do computador<br/>                                |
| \_nome da enumeração da impressora \_                                | "Provedor de impressão!! \\ \\ Tradução<br/>    | Todas as impressoras compartilhadas na \\ \\ máquina<br/>                                                     |
| \_nome da enumeração da impressora \_                                | Uma cadeia de caracteres vazia, ""<br/>              | Todas as impressoras locais.<br/>                                                                    |
| \_nome da enumeração da impressora \_                                | **NULL**<br/>                         | Todos os provedores de impressão no domínio do computador<br/>                                           |
| \_conexões de enum de impressora \_                         | O parâmetro *Name* é ignorado.<br/> | Todas as impressoras remotas conectadas<br/>                                                          |
| \_rede de enumeração de impressora \_                             | O parâmetro *Name* é ignorado.<br/> | Todas as impressoras no domínio do computador<br/>                                                  |
| \_remoto de enumeração de impressora \_                              | Uma cadeia de caracteres vazia, ""<br/>              | Todas as impressoras e servidores de impressão no domínio do computador<br/>                                |
| \_remoto de enumeração de impressora \_                              | "Provedor de impressão"<br/>                 | Igual ao \_ nome de enumeração da impressora \_<br/>                                                            |
| \_remoto de enumeração de impressora \_                              | "Provedor de impressão! Controlador<br/>          | Todas as impressoras e servidores de impressão no domínio do computador, independentemente do *domínio* especificado.<br/> |
| Categoria de enumeração de impressora \_ \_ \_ 3D                        | O parâmetro *Name* é ignorado.<br/> | Somente as impressoras 3D são enumeradas.<br/>                                                       |
| Categoria de enumeração de impressora \_ \_ \_ todos                       | O parâmetro *Name* é ignorado.<br/> | as impressoras 3D são enumeradas, junto com todas as outras impressoras.<br/>                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **EnumPrintersW** (Unicode) e **EnumPrintersA** (ANSI)<br/>                                       |



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

[**Getprinter**](getprinter.md)
</dt> <dt>

[**Informações da impressora \_ \_ 1**](printer-info-1.md)
</dt> <dt>

[**Informações da impressora \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**Informações da impressora \_ \_ 4**](printer-info-4.md)
</dt> <dt>

[**Informações da impressora \_ \_ 5**](printer-info-5.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> </dl>

 

