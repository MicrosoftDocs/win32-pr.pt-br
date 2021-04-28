---
description: Classe FileIo_V1_Name-essa classe é a classe de tipo de evento para eventos de e/s de arquivo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: a4ee38df-af75-4aec-89ec-5a1c39302c82
title: Classe FileIo_V1_Name
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
ms.openlocfilehash: 62069f8a462499dfbfd9cfa368b9f5985d4775e0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106544"
---
# <a name="fileio_v1_name-class"></a>\_Classe de \_ nome FileIo v1

Essa classe é a classe de tipo de evento para eventos de e/s de arquivo.

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

A classe de **\_ \_ nome FileIo v1** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ \_ nome FileIo v1** tem essas propriedades.

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

**Windows Server 2003:** Para recuperar a letra da unidade para o caminho do nome do arquivo, use o valor da propriedade **FileObject** para mapear para o evento [DiskIo \_ TypeGroup1](diskio-typegroup1.md) correspondente. No evento DiskIo \_ TypeGroup1, use os valores de propriedade **DiskNumber** e **ByteOffset** para mapear para o evento [SystemConfig \_ LogDisk](systemconfig-logdisk.md) correspondente (**ByteOffset** Maps para **StartOffset**). A propriedade **DriveLetterString** contém a letra da unidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




