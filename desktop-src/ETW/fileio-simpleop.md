---
description: Essa classe é a classe de tipo de evento para eventos de operação de arquivo simples. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 5b6374e0-b39a-4d5a-acbd-25b410f1ba52
title: Classe FileIo_SimpleOp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_SimpleOp
- FileIo_SimpleOp.IrpPtr
- FileIo_SimpleOp.TTID
- FileIo_SimpleOp.FileObject
- FileIo_SimpleOp.FileKey
api_type:
- NA
api_location: ''
ms.openlocfilehash: f7ff09830653278c9b37cfefa81b182b0f1dc054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968103"
---
# <a name="fileio_simpleop-class"></a>\_Classe SimpleOp FileIo

Essa classe é a classe de tipo de evento para eventos de operação de arquivo simples.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{65, 66, 73}, EventTypeName{"Cleanup", "Close", "Flush"}]
class FileIo_SimpleOp : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
};
```

## <a name="members"></a>Membros

A classe **FileIo \_ SimpleOp** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **FileIo \_ SimpleOp** tem essas propriedades.

<dl> <dt>

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

O evento de limpeza é registrado quando o último identificador do arquivo é fechado. O evento Close especifica que um objeto de arquivo está sendo liberado. O evento flush especifica quando os buffers de arquivo são totalmente liberados para o disco.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




