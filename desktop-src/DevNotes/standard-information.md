---
description: Contém o atributo de informações padrão. Esse atributo está presente em cada registro de arquivo base e deve ser residente.
ms.assetid: 8e668309-2722-4115-923d-bf0aa78d24f1
title: Estrutura de STANDARD_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STANDARD_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4927553ac593475f8659932468227362ae19fe59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010081"
---
# <a name="standard_information-structure"></a>\_Estrutura de informações padrão

\[Essa estrutura é válida somente para a versão 3 de volumes NTFS; Ele pode ser alterado em versões futuras.\]

Contém o atributo de informações padrão. Esse atributo está presente em cada registro de arquivo base e deve ser residente.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _STANDARD_INFORMATION {
  UCHAR Reserved[0x30];
  ULONG OwnerId;
  ULONG SecurityId;
} STANDARD_INFORMATION, *PSTANDARD_INFORMATION;
```



## <a name="members"></a>Membros

<dl> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**OwnerId**
</dt> <dd>

O identificador do proprietário do arquivo, do índice de segurança.

</dd> <dt>

**Securityid**
</dt> <dd>

O identificador de segurança do arquivo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Observe que não há nenhum arquivo de cabeçalho associado para essa estrutura.

Essa definição de estrutura é válida somente para a versão principal 3 e secundária 0 ou 1, conforme relatado [**pelo \_ fsctl \_ obter \_ \_ dados de volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tabela de arquivos mestre](master-file-table.md)
</dt> </dl>

 

 
