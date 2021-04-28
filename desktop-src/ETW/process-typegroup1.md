---
description: Classe Process_TypeGroup1-essa classe é a classe de tipo de evento para eventos de processo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 4f06e1af-3f9a-4346-aa50-50f3ee82cd98
title: Classe Process_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_TypeGroup1
- Process_TypeGroup1.UniqueProcessKey
- Process_TypeGroup1.ProcessId
- Process_TypeGroup1.ParentId
- Process_TypeGroup1.SessionId
- Process_TypeGroup1.ExitStatus
- Process_TypeGroup1.DirectoryTableBase
- Process_TypeGroup1.UserSID
- Process_TypeGroup1.ImageFileName
- Process_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: bd67059f5257dad9b66e1c21f642fef04f03719e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106374"
---
# <a name="process_typegroup1-class"></a>\_Classe Process TypeGroup1

Essa classe é a classe de tipo de evento para eventos de processo.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_TypeGroup1 : Process
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  uint32 DirectoryTableBase;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a>Membros

A classe **process \_ TypeGroup1** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **process \_ TypeGroup1** tem essas propriedades.

<dl> <dt>

CommandLine
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (9), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Linha de comando completa do processo.

</dd> <dt>

DirectoryTableBase
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (6), ponteiro
</dt> </dl>

O endereço físico da tabela de página do processo.

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

Qualificadores: WmiDataId (8), StringTermination ("NullTerminated")
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

Qualificadores: WmiDataId (7), extensão ("Sid")
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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Processar**](process.md)
</dt> </dl>

 

 




