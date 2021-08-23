---
description: A \_ estrutura info \_ 2 do documento descreve um documento que será impresso.
ms.assetid: d62333f3-cc39-4c9b-8fb3-02a2d24bbbad
title: Estrutura de DOC_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_2
- _DOC_INFO_2A
- _DOC_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 27d7753fa16abcfbc30b28bcc4343b2e1ef7996cad408b54fefb850feac9b17e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846256"
---
# <a name="doc_info_2-structure"></a>Estrutura de informações do documento \_ \_ 2

A **estrutura \_ info \_ 2** do documento descreve um documento que será impresso.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DOC_INFO_2 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwMode;
  DWORD  JobId;
} DOC_INFO_2, *PDOC_INFO_2;
```



## <a name="members"></a>Membros

<dl> <dt>

**pDocName**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do documento.

</dd> <dt>

**pOutputFile**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome de um arquivo de saída.

</dd> <dt>

**pDatatype**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que identifica o tipo de dados usado para gravar o documento.

</dd> <dt>

**dwMode**
</dt> <dd>

Informa ao spooler de impressão a natureza dos dados a serem seguidos. Se esse valor for zero, o spooler de impressão tratará os dados enviados por chamadas subsequentes para [**WritePrinter**](writeprinter.md) como um trabalho de impressão normal (se ele for ou não colocado no spool, depende da propriedade da impressora). Se esse valor for um \_ canal de di, apenas um canal de comunicação será aberto. Nesse caso, os dados passados para as chamadas subsequentes para **WritePrinter** são enviados para a impressora ou chamadas subsequentes para [**ReadPrinter**](readprinter.md) recuperar dados da impressora. Esse modo permanece efetivo até que [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) seja chamado.

</dd> <dt>

**JobId**
</dt> <dd>

Reservado para uso interno; deve ser zero.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ Informações do documento \_ \_ 2W** (Unicode) e **\_ info do documento \_ \_ 2a** (ANSI)<br/>                                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)
</dt> <dt>

[**ReadPrinter**](readprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




