---
description: A estrutura T do MXDC S0PAGE RESOURCE ESCAPE é uma estrutura T do MXDC ESCAPE HEADER concatenada com uma estrutura \_ \_ \_ \_ \_ \_ \_ MXDC \_ XPS \_ S0PAGE \_ RESOURCE \_ T.
ms.assetid: e5caa280-f0a5-4a89-b4f1-4f195a537dc6
title: MXDC_S0PAGE_RESOURCE_ESCAPE_T (Mxdc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_RESOURCE_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 1b7e937c28d3eb685770b2eac834c16dd629406a3c12850bc4414722f7796ba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118056330"
---
# <a name="mxdc_s0page_resource_escape_t-structure"></a>Estrutura T do MXDC \_ S0PAGE \_ RESOURCE \_ ESCAPE \_

A estrutura T do **MXDC \_ S0PAGE \_ RESOURCE \_ ESCAPE \_** é uma estrutura T do [**MXDC \_ ESCAPE \_ HEADER \_ concatenada**](mxdcescapeheader.md) com uma estrutura [**MXDC \_ XPS \_ S0PAGE \_ RESOURCE \_ T.**](mxdcxpss0pageresource.md)

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMxdcS0PageResourceEscape {
  MXDC_ESCAPE_HEADER_T       mxdcEscape;
  MXDC_XPS_S0PAGE_RESOURCE_T xpsS0PageResourcePassthrough;
} MXDC_S0PAGE_RESOURCE_ESCAPE_T, *P_MXDC_S0PAGE_RESOURCE_ESCAPE_T;
```



## <a name="members"></a>Membros

<dl> <dt>

**mxdcEscape**
</dt> <dd>

Uma [**estrutura T do MXDC ESCAPE \_ \_ HEADER \_**](mxdcescapeheader.md) com seu membro **opCode** definido como MXDCOP \_ SET \_ \_ S0PAGE RESOURCE.

</dd> <dt>

**xpsS0PageResourcePassthrough**
</dt> <dd>

Uma [**estrutura MXDC \_ XPS \_ S0PAGE \_ RESOURCE \_ T**](mxdcxpss0pageresource.md) que representa um recurso, como uma fonte ou arquivo de imagem, em uma página de documento XPS.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é passada no parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando essa função é chamada com o escape [**\_ escape do MXDC,**](mxdc-escape.md) e o membro **opCode** da estrutura T do [**MXDC \_ ESCAPE \_ HEADER \_ é**](mxdcescapeheader.md) **MXDCOP \_ SET \_ S0PAGE \_ RESOURCE**. O resultado é um recurso de página a ser enviado para o MXDC.

Alocar memória para o escape, conforme mostrado abaixo, definir os campos conforme necessário e, em seguida, chamar [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_RESOURCE_ESCAPE_T) + 
                        iS0PageResourceDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_RESOURCE_ESCAPE_T pS0PageResourceEscapeData = 
                        (P_MXDC_S0PAGE_RESOURCE_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



A chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve estar entre uma chamada para [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e uma chamada para [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); no entanto, pode haver mais de uma dessas chamadas entre as chamadas para **StartPage** **e EndPage**.

O consumo de streaming será mais eficiente se você chamar [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com o **opCode** **MXDCOP \_ SET \_ S0PAGE \_ RESOURCE** para cada recurso na página antes de chamar **ExtEscape** com o **opCode** **MXDCOP \_ SET \_ S0PAGE**.  

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

 

