---
description: Especifica quais bytes são criptografados em uma superfície de vídeo protegida.
ms.assetid: 076f4f00-e86b-47e2-80dd-4d7434200138
title: Estrutura de D3DENCRYPTED_BLOCK_INFO (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DENCRYPTED_BLOCK_INFO
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 94027dac3956376e32ad10cf7c1b600d9c65f3918e2781ab9da96d4d3891f43b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117879720"
---
# <a name="d3dencrypted_block_info-structure"></a>Estrutura de informações de \_ bloco D3DENCRYPTED \_

Especifica quais bytes são criptografados em uma superfície de vídeo protegida.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DENCRYPTED_BLOCK_INFO {
  UINT NumEncryptedBytesAtBeginning;
  UINT NumBytesInSkipPattern;
  UINT NumBytesInEncryptPattern;
} D3DENCRYPTED_BLOCK_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**NumEncryptedBytesAtBeginning**
</dt> <dd>

O número de bytes que são criptografados no início do buffer.

</dd> <dt>

**NumBytesInSkipPattern**
</dt> <dd>

O número de bytes que são ignorados após os primeiros **NumEncryptedBytesAtBeginning** bytes e depois de cada bloco de **NumBytesInEncryptPattern** bytes. Bytes ignorados não são criptografados.

</dd> <dt>

**NumBytesInEncryptPattern**
</dt> <dd>

O número de bytes que são criptografados após cada bloco de bytes ignorados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>D3d9types. h (incluir D3d9. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de vídeo do Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




