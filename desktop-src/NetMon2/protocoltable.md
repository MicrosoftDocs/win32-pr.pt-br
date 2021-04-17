---
description: A estrutura de PROTOCOLtable contém uma lista de protocolos.
ms.assetid: dad2b228-5916-44fe-b78e-ebc6507dc555
title: Estrutura de PROTOCOLtable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3ad79beca7ce79611747a02704ffc05da5fc3d4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759356"
---
# <a name="protocoltable-structure"></a>Estrutura de PROTOCOLtable

A estrutura de **protocoltable** contém uma lista de protocolos.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PROTOCOLTABLE {
  DWORD     nProtocols;
  HPROTOCOL hProtocol[1];
} PROTOCOLTABLE;
```



## <a name="members"></a>Membros

<dl> <dt>

**nProtocols**
</dt> <dd>

Número de protocolos habilitados.

</dd> <dt>

**hProtocol**
</dt> <dd>

Matriz de identificadores para protocolos habilitados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




