---
description: Essa classe é a classe de tipo de evento para eventos de perfil de amostra. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 75ea1e5e-2554-40bb-aa9d-c6d4942c5801
title: Classe SampledProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SampledProfile
- SampledProfile.InstructionPointer
- SampledProfile.ThreadId
- SampledProfile.Count
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3d7a69eef1a2a7988569ffcd930b73a559e18d90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968151"
---
# <a name="sampledprofile-class"></a>Classe SampledProfile

Essa classe é a classe de tipo de evento para eventos de perfil de amostra.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{46}, EventTypeName{"SampleProfile"}]
class SampledProfile : PerfInfo
{
  uint32 InstructionPointer;
  uint32 ThreadId;
  uint32 Count;
};
```

## <a name="members"></a>Membros

A classe **SampledProfile** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **SampledProfile** tem essas propriedades.

<dl> <dt>

**Count**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (3)
</dt> </dl>

Não usado.

</dd> <dt>

**InstructionPointer**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1), ponteiro
</dt> </dl>

Endereço da imagem que estava sendo executada no momento em que o processador foi amostrado.

</dd> <dt>

**ThreadId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2)
</dt> </dl>

Identificador de thread do thread que estava sendo executado no momento em que o processador foi amostrado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esses eventos fornecem um perfil de execução de amostra. O evento registra o que estava sendo executado no processador. Você pode usar os eventos de imagem para identificar o módulo binário que contém essa instrução. Você pode usar essas informações para produzir um perfil de execução para a duração do rastreamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 




