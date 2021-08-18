---
description: O atalho do Win32file \_&\# 32; A classe WMI representa os arquivos que são atalhos para outros arquivos, diretórios e comandos.
ms.assetid: 15973234-e418-4869-839e-a7c439512e4e
ms.tgt_platform: multiple
title: Classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile
- Win32_ShortcutFile.Caption
- Win32_ShortcutFile.Description
- Win32_ShortcutFile.InstallDate
- Win32_ShortcutFile.Status
- Win32_ShortcutFile.AccessMask
- Win32_ShortcutFile.Archive
- Win32_ShortcutFile.Compressed
- Win32_ShortcutFile.CompressionMethod
- Win32_ShortcutFile.CreationClassName
- Win32_ShortcutFile.CreationDate
- Win32_ShortcutFile.CSCreationClassName
- Win32_ShortcutFile.CSName
- Win32_ShortcutFile.Drive
- Win32_ShortcutFile.EightDotThreeFileName
- Win32_ShortcutFile.Encrypted
- Win32_ShortcutFile.EncryptionMethod
- Win32_ShortcutFile.Name
- Win32_ShortcutFile.Extension
- Win32_ShortcutFile.FileName
- Win32_ShortcutFile.FileSize
- Win32_ShortcutFile.FileType
- Win32_ShortcutFile.FSCreationClassName
- Win32_ShortcutFile.FSName
- Win32_ShortcutFile.Hidden
- Win32_ShortcutFile.InUseCount
- Win32_ShortcutFile.LastAccessed
- Win32_ShortcutFile.LastModified
- Win32_ShortcutFile.Path
- Win32_ShortcutFile.Readable
- Win32_ShortcutFile.System
- Win32_ShortcutFile.Writeable
- Win32_ShortcutFile.Manufacturer
- Win32_ShortcutFile.Version
- Win32_ShortcutFile.Target
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8f1951d4c52087330ac28e23e59e9403c67aff44bf7f9e94c63d3bfa7fc1bded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917496"
---
# <a name="win32_shortcutfile-class"></a>\_Classe de atalhofile Win32

A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ shortcutfile do Win32** representa arquivos que são atalhos para outros arquivos, diretórios e comandos.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE466-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_ShortcutFile : CIM_DataFile
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
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
  string   Name;
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
  string   Manufacturer;
  string   Version;
  string   Target;
};
```

## <a name="members"></a>Membros

A **classe \_ Shortcutfile do Win32** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ Shortcutfile do Win32** tem esses métodos.



| Método                                                                                                | Descrição                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-shortcutfile.md)     | Método de classe que altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.<br/>                                                                                                                     |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-win32-shortcutfile.md) | Método de classe que altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.<br/>                                                                                                                     |
| [**Compactar**](compress-method-in-class-win32-shortcutfile.md)                                       | Método de classe que compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                |
| [**CompressEx**](compressex-method-in-class-win32-shortcutfile.md)                                   | Método de classe que compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                |
| [**Copiar**](copy-method-in-class-win32-shortcutfile.md)                                               | Método de classe que copia o arquivo ou diretório lógico especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.<br/>                                                                                     |
| [**CopyEx**](copyex-method-in-class-win32-shortcutfile.md)                                           | Método de classe que copia o arquivo ou diretório lógico especificado no caminho do objeto para o local especificado pelo parâmetro *filename* .<br/>                                                                                |
| [**Excluir**](delete-method-in-class-win32-shortcutfile.md)                                           | Método de classe que exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                   |
| [**DeleteEx**](deleteex-method-in-class-win32-shortcutfile.md)                                       | Método de classe que exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                   |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md)           | Método de classe que determina se o chamador tem as permissões agregadas especificadas pelo argumento de permissão não apenas no objeto File, mas no compartilhamento o arquivo ou diretório reside (se estiver em um compartilhamento).<br/> |
| [**Nome**](rename-method-in-class-win32-shortcutfile.md)                                           | Método de classe que renomeia o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                   |
| [**TakeOwnerShip**](takeownership-method-in-class-win32-shortcutfile.md)                             | Método de classe que obtém a propriedade do arquivo lógico especificado no caminho do objeto.<br/>                                                                                                                                     |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-win32-shortcutfile.md)                         | Método de classe que obtém a propriedade do arquivo lógico especificado no caminho do objeto.<br/>                                                                                                                                     |
| [**Descompactar**](uncompress-method-in-class-win32-shortcutfile.md)                                   | Método de classe que descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                              |
| [**UncompressEx**](uncompressex-method-in-class-win32-shortcutfile.md)                               | Método de classe que descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                              |



 

### <a name="properties"></a>Propriedades

A **classe \_ Shortcutfile do Win32** tem essas propriedades.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("direitos de acesso")
</dt> </dl>

Bitmask que representa os direitos de acesso necessários para acessar ou executar operações específicas no arquivo. Para valores de bit, consulte [**constantes de direitos de acesso de arquivo e diretório**](../wmisdk/file-and-directory-access-rights-constants.md).

> [!Note]  
> Em volumes FAT, o valor de **\_ acesso completo** é retornado, o que indica que nenhuma segurança foi definida no objeto.

 

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

Do **arquivo \_ LER \_ os dados (arquivo) ou \_ \_ diretório de lista de arquivos (diretório)** (1)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

Do **arquivo \_ GRAVAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ arquivo (diretório)** (2)


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

Do **arquivo \_ ACRESCENTAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ subdiretório (diretório)** (4)


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

Do **arquivo \_ LER \_ ea** (8)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

Do **arquivo \_ GRAVAR \_ ea** (16)


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

Do **arquivo \_ EXECUTAR (arquivo) ou \_ atravessamento de arquivo (diretório)** (32)


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

Do **arquivo \_ EXCLUIR \_ filho (diretório)** (64)


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

Do **arquivo \_ \_Atributos de leitura** (128)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

Do **arquivo \_ \_Atributos de gravação** (256)


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

**Excluir** (65536)


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

**Ler \_ CONTROLE** (131072)


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

**Gravar \_ DAC** (262144)


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

**Gravar \_ PROPRIETÁRIO** (524288)


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

**Sincronizar** (1048576)


</dt> <dd></dd> </dl>

</dd> <dt>

**Arquivar**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("deve ser arquivado")
</dt> </dl>

Se **for true**, o arquivo deverá ser arquivado.

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Uma breve descrição textual do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Compactado**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("compactado")
</dt> </dl>

Se **for true**, o arquivo será compactado.

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("método de compactação")
</dt> </dl>

Cadeia de caracteres de forma livre que indica o algoritmo ou a ferramenta usada para compactar o arquivo lógico. Se o esquema de compactação for desconhecido ou não estiver descrito, use "desconhecido". Se o arquivo lógico estiver compactado, mas o esquema de compactação for desconhecido ou não estiver descrito, use "compactado". Se o arquivo lógico não estiver compactado, use "não compactado".

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome da classe")
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

Letra da unidade (incluindo os dois-pontos que segue a letra da unidade) do arquivo.

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

Nome do arquivo no formato 8,3.

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

Nome do arquivo sem a extensão de nome de arquivo.

Exemplo: "mydatafile"

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

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).

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

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Oculto**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Hidden")
</dt> </dl>

Se for **true**, o arquivo ficará oculto.

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")
</dt> </dl>

Indica quando o objeto foi instalado. A falta de um valor não indica que o objeto não está instalado.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**InUseCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("contagem de abertura de arquivo atual")
</dt> </dl>

Número de "aberturas de arquivo" que estão atualmente ativos no arquivo.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**LastAccessed**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("último acesso")
</dt> </dl>

Data e hora do último acesso ao arquivo.

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**LastModified**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("última modificação")
</dt> </dl>

Data e hora da última modificação do arquivo.

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("fabricante")
</dt> </dl>

Cadeia de caracteres do fabricante do recurso de versão (se houver um).

Esta propriedade é herdada [**do \_ arquivo**](cim-datafile.md)de propriedades CIM.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](../wmisdk/key-qualifier.md)
</dt> </dl>

A propriedade Name é uma cadeia de caracteres que representa o nome herdado que serve como uma chave de uma instância de arquivo lógico em um sistema de arquivos. Devem ser fornecidos nomes de caminho completos.

exemplo: C: \\ Windows \\ sistema \\win.ini

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Caminho**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**fixo**](../wmisdk/standard-wmi-qualifiers.md), [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Path")
</dt> </dl>

Caminho do arquivo, incluindo as barras invertidas à esquerda e à direita.

Exemplo: " \\ sistema do Windows \\ \\ "

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Seres**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("legível")
</dt> </dl>

Se **for true**, o arquivo poderá ser lido.

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")
</dt> </dl>

Cadeia de caracteres que indica o status atual do objeto. O status operacional e não operacional pode ser definido. O status operacional pode incluir "OK", "degradado" e "Pred falha". "Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).

O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço". O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Os valores incluem o seguinte:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erro** ("erro")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** ("desconhecido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Falha de Pred** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Iniciando** ("Iniciando")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Parando** ("parando")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Serviço** ("serviço")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Sob estresse** ("sob estresse")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

Não **recuperar** ("Recover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sem contato** ("sem contato")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Perda de comunicação** ("perda de comunicação")


</dt> <dd></dd> </dl>

</dd> <dt>

**System**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("arquivo do sistema")
</dt> </dl>

Se for **true**, o arquivo será um arquivo do sistema.

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Target (destino)**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| \_ beginthreadex")
</dt> </dl>

Nome do objeto para o qual este é um atalho.

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Version")
</dt> </dl>

Cadeia de caracteres da versão do recurso de versão (se houver uma).

Esta propriedade é herdada [**do \_ arquivo**](cim-datafile.md)de propriedades CIM.

</dd> <dt>

**Gravável**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("gravável")
</dt> </dl>

Se **for true**, o arquivo poderá ser gravado.

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ ShortcutFile Win32** é derivada de [**CIM \_ DataFile.**](cim-datafile.md)

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

 

 
