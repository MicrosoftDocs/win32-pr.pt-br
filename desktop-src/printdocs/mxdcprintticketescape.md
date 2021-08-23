---
description: A estrutura T do MXDC PRINTTICKET ESCAPE é uma estrutura T do MXDC ESCAPE HEADER concatenada com uma estrutura \_ \_ \_ \_ \_ \_ MXDC \_ PRINTTICKET \_ DATA \_ T.
ms.assetid: 79b4f830-3e3f-4c6f-9e61-98e8bf6e2824
title: MXDC_PRINTTICKET_ESCAPE_T estrutura (Mxdc.h)
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
ms.openlocfilehash: eca1858bbbf09d4e3c3af8a91f9bb91550eddfd703f59e86112e65c56a43d553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099060"
---
# <a name="mxdc_printticket_escape_t-structure"></a>Estrutura T do MXDC \_ PRINTTICKET \_ ESCAPE \_

A estrutura T do **MXDC \_ PRINTTICKET \_ ESCAPE \_** é uma estrutura T do [**MXDC \_ ESCAPE \_ HEADER \_ concatenada**](mxdcescapeheader.md) com uma estrutura [**MXDC \_ PRINTTICKET \_ DATA \_ T.**](mxdcprintticketpassthrough.md)

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

Uma [**estrutura T do \_ \_ HEADER ESCAPE \_ MXDC**](mxdcescapeheader.md) com seu membro **opCode** definido como MXDCOP \_ PRINTTICKET \_ FIXED \_ PAGE, MXDCOP \_ PRINTTICKET FIXED DOC ou \_ \_ MXDCOP \_ PRINTTICKET \_ FIXED DOC \_ \_ SEQ.

</dd> <dt>

**printTicketData**
</dt> <dd>

Uma [**estrutura MXDC \_ PRINTTICKET \_ DATA \_ T**](mxdcprintticketpassthrough.md) que contém o tíquete de impressão.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é passada no parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando essa função é chamada com o escape [**\_ ESCAPE do MXDC**](mxdc-escape.md) e o membro **opCode** da estrutura T do [**MXDC \_ ESCAPE \_ HEADER \_**](mxdcescapeheader.md) é **MXDCOP \_ PRINTTICKET \_ FIXED \_ PAGE**, **MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC** ou **MXDCOP \_ PRINTTICKET \_ FIXED DOC \_ \_ SEQ**. O resultado é gravar o tíquete de impressão no arquivo de documento XPS.

Alocar memória para o escape, conforme mostrado abaixo, definir os campos conforme necessário e, em seguida, chamar [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).


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



Se **o opCode** estiver definido como **MXDCOP \_ PRINTTICKET \_ FIXED \_ PAGE**, a chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deverá ocorrer entre uma chamada para [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e uma chamada para [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage). Se **o opCode** definido como **MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC** ou **MXDCOP \_ PRINTTICKET \_ FIXED DOC \_ \_ SEQ**, a chamada para **ExtEscape** deverá ocorrer entre uma chamada para [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) e uma chamada para [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                    |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Mxdc.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Imprimir estruturas de API do Spooler](printing-and-print-spooler-structures.md)
</dt> <dt>

[Funções de escape de impressora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**Extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**MXDC \_ ESCAPE**](mxdc-escape.md)
</dt> </dl>

 

