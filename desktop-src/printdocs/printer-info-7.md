---
description: A estrutura PRINTER \_ INFO \_ 7 especifica informações de impressora de serviços de diretório.
ms.assetid: 9443855e-df7d-41a1-a0df-5649a97b2915
title: PRINTER_INFO_7 (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_7
- _PRINTER_INFO_7A
- _PRINTER_INFO_7W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c8ba37176bb970883533be1e0ddcc47a09b164bf48767442f75096828c9bce5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867762"
---
# <a name="printer_info_7-structure"></a>Estrutura INFORMAÇÕES DA IMPRESSORA \_ \_ 7

A **estrutura PRINTER INFO \_ \_ 7** especifica informações de impressora de serviços de diretório. Use essa estrutura com a [**função SetPrinter**](setprinter.md) para publicar os dados de uma impressora no DS (serviço de diretório) ou para atualizar ou remover dados publicados de uma impressora do DS. Use essa estrutura com a [**função GetPrinter**](getprinter.md) para determinar se uma impressora é publicada no DS.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PRINTER_INFO_7 {
  LPTSTR pszObjectGUID;
  DWORD  dwAction;
} PRINTER_INFO_7, *PPRINTER_INFO_7;
```



## <a name="members"></a>Membros

<dl> <dt>

**pszObjectGUID**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o GUID do objeto de fila de impressão do serviço de diretório associado a uma impressora publicada. Use a [**função GetPrinter**](getprinter.md) para recuperar esse GUID.

Antes de [**chamar SetPrinter**](setprinter.md), de definido **pszObjectGUID** como **NULL.**

</dd> <dt>

**Dwaction**
</dt> <dd>

Indica a ação para a [**função SetPrinter**](setprinter.md) executar. Para a [**função GetPrinter,**](getprinter.md) esse membro indica se a impressora especificada foi publicada. Esse membro pode ser uma combinação dos valores a seguir.



| Valor                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DSPRINT_PENDING"></span><span id="dsprint_pending"></span><dl> <dt>**DSPRINT \_ PENDING**</dt> <dt>0x80000000</dt> </dl>       | [**GetPrinter**](getprinter.md): indica que o sistema está tentando concluir uma operação de publicação ou não publicação iniciada por uma [**chamada setPrinter.**](setprinter.md)<br/> [**SetPrinter:**](setprinter.md)esse valor não é válido. <br/>                                                |
| <span id="DSPRINT_PUBLISH"></span><span id="dsprint_publish"></span><dl> <dt>**DSPRINT \_ PUBLICAR**</dt> <dt>0x00000001</dt> </dl>       | [**SetPrinter:**](setprinter.md)publica os dados da impressora no DS.<br/> [**GetPrinter:**](getprinter.md)indica que a impressora foi publicada. <br/>                                                                                                                                      |
| <span id="DSPRINT_REPUBLISH"></span><span id="dsprint_republish"></span><dl> <dt>**DSPRINT \_ REPUBLICAR 0X00000008**</dt> <dt></dt> </dl> | [**SetPrinter:**](setprinter.md)os dados do DS para a impressora não são publicados e publicados novamente, atualize todas as propriedades na impressora publicada. A republicar também altera o GUID da impressora publicada.<br/> [**GetPrinter:**](getprinter.md)nunca retorna esse valor. <br/> |
| <span id="DSPRINT_UNPUBLISH"></span><span id="dsprint_unpublish"></span><dl> <dt>**DSPRINT \_ UNPUBLISH**</dt> <dt>0x00000004</dt> </dl> | [**SetPrinter:**](setprinter.md)remove os dados publicados da impressora do DS.<br/> [**GetPrinter:**](getprinter.md)indica que a impressora não foi publicada. <br/>                                                                                                                        |
| <span id="DSPRINT_UPDATE"></span><span id="dsprint_update"></span><dl> <dt>**DSPRINT \_ ATUALIZAÇÃO**</dt> <dt>0x00000002</dt> </dl>          | [**SetPrinter:**](setprinter.md)atualiza os dados publicados da impressora no DS.<br/> [**GetPrinter:**](getprinter.md)nunca retorna esse valor. <br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A **estrutura PRINTER INFO \_ \_ 7** é usada em uma [**chamada setPrinter**](setprinter.md) para publicar informações de impressora no serviço de diretório. Os dados publicados incluem todos os valores e dados da impressora especificada encontrada nas chaves \_ SPLDS SPOOLER KEY, SPLDS DRIVER KEY ou SPLDS USER KEY criadas por \_ \_ \_ \_ \_ [**SetPrinterDataEx.**](setprinterdataex.md)

Para [**SetPrinter,**](setprinter.md) *pszObjectGUID* deve ser definido como **NULL.** Para [**GetPrinter**](getprinter.md), *pszObjectGUID* retorna o GUID do objeto de fila de impressão dos serviços de diretório associado a uma impressora publicada. Você pode usar esse GUID com métodos ADSI (Interface de Serviços do Active Directory) para recuperar dados publicados para a impressora. No entanto, o método recomendado para recuperar dados publicados é chamar a [**função GetPrinterDataEx.**](getprinterdataex.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ INFORMAÇÕES \_ DA IMPRESSORA \_ 7W** (Unicode) e **\_ INFORMAÇÕES DA IMPRESSORA \_ \_ 7A** (ANSI)<br/>                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Imprimir estruturas de API do Spooler](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




