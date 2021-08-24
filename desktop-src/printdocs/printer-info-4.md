---
description: A \_ estrutura informações da impressora \_ 4 especifica informações gerais sobre a impressora. A estrutura pode ser usada para recuperar informações de impressora mínimas em uma chamada para EnumPrinters.
ms.assetid: 81bd0eab-dc1e-4cf1-8f63-3686f1711c1f
title: Estrutura de PRINTER_INFO_4 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_4
- _PRINTER_INFO_4A
- _PRINTER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3ba6e372b495c47dd92e61e51ba6487e6d9c2c0aca924bf6ed3a092ba0816820
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119446986"
---
# <a name="printer_info_4-structure"></a>Estrutura de informações da impressora \_ \_ 4

A **estrutura \_ informações \_ da impressora 4** especifica informações gerais sobre a impressora.

A estrutura pode ser usada para recuperar informações de impressora mínimas em uma chamada para [**EnumPrinters**](enumprinters.md). Essa chamada é uma maneira rápida e fácil de recuperar os nomes e os atributos de todas as impressoras instaladas localmente em um sistema e todas as conexões de impressora remota que um usuário estabeleceu.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PRINTER_INFO_4 {
  LPTSTR pPrinterName;
  LPTSTR pServerName;
  DWORD  Attributes;
} PRINTER_INFO_4, *PPRINTER_INFO_4;
```



## <a name="members"></a>Membros

<dl> <dt>

**pPrinterName**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da impressora (local ou remota).

</dd> <dt>

**pServerName**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que é o nome do servidor.

</dd> <dt>

**Atributos**
</dt> <dd>

Especifica informações sobre os dados retornados.



| Valor                       | Significado                          |
|-----------------------------|----------------------------------|
| atributo de impressora \_ \_ local   | A impressora é uma impressora local.  |
| \_rede de atributos da impressora \_ | A impressora é uma impressora remota. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A **estrutura \_ informações \_ da impressora 4** fornece uma maneira fácil e rápida de recuperar os nomes das impressoras instaladas em um computador local, bem como as conexões remotas que um usuário estabeleceu. Quando [**EnumPrinters**](enumprinters.md) é chamado com uma estrutura de dados de **informações de impressora \_ \_ 4** , essa função consulta o registro para obter as informações especificadas e retorna imediatamente. Isso difere do comportamento de **EnumPrinters** quando chamado com outros níveis de estruturas de dados de **informações de impressora \_ \_ xxx** . Em particular, quando **EnumPrinters** é chamado com uma estrutura de dados de nível 2 (**informações da impressora \_ \_ 2** ), ele executa uma chamada **OpenPrinter** em cada conexão remota. Se uma conexão remota estiver inativa, se o servidor remoto não existir mais, ou se a impressora remota não existir mais, a função deverá aguardar o RPC atingir o tempo limite e, consequentemente, falhará na chamada **OpenPrinter** . Isso pode levar algum tempo. Passar uma estrutura de **\_ informações sobre a impressora \_ 4** permite que um aplicativo recupere um mínimo de informações necessárias. se forem desejadas informações mais detalhadas, uma chamada subsequente de **EnumPrinter** nível 2 poderá ser feita.

Os **atributos** também podem conter valores definidos no campo **atributos** das informações da **impressora \_ \_ 2**.

algumas configurações de impressora, como conexões de impressora para alguns servidores de impressão não Windows, podem retornar o **atributo de \_ impressora \_ LOCAL** e **a \_ \_ rede de atributos de impressora**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | Informações de **\_ impressora \_ \_ 4W** (Unicode) e **\_ informações de impressora \_ \_ 4a** (ANSI)<br/>                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Getprinter**](getprinter.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Informações da impressora \_ \_ 1**](printer-info-1.md)
</dt> <dt>

[**Informações da impressora \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**Informações da impressora \_ \_ 3**](printer-info-3.md)
</dt> </dl>

 

 




