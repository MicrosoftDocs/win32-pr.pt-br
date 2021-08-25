---
description: FileIo_Name classe - essa classe é a classe de tipo de evento para eventos de E/S de arquivo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: ed72daa3-06c0-46f1-bb9d-c0b343228f28
title: FileIo_Name classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Name
- FileIo_Name.FileObject
- FileIo_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 147e7fd2cb28f7245d8366dc66d7b3859f37586f1bd7c9c0b96d2d7ef57e35d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829708"
---
# <a name="fileio_name-class"></a>Classe FileIo \_ Name

Essa classe é a classe de tipo de evento para eventos de E/S de arquivo.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{0, 32, 35, 36}, EventTypeName{"Name", "FileCreate", "FileDelete", "FileRundown"}]
class FileIo_Name : FileIo
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a>Membros

A **classe FileIo \_ Name** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe FileIo \_ Name** tem essas propriedades.

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(2), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Caminho completo para o arquivo, sem incluir a letra da unidade.

</dd> <dt>

FileObject
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(1), Pointer
</dt> </dl>

Corresponder o valor desse ponteiro ao valor do ponteiro **FileObject** em um evento [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) para determinar o tipo de operação de E/S.

</dd> </dl>

## <a name="remarks"></a>Comentários

**Windows Server 2003:** Para recuperar a letra da unidade para o caminho do nome do arquivo, use o valor da propriedade **FileObject** para mapear para o evento [DiskIo \_ TypeGroup1](diskio-typegroup1.md) correspondente. No evento DiskIo TypeGroup1, use os valores de propriedade \_ **DiskNumber** e **ByteOffset** para mapear para o evento [ \_ LogDisk do SystemConfig](systemconfig-logdisk.md) correspondente (**ByteOffset** é mapeado para **StartOffset**). A **propriedade DriveLetterString** contém a letra da unidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Fileio**](fileio.md)
</dt> </dl>

 

 




