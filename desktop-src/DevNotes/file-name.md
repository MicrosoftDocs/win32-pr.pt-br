---
description: Representa um atributo de nome de arquivo. Um arquivo tem um atributo de nome de arquivo para cada diretório no qual ele é inserido.
ms.assetid: 54458eee-b786-446c-80bd-213c13bdeb4a
title: FILE_NAME estrutura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_NAME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9b09b9c58228c9028a5ac9d26d834bdc21a5c02201338767af84dc713bc3aa60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076140"
---
# <a name="file_name-structure"></a>Estrutura NOME \_ DO ARQUIVO

\[Essa estrutura é válida somente para a versão 3 dos volumes NTFS; ele pode ser alterado em versões futuras.\]

Representa um atributo de nome de arquivo. Um arquivo tem um atributo de nome de arquivo para cada diretório no qual ele é inserido.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _FILE_NAME {
  FILE_REFERENCE ParentDirectory;
  UCHAR          Reserved[0x38];
  UCHAR          FileNameLength;
  UCHAR          Flags;
  WCHAR          FileName[1];
} FILE_NAME, *PFILE_NAME;
```



## <a name="members"></a>Membros

<dl> <dt>

**ParentDirectory**
</dt> <dd>

Uma referência de arquivo ao diretório que indexa esse nome. Consulte [**REFERÊNCIA DE SEGMENTO \_ MFT \_**](mft-segment-reference.md).

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**FileNameLength**
</dt> <dd>

O comprimento do nome do arquivo, em caracteres Unicode.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Os sinalizadores de nome de arquivo.

<dl> <dt>

<span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**ARQUIVO \_ NAME \_ NTFS** (0x01)
</dt> <dt>

<span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**ARQUIVO \_ \_NOME DOS** (0x02)
</dt> </dl> </dd> <dt>

**FileName**
</dt> <dd>

O primeiro caractere do nome do arquivo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Observe que não há nenhum arquivo de header associado para essa estrutura.

Essa definição de estrutura é válida somente para a versão principal 3 e a versão secundária 0 ou 1, conforme relatado por [**FSCTL \_ GET \_ NTFS \_ VOLUME \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tabela de arquivos mestre](master-file-table.md)
</dt> </dl>

 

 
