---
description: Essa classe é a classe de tipo de evento para eventos de e/s de divisão. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 0eb1f712-8b1c-4de1-b701-5c7dbabb0f55
title: Classe SplitIo_Info
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo_Info
- SplitIo_Info.ParentIrp
- SplitIo_Info.ChildIrp
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5ae5623f4d05bc4c0e5460415656f59d8b91eeedfe1671cae6a36c7a33e0a86f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766416"
---
# <a name="splitio_info-class"></a>Classe de informações de SplitIo \_

Essa classe é a classe de tipo de evento para eventos de e/s de divisão.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{32}, EventTypeName{"VolMgr"}]
class SplitIo_Info : SplitIo
{
  uint32 ParentIrp;
  uint32 ChildIrp;
};
```

## <a name="members"></a>Membros

A classe **SplitIo \_ info** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **SplitIo \_ info** tem essas propriedades.

<dl> <dt>

**ChildIrp**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2), ponteiro
</dt> </dl>

Pacote de solicitação de e/s filho.

</dd> <dt>

**ParentIrp**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1), ponteiro
</dt> </dl>

Pacote de solicitação de es pai.

</dd> </dl>

## <a name="remarks"></a>Comentários

Indica que o Gerenciador de volumes divide o IRP em dois IRPs.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 




