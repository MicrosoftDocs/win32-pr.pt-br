---
description: A função GetPrinter recupera informações sobre uma impressora especificada.
ms.assetid: f162edbb-83ee-40c3-8710-9c867301d652
title: Função GetPrinter (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinter
- GetPrinterA
- GetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: b6823795ea715ac72dfdb7150dac08fd7feb34445fcfab94412cb2dd0c6bd7a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949077"
---
# <a name="getprinter-function"></a>Função GetPrinter

A **função GetPrinter** recupera informações sobre uma impressora especificada.

## <a name="syntax"></a>Sintaxe


```C++
BOOL GetPrinter(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinter,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ Em\]
</dt> <dd>

Um alça para a impressora para a qual a função recupera informações. Use a [**função OpenPrinter**](openprinter.md) [**ou AddPrinter**](addprinter.md) para recuperar um alça de impressora.

</dd> <dt>

*Nível* \[ Em\]
</dt> <dd>

O nível ou o tipo de estrutura que a função armazena no buffer apontado por *pPrinter*.

Esse valor pode ser 1, 2, 3, 4, 5, 6, 7, 8 ou 9.

</dd> <dt>

*pPrinter* \[ out\]
</dt> <dd>

Um ponteiro para um buffer que recebe uma estrutura que contém informações sobre a impressora especificada. O buffer deve ser grande o suficiente para receber a estrutura e quaisquer cadeias de caracteres ou outros dados para os quais os membros da estrutura apontam. Se o buffer for muito pequeno, o *parâmetro pcbNeeded* retornará o tamanho do buffer necessário.

O tipo de estrutura é determinado pelo valor de *Level*.



| Nível                                                                                                | Estrutura                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Uma [**estrutura PRINTER INFO \_ \_ 1**](printer-info-1.md) que contém informações gerais da impressora.<br/>                                                                                                        |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Uma [**estrutura PRINTER INFO \_ \_ 2**](printer-info-2.md) que contém informações detalhadas sobre a impressora.<br/>                                                                                             |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Uma [**estrutura PRINTER INFO \_ \_ 3**](printer-info-3.md) que contém as informações de segurança da impressora.<br/>                                                                                                 |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Uma [**estrutura PRINTER INFO \_ \_ 4**](printer-info-4.md) que contém informações mínimas da impressora, incluindo o nome da impressora, o nome do servidor e se a impressora é remota ou local.<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | Uma [**estrutura PRINTER INFO \_ \_ 5**](printer-info-5.md) que contém informações de impressora, como atributos de impressora e configurações de tempo-out.<br/>                                                               |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | Uma [**estrutura PRINTER INFO \_ \_ 6**](printer-info-6.md) que especifica o valor de status de uma impressora.<br/>                                                                                                      |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | Uma [**estrutura PRINTER INFO \_ \_ 7**](printer-info-7.md) que indica se a impressora é publicada no serviço de diretório.<br/>                                                                      |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | Uma [**estrutura PRINTER INFO \_ \_ 8**](printer-info-8.md) que especifica as configurações globais de impressora padrão.<br/>                                                                                                |
| <span id="9"></span><dl> <dt>**9**</dt> </dl> | Uma [**estrutura PRINTER INFO \_ \_ 9**](printer-info-9.md) que especifica as configurações de impressora padrão por usuário.<br/>                                                                                              |



 

</dd> <dt>

*cbBuf* \[ Em\]
</dt> <dd>

O tamanho, em bytes, do buffer apontado por *pPrinter*.

</dd> <dt>

*pcbNeeded* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que a função define para o tamanho, em bytes, das informações da impressora. Se *cbBuf* for menor que esse valor, **GetPrinter** falhará e o valor representará o tamanho do buffer necessário. Se *cbBuf* for igual ou maior que esse valor, **GetPrinter** terá êxito e o valor representará o número de bytes armazenados no buffer.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um valor não zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração do servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

O **membro pDevMode** nas estruturas [**PRINTER INFO \_ \_ 2,**](printer-info-2.md) [**PRINTER INFO \_ \_ 8**](printer-info-8.md)e [**PRINTER INFO \_ \_ 9**](printer-info-9.md) pode ser **NULL.** Quando isso acontece, a impressora fica inutilizável até que o driver seja reinstalado com êxito.

Para as estruturas [**PRINTER \_ INFO \_ 2**](printer-info-2.md) e [**PRINTER INFO \_ \_ 3**](printer-info-3.md) que contêm um ponteiro para um descritor de segurança, a função recupera apenas os componentes do descritor de segurança que o chamador tem permissão para ler. Para recuperar componentes de descritor de segurança específicos, você deve especificar os direitos de acesso necessários ao chamar a [**função OpenPrinter**](openprinter.md) para recuperar um handle para a impressora. A tabela a seguir mostra os direitos de acesso necessários para ler os vários componentes do descritor de segurança.



| Direitos de acesso                        | Componente do Descritor de Segurança                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| CONTROLE \_ DE LEITURA<br/>            | Proprietário<br/> Grupo primário<br/> DACL (lista de controle de acesso discricionário)<br/> |
| SEGURANÇA \_ DO SISTEMA DE \_ ACESSO<br/> | SACL (lista de controle de acesso do sistema)<br/>                                                  |



 

Se você especificar o nível 7, o membro **dwAction** de [**PRINTER INFO \_ \_ 7**](printer-info-7.md) retornará um dos valores a seguir para indicar se a impressora é publicada no serviço de diretório.



| Valor dwAction     | Significado                                                                                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DSPRINT \_ PUBLISH   | A impressora é publicada. O **membro pszObjectGUID** contém o GUID do objeto de fila de impressão dos serviços de diretório associado à impressora.                                                                                                       |
| DSPRINT \_ UNPUBLISH | A impressora não é publicada.                                                                                                                                                                                                                            |
| DSPRINT \_ PENDENTE   | Indica que o sistema está tentando concluir uma operação de publicação ou não publicação. Se uma [**chamada setPrinter**](setprinter.md) falhar ao publicar ou não publicar uma impressora, o sistema tentará concluir a operação em segundo plano. |



 

A partir do Windows Vista, os dados da impressora retornados pelo **GetPrinter** são recuperados de um cache local quando *hPrinter* se refere a uma impressora hospedada por um servidor de impressão e há pelo menos uma conexão aberta com o servidor de impressão. Em todas as outras configurações, os dados da impressora são consultados do servidor de impressão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **GetPrinterW** (Unicode) e **GetPrinterA** (ANSI)<br/>                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AbortPrinter**](abortprinter.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA \_ IMPRESSORA 1**](printer-info-1.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA IMPRESSORA \_ 2**](printer-info-2.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA IMPRESSORA \_ 3**](printer-info-3.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA IMPRESSORA \_ 4**](printer-info-4.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA IMPRESSORA \_ 5**](printer-info-5.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA \_ IMPRESSORA 7**](printer-info-7.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA IMPRESSORA \_ 8**](printer-info-8.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA IMPRESSORA \_ 9**](printer-info-9.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

 




