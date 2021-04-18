---
description: A estrutura NMCOLUMNINFO define uma coluna no painel superior da Visualizador de Eventos.
ms.assetid: 21e0a129-464b-45b3-9c6b-6594e62fbce9
title: Estrutura NMCOLUMNINFO (Netmon. h)
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
ms.openlocfilehash: 2597b486590871f0af28736717d4c2f332aae342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770468"
---
# <a name="nmcolumninfo-structure"></a>Estrutura NMCOLUMNINFO

A estrutura **NMCOLUMNINFO** define uma coluna no painel superior da Visualizador de eventos.

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

Nome de exibição de uma coluna específica. Se o nome for muito longo, ele não estará totalmente visível na configuração de Visualizador de Eventos padrão.

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
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




