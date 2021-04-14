---
description: A estrutura ADDRESStable contém uma tabela de pares de endereços.
ms.assetid: 84577b6c-9d43-4e53-9f8d-33685329b11d
title: Estrutura de ADDRESStable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 41acab19f83fdcc88a384c0407b666a7f641a598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461230"
---
# <a name="addresstable-structure"></a>Estrutura de endereço de endereçamento

A estrutura **AddressTable** contém uma tabela de pares de endereços.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _ADDRESSTABLE {
  DWORD       nAddressPairs;
  DWORD       nNonMacAddressPairs;
  ADDRESSPAIR AddressPair[MAX_ADDRESS_PAIRS];
} ADDRESSTABLE, *LPADDRESSTABLE;
```



## <a name="members"></a>Membros

<dl> <dt>

**nAddressPairs**
</dt> <dd>

Número de pares de endereços na matriz **AddressPair** .

</dd> <dt>

**nNonMacAddressPairs**
</dt> <dd>

Número de pares de endereços não MAC.

</dd> <dt>

**AddressPair**
</dt> <dd>

Matriz de pares de endereços. Observe que você só pode armazenar até oito pares de endereços por estrutura de endereço.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use essa estrutura como parte do processo de construção do filtro de captura. Para obter mais informações sobre como implementar essa estrutura, consulte [filtros de captura](capture-filters.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ADDRESSPAIR](addresspair.md)
</dt> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




