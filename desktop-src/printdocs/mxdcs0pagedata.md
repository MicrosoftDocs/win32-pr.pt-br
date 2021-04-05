---
description: A \_ estrutura de T de dados MXDC S0PAGE \_ \_ contém uma página de documento XPS a ser passada para o arquivo de saída do Microsoft XPS Document Converter (MXDC) sem nenhum processamento.
ms.assetid: 3dc8e0b9-cf63-4345-93d2-3b60dac42546
title: Estrutura de MXDC_S0PAGE_DATA_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 2da9df454b8741f2203072fd25856118407ef5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662569"
---
# <a name="mxdc_s0page_data_t-structure"></a>\_Estrutura de \_ T de dados MXDC S0PAGE \_

A estrutura de **\_ T de \_ dados \_ MXDC S0PAGE** contém uma página de documento XPS a ser passada para o arquivo de saída do Microsoft XPS Document Converter (MXDC) sem nenhum processamento.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMxdcS0PageData {
  ULONG dwSize;
  BYTE  bData[1];
} MXDC_S0PAGE_DATA_T, *P_MXDC_S0PAGE_DATA_T;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwSize**
</dt> <dd>

O tamanho do buffer de saída, **bData**.

</dd> <dt>

**bData**
</dt> <dd>

A página do documento XPS.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é anexada a uma [**estrutura \_ \_ \_ T de cabeçalho de escape MXDC**](mxdcescapeheader.md) (que tem seu **opcode** definido como MXDCOP \_ set \_ S0PAGE) para fazer uma estrutura t de [**passagem de S0PAGE de MXDC de \_ \_ \_ saída \_**](mxdcs0pagepassthroughescape.md) . Essa estrutura é passada para o parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando ela é chamada com [**MXDC \_ escape**](mxdc-escape.md) como o escape. O resultado é que o MXDC passa a página para a saída sem processá-la.

A chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve estar entre uma chamada para [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e uma chamada para [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).

O aplicativo de chamada é responsável por validar o XML da página do documento XPS.

O consumo de streaming será mais eficiente se você chamar [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com o **\_ recurso MXDCOP Set \_ \_ S0PAGE** como **opcode** para cada recurso na página antes de chamá-lo com **MXDCOP \_ set \_ S0PAGE**.

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

 

