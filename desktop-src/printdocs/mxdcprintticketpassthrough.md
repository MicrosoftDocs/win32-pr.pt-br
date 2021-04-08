---
description: A \_ estrutura de dados T do MXDC PRINTTICKET \_ \_ contém um tíquete de impressão de documento XPS, que contém configurações de impressora e trabalho de impressão, para passar para o arquivo de saída do conversor de documento XPS da Microsoft (MXDC) sem nenhum processamento.
ms.assetid: d30ba8bb-f429-49d5-963c-b770c3086e97
title: Estrutura de MXDC_PRINTTICKET_DATA_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 94308527437316dda75fc5a50a6a7829e9315c3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828310"
---
# <a name="mxdc_printticket_data_t-structure"></a>\_Estrutura de \_ T de dados do MXDC PRINTTICKET \_

A estrutura de **\_ \_ dados \_ T do MXDC PRINTTICKET** contém um TÍQUETE de impressão de documento XPS, que contém configurações de impressora e trabalho de impressão, para passar para o arquivo de saída do conversor de documento XPS da Microsoft (MXDC) sem nenhum processamento.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMxdcPrintTicketData {
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_PRINTTICKET_DATA_T, *P_MXDC_PRINTTICKET_DATA_T;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwDataSize**
</dt> <dd>

O tamanho do tíquete de impressão em bytes.

</dd> <dt>

**bData**
</dt> <dd>

O tíquete de impressão do documento XPS.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é anexada a uma [**estrutura \_ \_ \_ T de cabeçalho de escape MXDC**](mxdcescapeheader.md) que tem o membro **opcode** definido como **MXDCOP de \_ \_ \_ página fixa PrintTicket**, **MXDCOP \_ PrintTicket \_ Fixed \_ Doc** ou **MXDCOP \_ PRINTTICKET \_ Fixed \_ doc \_ Seq** para fazer uma estrutura de [**escape do MXDC \_ PrintTicket \_ \_**](mxdcprintticketescape.md) . A estrutura de **\_ \_ escape \_ T do MXDC PRINTTICKET** é passada para o parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando ela é chamada com o escape de [**\_ escape MXDC**](mxdc-escape.md) . O efeito é gravar o tíquete de impressão no arquivo de documento XPS.

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

 

