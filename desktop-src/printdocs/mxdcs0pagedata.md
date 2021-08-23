---
description: A estrutura MXDC S0PAGE DATA T contém uma página de documento XPS a ser passada para o arquivo de saída do \_ \_ \_ MXDC (Conversor de Documentos) do Microsoft XPS sem nenhum processamento.
ms.assetid: 3dc8e0b9-cf63-4345-93d2-3b60dac42546
title: MXDC_S0PAGE_DATA_T (Mxdc.h)
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
ms.openlocfilehash: 1ff54325859acef6da136c4bce20286bc7c746d8880d8994ca834213adf57b58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776546"
---
# <a name="mxdc_s0page_data_t-structure"></a>Estrutura T de \_ DADOS S0PAGE \_ \_ do MXDC

A **estrutura MXDC \_ S0PAGE \_ DATA \_ T** contém uma página de documento XPS a ser passada para o arquivo de saída do MXDC (Conversor de Documentos) do Microsoft XPS sem nenhum processamento.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMxdcS0PageData {
  ULONG dwSize;
  BYTE  bData[1];
} MXDC_S0PAGE_DATA_T, *P_MXDC_S0PAGE_DATA_T;
```



## <a name="members"></a>Membros

<dl> <dt>

**Dwsize**
</dt> <dd>

O tamanho do buffer de saída, **bData.**

</dd> <dt>

**bData**
</dt> <dd>

A página do documento XPS.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é anexada a uma estrutura T do [**\_ \_ HEADER \_ T**](mxdcescapeheader.md) de ESCAPE do MXDC (que tem seu **opCode** definido como MXDCOP SET S0PAGE) para criar uma estrutura T de ESCAPE DE PASSAGEM DE \_ \_ [**\_ S0PAGE \_ \_ \_ do MXDC.**](mxdcs0pagepassthroughescape.md) Essa estrutura é então passada para o *parâmetro lpszInData* da [**função ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando ela é chamada com [**MXDC \_ ESCAPE**](mxdc-escape.md) como escape. O resultado é que o MXDC passa a página para a saída sem processá-la.

A chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve estar entre uma chamada para [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e uma chamada para [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).

O aplicativo de chamada é responsável por validar o XML da página do documento XPS.

O consumo de streaming será mais eficiente se você chamar [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com **MXDCOP \_ SET \_ S0PAGE \_ RESOURCE** como **opCode** para cada recurso na página antes de chamá-lo com **MXDCOP \_ SET \_ S0PAGE**.

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

 

