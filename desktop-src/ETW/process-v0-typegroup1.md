---
description: Process_V0_TypeGroup1 classe - essa classe é a classe de tipo de evento para eventos de processo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: fcf2897d-32b4-42b9-892c-f0106687d3c2
title: Process_V0_TypeGroup1 classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V0_TypeGroup1
- Process_V0_TypeGroup1.ProcessId
- Process_V0_TypeGroup1.ParentId
- Process_V0_TypeGroup1.UserSID
- Process_V0_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0d42ed4704eafcbb335b29c2c2d8d83e2ea82591c75855a6da096cb1e11a7572
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394432"
---
# <a name="process_v0_typegroup1-class"></a>Classe \_ Process V0 \_ TypeGroup1

Essa classe é a classe de tipo de evento para eventos de processo.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V0_TypeGroup1 : Process_V0
{
  uint32 ProcessId;
  uint32 ParentId;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a>Membros

A **classe Process \_ V0 \_ TypeGroup1** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Process \_ V0 \_ TypeGroup1** tem essas propriedades.

<dl> <dt>

ImageFileName
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(4), StringTermination("NullTerminated")
</dt> </dl>

Caminho para o arquivo executável do processo.

</dd> <dt>

ParentId
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(2), Pointer
</dt> </dl>

Identificador exclusivo do processo que cria um processo. Os números do identificador de processo são reutilizados, portanto, eles identificam apenas um processo durante o tempo de vida desse processo. É possível que o processo identificado por ParentProcessId seja encerrado, portanto, ParentProcessId pode não se referir a um processo em execução. Também é possível que ParentProcessId refere-se incorretamente a um processo que reutiliza um identificador de processo.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(1), Pointer
</dt> </dl>

Identificador de processo global que você pode usar para identificar um processo. O valor é válido desde o momento em que um processo é criado até ser encerrado.

</dd> <dt>

UserSID
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(3), Extension("Sid")
</dt> </dl>

SID (identificador de segurança) para o contexto do usuário no qual o evento ocorre.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Processo \_ V0**](process-v0.md)
</dt> </dl>

 

 




