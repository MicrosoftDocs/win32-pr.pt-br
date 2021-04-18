---
title: Estrutura de WMDRM_ENCRYPT_SCATTER_BLOCK (wmdrmsdk. h)
description: A \_ \_ \_ estrutura de bloco de dispersão de criptografia WMDRM contém um bloco de dados a ser criptografado.
ms.assetid: 73c871f0-3d0d-480f-856c-0f7d5dde5895
keywords:
- Formato de mídia do Windows de estrutura de WMDRM_ENCRYPT_SCATTER_BLOCK
- estruturar formato de mídia do Windows
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
ms.openlocfilehash: 8911ba1822b146de4a99ff1fe144afcfd8e212e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788791"
---
# <a name="wmdrm_encrypt_scatter_block-structure"></a>\_Estrutura de \_ bloco de dispersas do WMDRM Encrypt \_

A estrutura de **\_ \_ \_ bloco de dispersão de criptografia WMDRM** contém um bloco de dados a ser criptografado.

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

Essa estrutura é usada pelo método [**IWMDRMEncryptScatter:: EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md) para identificar blocos de dados a serem criptografados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





