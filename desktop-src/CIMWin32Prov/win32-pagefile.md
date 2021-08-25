---
description: O Arquivo de \_ Página win32&\# 32; A classe WMI representa o arquivo usado para lidar com a troca de arquivos de memória virtual em um sistema Win32. Essa classe foi substituída.
ms.assetid: 5599d09d-a2fd-4217-8560-5fd56f09d47b
ms.tgt_platform: multiple
title: Win32_PageFile classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile
- Win32_PageFile.Caption
- Win32_PageFile.Description
- Win32_PageFile.InstallDate
- Win32_PageFile.Archive
- Win32_PageFile.Compressed
- Win32_PageFile.CompressionMethod
- Win32_PageFile.CreationClassName
- Win32_PageFile.CreationDate
- Win32_PageFile.CSCreationClassName
- Win32_PageFile.CSName
- Win32_PageFile.Drive
- Win32_PageFile.EightDotThreeFileName
- Win32_PageFile.Encrypted
- Win32_PageFile.EncryptionMethod
- Win32_PageFile.Extension
- Win32_PageFile.FileName
- Win32_PageFile.FileSize
- Win32_PageFile.FileType
- Win32_PageFile.FSCreationClassName
- Win32_PageFile.FSName
- Win32_PageFile.Hidden
- Win32_PageFile.InUseCount
- Win32_PageFile.LastAccessed
- Win32_PageFile.LastModified
- Win32_PageFile.Path
- Win32_PageFile.Readable
- Win32_PageFile.System
- Win32_PageFile.Writeable
- Win32_PageFile.AccessMask
- Win32_PageFile.Manufacturer
- Win32_PageFile.Status
- Win32_PageFile.Version
- Win32_PageFile.FreeSpace
- Win32_PageFile.InitialSize
- Win32_PageFile.MaximumSize
- Win32_PageFile.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d7b144153d94ba1c28234e38e3983eb4a1ab165f4bda26b97eac00799cb3e9ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972296"
---
# <a name="win32_pagefile-class"></a>Classe PageFile do Win32 \_

A classe [WMI](../wmisdk/retrieving-a-class.md) **\_ Win32 PageFile** representa o arquivo usado para lidar com a troca de arquivos de memória virtual em um sistema Win32. Essa classe foi substituída.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{8502C4C6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_PageFile : CIM_DataFile
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  boolean  Archive;
  boolean  Compressed;
  string   CompressionMethod;
  string   CreationClassName;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Drive;
  string   EightDotThreeFileName;
  boolean  Encrypted;
  string   EncryptionMethod;
  string   Extension;
  string   FileName;
  uint64   FileSize;
  string   FileType;
  string   FSCreationClassName;
  string   FSName;
  boolean  Hidden;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Path;
  boolean  Readable;
  boolean  System;
  boolean  Writeable;
  uint32   AccessMask;
  string   Manufacturer;
  string   Status;
  string   Version;
  uint32   FreeSpace;
  uint32   InitialSize;
  uint32   MaximumSize;
  string   Name;
};
```

## <a name="members"></a>Membros

A **classe \_ PageFile win32** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ PageFile win32** tem esses métodos.



| Método                                                                                            | Descrição                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-pagefile.md)     | Método de classe que altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.<br/>                                                                                                                       |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-win32-pagefile.md) | Método de classe que altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.<br/>                                                                                                                       |
| [**Comprimir**](compress-method-in-class-win32-pagefile.md)                                       | Método de classe que compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                  |
| [**CompressEx**](compressex-method-in-class-win32-pagefile.md)                                   | Método de classe que compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                  |
| [**Copiar**](copy-method-in-class-win32-pagefile.md)                                               | Método de classe que copia o arquivo lógico ou diretório especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.<br/>                                                                                       |
| [**CopyEx**](copyex-method-in-class-win32-pagefile.md)                                           | Método de classe que copia o arquivo lógico ou diretório especificado no caminho do objeto para o local especificado pelo parâmetro FileName.<br/>                                                                                    |
| [**Excluir**](delete-method-in-class-win32-pagefile.md)                                           | Método de classe que exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                     |
| [**DeleteEx**](deleteex-method-in-class-win32-pagefile.md)                                       | Método de classe que exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                     |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-pagefile.md)           | Método de classe que determina se o chamador tem as permissões agregadas especificadas pelo argumento *Permission* não apenas no objeto de arquivo, mas no compartilhamento em que o arquivo ou diretório reside (se ele estiver em um compartilhamento).<br/> |
| [**Renomear**](rename-method-in-class-win32-pagefile.md)                                           | Método de classe que renomeia o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                     |
| [**Takeownership**](takeownership-method-in-class-win32-pagefile.md)                             | Método de classe que obtém a propriedade do arquivo lógico especificado no caminho do objeto.<br/>                                                                                                                                       |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-win32-pagefile.md)                         | Método de classe que obtém a propriedade do arquivo lógico especificado no caminho do objeto.<br/>                                                                                                                                       |
| [**Descompactar**](uncompress-method-in-class-win32-pagefile.md)                                   | Método de classe que descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                |
| [**UncompressEx**](uncompressex-method-in-class-win32-pagefile.md)                               | Método de classe que descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                |



 

### <a name="properties"></a>Propriedades

A **classe \_ PageFile win32** tem essas propriedades.

<dl> <dt>

**Accessmask**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Direitos de Acesso")
</dt> </dl>

Bitmask que representa os direitos de acesso necessários para acessar ou executar operações específicas no arquivo. Para valores, consulte [**Constantes de direitos de acesso de**](../wmisdk/file-and-directory-access-rights-constants.md)arquivo e diretório .

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

**ARQUIVO \_ READ \_ DATA (arquivo) ou FILE \_ LIST DIRECTORY \_ (diretório)** (1)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

**ARQUIVO \_ WRITE \_ DATA (arquivo) ou FILE \_ ADD FILE \_ (diretório)** (2)


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

**ARQUIVO \_ ACRESCENTAR \_ DADOS (arquivo) ou ADICIONAR \_ \_ ARQUIVO SUBDIRETÓRIO (diretório)** (4)


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

**ARQUIVO \_ READ \_ EA** (8)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

**ARQUIVO \_ WRITE \_ EA** (16)


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

**ARQUIVO \_ EXECUTE (arquivo) ou \_ FILE TRAVERSE (diretório)** (32)


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

**ARQUIVO \_ DELETE \_ CHILD (diretório)** (64)


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

**ARQUIVO \_ ATRIBUTOS \_ DE LEITURA** (128)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

**ARQUIVO \_ ATRIBUTOS \_ DE** GRAVAÇÃO (256)


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

**DELETE** (65536)


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

**LEITURA \_ CONTROL** (131072)


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

**GRAVAÇÃO \_ DAC** (262144)


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

**GRAVAÇÃO \_ OWNER** (524288)


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

**SYNCHRONIZE** (1048576)


</dt> <dd></dd> </dl>

</dd> <dt>

**Arquivar**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Deve ser arquivado")
</dt> </dl>

Se **True**, o arquivo deverá ser arquivado.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Legenda")
</dt> </dl>

Uma breve descrição textual do objeto .

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Compactado**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compactado")
</dt> </dl>

Se **True**, o arquivo será compactado.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Método de Compactação")
</dt> </dl>

Cadeia de caracteres de forma livre que indica o algoritmo ou a ferramenta usada para compactar o arquivo lógico. Se o esquema de compactação for desconhecido ou não for descrito, use "Desconhecido". Se o arquivo lógico for compactado, mas o esquema de compactação for desconhecido ou não for descrito, use "Compactado". Se o arquivo lógico não for compactado, use "Não Compactado".

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**\_ Chave CIM,**](../wmisdk/standard-wmi-qualifiers.md) [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Nome da Classe")
</dt> </dl>

Nome da classe.

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("data de criação")
</dt> </dl>

Data e hora da criação do arquivo.

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome da classe do sistema de computador ")
</dt> </dl>

Classe do sistema de computador.

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CSName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome do sistema de computador ")
</dt> </dl>

Nome do sistema de computador.

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")
</dt> </dl>

Uma descrição textual do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Unidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**fixo**](../wmisdk/standard-wmi-qualifiers.md), [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("drive")
</dt> </dl>

Letra da unidade (incluindo os dois-pontos que segue a letra da unidade) do arquivo. Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

Exemplo: "c:"

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**EightDotThreeFileName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("oito pontos três nome de arquivo")
</dt> </dl>

Nome de arquivo compatível com o DOS.

Exemplo: "c: \\ progra ~ 1"

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Criptografado**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encrypted")
</dt> </dl>

Se **for true**, o arquivo será criptografado.

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**EncryptionMethod**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("método de criptografia")
</dt> </dl>

Cadeia de caracteres de forma livre que identifica o algoritmo ou a ferramenta usada para criptografar um arquivo lógico. Se o esquema de criptografia não for indulged (por motivos de segurança, por exemplo), use "desconhecido". Se o arquivo estiver criptografado, mas seu esquema de criptografia for desconhecido ou não for divulgado, use "Encrypted". Se o arquivo lógico não estiver criptografado, use "não criptografado".

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Extensão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**fixo**](../wmisdk/standard-wmi-qualifiers.md), [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("extensão de arquivo")
</dt> </dl>

Extensão de nome de arquivo sem o ponto anterior (ponto).

Exemplo: "txt", "MOF", "mdb"

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**fixo**](../wmisdk/standard-wmi-qualifiers.md), [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome do arquivo")
</dt> </dl>

Nome do arquivo sem a extensão de nome de arquivo. Exemplo: "mydatafile"

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("tamanho"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Tamanho do arquivo, em bytes.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**FileType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("tipo de arquivo")
</dt> </dl>

Descritor que representa o tipo de arquivo indicado pela propriedade de **extensão** .

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**FreeSpace**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de gerenciamento de memória win32api \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwAvailPageFile"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")
</dt> </dl>

Espaço disponível no arquivo de paginação. O sistema operacional pode aumentar o arquivo de paginação conforme necessário, até o limite imposto pelo usuário. Essa propriedade mostra a diferença entre o tamanho da memória confirmada atual e o tamanho atual do arquivo de paginação; Ele não mostra o maior tamanho possível do arquivo de paginação.

</dd> <dt>

**FSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome da classe do sistema de arquivos ")
</dt> </dl>

Classe do sistema de arquivos.

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**FSName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome do sistema de arquivos ")
</dt> </dl>

Nome do sistema de arquivos.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Oculto**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Oculto")
</dt> </dl>

Se **True**, o arquivo será oculto.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**InitialSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Regstry \| System \\ \\ CurrentControlSet Control Session \\ \\ Manager Memory Management \\ \\ \\ \\ \| PagingFiles"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")
</dt> </dl>

Tamanho inicial do arquivo de página.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Data de instalação")
</dt> </dl>

Indica quando o objeto foi instalado. A falta de um valor não indica que o objeto não está instalado.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**InUseCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Contagem Aberta do Arquivo Atual")
</dt> </dl>

Número de "aberturas de arquivo" que estão ativas no momento no arquivo.

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/previous-versions//aa393262(v=vs.85)).

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**LastAccessed**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Último Acessado")
</dt> </dl>

Data e hora em que o arquivo foi acessado pela última vez.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Lastmodified**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Última Modificação")
</dt> </dl>

Data e hora em que o arquivo foi modificado pela última vez.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Fabricante**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Fabricante")
</dt> </dl>

Cadeia de caracteres de fabricante do recurso de versão (se uma estiver presente).

Essa propriedade é herdada de [**CIM \_ DataFile.**](cim-datafile.md)

</dd> <dt>

**Maximumsize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Memory Management Structures \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwTotalPageFile"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")
</dt> </dl>

Tamanho máximo do arquivo de página conforme definido pelo usuário. O sistema operacional não permitirá que o arquivo de página exceda esse limite.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO**](../wmisdk/standard-wmi-qualifiers.md) [**,**](../wmisdk/standard-qualifiers.md) Substituir ("Nome"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32DLL \|NTDLL.DLL\| [**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation) \| SystemPageFileInformation \| PageFileName")
</dt> </dl>

Nome do arquivo de página.

Exemplo: "C: \\PAGEFILE.SYS"

</dd> <dt>

**Caminho**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**corrigido,**](../wmisdk/standard-wmi-qualifiers.md) [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caminho")
</dt> </dl>

Caminho do arquivo, incluindo as malhas instingas à frente e à parte final.

Exemplo: " \\ windows \\ system \\ "

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Legível**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Acessível")
</dt> </dl>

Se **True**, o arquivo poderá ser lido.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Cadeia de caracteres que indica o status atual do objeto.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Os valores incluem o seguinte:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erro** ("Erro")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("Degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** ("Desconhecido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Iniciando** ("Iniciando")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Parando** ("Parando")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Serviço** ("Serviço")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** ("Stressed")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sem contato** ("Sem contato")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Perda de vírgula** ("comm perdida")


</dt> <dd></dd> </dl>

</dd> <dt>

**System**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Arquivo do Sistema")
</dt> </dl>

Se **True**, o arquivo será um arquivo do sistema.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Versão")
</dt> </dl>

Cadeia de caracteres de versão do recurso de versão (se uma estiver presente).

Essa propriedade é herdada de [**CIM \_ DataFile.**](cim-datafile.md)

</dd> <dt>

**Gravável**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Writeable")
</dt> </dl>

Se **True**, o arquivo poderá ser gravado.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ PageFile win32** é derivada do [**diretório CIM. \_**](cim-directory.md)

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir demonstra como recuperar estatísticas de arquivo de página de instâncias do **Win32 \_ PageFile.**


```VB
Set PageFileSet = GetObject("winmgmts:").InstancesOf ("Win32_PageFile")

for each PageFile in PageFileSet
 WScript.Echo PageFile.Name & Chr(13) 
 WScript.Echo " Initial: " & PageFile.InitialSize & " MB"
 WScript.Echo " Max: " & PageFile.MaximumSize & " MB" 

next
```



O exemplo de código Perl a seguir demonstra como recuperar estatísticas de arquivo de página de instâncias do **Win32 \_ PageFile.**


```
use strict;
use Win32::OLE;

my $PageFileSet;

eval { $PageFileSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 InstancesOf ("Win32_PageFile"); };
if (!$@ && defined $PageFileSet)
{
 foreach my $PageFileInst (in $PageFileSet)
 {
  print "\n$PageFileInst->{Name}\n";
  print " Initial: $PageFileInst->{InitialSize} MB\n";
  print " Maximum: $PageFileInst->{MaximumSize} MB\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ DataFile**](cim-datafile.md)
</dt> <dt>

[Classes do sistema operacional](./operating-system-classes.md)
</dt> </dl>

 

 
