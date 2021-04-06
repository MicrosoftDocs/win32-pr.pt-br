---
description: A \_ \_ estrutura T do recurso MXDC XPS S0PAGE \_ \_ contém informações sobre um recurso, como uma imagem ou uma fonte, que está associada a uma página de documento XPS e que deve ser passada para o arquivo de saída do Microsoft XPS Document Converter (MXDC).
ms.assetid: af0690a6-3047-4e95-b719-2305948c0f5d
title: Estrutura de MXDC_XPS_S0PAGE_RESOURCE_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_XPS_S0PAGE_RESOURCE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 90f8a52ed3bd1bcba4c8f21a086627781bdbbf67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828765"
---
# <a name="mxdc_xps_s0page_resource_t-structure"></a>\_Estrutura MXDC XPS \_ S0PAGE \_ Resource \_ T

A **estrutura \_ \_ T do \_ recurso \_ MXDC XPS S0PAGE** contém informações sobre um recurso, como uma imagem ou uma fonte, que está associada a uma página de documento XPS e que deve ser passada para o arquivo de saída do Microsoft XPS Document Converter (MXDC).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMxdcXpsS0PageResource {
  DWORD dwSize;
  DWORD dwResourceType;
  BYTE  szUri[MAX_PATH];
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_XPS_S0PAGE_RESOURCE_T, *P_MXDC_XPS_S0PAGE_RESOURCE_T;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwSize**
</dt> <dd>

O tamanho total dessa estrutura e o recurso para o qual ela aponta.

</dd> <dt>

**dwResourceType**
</dt> <dd>

Um valor do tipo [**\_ \_ \_ enums de página MXDC S0**](mxdcs0pageenums.md) indicando o tipo de recurso, como imagem TIFF ou fonte TrueType.

</dd> <dt>

**szUri**
</dt> <dd>

O URI do recurso. Isso não pode ter mais de 260 bytes.

</dd> <dt>

**dwDataSize**
</dt> <dd>

O tamanho do recurso em bytes.

</dd> <dt>

**bData**
</dt> <dd>

Os dados do recurso em uma matriz de bytes com tamanho 1 + o tamanho do recurso.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é anexada a uma [**estrutura \_ \_ \_ T do cabeçalho de escape MXDC**](mxdcescapeheader.md) (que tem seu **opcode** definido como **MXDCOP \_ set \_ S0PAGERESOURCE**) para tornar uma estrutura de [**\_ \_ \_ escape \_ t do recurso MXDC S0PAGE**](mxdcs0pageresourceescape.md) . A estrutura de **MXDC de \_ \_ \_ escape \_ de recurso S0PAGE** resultante é passada no parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) que é chamada com o escape de [**\_ escape MXDC**](mxdc-escape.md) . O efeito é enviar o recurso para o MXDC para conversão e para ser gravado no arquivo de saída.

A chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve estar entre uma chamada para [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e uma chamada para [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); no entanto, pode haver mais de uma dessas chamadas entre as chamadas para **Startpage** e **EndPage**.

O consumo de streaming será mais eficiente se você chamar [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com o **opcode** do **\_ recurso MXDCOP Set \_ S0PAGE \_** para cada recurso na página antes de chamar **ExtEscape** com o **opcode** MXDCOP **\_ set \_ S0PAGE** .

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

 

