---
title: WMDRM_ENCRYPT_SCATTER_BLOCK estrutura (Wmdrmsdk.h)
description: A estrutura WMDRM \_ ENCRYPT SCATTER BLOCK contém um bloco de dados a serem \_ \_ criptografados.
ms.assetid: 73c871f0-3d0d-480f-856c-0f7d5dde5895
keywords:
- WMDRM_ENCRYPT_SCATTER_BLOCK formato de mídia do Windows
- formato de mídia de janelas de estrutura
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_BLOCK
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 258cb7e0d8d2cac8da40197aaa45028a56af0ff3a313d65c1a98c50d45b8d3b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658156"
---
# <a name="wmdrm_encrypt_scatter_block-structure"></a>Estrutura WMDRM \_ ENCRYPT \_ SCATTER \_ BLOCK

A **estrutura WMDRM \_ ENCRYPT SCATTER \_ \_ BLOCK** contém um bloco de dados a serem criptografados.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_BLOCK {
  DWORD dwStreamID;
  DWORD cbBlock;
  BYTE  *pbBlock;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwStreamID**
</dt> <dd>

Identificador do fluxo ao qual o bloco de dados pertence.

</dd> <dt>

**cbBlock**
</dt> <dd>

Tamanho do bloco em bytes.

</dd> <dt>

**pbBlock**
</dt> <dd>

Ponteiro para um buffer que contém o bloco de dados.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada pelo método [**IWMDRMEncryptScatter::EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md) para identificar blocos de dados a criptografar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





