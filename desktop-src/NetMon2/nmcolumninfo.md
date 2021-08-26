---
description: A estrutura NMCOLUMNINFO define uma coluna no painel superior do Visualizador de Eventos.
ms.assetid: 21e0a129-464b-45b3-9c6b-6594e62fbce9
title: Estrutura NMCOLUMNINFO (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EVENTCOLUMNINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 95683eb812a2b8a668664f7ad8092a91c1940d2c3f7185225e8364959777538b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037116"
---
# <a name="nmcolumninfo-structure"></a>Estrutura NMCOLUMNINFO

A **estrutura NMCOLUMNINFO** define uma coluna no painel superior do Visualizador de Eventos.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  LPSTR           szColumnName;
  NMCOLUMNVARIANT VariantData;
} EVENTCOLUMNINFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**szColumnName**
</dt> <dd>

Nome exibivel de uma coluna específica. Se o nome for muito longo, ele não ficará completamente visível na configuração Visualizador de Eventos padrão.

</dd> <dt>

**VariantData**
</dt> <dd>

Os dados inseridos na coluna.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




