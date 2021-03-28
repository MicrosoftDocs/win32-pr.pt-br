---
description: Essa classe é a classe de tipo de evento para eventos de processo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: ff5c1f64-2087-4238-81f9-6283f0f0e68a
title: Classe Process_V2_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup1
- Process_V2_TypeGroup1.UniqueProcessKey
- Process_V2_TypeGroup1.ProcessId
- Process_V2_TypeGroup1.ParentId
- Process_V2_TypeGroup1.SessionId
- Process_V2_TypeGroup1.ExitStatus
- Process_V2_TypeGroup1.UserSID
- Process_V2_TypeGroup1.ImageFileName
- Process_V2_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: 01da5a8254627d6378c9f99aa2ba36dc6714e6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968114"
---
# <a name="process_v2_typegroup1-class"></a>\_Classe Process v2 \_ TypeGroup1

Essa classe é a classe de tipo de evento para eventos de processo.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_V2_TypeGroup1 : Process_V2
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a>Membros

A classe **process \_ v2 \_ TypeGroup1** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **process \_ v2 \_ TypeGroup1** tem essas propriedades.

<dl> <dt>

CommandLine
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (8), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Linha de comando completa do processo.

</dd> <dt>

ExitStatus
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (5)
</dt> </dl>

Status de saída do processo interrompido.

</dd> <dt>

ImageFileName
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (7), StringTermination ("NullTerminated")
</dt> </dl>

Caminho para o arquivo executável do processo.

</dd> <dt>

ParentId
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (3), formato ("x")
</dt> </dl>

Identificador exclusivo do processo que cria esse processo. Os números de identificador de processo são reutilizados, portanto, eles identificam apenas um processo durante o tempo de vida desse processo. É possível que o processo identificado pelo ParentProcessId seja encerrado; portanto, ParentProcessId pode não se referir a um processo em execução. Também é possível que o ParentProcessId incorretamente faça referência a um processo que reutiliza um identificador de processo.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2), formato ("x")
</dt> </dl>

Identificador de processo global que você pode usar para identificar um processo. O valor é válido a partir do momento em que um processo é criado até ser encerrado.

</dd> <dt>

SessionId
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (4)
</dt> </dl>

Identificador exclusivo que um sistema operacional gera ao criar uma nova sessão. Uma sessão abrange um período de tempo do logon até o logoff de um sistema específico.

</dd> <dt>

UniqueProcessKey
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1), ponteiro
</dt> </dl>

O endereço do objeto de processo no kernel.

</dd> <dt>

UserSID
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (6), extensão ("Sid")
</dt> </dl>

SID (identificador de segurança) para o contexto do usuário no qual o evento ocorre.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os tipos de evento DCStart e DCEnd enumeram o processo que está em execução no momento, incluindo o processo de ociosidade e do sistema, no momento em que a sessão do kernel é iniciada e termina, respectivamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Processo \_ v2**](process-v2.md)
</dt> </dl>

 

 




