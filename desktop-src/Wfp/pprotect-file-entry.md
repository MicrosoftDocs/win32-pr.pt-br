---
description: Estrutura usada pela função SfcGetFiles.
ms.assetid: 958167e3-3eb3-406a-85bf-ffe2851a95a1
title: Estrutura de PPROTECT_FILE_ENTRY (sfcfiles. h)
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
ms.openlocfilehash: 98cda570a3677560d51800d58822d93a942847c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771553"
---
# <a name="pprotect_file_entry-structure"></a>Estrutura de entrada de \_ arquivo PPROTECT \_

\[Essa estrutura está disponível para uso nos sistemas operacionais especificados na seção requisitos. O suporte para essa estrutura foi removido no Windows Vista e no Windows Server 2008. Use as funções com suporte listadas em [funções WRP](wfp-functions.md) em vez disso.\]

Estrutura usada pela função [**SfcGetFiles**](sfcgetfiles.md) .

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

Ponteiro para um valor de cadeia de caracteres que contém o nome do arquivo de origem. Isso será **nulo** se o arquivo não for renomeado na instalação.

</dd> <dt>

**FileName**
</dt> <dd>

Ponteiro para o valor de cadeia de caracteres que contém o nome de arquivo de destino mais o caminho completo para o arquivo.

</dd> <dt>

**InfName**
</dt> <dd>

Ponteiro para o valor da cadeia de caracteres que contém o nome do arquivo INF que fornece informações de layout. Esse parâmetro pode ser **nulo** ao usar o layout padrão.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                 |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                        |
| parâmetro<br/>                   | <dl> <dt>Sfcfiles. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SfcGetFiles**](sfcgetfiles.md)
</dt> </dl>

 

 




