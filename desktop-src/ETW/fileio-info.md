---
description: Essa classe é a classe de tipo de evento para o evento de informações de arquivo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 41ae1f8a-a90f-43d0-a848-a2c095f046d4
title: Classe FileIo_Info
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Info
- FileIo_Info.IrpPtr
- FileIo_Info.TTID
- FileIo_Info.FileObject
- FileIo_Info.FileKey
- FileIo_Info.ExtraInfo
- FileIo_Info.InfoClass
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8a77d135fa5140f5d8d51a26164cd96009f06bacee654d13bec8dbaa9dcd76a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041996"
---
# <a name="fileio_info-class"></a>Classe de informações de FileIo \_

Essa classe é a classe de tipo de evento para o evento de informações de arquivo.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{69, 70, 71, 74, 75}, EventTypeName{"SetInfo", "Delete", "Rename", "QueryInfo", "FSControl"}]
class FileIo_Info : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 ExtraInfo;
  uint32 InfoClass;
};
```

## <a name="members"></a>Membros

A classe de **\_ informações de FileIo** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ informações de FileIo** tem essas propriedades.

<dl> <dt>

**ExtraInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (5), ponteiro
</dt> </dl>

Para solicitações FileDispositionInformation, esse campo contém a disposição solicitada. Para solicitações FileEndOfFileInformation e FileAllocationInformation, esse campo contém o tamanho de arquivo especificado.

</dd> <dt>

**FileKey**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (4), ponteiro
</dt> </dl>

Para determinar o nome do arquivo, corresponda ao valor dessa propriedade à propriedade **FileObject** de um evento [**de \_ nome de FileIo**](fileio-name.md) .

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (3), ponteiro
</dt> </dl>

Identificador que pode ser usado para correlacionar operações para a mesma instância de objeto de arquivo aberta entre eventos de criação e fechamento de arquivo.

</dd> <dt>

**InfoClass**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (6)
</dt> </dl>

Classe de informações de arquivo solicitada.

</dd> <dt>

**IrpPtr**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1), ponteiro
</dt> </dl>

Pacote de solicitação de e/s. Essa propriedade identifica a atividade de e/s.

</dd> <dt>

**TTID**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2), ponteiro
</dt> </dl>

Identificador de thread do thread que está executando a operação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Definir informações e eventos de informações de consulta indicam que os atributos de arquivo foram definidos ou consultados. Um evento de controle do sistema de arquivos (FSControl) é registrado quando um comando FSCTL é emitido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




