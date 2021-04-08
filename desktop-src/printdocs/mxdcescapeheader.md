---
description: A \_ estrutura T do cabeçalho de escape MXDC \_ \_ contém o código da operação para uma chamada para ExtEscape com MXDC \_ escape como o parâmetro nEscape. Ele também fornece os tamanhos dos buffers de entrada e saída.
ms.assetid: 3d1f909c-0c3c-49ac-b530-4ce077ad6d94
title: Estrutura de MXDC_ESCAPE_HEADER_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE_HEADER_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: a16e0d5bb1a8ce48e071fe1b32543610d8433e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837144"
---
# <a name="mxdc_escape_header_t-structure"></a>\_ \_ Estrutura T do cabeçalho de escape MXDC \_

A **estrutura \_ \_ \_ T do cabeçalho de escape MXDC** contém o código da operação para uma chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com [**MXDC \_ escape**](mxdc-escape.md) como o parâmetro *nEscape* . Ele também fornece os tamanhos dos buffers de entrada e saída.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMxdcEscapeHeader {
  ULONG cbInput;
  ULONG cbOutput;
  ULONG opCode;
} MXDC_ESCAPE_HEADER_T, *P_MXDC_ESCAPE_HEADER_T;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbInput**
</dt> <dd>

O tamanho do buffer de entrada que será passado para o parâmetro *lpszOutData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .

</dd> <dt>

**cbOutput**
</dt> <dd>

O tamanho do buffer de saída. Esse é o mesmo valor que o parâmetro *cbOutput* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .

</dd> <dt>

**opCode**
</dt> <dd>

A constante de código que diz ao MXDC o que fazer.



| Código de operações                      | Description                                                                                                                                                                                                            |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MXDCOP \_ obter \_ nome de arquivo                | Retorna, no parâmetro *lpszOutData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) , o caminho completo do arquivo de saída como uma cadeia de caracteres terminada em zero ou o tamanho dessa cadeia de caracteres. Consulte Observações.                   |
| \_Seq de \_ \_ Doc fixo \_ do MXDCOP PRINTTICKET | Associa um tíquete de impressão a uma sequência de documento fixa XPS.                                                                                                                                                         |
| \_ \_ Doc fixo do MXDCOP PRINTTICKET \_      | Associa um tíquete de impressão a um documento XPS.                                                                                                                                                                        |
| \_ \_ página fixa do MXDCOP PRINTTICKET \_     | Associa um tíquete de impressão a uma página XPS.                                                                                                                                                                            |
| MXDCOP \_ set \_ S0PAGE                  | Envia a marcação XPS da página atual para a saída.                                                                                                                                                                |
| MXDCOP \_ definir \_ \_ recurso S0PAGE        | Envia um recurso na página, como uma imagem ou fonte, para a saída.                                                                                                                                                 |
| MXDCOP \_ definir \_ \_ modo XPSPASSTHRU       | Coloca o MXDC em um estado de passagem, permitindo que um aplicativo grave o XPS diretamente no arquivo de saída sem nenhum processamento pelo MXDC. Um documento inteiro ou até mesmo uma sequência de documento pode ser escrito dessa maneira. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Antes de chamar [**MXDC \_ escape**](mxdc-escape.md), os \_ aplicativos devem primeiro verificar se o driver é MXDC chamando [**EXTESCAPE**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com o escape [**gettechnology**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) . Se o driver for o MXDC, a função retornará a cadeia de caracteres terminada em zero " http://schemas.microsoft.com/xps/2005/06 ".

Essa estrutura está sempre no início dos dados passados para a função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) em seu parâmetro *lpszInData* .

Quando **opcode** é MXDCOP, \_ Get \_ filename:

-   O parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) consiste apenas na estrutura T do **\_ \_ cabeçalho de \_ escape MXDC** .
-   Obtenha o nome de arquivo de saída chamando [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) duas vezes.
    1.  Na primeira vez, passe 4 para o parâmetro *cbOutput* de [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape). Defina o parâmetro *lpszOutData* para apontar para todos os 4 bytes alocados de memória. O tamanho do caminho de arquivo totalmente qualificado será retornado no parâmetro *lpszOutData* de **ExtEscape**.
    2.  Em seguida, chame a função novamente. Dessa vez, defina *cbOutput* e *cbInput* como 4 + Data *size*. O caminho de arquivo totalmente qualificado será retornado em uma estrutura [**MxdcGetFileNameData**](mxdcgetfilenamedata.md) .

Quando **opcode** for MXDCOP \_ PrintTicket \_ Fixed \_ doc \_ Seq ou MXDCOP \_ PrintTicket \_ Fixed \_ doc:

-   O parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) consiste na estrutura T do **\_ \_ cabeçalho de \_ escape MXDC** e em uma estrutura [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) concatenada em uma estrutura [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) .
-   A chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve ocorrer entre uma chamada para [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) e uma chamada para [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).

Quando **opcode** é uma \_ página fixa do MXDCOP PRINTTICKET \_ \_ :

-   O parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) consiste na estrutura T do **\_ \_ cabeçalho de \_ escape MXDC** e em uma estrutura [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) concatenada em uma estrutura [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) .
-   A chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve ocorrer entre uma chamada para [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e uma chamada para [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).

Quando **opcode** é MXDCOP, \_ defina \_ S0PAGE:

-   O parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) consiste na estrutura T do **\_ \_ cabeçalho de \_ escape MXDC** e em uma estrutura [**MxdcS0PageData**](mxdcs0pagedata.md) concatenada em uma estrutura [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) .
-   A chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve ocorrer entre uma chamada para [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e uma chamada para [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).
-   O aplicativo de chamada é responsável por validar o XML.
-   O consumo de streaming será mais eficiente se você chamar [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com \_ \_ o recurso MXDCOP Set S0PAGE \_ como **opcode** para cada recurso na página antes de chamá-lo com MXDCOP \_ set \_ S0PAGE.

Quando **opcode** é MXDCOP, \_ defina o \_ \_ recurso S0PAGE:

-   O parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) consiste na estrutura T do **\_ \_ cabeçalho de \_ escape MXDC** e em uma estrutura [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md) concatenada em uma estrutura [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md) .
-   A chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve ocorrer entre uma chamada para [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e uma chamada para [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage), mas pode haver várias chamadas entre as chamadas **Startpage** e **EndPage** .
-   O consumo de streaming será mais eficiente se você chamar [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com \_ \_ o recurso MXDCOP Set S0PAGE \_ como **opcode** para cada recurso na página antes de chamá-lo com MXDCOP \_ set \_ S0PAGE.

Quando **opcode** é MXDCOP, \_ defina o \_ \_ modo XPSPASSTHRU:

-   O parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) consiste apenas na estrutura T do **\_ \_ cabeçalho de \_ escape MXDC** .
-   Essa chamada deve ocorrer antes da chamada para [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).

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

 

