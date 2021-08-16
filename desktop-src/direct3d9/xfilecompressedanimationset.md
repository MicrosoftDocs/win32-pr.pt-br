---
description: Identifica dados de animação de quadro chave compactados.
ms.assetid: 2aab46db-e0ad-4bbb-b1c5-a254ec6cb984
title: Estrutura XFILECOMPRESSEDANIMATIONSET (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XFILECOMPRESSEDANIMATIONSET
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 41c64ae7bb2ca4acf87e1b63de90f2ccfc78e8d769adf334aa1f68b9bf79de0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518553"
---
# <a name="xfilecompressedanimationset-structure"></a>Estrutura XFILECOMPRESSEDANIMATIONSET

Identifica dados de animação de quadro chave compactados.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct XFILECOMPRESSEDANIMATIONSET {
  DWORD CompressedBlockSize;
  FLOAT TicksPerSec;
  DWORD PlaybackType;
  DWORD BufferLength;
} XFILECOMPRESSEDANIMATIONSET, *LPXFILECOMPRESSEDANIMATIONSET;
```



## <a name="members"></a>Membros

<dl> <dt>

**CompressedBlockSize**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamanho total, em bytes, dos dados compactados no buffer de dados da animação do quadro chave compactado.

</dd> <dt>

**TicksPerSec**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de tiques de quadros-chave de animação que ocorrem por segundo.

</dd> <dt>

**Reproduztype**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Tipo do loop de reprodução do conjunto de animações. Consulte [**\_ tipo de D3DXPLAYBACK**](./d3dxplayback-type.md).

</dd> <dt>

**BufferLength**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

O tamanho mínimo do buffer, em bytes, necessário para manter os dados da animação do quadro chave compactado. Valor é igual a ((CompressedBlockSize + 3)/4).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de arquivo D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> <dt>

[**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md)
</dt> </dl>

 

 
