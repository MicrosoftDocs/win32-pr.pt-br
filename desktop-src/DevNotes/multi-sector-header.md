---
description: Representa o cabeçalho de multisetor.
ms.assetid: 0fad0e93-b940-4b52-be16-c5f177884dfb
title: Estrutura de MULTI_SECTOR_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MULTI_SECTOR_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9e34e23d3d2bf2ecfbc1c668e02c177e4d1516c73acabccc88aa7190ec33e211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667213"
---
# <a name="multi_sector_header-structure"></a>Estrutura de cabeçalho de vários \_ setores \_

\[Essa estrutura é válida somente para a versão 3 de volumes NTFS; Ele pode ser alterado em versões futuras.\]

Representa o cabeçalho de multisetor.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _MULTI_SECTOR_HEADER {
  UCHAR  Signature[4];
  USHORT UpdateSequenceArrayOffset;
  USHORT UpdateSequenceArraySize;
} MULTI_SECTOR_HEADER, *PMULTI_SECTOR_HEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**Signature**
</dt> <dd>

A assinatura. Esse valor é uma conveniência para o usuário.

</dd> <dt>

**UpdateSequenceArrayOffset**
</dt> <dd>

O deslocamento para a matriz de sequência de atualização, desde o início desta estrutura. A matriz de sequência de atualização deve terminar antes do último valor USHORT no primeiro setor.

</dd> <dt>

**UpdateSequenceArraySize**
</dt> <dd>

O tamanho da matriz de sequência de atualização, em bytes.

</dd> </dl>

## <a name="remarks"></a>Comentários

Observe que não há nenhum arquivo de cabeçalho associado para essa estrutura.

Essa definição de estrutura é válida somente para a versão principal 3 e secundária 0 ou 1, conforme relatado [**pelo \_ fsctl \_ obter \_ \_ dados de volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

O cabeçalho multisetor e a matriz de sequência de atualização fornecem detecção de transferências de vários setores incompletas para dispositivos que têm um tamanho de setor físico maior ou igual ao número de sequência Stride (512) ou que não transferem os setores fora de ordem. Se existir um dispositivo que tenha um tamanho de setor menor do que o stride do número de sequência e, às vezes, transferir os setores fora de ordem, a matriz de sequência de atualização não fornecerá a detecção absoluta de transferências incompletas. O stride do número de sequência é definido como um número pequeno o suficiente para fornecer proteção absoluta para todos os discos rígidos conhecidos. Ele não está definido como menor ou pode haver excesso de tempo de execução ou sobrecarga de espaço.

A matriz de sequência de atualização consiste em uma matriz de *n* valores **UShort** , em que *n* é o tamanho da estrutura que está sendo protegida dividida pelo Stride do número de sequência. A primeira palavra contém o número de sequência de atualização, que é um contador cíclico do número de vezes que a estrutura que contém foi gravada no disco. Em seguida, estão os *n* valores **UShort** salvos que foram substituídos pelo número de sequência de atualização na última vez em que a estrutura que a contém foi gravada no disco.

Cada vez que a estrutura protegida está prestes a ser gravada no disco, a última palavra em cada Stride de número de sequência é salva em sua respectiva posição na matriz de números de sequência e, em seguida, é substituída pelo próximo número de sequência de atualização. Após a gravação, ou sempre que a estrutura for lida, a palavra salva da matriz de números de sequência será restaurada para sua posição real na estrutura. Antes de restaurar as palavras salvas em leituras, todos os números de sequência no final de cada Stride são comparados com o número de sequência real no início da matriz. Se qualquer uma dessas comparações não for igual, uma transferência de multisetor com falha será detectada.

O tamanho da matriz é determinado pelo tamanho da estrutura que a contém. A matriz de sequência de atualização deve ser incluída no final do cabeçalho da estrutura que está sendo protegida devido a seu tamanho variável. O usuário deve garantir que o espaço correto seja reservado para a estrutura recipiente: (tamanho da estrutura/512 + 1) \* sizeof (UShort).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tabela de arquivos mestre](master-file-table.md)
</dt> </dl>

 

 
