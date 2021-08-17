---
title: Descritores de segurança em arquivos e chaves do registro
description: A ADSI (Active Directory Service Interfaces) pode ser usada para gerenciar e proteger sistemas de arquivos em uma organização, incluindo a capacidade de definir ou modificar ACLs em arquivos ou compartilhamentos de arquivos criados por usuários.
ms.assetid: 7233a82f-fc38-4718-b674-4e6a00666184
ms.tgt_platform: multiple
keywords:
- Descritores de segurança em arquivos e chaves do registro ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae567e9550989153f0b85207be49a729bc0499c320f410c92fc993269d997da7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119333216"
---
# <a name="security-descriptors-on-files-and-registry-keys"></a>Descritores de segurança em arquivos e chaves do registro

A ADSI (Active Directory Service Interfaces) pode ser usada para gerenciar e proteger sistemas de arquivos em uma organização, incluindo a capacidade de definir ou modificar ACLs em arquivos ou compartilhamentos de arquivos criados por usuários. interfaces de segurança, como [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)e [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) , definem ACLs em Active Directory, Exchange, arquivo, compartilhamento de arquivos ou objetos de chave do registro. Antes de usar essas interfaces, talvez seja necessário modificar o descritor de segurança se ele usar um formato diferente da interface ou se você não tiver direitos de acesso à SACL do descritor de segurança, pois você não é um membro do grupo de administradores de segurança.

Para obter, definir ou modificar o descritor de segurança, use a interface [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) . essa interface permite que você recupere um descritor de segurança de vários recursos em seu formato original, como o formato ADSI [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), um descritor de segurança bruto ou como uma cadeia de caracteres hexadecimal como usado no Exchange 5,5. Quando recuperada, você pode convertê-la em outro formato, por exemplo, de um descritor de segurança bruto para **IADsSecurityDescriptor**. Em seguida, você pode gravar o novo formato de volta no recurso.

Alguns dos valores de propriedade [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) , como [**AccessMask**](iadsaccesscontrolentry-property-methods.md) e **AceFlags**, serão diferentes para tipos de objeto diferentes. Por exemplo, um objeto Active Directory usará o membro de **\_ \_ \_ leitura genérico do ADS** da enumeração de [**\_ \_ enumeração de direitos do ADS**](/windows/win32/api/iads/ne-iads-ads_rights_enum) para a propriedade **IADsAccessControlEntry. AccessMask** , mas o direito de acesso equivalente para um objeto de arquivo será **\_ \_ leitura genérica de arquivo**. Não é seguro pressupor que todos os valores de propriedade serão os mesmos para objetos Active Directory e objetos não Active Directory. A lista a seguir mostra as propriedades **IADsAccessControlEntry** que diferem para objetos não Active Directory e onde os valores adequados podem ser obtidos.

<dl> <dt>

<span id="AccessMask"></span><span id="accessmask"></span><span id="ACCESSMASK"></span>[**AccessMask**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Para obter mais informações e uma lista de valores possíveis para objetos de compartilhamento de arquivos ou arquivos, consulte [segurança de arquivos e direitos de acesso](/windows/desktop/FileIO/file-security-and-access-rights).

Para obter mais informações e uma lista de valores possíveis para objetos do registro, consulte [segurança da chave do registro e direitos de acesso](/windows/desktop/SysInfo/registry-key-security-and-access-rights).

</dd> <dt>

<span id="AceType"></span><span id="acetype"></span><span id="ACETYPE"></span>[**AceType**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Para obter mais informações, consulte o membro **AceType** da estrutura de [**\_ cabeçalho Ace**](/windows/desktop/api/winnt/ns-winnt-ace_header) .

</dd> <dt>

<span id="AceFlags"></span><span id="aceflags"></span><span id="ACEFLAGS"></span>[**AceFlags**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Para obter mais informações, consulte o membro **AceFlags** da estrutura de [**\_ cabeçalho Ace**](/windows/desktop/api/winnt/ns-winnt-ace_header) .

</dd> <dt>

<span id="Flags"></span><span id="flags"></span><span id="FLAGS"></span>[**Flags**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Contém zero ou uma combinação de um ou mais dos seguintes valores de WinNT. h.

<dl> <dt>

<span id="ACE_OBJECT_TYPE_PRESENT__1_"></span><span id="ace_object_type_present__1_"></span>**Ace \_ Tipo de objeto \_ \_ presente** (1)
</dt> <dd>

[**Objecttype**](iadsaccesscontrolentry-property-methods.md) contém um valor válido.

</dd> <dt>

<span id="ACE_INHERITED_OBJECT_TYPE_PRESENT__2_"></span><span id="ace_inherited_object_type_present__2_"></span>**Ace \_ Tipo de objeto HERDAdo \_ \_ \_ presente** (2)
</dt> <dd>

[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md) contém um valor válido.

</dd> </dl> </dd> <dt>

<span id="ObjectType"></span><span id="objecttype"></span><span id="OBJECTTYPE"></span>[**ObjectType**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Para obter mais informações, consulte o membro **objecttype** da [**\_ ACE de \_ objeto \_ acesso negado**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), [**Access \_ \_ \_ Ace Object allowed**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)e estruturas semelhantes. Essa propriedade não deve ser definida ou modificada para objetos não Active Directory.

</dd> <dt>

<span id="InheritedObjectType"></span><span id="inheritedobjecttype"></span><span id="INHERITEDOBJECTTYPE"></span>[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Para obter mais informações, consulte o membro **InheritedObjectType** da [**\_ ACE de \_ objeto \_ acesso negado**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), [**Access \_ \_ \_ Ace Object allowed**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)e estruturas semelhantes. Essa propriedade não deve ser definida ou modificada para objetos não Active Directory.

</dd> </dl>

Normalmente, [**IADsSecurityUtility. GetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-getsecuritydescriptor) recuperará todas as partes do descritor de segurança, como Owner, Group, SACL ou DACL. Da mesma forma, [**IADsSecurityUtility. SetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-setsecuritydescriptor) substituirá todas as partes do descritor de segurança por padrão. Você pode usar a propriedade [**IADsSecurityUtility. SecurityMask**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-get_securitymask) para especificar partes individuais do descritor de segurança a serem recuperadas ou definidas. Por exemplo, você pode definir **SecurityMask** para [**a \_ \_ \_ DACL de informações de segurança do ADS**](/windows/win32/api/iads/ne-iads-ads_security_info_enum) antes de chamar **GetSecurityDescriptor** para recuperar apenas a DACL sem recuperar as outras partes do descritor de segurança.

Para obter mais informações e um exemplo de código que usa a interface [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) para adicionar uma ACE a um arquivo, consulte [exemplo de código para adicionar uma ACE a um arquivo](example-code-for-adding-an-ace-to-a-file.md).

o código de exemplo a seguir fornece os identificadores de constante para objetos de arquivo, compartilhamento de arquivo e registro para as propriedades [**AccessMask**](iadsaccesscontrolentry-property-methods.md), **AceType**, **AceFlags** e **Flags** para uso com Visual Basic e o Microsoft Visual Basic scripting Edition.


```VB
' Identifiers for the IADsAccessControlEntry.AccessMask property for file,
' file share, and registry objects.
Const DELETE = &H10000
Const READ_CONTROL = &H20000
Const WRITE_DAC = &H40000
Const WRITE_OWNER = &H80000
Const SYNCHRONIZE = &H100000

Const STANDARD_RIGHTS_REQUIRED = &HF0000

Const STANDARD_RIGHTS_READ = &H20000
Const STANDARD_RIGHTS_WRITE = &H20000
Const STANDARD_RIGHTS_EXECUTE = &H20000

Const STANDARD_RIGHTS_ALL = &H1F0000

Const SPECIFIC_RIGHTS_ALL = &HFFFF

' Identifiers for the IADsAccessControlEntry.AccessMask property for file and
' file share objects.
Const FILE_READ_DATA = &H1                  '  file & pipe
Const FILE_LIST_DIRECTORY = &H1             '  directory

Const FILE_WRITE_DATA = &H2                 '  file & pipe
Const FILE_ADD_FILE = &H2                   '  directory

Const FILE_APPEND_DATA = &H4                '  file
Const FILE_ADD_SUBDIRECTORY = &H4           '  directory
Const FILE_CREATE_PIPE_INSTANCE = &H4       '  named pipe

Const FILE_READ_EA = &H8                    '  file & directory

Const FILE_WRITE_EA = &H10                  '  file & directory

Const FILE_EXECUTE = &H20                   '  file
Const FILE_TRAVERSE = &H20                  '  directory

Const FILE_DELETE_CHILD = &H40              '  directory

Const FILE_READ_ATTRIBUTES = &H80           '  all

Const FILE_WRITE_ATTRIBUTES = &H100         '  all

Const FILE_ALL_ACCESS = STANDARD_RIGHTS_REQUIRED Or SYNCHRONIZE Or &H1FF

Const FILE_GENERIC_READ = STANDARD_RIGHTS_READ Or FILE_READ_DATA Or FILE_READ_ATTRIBUTES Or _
                          FILE_READ_EA Or SYNCHRONIZE

Const FILE_GENERIC_WRITE = STANDARD_RIGHTS_WRITE Or FILE_WRITE_DATA Or FILE_WRITE_ATTRIBUTES Or _
                           FILE_WRITE_EA Or FILE_APPEND_DATA Or SYNCHRONIZE

Const FILE_GENERIC_EXECUTE = STANDARD_RIGHTS_EXECUTE Or FILE_READ_ATTRIBUTES Or FILE_EXECUTE Or SYNCHRONIZE


' Identifiers for the IADsAccessControlEntry.AccessMask property for registry
' objects.
Const KEY_QUERY_VALUE = &H1
Const KEY_SET_VALUE = &H2
Const KEY_CREATE_SUB_KEY = &H4
Const KEY_ENUMERATE_SUB_KEYS = &H8
Const KEY_NOTIFY = &H10
Const KEY_CREATE_LINK = &H20
Const KEY_WOW64_32KEY = &H200
Const KEY_WOW64_64KEY = &H100
Const KEY_WOW64_RES = &H300

Const KEY_READ = ((STANDARD_RIGHTS_READ Or KEY_QUERY_VALUE Or KEY_ENUMERATE_SUB_KEYS Or KEY_NOTIFY) And _
                  (Not SYNCHRONIZE))

Const KEY_WRITE = ((STANDARD_RIGHTS_WRITE Or KEY_SET_VALUE Or KEY_CREATE_SUB_KEY) And (Not SYNCHRONIZE))

Const KEY_EXECUTE = ((KEY_READ) And (Not SYNCHRONIZE))

Const KEY_ALL_ACCESS = ((STANDARD_RIGHTS_ALL Or KEY_QUERY_VALUE Or KEY_SET_VALUE Or KEY_CREATE_SUB_KEY Or _
                         KEY_ENUMERATE_SUB_KEYS Or KEY_NOTIFY Or KEY_CREATE_LINK) And (Not SYNCHRONIZE))
    

' Identifiers for the IADsAccessControlEntry.AceFlags property for file and
' file share objects.
Const OBJECT_INHERIT_ACE = &H1
Const CONTAINER_INHERIT_ACE = &H2
Const NO_PROPAGATE_INHERIT_ACE = &H4
Const INHERIT_ONLY_ACE = &H8
Const INHERITED_ACE = &H10
    

' Identifiers for the IADsAccessControlEntry.Flags property.
Const ACE_OBJECT_TYPE_PRESENT = 1
Const ACE_INHERITED_OBJECT_TYPE_PRESENT = 2
```



 

 