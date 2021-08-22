---
description: A \_ classe de diretório CIM representa um tipo de arquivo que agrupa logicamente os arquivos de dados que ele contém e fornece informações de caminho para os arquivos agrupados.
ms.assetid: a9594f53-08f0-4a47-9edc-51686c80c5ea
ms.tgt_platform: multiple
title: Classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory
- CIM_Directory.AccessMask
- CIM_Directory.Archive
- CIM_Directory.Caption
- CIM_Directory.Compressed
- CIM_Directory.CompressionMethod
- CIM_Directory.CreationClassName
- CIM_Directory.CreationDate
- CIM_Directory.CSCreationClassName
- CIM_Directory.CSName
- CIM_Directory.Description
- CIM_Directory.Drive
- CIM_Directory.EightDotThreeFileName
- CIM_Directory.Encrypted
- CIM_Directory.EncryptionMethod
- CIM_Directory.Extension
- CIM_Directory.FileName
- CIM_Directory.FileSize
- CIM_Directory.FileType
- CIM_Directory.FSCreationClassName
- CIM_Directory.FSName
- CIM_Directory.Hidden
- CIM_Directory.InstallDate
- CIM_Directory.InUseCount
- CIM_Directory.LastAccessed
- CIM_Directory.LastModified
- CIM_Directory.Name
- CIM_Directory.Path
- CIM_Directory.Readable
- CIM_Directory.Status
- CIM_Directory.System
- CIM_Directory.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 38f41b28689ac8ae4bebc29248e27d8e6b17eae1b265237acd91ed2b03d97c9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119321596"
---
# <a name="cim_directory-class"></a>\_Classe de diretório CIM

A classe de **\_ diretório CIM** representa um tipo de arquivo que agrupa logicamente os arquivos de dados que ele contém e fornece informações de caminho para os arquivos agrupados.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{8502C55F-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Directories (CIM)"), AMENDMENT]
class CIM_Directory : CIM_LogicalFile
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
  boolean  Hidden;
  datetime InstallDate;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Name;
  string   Path;
  boolean  Readable;
  string   Status;
  boolean  System;
  boolean  Writeable;
};
```

## <a name="members"></a>Membros

A classe de **\_ diretório CIM** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe de **\_ diretório CIM** tem esses métodos.



| Método                                                                                           | Descrição                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-directory.md)     | Altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto. Não implementado pelo WMI.<br/>                                   |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-cim-directory.md) | Altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto. Não implementado pelo WMI.<br/>                                   |
| [**Compactar**](compress-method-in-class-cim-directory.md)                                       | Compacta o arquivo lógico (ou diretório) especificado no caminho do objeto. Não implementado pelo WMI.<br/>                                              |
| [**CompressEx**](compressex-method-in-class-cim-directory.md)                                   | Compacta o arquivo lógico (ou diretório) especificado no caminho do objeto. Não implementado pelo WMI.<br/>                                              |
| [**Copiar**](copy-method-in-class-cim-directory.md)                                               | Copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro de entrada. Não implementado pelo WMI.<br/> |
| [**CopyEx**](copyex-method-in-class-cim-directory.md)                                           | Copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro de entrada. Não implementado pelo WMI.<br/> |
| [**Excluir**](delete-method-in-class-cim-directory.md)                                           | Exclui o arquivo lógico (ou diretório) especificado no caminho do objeto. Não implementado pelo WMI.<br/>                                                 |
| [**DeleteEx**](deleteex-method-in-class-cim-directory.md)                                       | Exclui o arquivo lógico (ou diretório) especificado no caminho do objeto. Não implementado pelo WMI.<br/>                                                 |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-cim-directory.md)           | Determina se o chamador tem as permissões agregadas especificadas pelo argumento de **permissão** . Não implementado pelo WMI.<br/>                |
| [**Nome**](rename-method-in-class-cim-directory.md)                                           | Renomeia o arquivo lógico (ou diretório) especificado no caminho do objeto. Não implementado pelo WMI.<br/>                                                 |
| [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md)                             | Obtém a propriedade do arquivo lógico especificado no caminho do objeto. Não implementado pelo WMI.<br/>                                                   |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-directory.md)                         | Obtém a propriedade do arquivo lógico especificado no caminho do objeto. Não implementado pelo WMI.<br/>                                                   |
| [**Descompactar**](uncompress-method-in-class-cim-directory.md)                                   | Descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto. Não implementado pelo WMI.<br/>                                            |
| [**UncompressEx**](uncompressex-method-in-class-cim-directory.md)                               | Descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto. Não implementado pelo WMI.<br/>                                            |



 

### <a name="properties"></a>Propriedades

A classe de **\_ diretório CIM** tem essas propriedades.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("direitos de acesso")
</dt> </dl>

Bitmask que representa os direitos de acesso necessários para acessar ou executar operações específicas no diretório. Para obter valores, consulte [**constantes de direitos de acesso de arquivo e diretório**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).

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

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("deve ser arquivado")
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

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descrição textual do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Compactado**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("compactado")
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

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de compactação")
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

Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome da classe")
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

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("data de criação")
</dt> </dl>

Data e hora em que o arquivo foi criado.

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome da classe do sistema de computador ")
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

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CSName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome do sistema de computador ")
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

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")
</dt> </dl>

Descrição textual do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Unidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("drive")
</dt> </dl>

Letra da unidade (incluindo os dois-pontos que segue a letra da unidade) do arquivo. Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

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

Nome de arquivo compatível com o DOS. Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

Exemplo: "c: \\ progra ~ 1"

</dd> <dt>

**Criptografado**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")
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

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de criptografia")
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

Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("extensão de arquivo")
</dt> </dl>

Extensão de nome de arquivo sem o ponto anterior (ponto).

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

Exemplo: "txt", "MOF", "mdb"

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome do arquivo")
</dt> </dl>

Nome do arquivo sem a extensão de nome de arquivo.

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

Exemplo: "mydatafile"

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tamanho"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Tamanho do arquivo, em bytes.

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**FileType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de arquivo")
</dt> </dl>

Descritor que representa o tipo de arquivo (indicado pela propriedade de **extensão** ).

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**FSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome da classe do sistema de arquivos ")
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

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome do sistema de arquivos ")
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

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")
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

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")
</dt> </dl>

Data e hora em que o objeto foi instalado. Essa propriedade não precisa de um valor para indicar que o objeto está instalado.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**InUseCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("contagem de abertura de arquivo atual")
</dt> </dl>

Número de "aberturas de arquivo" que estão atualmente ativos no arquivo.

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**LastAccessed**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("último acesso")
</dt> </dl>

Data e hora em que o arquivo foi acessado pela última vez.

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**LastModified**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("última modificação")
</dt> </dl>

Data e hora em que o arquivo foi modificado pela última vez.

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome herdado que serve como uma chave de uma instância de arquivo lógico em um sistema de arquivos (forneça nomes de caminho completos).

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

exemplo: "C: \\ Windows do \\ sistema \\win.ini"

</dd> <dt>

**Caminho**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")
</dt> </dl>

Caminho do arquivo, incluindo as barras invertidas à esquerda e à direita. Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

Exemplo: " \\ sistema do Windows \\ \\ "

</dd> <dt>

**Seres**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("legível")
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

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")
</dt> </dl>

Cadeia de caracteres que indica o status atual do objeto.

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

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("arquivo do sistema")
</dt> </dl>

Se for **true**, o arquivo será um arquivo do sistema.

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Gravável**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("gravável")
</dt> </dl>

Se **for true**, o arquivo poderá ser gravado.

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe de **\_ diretório CIM** é derivada de [**CIM \_ LogicalFile**](cim-logicalfile.md).

O WMI não implementa essa classe. Para obter mais informações sobre classes derivadas **do \_ diretório CIM**, consulte [classes Win32](win32-provider.md).

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

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

[**CIM \_ LogicalFile**](cim-logicalfile.md)
</dt> </dl>

 

