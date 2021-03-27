---
description: A classe de nome de V0 de FileIo \_ \_ é uma versão mais antiga da classe de tipo de evento para eventos de e/s de arquivo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: dcbe37f2-6df0-41a5-b85f-dcd06cbd5901
title: Classe FileIo_V0_Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V0_Name
- FileIo_V0_Name.FileObject
- FileIo_V0_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6e88d1b9b5b36815b1a833062c30e804e4db744a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662797"
---
# <a name="fileio_v0_name-class"></a>Classe de nome de \_ V0 FileIo \_

A classe de **\_ \_ nome de V0 de FileIo** é uma versão mais antiga da classe de tipo de evento para eventos de e/s de arquivo.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType(0), EventTypeName("Name")]
class FileIo_V0_Name : FileIo_V0
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a>Membros

A classe de **\_ \_ nome V0 do FileIo** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ \_ nome V0 de FileIo** tem essas propriedades.

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Caminho completo do arquivo, não incluindo a letra da unidade.

</dd> <dt>

FileObject
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1), ponteiro
</dt> </dl>

Corresponda o valor desse ponteiro ao valor do ponteiro **FileObject** em um evento [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) para determinar o tipo de operação de e/s.

</dd> </dl>

## <a name="remarks"></a>Comentários

**Windows Server 2003:** Para recuperar a letra da unidade para o caminho do nome do arquivo, use o valor da propriedade **FileObject** para mapear para o evento [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) correspondente. No evento **DiskIo \_ TypeGroup1** , use os valores de propriedade **DiskNumber** e **ByteOffset** para mapear para o evento [**SystemConfig \_ LogDisk**](systemconfig-logdisk.md) correspondente. A propriedade **DriveLetterString** contém a letra da unidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_V0 FileIo**](fileio-v0.md)
</dt> </dl>

 

 




