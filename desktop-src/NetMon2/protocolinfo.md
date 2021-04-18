---
description: A estrutura PROTOCOLINFO descreve um protocolo.
ms.assetid: 7f936c93-a942-4591-9abc-59872df0964e
title: Estrutura PROTOCOLINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ed1410148a72c57b860fdfdaee447dcca505d99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778417"
---
# <a name="protocolinfo-structure"></a>Estrutura PROTOCOLINFO

A estrutura **PROTOCOLINFO** descreve um protocolo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PROTOCOLINFO {
  DWORD              ProtocolID;
  LPPROPERTYDATABASE PropertyDatabase;
  BYTE               ProtocolName[16];
  BYTE               HelpFile[16];
  BYTE               Comment[128];
} PROTOCOLINFO, *LPPROTOCOLINFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**Protocolid**
</dt> <dd>

Identificador de protocolo atribuído pelo sistema da sessão de execução especificada.

</dd> <dt>

**PropertyDatabase**
</dt> <dd>

Banco de dados de propriedades do protocolo especificado.

</dd> <dt>

**ProtocolName**
</dt> <dd>

Nome de protocolo abreviado.

</dd> <dt>

**HelpFile**
</dt> <dd>

Nome de arquivo de ajuda opcional associado ao protocolo.

</dd> <dt>

**Comentário**
</dt> <dd>

Um comentário que descreve o protocolo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




