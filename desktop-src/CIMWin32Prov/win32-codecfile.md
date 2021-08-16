---
description: O CodecFile do Win32 \_&\# 32; A classe WMI representa o codec de áudio ou vídeo instalado no sistema de computador.
ms.assetid: 48ea3b92-0ea1-4aba-b067-bce0ec356cd2
ms.tgt_platform: multiple
title: Win32_CodecFile classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile
- Win32_CodecFile.AccessMask
- Win32_CodecFile.Archive
- Win32_CodecFile.Caption
- Win32_CodecFile.Compressed
- Win32_CodecFile.CompressionMethod
- Win32_CodecFile.CreationClassName
- Win32_CodecFile.CreationDate
- Win32_CodecFile.CSCreationClassName
- Win32_CodecFile.CSName
- Win32_CodecFile.Description
- Win32_CodecFile.Drive
- Win32_CodecFile.EightDotThreeFileName
- Win32_CodecFile.Encrypted
- Win32_CodecFile.EncryptionMethod
- Win32_CodecFile.Extension
- Win32_CodecFile.FileName
- Win32_CodecFile.FileSize
- Win32_CodecFile.FileType
- Win32_CodecFile.FSCreationClassName
- Win32_CodecFile.FSName
- Win32_CodecFile.Group
- Win32_CodecFile.Hidden
- Win32_CodecFile.InstallDate
- Win32_CodecFile.InUseCount
- Win32_CodecFile.LastAccessed
- Win32_CodecFile.LastModified
- Win32_CodecFile.Manufacturer
- Win32_CodecFile.Name
- Win32_CodecFile.Path
- Win32_CodecFile.Readable
- Win32_CodecFile.Status
- Win32_CodecFile.System
- Win32_CodecFile.Version
- Win32_CodecFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d9f41178c69f40513b26de5221af6eb7b5e425acf5c4893f2de87fb18211291
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079906"
---
# <a name="win32_codecfile-class"></a>Classe CodecFile do Win32 \_

A **classe WMI \_ CodecFile** [do](/windows/desktop/WmiSdk/retrieving-a-class) Win32 representa o codec de áudio ou vídeo instalado no sistema de computador. Os codecs convertem um tipo de formato de mídia em outro, normalmente um formato compactado em um formato descompactado. O nome "codec" é derivado de uma combinação de compactação e descompactar. Por exemplo, um codec pode converter um formato compactado, como MS-ADPCM, em um formato descompactado, como PCM, que a maioria dos hardwares de áudio pode reproduzir diretamente.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CodecFile : CIM_DataFile
{
  uint32   AccessMask;
  boolean  Archive;
  string   Caption;
  boolean  Compressed;
  string   CompressionMethod;
  string   CreationClassName;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
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
  string   Group;
  boolean  Hidden;
  datetime InstallDate;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Manufacturer;
  string   Name;
  string   Path;
  boolean  Readable;
  string   Status;
  boolean  System;
  string   Version;
  boolean  Writeable;
};
```

## <a name="members"></a>Membros

A **classe \_ CodecFile do Win32** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ CodecFile do Win32** tem esses métodos.



| Método                                                                                             | Descrição                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-codecfile.md)     | Altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.<br/>                                                                                                                         |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-win32-codecfile.md) | Altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.<br/>                                                                                                                         |
| [**Comprimir**](compress-method-in-class-win32-codecfile.md)                                       | Compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                    |
| [**CompressEx**](compressex-method-in-class-win32-codecfile.md)                                   | Compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                    |
| [**Copiar**](copy-method-in-class-win32-codecfile.md)                                               | Copia o arquivo lógico ou diretório especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.<br/>                                                                                         |
| [**CopyEx**](copyex-method-in-class-win32-codecfile.md)                                           | Método de classe que copia o arquivo lógico ou diretório especificado no caminho do objeto para o local especificado pelo parâmetro FileName.<br/>                                                                    |
| [**Excluir**](delete-method-in-class-win32-codecfile.md)                                           | Exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                       |
| [**DeleteEx**](deleteex-method-in-class-win32-codecfile.md)                                       | Exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                       |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-codecfile.md)           | Determina se o chamador tem as permissões agregadas especificadas pelo argumento de permissão não apenas no objeto de arquivo, mas no compartilhamento em que o arquivo ou diretório reside (se ele estiver em um compartilhamento). <br/> |
| [**Renomear**](rename-method-in-class-win32-codecfile.md)                                           | Método de classe que renomeia o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                     |
| [**Takeownership**](takeownership-method-in-class-win32-codecfile.md)                             | Obtém a propriedade do arquivo lógico especificado no caminho do objeto.<br/>                                                                                                                                         |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-win32-codecfile.md)                         | Método de classe que obtém a propriedade do arquivo lógico especificado no caminho do objeto.<br/>                                                                                                                       |
| [**Descompactar**](uncompress-method-in-class-win32-codecfile.md)                                   | Descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                  |
| [**UncompressEx**](uncompressex-method-in-class-win32-codecfile.md)                               | Descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                  |



 

### <a name="properties"></a>Propriedades

A **classe \_ CodecFile do Win32** tem essas propriedades.

<dl> <dt>

**Accessmask**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Direitos de Acesso")
</dt> </dl>

Bitmask que representa os direitos de acesso necessários para acessar ou executar operações específicas no arquivo codec. Para valores de bit, consulte [**Constantes de direitos**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)de acesso de arquivo e diretório .

> [!Note]  
> Em volumes FAT, o **valor \_ FULL ACCESS** é retornado, o que indica que nenhuma segurança foi definida no objeto .

 

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

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Deve ser arquivado")
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

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Legenda")
</dt> </dl>

Descrição curta do objeto.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Compactado**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compactado")
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

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Método de Compactação")
</dt> </dl>

Algoritmo ou ferramenta usada para compactar o arquivo lógico. Se não for possível (ou não desejar) descrever o esquema de compactação (talvez porque ele não seja conhecido), use as seguintes palavras: "Desconhecido" para representar que não se sabe se o arquivo lógico está compactado ou não; "Compactado" para representar que o arquivo está compactado, mas seu esquema de compactação não é conhecido ou não é divulgado; e "Não Compactado" para representar que o arquivo lógico não está compactado.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**\_ Chave CIM,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome da Classe")
</dt> </dl>

Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância. Quando usada com as outras propriedades de chave da classe , a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Data de criação")
</dt> </dl>

Data de criação do arquivo.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Cim \_ FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**Chave \_ CIM,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome da Classe do Sistema de Computador")
</dt> </dl>

Classe do sistema de computador.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Cim \_ FileSystem**](cim-filesystem.md).**CSName**"), [**Chave CIM, \_**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome do Sistema de Computador")
</dt> </dl>

Cadeia de caracteres que representa o nome do sistema de computador.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Description), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet control \\ \\ \\ \\ MediaResources \\ \\ icm \| Description")
</dt> </dl>

Nome completo do driver codec. Essa cadeia de caracteres destina-se a ser exibida em espaços grandes (descritivos).

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Exemplo: "Microsoft PCM Converter"

</dd> <dt>

**Unidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**corrigido,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Unidade")
</dt> </dl>

Letra da unidade (incluindo dois-pontos) do arquivo.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

Exemplo: "c:"

</dd> <dt>

**EightDotThreeFileName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("oito pontos três nome de arquivo")
</dt> </dl>

Nome de arquivo compatível com OS para esse arquivo.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

Exemplo: "c: \\ progra~1"

</dd> <dt>

**Criptografado**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Criptografado")
</dt> </dl>

Se **True**, o arquivo será criptografado.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**EncryptionMethod**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Método de Criptografia")
</dt> </dl>

Algoritmo ou ferramenta usada para criptografar o arquivo lógico. Se não for possível (ou não desejar) descrever o esquema de criptografia (talvez por motivos de segurança), use as seguintes palavras: "Desconhecido" para representar que não se sabe se o arquivo lógico está criptografado ou não; "Criptografado" para representar que o arquivo está criptografado, mas seu esquema de criptografia não é conhecido ou não é divulgado; e "Não Criptografado" para representar que o arquivo lógico não está criptografado.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Extensão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**corrigido,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Extensão de Arquivo")
</dt> </dl>

Extensão de nome de arquivo (sem o ponto).

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

Exemplos: "txt", "mof", "mdb"

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**corrigido,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome do Arquivo")
</dt> </dl>

Nome (sem a extensão) do arquivo.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

Exemplo: "autoexec"

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Tamanho do arquivo (em bytes).

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**FileType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tipo de Arquivo")
</dt> </dl>

Tipo de arquivo (indicado pela **propriedade Extension).**

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**FSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Cim \_ FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome da Classe do Sistema de Arquivos")
</dt> </dl>

Classe do sistema de arquivos.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**FSName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Cim \_ FileSystem**](cim-filesystem.md).**Name**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome do Sistema de Arquivos")
</dt> </dl>

Nome do sistema de arquivos.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Grupo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| SOFTWARE Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \\ \\ drivers.desc")
</dt> </dl>

Codec representado por essa classe.

Os valores são:

<dl> <dd>"Áudio"</dd> <dd>"Vídeo"</dd> </dl>

<dt>

<span id="Audio"></span><span id="audio"></span><span id="AUDIO"></span>

**Áudio** ("Áudio")


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

**Vídeo** ("Vídeo")


</dt> <dd></dd> </dl>

</dd> <dt>

**Oculto**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Oculto")
</dt> </dl>

Se **True**, o arquivo será oculto.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Data de instalação")
</dt> </dl>

O objeto foi instalado. Essa propriedade não requer um valor para indicar que o objeto está instalado.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**InUseCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Contagem Aberta do Arquivo Atual")
</dt> </dl>

Número de "aberturas de arquivo" que estão ativas no momento no arquivo.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**LastAccessed**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Último Acessado")
</dt> </dl>

O arquivo foi acessado pela última vez.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Lastmodified**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Última Modificação")
</dt> </dl>

O arquivo foi modificado pela última vez.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Fabricante**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Fabricante")
</dt> </dl>

Cadeia de caracteres de fabricante do recurso de versão, se uma estiver presente.

Essa propriedade é herdada de [**CIM \_ DataFile.**](cim-datafile.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **Chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome herdado que serve como uma chave de uma instância de arquivo lógico em um sistema de arquivos. Nomes de caminho completos devem ser fornecidos.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Exemplo: "C: \\ Windows \\ sistema \\win.ini"

</dd> <dt>

**Caminho**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**corrigido,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caminho")
</dt> </dl>

Caminho do arquivo. Isso inclui as malhas inoctivas à frente e à frente.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

Exemplo: " \\ windows \\ system \\ "

</dd> <dt>

**Legível**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Acessível")
</dt> </dl>

O arquivo pode ser lido.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Status atual do objeto. Vários status operacionais e não operacionais podem ser definidos. Os status operacionais incluem: "OK", "Degradado" e "Pred Fail" (um elemento, como uma unidade de disco rígido habilitada para SMART, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo). Os status nãooperacionais incluem: "Error", "Starting", "Stopping" e "Service". O último, "Serviço", pode ser aplicado durante o espelhamento de um disco, o recarregamento de uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros estados.

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

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Arquivo do Sistema")
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

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Versão")
</dt> </dl>

Cadeia de caracteres de versão do recurso de versão, se uma estiver presente.

Essa propriedade é herdada de [**CIM \_ DataFile.**](cim-datafile.md)

</dd> <dt>

**Gravável**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")
</dt> </dl>

Se **True**, o arquivo poderá ser gravado.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ CodecFile do Win32** é derivada de [**CIM \_ DataFile.**](cim-datafile.md)

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

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

