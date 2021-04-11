---
description: O \_ diretório Win32&\# 32; A classe WMI representa uma entrada de diretório em um sistema de computador que executa o Windows.
ms.assetid: d61cb5ee-8e87-4604-95e6-325c9b543411
ms.tgt_platform: multiple
title: Classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory
- Win32_Directory.Caption
- Win32_Directory.Description
- Win32_Directory.InstallDate
- Win32_Directory.Name
- Win32_Directory.Status
- Win32_Directory.AccessMask
- Win32_Directory.Archive
- Win32_Directory.Compressed
- Win32_Directory.CompressionMethod
- Win32_Directory.CreationClassName
- Win32_Directory.CreationDate
- Win32_Directory.CSCreationClassName
- Win32_Directory.CSName
- Win32_Directory.Drive
- Win32_Directory.EightDotThreeFileName
- Win32_Directory.Encrypted
- Win32_Directory.EncryptionMethod
- Win32_Directory.Extension
- Win32_Directory.FileName
- Win32_Directory.FileSize
- Win32_Directory.FileType
- Win32_Directory.FSCreationClassName
- Win32_Directory.FSName
- Win32_Directory.Hidden
- Win32_Directory.InUseCount
- Win32_Directory.LastAccessed
- Win32_Directory.LastModified
- Win32_Directory.Path
- Win32_Directory.Readable
- Win32_Directory.System
- Win32_Directory.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6185b9c0d427b7410d36f3fddfaf70c0ed8d364b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164123"
---
# <a name="win32_directory-class"></a>\_Classe de diretório Win32

A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ diretório do Win32** representa uma entrada de diretório em um sistema de computador executando o Windows. Um diretório é um tipo de arquivo que agrupa logicamente os arquivos de dados e fornece informações de caminho para os arquivos agrupados. Exemplo: C: \\ Temp. **Win32 \_ O diretório** não inclui diretórios de unidades de rede.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Directory : CIM_Directory
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
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
};
```

## <a name="members"></a>Membros

A classe do **\_ diretório Win32** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe de **\_ diretório Win32** tem esses métodos.



| Método                                                                                             | Descrição                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md)     | Método de classe que altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.<br/>                                                                                                                        |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-win32-directory.md) | Método de classe que altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.<br/>                                                                                                                        |
| [**Compactar**](compress-method-in-class-win32-directory.md)                                       | Método de classe que compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                   |
| [**CompressEx**](compressex-method-in-class-win32-directory.md)                                   | Método de classe que compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                   |
| [**Copiar**](copy-method-in-class-win32-directory.md)                                               | Método de classe que copia o arquivo ou diretório lógico especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.<br/>                                                                                        |
| [**CopyEx**](copyex-method-in-class-win32-directory.md)                                           | Método de classe que copia o arquivo ou diretório lógico especificado no caminho do objeto para o local especificado pelo parâmetro *filename* .<br/>                                                                                   |
| [**Excluir**](delete-method-in-class-win32-directory.md)                                           | Método de classe que exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                      |
| [**DeleteEx**](deleteex-method-in-class-win32-directory.md)                                       | Método de classe que exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                      |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-directory.md)           | Método de classe que determina se o chamador tem as permissões agregadas especificadas pelo argumento *Permissions* não apenas no objeto File, mas no compartilhamento o arquivo ou diretório reside (se estiver em um compartilhamento).<br/> |
| [**Renomear**](rename-method-in-class-win32-directory.md)                                           | Método de classe que renomeia o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                      |
| [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md)                             | Método de classe que obtém a propriedade do arquivo lógico especificado no caminho do objeto.<br/>                                                                                                                                        |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-win32-directory.md)                         | Método de classe que obtém a propriedade do arquivo lógico especificado no caminho do objeto.<br/>                                                                                                                                        |
| [**Descompactar**](uncompress-method-in-class-win32-directory.md)                                   | Método de classe que descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                 |
| [**UncompressEx**](uncompressex-method-in-class-win32-directory.md)                               | Método de classe que descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.<br/>                                                                                                                                 |



 

### <a name="properties"></a>Propriedades

A classe de **\_ diretório Win32** tem essas propriedades.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("direitos de acesso")
</dt> </dl>

Bitmask que representa os direitos de acesso necessários para acessar ou executar operações específicas no diretório. Para valores de bit, consulte [**constantes de direitos de acesso de arquivo e diretório**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).

> [!Note]  
> Em volumes FAT, o valor de **\_ acesso completo** é retornado, o que indica que nenhuma segurança foi definida no objeto.

 

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>Do **arquivo \_ LER \_ os dados (arquivo) ou \_ \_ diretório de lista de arquivos (diretório)** (1)


</dt> <dd>

Concede o direito de ler dados do arquivo. Para um diretório, esse valor concede o direito de listar o conteúdo do diretório.

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>Do **arquivo \_ GRAVAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ arquivo (diretório)** (2)


</dt> <dd>

Concede o direito de gravar dados no arquivo. Para um diretório, esse valor concede o direito de criar um arquivo no diretório.

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>Do **arquivo \_ ACRESCENTAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ subdiretório** (4)


</dt> <dd>

Concede o direito de acrescentar dados ao arquivo. Para um diretório, esse valor concede o direito de criar um subdiretório.

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>Do **arquivo \_ LER \_ ea** (8)


</dt> <dd>

Concede o direito de ler atributos estendidos.

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>Do **arquivo \_ GRAVAR \_ ea** (16)


</dt> <dd>

Concede o direito de gravar atributos estendidos.

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>Do **arquivo \_ EXECUTAR (arquivo) ou \_ atravessamento de arquivo (diretório)** (32)


</dt> <dd>

Concede o direito de executar um arquivo. Para um diretório, o diretório pode ser atravessado.

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>Do **arquivo \_ EXCLUIR \_ filho (diretório)** (64)


</dt> <dd>

Concede o direito de excluir um diretório e todos os arquivos que ele contém (seus filhos), mesmo que os arquivos sejam somente leitura.

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>Do **arquivo \_ \_Atributos de leitura** (128)


</dt> <dd>

Concede o direito de ler atributos de arquivo.

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>Do **arquivo \_ \_Atributos de gravação** (256)


</dt> <dd>

Concede o direito de alterar atributos de arquivo.

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span id="DELETE"></span><span id="delete"></span>**Excluir** (65536)


</dt> <dd>

Concede acesso de exclusão.

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**Ler \_ CONTROLE** (131072)


</dt> <dd>

Concede acesso de leitura ao descritor de segurança e ao proprietário.

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**Gravar \_ DAC** (262144)


</dt> <dd>

Concede acesso de gravação à ACL discricionária.

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**Gravar \_ PROPRIETÁRIO** (524288)


</dt> <dd>

Atribui o proprietário da gravação.

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizar** (1048576)


</dt> <dd>

Sincroniza o acesso e permite que um processo Aguarde um objeto para entrar no estado sinalizado.

</dd> <dt>

<span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>

<span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>**Acesso \_ ao \_Segurança do sistema** (18809343)


</dt> <dd>

Controla a capacidade de obter ou definir a SACL no descritor de segurança de um objeto.

</dd> </dl>

</dd> <dt>

**Arquivar**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("deve ser arquivado")
</dt> </dl>

Indica se o bit de arquivo na pasta foi definido. O bit de arquivo é usado pelos programas de backup para identificar os arquivos cujo backup deve ser feito. Se **for true**, o arquivo deverá ser arquivado.

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

Uma breve descrição textual do objeto.

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

Indica se a pasta foi compactada ou não. O WMI reconhece pastas compactadas usando o próprio WMI ou usando a interface gráfica do usuário; no entanto, ele não reconhece. Arquivos ZIP como compactados. Se **for true**, o arquivo será compactado.

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

Algoritmo ou ferramenta (geralmente um método) usado para compactar o arquivo lógico. Se não for possível (ou não desejar) descrever o esquema de compactação (talvez porque não seja conhecido), use as seguintes palavras: "desconhecido" para representar que não é conhecido se o arquivo lógico está compactado; "Compactado" para representar que o arquivo está compactado, mas o esquema de compactação não é conhecido ou não é divulgado; e "não compactado" para representar que o arquivo lógico não está compactado.

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

Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância. Quando usado com as outras propriedades de chave da classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.

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

Data em que o objeto do sistema de arquivos foi criado. Para obter mais informações sobre como trabalhar com formatos de data e hora do WMI, consulte [tarefas do WMI: datas e horas](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).

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

Nome da classe de criação do sistema de computador de escopo.

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

Nome do computador em que o objeto do sistema de arquivos está armazenado.

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

Uma descrição textual do objeto.

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

Letra da unidade da unidade (incluindo dois-pontos) em que o objeto do sistema de arquivos está armazenado.

Exemplo: "c:"

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**EightDotThreeFileName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("oito pontos três nome de arquivo")
</dt> </dl>

Nome compatível com MS-DOS para a pasta.

Exemplo: "c: \\ progra ~ 1"

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Criptografado**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")
</dt> </dl>

Indica se a pasta foi criptografada ou não. Se for **true**, a pasta será criptografada.

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

Algoritmo ou ferramenta usada para criptografar o arquivo lógico. Se não for possível (ou não desejar) descrever o esquema de criptografia (talvez por motivos de segurança), use as seguintes palavras: "desconhecido" para representar que não é conhecido se o arquivo lógico está criptografado; "Encrypted" para representar que o arquivo está criptografado, mas seu esquema de criptografia não é conhecido ou não é divulgado; e "não criptografado" para representar que o arquivo lógico não está criptografado.

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

Extensão de nome de arquivo para o objeto do sistema de arquivos, sem incluir o ponto (.) que separa a extensão do nome do arquivo.

Exemplos: "txt", "MOF", "mdb"

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome do arquivo")
</dt> </dl>

Nome do arquivo (sem o ponto ou a extensão) do arquivo.

Exemplo: "autoexec"

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Tamanho**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tamanho"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Tamanho do objeto do sistema de arquivos, em bytes. Embora as pastas possuam uma propriedade **filesize** , o valor 0 sempre é retornado. Para determinar o tamanho de uma pasta, use FileSystemObject ou adicione o tamanho de todos os arquivos armazenados na pasta.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Talvez**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de arquivo")
</dt> </dl>

Tipo de arquivo (indicado pela propriedade de **extensão** ).

Por exemplo, um arquivo. mdb provavelmente terá o tipo de arquivo aplicativo Microsoft Access. Um arquivo. asp provavelmente tem o tipo de arquivo documento HTML. Normalmente, as pastas são relatadas simplesmente como pasta.

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

Tipo de sistema de arquivos (NTFS, FAT, FAT32) instalado na unidade em que o arquivo ou pasta está localizado.

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

Indica se o objeto do sistema de arquivos está oculto. Se for **true**, o arquivo ficará oculto.

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

Indica quando o objeto foi instalado. A falta de um valor não indica que o objeto não está instalado.

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

Data em que o arquivo foi acessado pela última vez. Para obter mais informações sobre como trabalhar com formatos de data e hora do WMI, consulte [tarefas do WMI: datas e horas](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).

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

Data em que o arquivo foi modificado pela última vez. Para obter mais informações sobre como trabalhar com formatos de data e hora do WMI, consulte [tarefas do WMI: datas e horas](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).

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

A propriedade Name é uma cadeia de caracteres que representa o nome herdado que serve como uma chave de uma instância de arquivo lógico em um sistema de arquivos. Devem ser fornecidos nomes de caminho completos. Exemplo: C: \\ \\ sistema Windows \\win.ini

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Caminho**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")
</dt> </dl>

Caminho para o arquivo. O caminho inclui as barras invertidas à esquerda e à direita, mas não a letra da unidade ou o nome da pasta.

Para a pasta c: \\ Windows \\ System32 \\ WBEM, o caminho é \\ Windows \\ System32 \\ . Para a pasta c: \\ scripts, o caminho é \\ .

Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Seres**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("legível")
</dt> </dl>

Indica se você pode ler itens na pasta. Se **for true**, o arquivo poderá ser lido.

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

Indica se o objeto é um arquivo do sistema. Se for **true**, o arquivo será um arquivo do sistema

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

A classe do **\_ diretório Win32** é derivada [**do \_ diretório CIM**](cim-directory.md).

**Visão geral**

As pastas são objetos do sistema de arquivos criados para conter outros objetos do sistema de arquivos. No entanto, isso não significa que todas as pastas são semelhantes. Em vez disso, as pastas podem variar consideravelmente. Algumas pastas são pastas do sistema operacional, que geralmente não devem ser modificadas por um script. Algumas pastas são somente leitura, o que significa que os usuários podem acessar o conteúdo dessa pasta, mas não podem adicionar, excluir ou modificar esses conteúdos. Algumas pastas são compactadas para armazenamento ideal, enquanto outras ficam ocultas e não são visíveis para os usuários.

O WMI usa a classe de **\_ diretório do Win32** para gerenciar pastas. Significativamente, as propriedades e os métodos disponíveis nessa classe são idênticos às propriedades e aos métodos disponíveis na classe de [**\_ arquivo**](cim-datafile.md) de arquivos CIM, a classe usada para gerenciar arquivos. Isso significa que, depois de aprender a gerenciar pastas usando o WMI, você terá, sem qualquer trabalho extra, também saberá como gerenciar arquivos.

A classe de associação de [**\_ subdiretório Win32**](win32-subdirectory.md) também é usada para gerenciar arquivos e pastas. A classe de **\_ subdiretório Win32** relaciona uma pasta e suas subpastas imediatas. Por exemplo, na estrutura de pastas C: \\ scripts \\ logs, logs é uma subpasta de scripts e scripts é uma subpasta da pasta raiz C: \\ . No entanto, os logs não são considerados uma subpasta de C: \\ .

Você pode recuperar as propriedades de qualquer pasta no sistema de arquivos usando a classe de **\_ diretório Win32** . As propriedades disponíveis usando essa classe são mostradas na tabela 11,1. Para recuperar as propriedades de uma única pasta, construa uma consulta WQL (linguagem de consulta do Windows) para a classe do **\_ diretório Win32** , certificando-se de incluir o nome da pasta. Por exemplo, essa consulta é vinculada à pasta D: \\ arquivo morto:

`        Copy     "SELECT * FROM Win32_Directory WHERE Name = 'D:\\Archive'"`

Ao especificar um nome de arquivo ou pasta em uma consulta WQL, certifique-se de usar duas barras invertidas ( \\ \\ ) para separar componentes de caminho.

Se você quiser limitar a recuperação de dados a uma única unidade de disco, inclua uma cláusula WHERE especificando a letra da unidade. Por exemplo, essa consulta retorna uma lista de todas as pastas na unidade C:

`"SELECT * FROM Win32_Directory WHERE Drive = 'C:'"`

Se você precisar enumerar todas as pastas em um computador, lembre-se de que essa consulta pode levar um tempo estendido para ser concluída.

## <a name="examples"></a>Exemplos

O exemplo de VBScript a seguir recupera as propriedades da pasta C: \\ scripts.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 Wscript.Echo "Archive: " & objFolder.Archive
 Wscript.Echo "Caption: " & objFolder.Caption
 Wscript.Echo "Compressed: " & objFolder.Compressed
 Wscript.Echo "Compression method: " & objFolder.CompressionMethod
 Wscript.Echo "Creation date: " & objFolder.CreationDate
 Wscript.Echo "Encrypted: " & objFolder.Encrypted
 Wscript.Echo "Encryption method: " & objFolder.EncryptionMethod
 Wscript.Echo "Hidden: " & objFolder.Hidden
 Wscript.Echo "In use count: " & objFolder.InUseCount
 Wscript.Echo "Last accessed: " & objFolder.LastAccessed
 Wscript.Echo "Last modified: " & objFolder.LastModified
 Wscript.Echo "Name: " & objFolder.Name
 Wscript.Echo "Path: " & objFolder.Path
 Wscript.Echo "Readable: " & objFolder.Readable
 Wscript.Echo "System: " & objFolder.System
 Wscript.Echo "Writeable: " & objFolder.Writeable
Next
```



O exemplo de VBScript a seguir retorna uma lista de todas as pastas ocultas em um computador.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("SELECT * FROM Win32_Directory WHERE Hidden = True")
For Each objFile in colFiles
 Wscript.Echo objFile.Name
Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Diretório CIM**](cim-directory.md)
</dt> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

