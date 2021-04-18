---
description: A função getprinter recupera informações sobre uma impressora especificada.
ms.assetid: f162edbb-83ee-40c3-8710-9c867301d652
title: Função getprinter (winspool. h)
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
ms.openlocfilehash: e99b3574762b84b830845da8149b0406664b6da7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784646"
---
# <a name="getprinter-function"></a>Função getprinter

A função **Getprinter** recupera informações sobre uma impressora especificada.

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

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para a impressora para a qual a função recupera informações. Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.

</dd> <dt>

*Nível* \[ do no\]
</dt> <dd>

O nível ou tipo de estrutura que a função armazena no buffer apontado por *pPrinter*.

Esse valor pode ser 1, 2, 3, 4, 5, 6, 7, 8 ou 9.

</dd> <dt>

*pPrinter* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe uma estrutura que contém informações sobre a impressora especificada. O buffer deve ser grande o suficiente para receber a estrutura e quaisquer cadeias de caracteres ou outros dados aos quais os membros da estrutura apontam. Se o buffer for muito pequeno, o parâmetro *pcbNeeded* retornará o tamanho de buffer necessário.

O tipo de estrutura é determinado pelo valor do *nível*.



| Nível                                                                                                | Estrutura                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Uma estrutura de [**informações da impressora \_ \_ 1**](printer-info-1.md) que contém informações gerais sobre a impressora.<br/>                                                                                                        |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Uma estrutura de [**informações da impressora \_ \_ 2**](printer-info-2.md) que contém informações detalhadas sobre a impressora.<br/>                                                                                             |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Uma estrutura de [**informações da impressora \_ \_ 3**](printer-info-3.md) que contém as informações de segurança da impressora.<br/>                                                                                                 |
| <span id="4"></span><dl> <dt>**quatro**</dt> </dl> | Uma estrutura de [**informações da impressora \_ \_ 4**](printer-info-4.md) que contém informações de impressora mínimas, incluindo o nome da impressora, o nome do servidor e se a impressora é remota ou local.<br/> |
| <span id="5"></span><dl> <dt>**05**</dt> </dl> | Uma estrutura de [**informações da impressora \_ \_ 5**](printer-info-5.md) que contém informações de impressora, como atributos de impressora e configurações de tempo limite.<br/>                                                               |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | Uma estrutura de [**informações da impressora \_ \_ 6**](printer-info-6.md) especificando o valor de status de uma impressora.<br/>                                                                                                      |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | Uma estrutura de [**informações da impressora \_ \_ 7**](printer-info-7.md) que indica se a impressora está publicada no serviço de diretório.<br/>                                                                      |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | Uma estrutura de [**informações da impressora \_ \_ 8**](printer-info-8.md) especificando as configurações de impressora padrão globais.<br/>                                                                                                |
| <span id="9"></span><dl> <dt>**9**</dt> </dl> | Uma estrutura de [**informações da impressora \_ \_ 9**](printer-info-9.md) especificando as configurações de impressora padrão por usuário.<br/>                                                                                              |



 

</dd> <dt>

*cbBuf* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer apontado por *pPrinter*.

</dd> <dt>

*pcbNeeded* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que a função define para o tamanho, em bytes, das informações da impressora. Se *cbBuf* for menor que esse valor, **getprinter** falhará e o valor representará o tamanho de buffer necessário. Se *cbBuf* for igual a ou maior que esse valor, **getprinter** terá sucesso e o valor representará o número de bytes armazenados no buffer.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

O membro **pDevMode** nas estruturas [**\_ info \_ 2**](printer-info-2.md), [**Printer \_ info \_ 8**](printer-info-8.md)e [**Printer \_ info \_ 9**](printer-info-9.md) da impressora pode ser **nulo**. Quando isso acontecer, a impressora ficará inutilizável até que o driver seja reinstalado com êxito.

Para as [**estruturas \_ informações \_ da impressora 2**](printer-info-2.md) e [**informações da impressora \_ \_ 3**](printer-info-3.md) que contêm um ponteiro para um descritor de segurança, a função recupera somente os componentes do descritor de segurança que o chamador tem permissão para ler. Para recuperar componentes específicos do descritor de segurança, você deve especificar os direitos de acesso necessários ao chamar a função [**OpenPrinter**](openprinter.md) para recuperar um identificador para a impressora. A tabela a seguir mostra os direitos de acesso necessários para ler os vários componentes do descritor de segurança.



| Direitos de acesso                        | Componente de descritor de segurança                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| controle de leitura \_<br/>            | Proprietário<br/> Grupo primário<br/> DACL (lista de controle de acesso discricionário)<br/> |
| \_segurança do sistema de acesso \_<br/> | Lista de controle de acesso (SACL) do sistema<br/>                                                  |



 

Se você especificar nível 7, o membro **dwAction** das [**informações da impressora \_ \_ 7**](printer-info-7.md) retornará um dos seguintes valores para indicar se a impressora está publicada no serviço de diretório.



| valor de dwAction     | Significado                                                                                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| publicação do DSPRINT \_   | A impressora é publicada. O membro **pszObjectGUID** contém o GUID do objeto de fila de impressão dos serviços de diretório associado à impressora.                                                                                                       |
| DSPRINT \_ Cancelar publicação | A impressora não está publicada.                                                                                                                                                                                                                            |
| DSPRINT \_ pendente   | Indica que o sistema está tentando concluir uma operação de publicação ou cancelamento de publicação. Se uma chamada [**Setprintr**](setprinter.md) falhar ao publicar ou cancelar a publicação de uma impressora, o sistema fará outras tentativas de concluir a operação em segundo plano. |



 

A partir do Windows Vista, os dados da impressora retornados pelo **Getprinter** são recuperados de um cache local quando o *hPrinter* refere-se a uma impressora hospedada por um servidor de impressão e há pelo menos uma conexão aberta com o servidor de impressão. Em todas as outras configurações, os dados da impressora são consultados do servidor de impressão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **GetPrinterW** (Unicode) e **getprintera** (ANSI)<br/>                                           |



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

[**Informações da impressora \_ \_ 1**](printer-info-1.md)
</dt> <dt>

[**Informações da impressora \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**Informações da impressora \_ \_ 3**](printer-info-3.md)
</dt> <dt>

[**Informações da impressora \_ \_ 4**](printer-info-4.md)
</dt> <dt>

[**Informações da impressora \_ \_ 5**](printer-info-5.md)
</dt> <dt>

[**Informações da impressora \_ \_ 7**](printer-info-7.md)
</dt> <dt>

[**Informações da impressora \_ \_ 8**](printer-info-8.md)
</dt> <dt>

[**Informações da impressora \_ \_ 9**](printer-info-9.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> </dl>

 

 




