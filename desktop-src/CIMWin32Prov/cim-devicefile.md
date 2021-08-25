---
description: A classe DeviceFile CIM \_ representa um tipo de arquivo lógico, que representa um dispositivo.
ms.assetid: b07f039c-8ab0-4e13-96d5-3621da19e66d
ms.tgt_platform: multiple
title: CIM_DeviceFile classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile
- CIM_DeviceFile.AccessMask
- CIM_DeviceFile.Archive
- CIM_DeviceFile.Caption
- CIM_DeviceFile.Compressed
- CIM_DeviceFile.CompressionMethod
- CIM_DeviceFile.CreationClassName
- CIM_DeviceFile.CreationDate
- CIM_DeviceFile.CSCreationClassName
- CIM_DeviceFile.CSName
- CIM_DeviceFile.Description
- CIM_DeviceFile.Drive
- CIM_DeviceFile.EightDotThreeFileName
- CIM_DeviceFile.Encrypted
- CIM_DeviceFile.EncryptionMethod
- CIM_DeviceFile.Extension
- CIM_DeviceFile.FileName
- CIM_DeviceFile.FileSize
- CIM_DeviceFile.FileType
- CIM_DeviceFile.FSCreationClassName
- CIM_DeviceFile.FSName
- CIM_DeviceFile.Hidden
- CIM_DeviceFile.InstallDate
- CIM_DeviceFile.InUseCount
- CIM_DeviceFile.LastAccessed
- CIM_DeviceFile.LastModified
- CIM_DeviceFile.Name
- CIM_DeviceFile.Path
- CIM_DeviceFile.Readable
- CIM_DeviceFile.Status
- CIM_DeviceFile.System
- CIM_DeviceFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71eefcc6a0c33f1981c6b83a03a2d4fe59acf9d438c6710e2381f887be76b5e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924516"
---
# <a name="cim_devicefile-class"></a>Classe \_ DeviceFile CIM

A **classe \_ DeviceFile CIM** representa um tipo de arquivo lógico, que representa um dispositivo. Essa convenção é útil para sistemas operacionais que gerenciam dispositivos usando um modelo de E/S de fluxo de byte. O dispositivo lógico associado a esse arquivo é especificado usando a relação [**\_ DeviceAccessedByFile cim.**](cim-deviceaccessedbyfile.md)

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{4333BD60-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceFile : CIM_LogicalFile
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

A **classe \_ DeviceFile CIM** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ DeviceFile CIM** tem esses métodos.



| Método                                                                                            | Descrição                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-devicefile.md)     | Altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto. Não implementado pelo WMI.<br/>                                   |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-cim-devicefile.md) | Altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto. Não implementado pelo WMI.<br/>                                   |
| [**Comprimir**](compress-method-in-class-cim-devicefile.md)                                       | Compacta o arquivo lógico (ou diretório) especificado no caminho do objeto. Não implementado pelo WMI.<br/>                                              |
| [**CompressEx**](compressex-method-in-class-cim-devicefile.md)                                   | Compacta o arquivo lógico (ou diretório) especificado no caminho do objeto. Não implementado pelo WMI.<br/>                                              |
| [**Copiar**](copy-method-in-class-cim-devicefile.md)                                               | Copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro de entrada. Não implementado pelo WMI.<br/> |
| [**CopyEx**](copyex-method-in-class-cim-devicefile.md)                                           | Copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro de entrada. Não implementado pelo WMI.<br/> |
| [**Excluir**](delete-method-in-class-cim-devicefile.md)                                           | Exclui o arquivo lógico (ou diretório) especificado no caminho do objeto. Não implementado pelo WMI.<br/>                                                 |
| [**DeleteEx**](deleteex-method-in-class-cim-devicefile.md)                                       | Exclui o arquivo lógico (ou diretório) especificado no caminho do objeto. Não implementado pelo WMI.<br/>                                                 |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-cim-devicefile.md)           | Determina se o chamador tem as permissões agregadas especificadas pelo **argumento Permission.** Não implementado pelo WMI.<br/>                |
| [**Renomear**](rename-method-in-class-cim-devicefile.md)                                           | Renomeia o arquivo lógico (ou diretório) especificado no caminho do objeto. Não implementado pelo WMI.<br/>                                                 |
| [**Takeownership**](takeownership-method-in-class-cim-devicefile.md)                             | Obtém a propriedade do arquivo lógico especificado no caminho do objeto. Não implementado pelo WMI.<br/>                                                   |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-devicefile.md)                         | Obtém a propriedade do arquivo lógico especificado no caminho do objeto. Não implementado pelo WMI.<br/>                                                   |
| [**Descompactar**](uncompress-method-in-class-cim-devicefile.md)                                   | Descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto. Não implementado pelo WMI.<br/>                                            |
| [**UncompressEx**](uncompressex-method-in-class-cim-devicefile.md)                               | Descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto. Não implementado pelo WMI.<br/>                                            |



 

### <a name="properties"></a>Propriedades

A **classe \_ DeviceFile CIM** tem essas propriedades.

<dl> <dt>

**Accessmask**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Direitos de Acesso")
</dt> </dl>

Matriz de bits que representa os direitos de acesso ao arquivo ou diretório determinado mantido pelo usuário ou grupo em cujo nome a instância é retornada. Em volumes FAT, **FULL \_ ACCESS** é retornado, o que indica que nenhuma segurança foi definida no objeto .

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**ARQUIVO \_ READ \_ DATA (arquivo) ou FILE \_ LIST DIRECTORY \_ (diretório)** (1)


</dt> <dd>

Concede o direito de ler dados do arquivo. Para um diretório, esse valor concede o direito de listar o conteúdo do diretório.

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**ARQUIVO \_ WRITE \_ DATA (arquivo) ou FILE \_ ADD FILE \_ (diretório)** (2)


</dt> <dd>

Concede o direito de gravar dados no arquivo. Para um diretório, esse valor concede o direito de criar um arquivo no diretório .

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**ARQUIVO \_ ACRESCENTAR \_ DADOS (arquivo) ou ADICIONAR \_ \_ ARQUIVO SUBDIRETÓRIO (diretório)** (4)


</dt> <dd>

Concede o direito de anexar dados ao arquivo. Para um diretório, esse valor concede o direito de criar um subdiretório.

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**ARQUIVO \_ READ \_ EA** (8)


</dt> <dd>

Concede o direito de ler atributos estendidos.

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**ARQUIVO \_ WRITE \_ EA** (16)


</dt> <dd>

Concede o direito de gravar atributos estendidos.

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**ARQUIVO \_ EXECUTE (arquivo) ou \_ FILE TRAVERSE (diretório)** (32)


</dt> <dd>

Concede o direito de executar um arquivo. Para um diretório, o diretório pode ser percorrido.

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**ARQUIVO \_ DELETE \_ CHILD (diretório)** (64)


</dt> <dd>

Concede o direito de excluir um diretório e todos os arquivos que ele contém (seus filhos), mesmo que os arquivos sejam somente leitura.

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**ARQUIVO \_ ATRIBUTOS \_ DE LEITURA** (128)


</dt> <dd>

Concede o direito de ler atributos de arquivo.

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**ARQUIVO \_ ATRIBUTOS \_ DE** GRAVAÇÃO (256)


</dt> <dd>

Concede o direito de alterar atributos de arquivo.

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)


</dt> <dd>

Concede acesso de exclusão.

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**LEITURA \_ CONTROL** (131072)


</dt> <dd>

Concede acesso de leitura ao descritor de segurança e ao proprietário.

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**GRAVAÇÃO \_ DAC** (262144)


</dt> <dd>

Concede acesso de gravação à ACL discricionário.

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**GRAVAÇÃO \_ OWNER** (524288)


</dt> <dd>

Atribui o proprietário de gravação.

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)


</dt> <dd>

Sincroniza o acesso e permite que um processo aguarde até que um objeto entre no estado sinalizado.

</dd> </dl>

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

Descrição textual curta do objeto.

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

Cadeia de caracteres de forma livre que indica o algoritmo ou a ferramenta usada para compactar o arquivo lógico. Se o esquema de compactação for desconhecido ou não for descrito, use "Desconhecido". Se o arquivo lógico for compactado, mas o esquema de compactação for desconhecido ou não for descrito, use "Compactado". Se o arquivo lógico não for compactado, use "Não Compactado".

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

Nome da classe.

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

Nome do sistema de computador.

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

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

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Unidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**corrigido,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Unidade")
</dt> </dl>

Letra da unidade (incluindo os dois-pontos que seguem a letra da unidade) do arquivo. Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

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

Nome de arquivo compatível com OS para o arquivo. Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

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

Cadeia de caracteres de forma livre que identifica o algoritmo ou a ferramenta usada para criptografar um arquivo lógico. Se o esquema de criptografia não for substituído (por motivos de segurança, por exemplo), use "Desconhecido". Se o arquivo for criptografado, mas seu esquema de criptografia for desconhecido ou não for divulgado, use "Criptografado". Se o arquivo lógico não estiver criptografado, use "Não Criptografado".

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

Extensão de nome de arquivo sem o período anterior (ponto).

Essa propriedade é herdada de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

Exemplo: "txt", "mof", "mdb"

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**corrigido,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome do Arquivo")
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

Caminho do arquivo, incluindo barras invertidas à esquerda e à direita. Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

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

Cadeia de caracteres que indica o status atual do objeto. Pode ser definido um status operacional e não operacional. O status operacional pode incluir "OK", "degradado" e "Pred falha". "Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).

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

A **classe \_ DeviceFile CIM** é derivada de CIM [**\_ LogicalFile.**](cim-logicalfile.md)

O WMI não implementa essa classe.

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

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

 

