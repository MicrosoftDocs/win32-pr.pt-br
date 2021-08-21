---
description: Estrutura usada pela função SfcGetFiles.
ms.assetid: 958167e3-3eb3-406a-85bf-ffe2851a95a1
title: PPROTECT_FILE_ENTRY estrutura (Sfcfiles.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PPROTECT_FILE_ENTRY
api_type:
- HeaderDef
api_location:
- Sfcfiles.h
ms.openlocfilehash: c9070290170febf08e532b071812600fb0ef8755302a4bd1603858659196d0c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053194"
---
# <a name="pprotect_file_entry-structure"></a>Estrutura PPROTECT \_ FILE \_ ENTRY

\[Essa estrutura está disponível para uso nos sistemas operacionais especificados na seção Requisitos. O suporte para essa estrutura foi removido no Windows Vista e Windows Server 2008. Em vez disso, use as funções com suporte listadas [no WRP Functions.](wfp-functions.md)\]

Estrutura usada pela [**função SfcGetFiles.**](sfcgetfiles.md)

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PPROTECT_FILE_ENTRY {
  PWSTR SourceFileName;
  PWSTR FileName;
  PWSTR InfName;
} PPROTECT_FILE_ENTRY, *PPPROTECT_FILE_ENTRY;
```



## <a name="members"></a>Membros

<dl> <dt>

**SourceFileName**
</dt> <dd>

Ponteiro para um valor de cadeia de caracteres que contém o nome do arquivo de origem. Isso será **NULL se** o arquivo não for renomeado na instalação.

</dd> <dt>

**FileName**
</dt> <dd>

Ponteiro para o valor da cadeia de caracteres que contém o nome do arquivo de destino mais o caminho completo para o arquivo.

</dd> <dt>

**InfName**
</dt> <dd>

Ponteiro para o valor da cadeia de caracteres que contém o nome do arquivo INF que fornece informações de layout. Esse parâmetro pode ser **NULL** ao usar o layout padrão.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                 |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                        |
| Cabeçalho<br/>                   | <dl> <dt>Sfcfiles.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SfcGetFiles**](sfcgetfiles.md)
</dt> </dl>

 

 




