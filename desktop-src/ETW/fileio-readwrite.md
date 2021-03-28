---
description: Essa classe é a classe de tipo de evento para eventos de leitura e gravação de arquivo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 88c380fb-e043-40ab-aa74-550bce43c52b
title: Classe FileIo_ReadWrite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_ReadWrite
- FileIo_ReadWrite.Offset
- FileIo_ReadWrite.IrpPtr
- FileIo_ReadWrite.TTID
- FileIo_ReadWrite.FileObject
- FileIo_ReadWrite.FileKey
- FileIo_ReadWrite.IoSize
- FileIo_ReadWrite.IoFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: c684444ea35efe0fee9c38b15be8fe7e45e9a102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968104"
---
# <a name="fileio_readwrite-class"></a>\_Classe FileIo ReadWrite

Essa classe é a classe de tipo de evento para eventos de leitura e gravação de arquivo.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{67, 68}, EventTypeName{"Read", "Write"}]
class FileIo_ReadWrite : FileIo
{
  uint64 Offset;
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 IoSize;
  uint32 IoFlags;
};
```

## <a name="members"></a>Membros

A classe **FileIo \_ ReadWrite** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **FileIo \_ ReadWrite** tem essas propriedades.

<dl> <dt>

**FileKey**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (5), ponteiro
</dt> </dl>

Para determinar o nome do arquivo, corresponda ao valor dessa propriedade à propriedade **FileObject** de um evento [**de \_ nome de FileIo**](fileio-name.md) .

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (4), ponteiro
</dt> </dl>

Identificador que pode ser usado para correlacionar operações para a mesma instância de objeto de arquivo aberta entre eventos de criação e fechamento de arquivo.

</dd> <dt>

**IoFlags**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (7)
</dt> </dl>

Sinalizadores de pacote de solicitação de e/s especificados para esta operação.

</dd> <dt>

**IoSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (6)
</dt> </dl>

Número de bytes solicitados.

</dd> <dt>

**IrpPtr**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2), ponteiro
</dt> </dl>

Pacote de solicitação de e/s. Essa propriedade identifica a atividade de e/s.

</dd> <dt>

**Deslocamento**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1)
</dt> </dl>

Iniciando o deslocamento do arquivo para a operação solicitada.

</dd> <dt>

**TTID**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (3), ponteiro
</dt> </dl>

Identificador de thread do thread que está executando a operação.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




