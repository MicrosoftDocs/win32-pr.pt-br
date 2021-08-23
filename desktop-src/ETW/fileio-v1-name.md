---
description: FileIo_V1_Name classe - essa classe é a classe de tipo de evento para eventos de E/S de arquivo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: a4ee38df-af75-4aec-89ec-5a1c39302c82
title: FileIo_V1_Name classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V1_Name
- FileIo_V1_Name.FileObject
- FileIo_V1_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: c9a2488bb8f225df94e530e1964f0721c064c256423fe3218feb54adece7d0a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582396"
---
# <a name="fileio_v1_name-class"></a>Classe Nome do FileIo \_ V1 \_

Essa classe é a classe de tipo de evento para eventos de E/S de arquivo.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{0, 32}, EventTypeName{"Name", "FileCreate"}]
class FileIo_V1_Name : FileIo
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a>Membros

A **classe FileIo \_ V1 \_ Name** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe FileIo \_ V1 \_ Name** tem essas propriedades.

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
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Fileio**](fileio.md)
</dt> </dl>

 

 




