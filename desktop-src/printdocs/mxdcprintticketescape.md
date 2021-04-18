---
description: A \_ estrutura t de escape do MXDC PRINTTICKET \_ \_ é uma \_ estrutura t do cabeçalho de escape do MXDC \_ \_ concatenada com uma \_ estrutura de dados t do MXDC PRINTTICKET \_ \_ .
ms.assetid: 79b4f830-3e3f-4c6f-9e61-98e8bf6e2824
title: Estrutura de MXDC_PRINTTICKET_ESCAPE_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 158ee2038c83b74077d00e6922b2c7050b76bc62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751804"
---
# <a name="mxdc_printticket_escape_t-structure"></a>\_ \_ Estrutura T de escape do MXDC PRINTTICKET \_

A **estrutura \_ \_ \_ t de escape do MXDC PRINTTICKET** é uma estrutura [**\_ \_ \_ t do cabeçalho de escape do MXDC**](mxdcescapeheader.md) concatenada com uma estrutura de [**\_ \_ dados \_ t do MXDC PRINTTICKET**](mxdcprintticketpassthrough.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMxdcPrintTicketEscape {
  MXDC_ESCAPE_HEADER_T    mxdcEscape;
  MXDC_PRINTTICKET_DATA_T printTicketData;
} MXDC_PRINTTICKET_ESCAPE_T, *P_MXDC_PRINTTICKET_ESCAPE_T;
```



## <a name="members"></a>Membros

<dl> <dt>

**mxdcEscape**
</dt> <dd>

Uma [**estrutura \_ \_ \_ T de cabeçalho de escape MXDC**](mxdcescapeheader.md) com seu membro **opcode** definido como página fixa do MXDCOP \_ PrintTicket \_ \_ , \_ documento fixo MXDCOP PrintTicket \_ \_ ou MXDCOP \_ PrintTicket \_ fixo \_ doc \_ Seq.

</dd> <dt>

**printTicketData**
</dt> <dd>

Uma estrutura de [**\_ \_ dados \_ de MXDC PRINTTICKET**](mxdcprintticketpassthrough.md) que contém o tíquete de impressão.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é passada no parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando essa função é chamada com o escape de [**escape \_ MXDC**](mxdc-escape.md) e o membro **de opcode** da estrutura [**\_ \_ \_ T do cabeçalho de escape MXDC**](mxdcescapeheader.md) é a **\_ \_ \_ página fixa MXDCOP PrintTicket**, **MXDCOP \_ PrintTicket \_ Fixed \_ Doc** ou **MXDCOP \_ PrintTicket \_ Fixed \_ doc \_ Seq**. O resultado é gravar o tíquete de impressão no arquivo de documento XPS.

Aloque memória para o escape, conforme mostrado abaixo, defina os campos conforme necessário e, em seguida, chame [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_PRINTTICKET_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_PRINTTICKET_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_PRINTTICKET_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



Se o **opcode** for definido como **\_ \_ \_ página fixa do MXDCOP PRINTTICKET**, a chamada [**para ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deverá ocorrer entre uma chamada para [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e uma chamada para [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage). Se o **opcode** estiver definido como **MXDCOP \_ PrintTicket \_ Fixed \_ Doc** ou **MXDCOP \_ PrintTicket \_ Fixed \_ doc \_ Seq**, a chamada para **ExtEscape** deverá ocorrer entre uma chamada para [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) e uma chamada para [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Mxdc. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[Funções de escape de impressora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**MXDC \_ escape**](mxdc-escape.md)
</dt> </dl>

 

