---
description: Contém um vetor de inicialização (IV) para CTR de 128 bits criptografia AES modo de criptografia de codificação de bloco (AES-CTR).
ms.assetid: 2ee738c2-d56c-4a50-94b8-b7180918aa8c
title: Estrutura de D3DAES_CTR_IV (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAES_CTR_IV
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 09535b432ff1af60ad33b622810d0d8a4d190cb81650214aa71b445ba3c22f4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974785"
---
# <a name="d3daes_ctr_iv-structure"></a>\_Estrutura D3DAES CTR \_ IV

Contém um vetor de inicialização (IV) para CTR de 128 bits criptografia AES modo de criptografia de codificação de bloco (AES-CTR).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DAES_CTR_IV {
  UINT64 IV;
  UINT64 Count;
} D3DAES_CTR_IV;
```



## <a name="members"></a>Membros

<dl> <dt>

**IV**
</dt> <dd>

O IV, no formato big-endian.

</dd> <dt>

**Count**
</dt> <dd>

A contagem de blocos, no formato big-endian.

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura **D3DAES \_ CTR \_ IV** e a estrutura [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) são equivalentes.

Para obter detalhes, consulte [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv).

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

 

 




