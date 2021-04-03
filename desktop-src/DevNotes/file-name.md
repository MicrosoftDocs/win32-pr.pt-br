---
description: Representa um atributo de nome de arquivo. Um arquivo tem um atributo de nome de arquivo para cada diretório no qual é inserido.
ms.assetid: 54458eee-b786-446c-80bd-213c13bdeb4a
title: Estrutura de FILE_NAME
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
ms.openlocfilehash: 609725c21f0c0811a4222cd9dfd662b3e25673f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010089"
---
# <a name="file_name-structure"></a>Estrutura de nome de arquivo \_

\[Essa estrutura é válida somente para a versão 3 de volumes NTFS; Ele pode ser alterado em versões futuras.\]

Representa um atributo de nome de arquivo. Um arquivo tem um atributo de nome de arquivo para cada diretório no qual é inserido.

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

Uma referência de arquivo para o diretório que indexa para esse nome. Consulte [**\_ \_ referência de segmento de MFT**](mft-segment-reference.md).

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

<span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>Do **arquivo \_ NOME \_ NTFS** (0x01)
</dt> <dt>

<span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>Do **arquivo \_ NOME \_ dos** (0x02)
</dt> </dl> </dd> <dt>

**FileName**
</dt> <dd>

O primeiro caractere do nome do arquivo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Observe que não há nenhum arquivo de cabeçalho associado para essa estrutura.

Essa definição de estrutura é válida somente para a versão principal 3 e secundária 0 ou 1, conforme relatado [**pelo \_ fsctl \_ obter \_ \_ dados de volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tabela de arquivos mestre](master-file-table.md)
</dt> </dl>

 

 
