---
description: A estrutura EXPERTFRAMEDESCRIPTOR contém informações sobre um quadro. Quando o especialista chama a função ExpertGetFrame com êxito, Monitor de Rede passa a estrutura EXPERTFRAMEDESCRIPTOR de volta para o especialista.
ms.assetid: 6cf99498-3cf9-46da-b6a0-3012229f6908
title: Estrutura EXPERTFRAMEDESCRIPTOR (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTFRAMEDESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4a11c131188cdd5230d309a6ff2e39a77ac7886333dafd9860d565fdcb10efc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939023"
---
# <a name="expertframedescriptor-structure"></a>Estrutura EXPERTFRAMEDESCRIPTOR

A estrutura **EXPERTFRAMEDESCRIPTOR** contém informações sobre um quadro. Quando o especialista chama a função [**ExpertGetFrame**](expertgetframe.md) com êxito, monitor de rede passa a estrutura **EXPERTFRAMEDESCRIPTOR** de volta para o especialista.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD                FrameNumber;
  HFRAME               hFrame;
  ULPFRAME             pFrame;
  LPRECOGNIZEDATATABLE lpRecognizeDataTable;
  LPPROPERTYTABLE      lpPropertyTable;
} EXPERTFRAMEDESCRIPTOR, *LPEXPERTFRAMEDESCRIPTOR;
```



## <a name="members"></a>Membros

<dl> <dt>

**FrameNumber**
</dt> <dd>

Número de um quadro especificado.

</dd> <dt>

**hFrame**
</dt> <dd>

Identificador para um quadro.

</dd> <dt>

**pFrame**
</dt> <dd>

Ponteiro para um quadro bruto.

</dd> <dt>

**lpRecognizeDataTable**
</dt> <dd>

Tabela que indica onde cada analisador identifica o início dos dados.

</dd> <dt>

**lpPropertyTable**
</dt> <dd>

Tabela de propriedades de quadro que o analisador identifica.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se o especialista especificar \_ as propriedades de anexação de sinalizadores \_ ao chamar [**ExpertGetFrame**](expertgetframe.md), o membro **szPropertyText** em cada estrutura [**PROPERTYINST**](propertyinst.md) será **nulo**.

Se o especialista não especificar \_ \_ as propriedades de anexação de sinalizadores ao chamar a função [**ExpertGetFrame**](expertgetframe.md) , o membro **lpPropertyTable** será **nulo** no retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




