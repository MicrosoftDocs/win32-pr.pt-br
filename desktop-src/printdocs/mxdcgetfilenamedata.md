---
description: A \_ estrutura MXDC get \_ filename \_ Data \_ T contém o caminho completo e o nome do arquivo de um arquivo de saída do conversor de documento XPS da Microsoft (MXDC).
ms.assetid: 070bce2e-5055-47e8-9412-2094a636635f
title: Estrutura de MXDC_GET_FILENAME_DATA_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_GET_FILENAME_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: dd29696ae21924f245e508469acfbb88c78b034b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828311"
---
# <a name="mxdc_get_filename_data_t-structure"></a>MXDC \_ obter \_ nome de arquivo \_ Data \_ T estrutura

A estrutura **MXDC \_ Get \_ filename \_ Data \_ T** contém o caminho completo e o nome do arquivo de um arquivo de saída do conversor de documento XPS da Microsoft (MXDC).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _tagMxdcGetFileNameData {
  ULONG   cbOutput;
  wchar_t wszData[1];
} MXDC_GET_FILENAME_DATA_T, *P_MXDC_GET_FILENAME_DATA_T;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbOutput**
</dt> <dd>

O tamanho do buffer de saída, **wszData**.

</dd> <dt>

**wszData**
</dt> <dd>

O caminho totalmente qualificado e o nome de arquivo do arquivo de saída.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é retornada por [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando chamada com o escape de [**escape \_ MXDC**](mxdc-escape.md) e a estrutura [**\_ T de \_ cabeçalho \_ de escape MXDC**](mxdcescapeheader.md) que é passada no parâmetro *lpszInData* tem seu **opcode** definido como **MXDCOP \_ Get \_ filename**.

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

 

