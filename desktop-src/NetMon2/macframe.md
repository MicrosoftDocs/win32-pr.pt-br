---
description: A estrutura MACFRAME é uma União dos protocolos iniciais mais comuns.
ms.assetid: ec7e3a54-a47f-4390-a137-9574c63c9a11
title: MACFRAME Union (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MACFRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a7901daf467a63586543c52ca8a214d5d0094982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769304"
---
# <a name="macframe-union"></a>MACFRAME Union

A estrutura **MACFRAME** é uma União dos protocolos iniciais mais comuns.

## <a name="syntax"></a>Sintaxe


```C++
typedef union {
  LPBYTE      MacHeader;
  LPETHERNET  Ethernet;
  LPTOKENRING Tokenring;
  LPFDDI      Fddi;
} MACFRAME, *LPMACFRAME;
```



## <a name="members"></a>Membros

<dl> <dt>

**MacHeader**
</dt> <dd>

Ponteiro genérico para um quadro.

</dd> <dt>

**Ethernet**
</dt> <dd>

Ponteiro Ethernet para um quadro.

</dd> <dt>

**Tokenring**
</dt> <dd>

Ponteiro de token ring para um quadro.

</dd> <dt>

**FDDI**
</dt> <dd>

Ponteiro FDDI para um quadro.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada com mais frequência como uma sobreposição. Para tornar as propriedades do primeiro protocolo acessíveis, converta o quadro como o mesmo tipo do protocolo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




