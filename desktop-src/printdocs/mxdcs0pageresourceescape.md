---
description: A \_ estrutura t de escape de recursos do MXDC S0PAGE \_ \_ \_ é uma \_ estrutura t de cabeçalho de escape MXDC \_ \_ concatenada com uma \_ estrutura de \_ \_ f Resource T MXDC XPS S0PAGE \_ .
ms.assetid: e5caa280-f0a5-4a89-b4f1-4f195a537dc6
title: Estrutura de MXDC_S0PAGE_RESOURCE_ESCAPE_T (Mxdc. h)
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
ms.openlocfilehash: ed1d78aad1ede2a318dcde2d3a2d39fd8e666ddc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169458"
---
# <a name="mxdc_s0page_resource_escape_t-structure"></a>\_Estrutura T MXDC S0PAGE de \_ recursos de \_ escape \_

A **estrutura \_ \_ t de \_ escape \_ de recursos do MXDC S0PAGE** é uma estrutura [**\_ \_ \_ t de cabeçalho de escape MXDC**](mxdcescapeheader.md) concatenada com uma estrutura de [**\_ \_ \_ f Resource \_ T MXDC XPS S0PAGE**](mxdcxpss0pageresource.md) .

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

Uma [**estrutura \_ \_ \_ T de cabeçalho de escape MXDC**](mxdcescapeheader.md) com seu membro **opcode** definido como MXDCOP \_ set \_ S0PAGE \_ Resource.

</dd> <dt>

**xpsS0PageResourcePassthrough**
</dt> <dd>

Uma estrutura [**T do MXDC \_ XPS \_ S0PAGE \_ \_**](mxdcxpss0pageresource.md) que representa um recurso, como um arquivo de fonte ou imagem, em uma página de documento XPS.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é passada no parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando essa função é chamada com o escape de [**escape \_ MXDC**](mxdc-escape.md) e o membro **opcode** da estrutura T do [**\_ cabeçalho de \_ escape \_ MXDC**](mxdcescapeheader.md) é **MXDCOP \_ \_ \_ recurso S0PAGE**. O resultado é um recurso de página a ser enviado para o MXDC.

Aloque memória para o escape, conforme mostrado abaixo, defina os campos conforme necessário e, em seguida, chame [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).


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



A chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve estar entre uma chamada para [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e uma chamada para [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); no entanto, pode haver mais de uma dessas chamadas entre as chamadas para **Startpage** e **EndPage**.

O consumo de streaming será mais eficiente se você chamar [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com o **opcode** do **\_ recurso MXDCOP Set \_ S0PAGE \_** para cada recurso na página antes de chamar **ExtEscape** com o **opcode** MXDCOP **\_ set \_ S0PAGE**.  

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

 

