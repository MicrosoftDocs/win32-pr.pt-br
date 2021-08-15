---
description: A estrutura MACFRAME é uma união dos protocolos iniciais mais comuns.
ms.assetid: ec7e3a54-a47f-4390-a137-9574c63c9a11
title: União MACFRAME (Netmon.h)
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
ms.openlocfilehash: dcff7294d2800e797b43b3a05bd25c35418c6fb466c95130b97be73f25040d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364704"
---
# <a name="macframe-union"></a>União do MACFRAME

A **estrutura MACFRAME** é uma união dos protocolos iniciais mais comuns.

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

**Tokening**
</dt> <dd>

Ponteiro de anel de token para um quadro.

</dd> <dt>

**Fddi**
</dt> <dd>

Ponteiro FDDI para um quadro.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada com mais frequência como uma sobreposição. Para tornar as propriedades do primeiro protocolo acessíveis, caste o quadro como o mesmo tipo que o protocolo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




