---
description: A \_ \_ estrutura t de escape de passagem MXDC S0PAGE \_ \_ é uma \_ estrutura t de cabeçalho de escape MXDC \_ \_ concatenada com uma \_ estrutura de \_ f Data T MXDC S0PAGE \_ .
ms.assetid: 949c1ed4-92d5-4c11-a7da-f9d94bafe3f8
title: Estrutura de MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: f8e0a46766f38aec16758a1efc9c0cbc775c2131b1279dcc47f92ed41e77c0e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099050"
---
# <a name="mxdc_s0page_passthrough_escape_t-structure"></a>\_ \_ \_ Estrutura T de escape de passagem MXDC S0PAGE \_

A **estrutura \_ \_ t de \_ escape \_ de passagem MXDC S0PAGE** é uma estrutura [**\_ \_ \_ t de cabeçalho de escape MXDC**](mxdcescapeheader.md) concatenada com uma estrutura de [**\_ \_ f Data \_ T MXDC S0PAGE**](mxdcs0pagedata.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMxdcS0PagePassthroughEscape {
  MXDC_ESCAPE_HEADER_T mxdcEscape;
  MXDC_S0PAGE_DATA_T   xpsS0PageData;
} MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T, *P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T;
```



## <a name="members"></a>Membros

<dl> <dt>

**mxdcEscape**
</dt> <dd>

Uma [**estrutura \_ \_ \_ T de cabeçalho de escape MXDC**](mxdcescapeheader.md) com seu membro **opcode** definido como **MXDCOP \_ set \_ S0PAGE**.

</dd> <dt>

**xpsS0PageData**
</dt> <dd>

Uma estrutura [**MxdcS0PageData**](mxdcs0pagedata.md) que representa uma página de documento XPS.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é passada no parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando ela é chamada com o escape de [**escape \_ MXDC**](mxdc-escape.md) e o membro **opcode** da estrutura [**T do \_ \_ cabeçalho de \_ escape MXDC**](mxdcescapeheader.md) é **MXDCOP \_ set \_ S0PAGE**. O resultado é que o conversor de documento XML da Microsoft (MXDC) passa a página para a impressora sem processá-la.

Aloque memória para o escape, conforme mostrado abaixo, defina os campos conforme necessário e, em seguida, chame [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



A chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve estar entre uma chamada para [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e uma chamada para [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).

O aplicativo de chamada é responsável por validar o XML da página do documento XPS.

O consumo de streaming será mais eficiente se você chamar [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com o **\_ recurso MXDCOP Set \_ \_ S0PAGE** como **opcode** para cada recurso na página antes de chamá-lo com **MXDCOP \_ set \_ S0PAGE**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                    |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Mxdc. h</dt> </dl> |



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

 

