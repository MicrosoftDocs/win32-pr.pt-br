---
title: Estrutura de WINBIO_BIR_DATA (WinBio \_ Types. h)
description: Especifica o tamanho, em bytes, e o deslocamento de um bloco de informações biométricas.
ms.assetid: 2f73eb1f-f1a1-4831-a8f7-eec28aa51645
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_BIR_DATA
topic_type:
- apiref
api_name:
- WINBIO_BIR_DATA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01978cf55d90e217aa50fb8fad696f6af90b33ab9e59975a901daa99db633181
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911039"
---
# <a name="winbio_bir_data-structure"></a>\_Estrutura de \_ dados WINBIO Bir

A estrutura de **\_ \_ dados WINBIO Bir** especifica o tamanho, em bytes, e o deslocamento de um bloco de informações biométricas. Essa estrutura é usada pela estrutura [**WINBIO \_ Bir**](winbio-bir.md) para especificar onde as várias partes de um registro de informações biométricas estão localizadas.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WINBIO_BIR_DATA {
  ULONG Size;
  ULONG Offset;
} WINBIO_BIR_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**Tamanho**
</dt> <dd>

Tamanho, em bytes, das informações biométricas.

</dd> <dt>

**Deslocamento**
</dt> <dd>

Offset, em bytes do início da estrutura [**WINBIO \_ Bir**](winbio-bir.md) , das informações biométricas.

</dd> </dl>

## <a name="remarks"></a>Comentários

O uso de deslocamentos em vez de ponteiros permite uma fácil serialização do BIR e para uma tradução menos complicada entre os ambientes de 32 e 64 bits ou entre o modo de usuário e kernel.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de aplicativo cliente](client-application-structures.md)
</dt> <dt>

[**WINBIO \_ Bir**](winbio-bir.md)
</dt> <dt>

[**\_cabeçalho WINBIO Bir \_**](winbio-bir-header.md)
</dt> </dl>

 

 





