---
title: Descritores de segurança em arquivos e chaves do registro
description: A ADSI (Active Directory Service Interfaces) pode ser usada para gerenciar e proteger sistemas de arquivos em uma organização, incluindo a capacidade de definir ou modificar ACLs em arquivos ou compartilhamentos de arquivos criados por usuários.
ms.assetid: 7233a82f-fc38-4718-b674-4e6a00666184
ms.tgt_platform: multiple
keywords:
- Descritores de segurança em arquivos e chaves do registro ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11600a495b9a70513b9bd401777e9cdd61449ede
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454346"
---
# <a name="security-descriptors-on-files-and-registry-keys"></a><span data-ttu-id="fd87e-104">Descritores de segurança em arquivos e chaves do registro</span><span class="sxs-lookup"><span data-stu-id="fd87e-104">Security Descriptors on Files and Registry Keys</span></span>

<span data-ttu-id="fd87e-105">A ADSI (Active Directory Service Interfaces) pode ser usada para gerenciar e proteger sistemas de arquivos em uma organização, incluindo a capacidade de definir ou modificar ACLs em arquivos ou compartilhamentos de arquivos criados por usuários.</span><span class="sxs-lookup"><span data-stu-id="fd87e-105">Active Directory Service Interfaces (ADSI) can be used to manage and secure file systems within an organization, including the ability to set or modify ACLs on files or file shares created by users.</span></span> <span data-ttu-id="fd87e-106">Interfaces de segurança, como [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)e [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) definem ACLs em objetos de Active Directory, Exchange, arquivo, compartilhamento de arquivos ou chave do registro.</span><span class="sxs-lookup"><span data-stu-id="fd87e-106">Security interfaces, such as [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist), and [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) set ACLs on Active Directory, Exchange, file, file share, or registry key objects.</span></span> <span data-ttu-id="fd87e-107">Antes de usar essas interfaces, talvez seja necessário modificar o descritor de segurança se ele usar um formato diferente da interface ou se você não tiver direitos de acesso à SACL do descritor de segurança, pois você não é um membro do grupo de administradores de segurança.</span><span class="sxs-lookup"><span data-stu-id="fd87e-107">Before using these interfaces, the security descriptor may need to be modified if it uses a different format from the interface, or if you do not have access rights to the SACL of the security descriptor because you are not a member of the security administrator group.</span></span>

<span data-ttu-id="fd87e-108">Para obter, definir ou modificar o descritor de segurança, use a interface [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) .</span><span class="sxs-lookup"><span data-stu-id="fd87e-108">To get, set, or modify the security descriptor, use the [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) interface.</span></span> <span data-ttu-id="fd87e-109">Essa interface permite que você recupere um descritor de segurança de vários recursos em seu formato original, como o formato ADSI [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), um descritor de segurança bruto ou como uma cadeia de caracteres hexadecimal como usado no Exchange 5,5.</span><span class="sxs-lookup"><span data-stu-id="fd87e-109">This interface enables you to retrieve a security descriptor from various resources in its original format, such as the ADSI format [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), a raw security descriptor, or as a hexadecimal string as used in Exchange 5.5.</span></span> <span data-ttu-id="fd87e-110">Quando recuperada, você pode convertê-la em outro formato, por exemplo, de um descritor de segurança bruto para **IADsSecurityDescriptor**.</span><span class="sxs-lookup"><span data-stu-id="fd87e-110">When retrieved, you can convert it to another format, for example, from a raw security descriptor to **IADsSecurityDescriptor**.</span></span> <span data-ttu-id="fd87e-111">Em seguida, você pode gravar o novo formato de volta no recurso.</span><span class="sxs-lookup"><span data-stu-id="fd87e-111">You can then write the new format back to the resource.</span></span>

<span data-ttu-id="fd87e-112">Alguns dos valores de propriedade [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) , como [**AccessMask**](iadsaccesscontrolentry-property-methods.md) e **AceFlags**, serão diferentes para tipos de objeto diferentes.</span><span class="sxs-lookup"><span data-stu-id="fd87e-112">Some of the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) property values, such as [**AccessMask**](iadsaccesscontrolentry-property-methods.md) and **AceFlags**, will be different for different object types.</span></span> <span data-ttu-id="fd87e-113">Por exemplo, um objeto Active Directory usará o membro de **\_ \_ \_ leitura genérico do ADS** da enumeração de [**\_ \_ enumeração de direitos do ADS**](/windows/win32/api/iads/ne-iads-ads_rights_enum) para a propriedade **IADsAccessControlEntry. AccessMask** , mas o direito de acesso equivalente para um objeto de arquivo será **\_ \_ leitura genérica de arquivo**.</span><span class="sxs-lookup"><span data-stu-id="fd87e-113">For example, an Active Directory object will use the **ADS\_RIGHT\_GENERIC\_READ** member of the [**ADS\_RIGHTS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_rights_enum) enumeration for the **IADsAccessControlEntry.AccessMask** property, but the equivalent access right for a file object is **FILE\_GENERIC\_READ**.</span></span> <span data-ttu-id="fd87e-114">Não é seguro pressupor que todos os valores de propriedade serão os mesmos para objetos Active Directory e objetos não Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fd87e-114">It is not safe to assume that all property values will be the same for Active Directory objects and non-Active Directory objects.</span></span> <span data-ttu-id="fd87e-115">A lista a seguir mostra as propriedades **IADsAccessControlEntry** que diferem para objetos não Active Directory e onde os valores adequados podem ser obtidos.</span><span class="sxs-lookup"><span data-stu-id="fd87e-115">The following list shows the **IADsAccessControlEntry** properties that differ for non-Active Directory objects and where the proper values can be obtained.</span></span>

<dl> <dt>

<span data-ttu-id="fd87e-116"><span id="AccessMask"></span><span id="accessmask"></span><span id="ACCESSMASK"></span>[**AccessMask**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="fd87e-116"><span id="AccessMask"></span><span id="accessmask"></span><span id="ACCESSMASK"></span>[**AccessMask**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="fd87e-117">Para obter mais informações e uma lista de valores possíveis para objetos de compartilhamento de arquivos ou arquivos, consulte [segurança de arquivos e direitos de acesso](/windows/desktop/FileIO/file-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="fd87e-117">For more information and a list of possible values for file or file share objects, see [File Security and Access Rights](/windows/desktop/FileIO/file-security-and-access-rights).</span></span>

<span data-ttu-id="fd87e-118">Para obter mais informações e uma lista de valores possíveis para objetos do registro, consulte [segurança da chave do registro e direitos de acesso](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="fd87e-118">For more information and a list of possible values for registry objects, see [Registry Key Security and Access Rights](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span></span>

</dd> <dt>

<span data-ttu-id="fd87e-119"><span id="AceType"></span><span id="acetype"></span><span id="ACETYPE"></span>[**AceType**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="fd87e-119"><span id="AceType"></span><span id="acetype"></span><span id="ACETYPE"></span>[**AceType**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="fd87e-120">Para obter mais informações, consulte o membro **AceType** da estrutura de [**\_ cabeçalho Ace**](/windows/desktop/api/winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="fd87e-120">For more information, see the **AceType** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fd87e-121"><span id="AceFlags"></span><span id="aceflags"></span><span id="ACEFLAGS"></span>[**AceFlags**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="fd87e-121"><span id="AceFlags"></span><span id="aceflags"></span><span id="ACEFLAGS"></span>[**AceFlags**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="fd87e-122">Para obter mais informações, consulte o membro **AceFlags** da estrutura de [**\_ cabeçalho Ace**](/windows/desktop/api/winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="fd87e-122">For more information, see the **AceFlags** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fd87e-123"><span id="Flags"></span><span id="flags"></span><span id="FLAGS"></span>[**Flags**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="fd87e-123"><span id="Flags"></span><span id="flags"></span><span id="FLAGS"></span>[**Flags**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="fd87e-124">Contém zero ou uma combinação de um ou mais dos seguintes valores de WinNT. h.</span><span class="sxs-lookup"><span data-stu-id="fd87e-124">Contains zero or a combination of one or more of the following values from WinNT.h.</span></span>

<dl> <dt>

<span data-ttu-id="fd87e-125"><span id="ACE_OBJECT_TYPE_PRESENT__1_"></span><span id="ace_object_type_present__1_"></span>**Ace \_ Tipo de objeto \_ \_ presente** (1)</span><span class="sxs-lookup"><span data-stu-id="fd87e-125"><span id="ACE_OBJECT_TYPE_PRESENT__1_"></span><span id="ace_object_type_present__1_"></span>**ACE\_OBJECT\_TYPE\_PRESENT** (1)</span></span>
</dt> <dd>

<span data-ttu-id="fd87e-126">[**Objecttype**](iadsaccesscontrolentry-property-methods.md) contém um valor válido.</span><span class="sxs-lookup"><span data-stu-id="fd87e-126">[**ObjectType**](iadsaccesscontrolentry-property-methods.md) contains a valid value.</span></span>

</dd> <dt>

<span data-ttu-id="fd87e-127"><span id="ACE_INHERITED_OBJECT_TYPE_PRESENT__2_"></span><span id="ace_inherited_object_type_present__2_"></span>**Ace \_ Tipo de objeto HERDAdo \_ \_ \_ presente** (2)</span><span class="sxs-lookup"><span data-stu-id="fd87e-127"><span id="ACE_INHERITED_OBJECT_TYPE_PRESENT__2_"></span><span id="ace_inherited_object_type_present__2_"></span>**ACE\_INHERITED\_OBJECT\_TYPE\_PRESENT** (2)</span></span>
</dt> <dd>

<span data-ttu-id="fd87e-128">[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md) contém um valor válido.</span><span class="sxs-lookup"><span data-stu-id="fd87e-128">[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md) contains a valid value.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fd87e-129"><span id="ObjectType"></span><span id="objecttype"></span><span id="OBJECTTYPE"></span>[**ObjectType**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="fd87e-129"><span id="ObjectType"></span><span id="objecttype"></span><span id="OBJECTTYPE"></span>[**ObjectType**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="fd87e-130">Para obter mais informações, consulte o membro **objecttype** da [**\_ ACE de \_ objeto \_ acesso negado**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), [**Access \_ \_ \_ Ace Object allowed**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)e estruturas semelhantes.</span><span class="sxs-lookup"><span data-stu-id="fd87e-130">For more information, see the **ObjectType** member of the [**ACCESS\_DENIED\_OBJECT\_ACE**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace), and similar structures.</span></span> <span data-ttu-id="fd87e-131">Essa propriedade não deve ser definida ou modificada para objetos não Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fd87e-131">This property should not be set or modified for non-Active Directory objects.</span></span>

</dd> <dt>

<span data-ttu-id="fd87e-132"><span id="InheritedObjectType"></span><span id="inheritedobjecttype"></span><span id="INHERITEDOBJECTTYPE"></span>[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="fd87e-132"><span id="InheritedObjectType"></span><span id="inheritedobjecttype"></span><span id="INHERITEDOBJECTTYPE"></span>[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="fd87e-133">Para obter mais informações, consulte o membro **InheritedObjectType** da [**\_ ACE de \_ objeto \_ acesso negado**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), [**Access \_ \_ \_ Ace Object allowed**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)e estruturas semelhantes.</span><span class="sxs-lookup"><span data-stu-id="fd87e-133">For more information, see the **InheritedObjectType** member of the [**ACCESS\_DENIED\_OBJECT\_ACE**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace), and similar structures.</span></span> <span data-ttu-id="fd87e-134">Essa propriedade não deve ser definida ou modificada para objetos não Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fd87e-134">This property should not be set or modified for non-Active Directory objects.</span></span>

</dd> </dl>

<span data-ttu-id="fd87e-135">Normalmente, [**IADsSecurityUtility. GetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-getsecuritydescriptor) recuperará todas as partes do descritor de segurança, como Owner, Group, SACL ou DACL.</span><span class="sxs-lookup"><span data-stu-id="fd87e-135">Normally, [**IADsSecurityUtility.GetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-getsecuritydescriptor) will retrieve all parts of the security descriptor, such as owner, group, SACL, or DACL.</span></span> <span data-ttu-id="fd87e-136">Da mesma forma, [**IADsSecurityUtility. SetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-setsecuritydescriptor) substituirá todas as partes do descritor de segurança por padrão.</span><span class="sxs-lookup"><span data-stu-id="fd87e-136">Similarly, [**IADsSecurityUtility.SetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-setsecuritydescriptor) will overwrite all parts of the security descriptor by default.</span></span> <span data-ttu-id="fd87e-137">Você pode usar a propriedade [**IADsSecurityUtility. SecurityMask**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-get_securitymask) para especificar partes individuais do descritor de segurança a serem recuperadas ou definidas.</span><span class="sxs-lookup"><span data-stu-id="fd87e-137">You can use the [**IADsSecurityUtility.SecurityMask**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-get_securitymask) property to specify individual parts of the security descriptor to retrieve or set.</span></span> <span data-ttu-id="fd87e-138">Por exemplo, você pode definir **SecurityMask** para [**a \_ \_ \_ DACL de informações de segurança do ADS**](/windows/win32/api/iads/ne-iads-ads_security_info_enum) antes de chamar **GetSecurityDescriptor** para recuperar apenas a DACL sem recuperar as outras partes do descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="fd87e-138">For example, you can set **SecurityMask** to [**ADS\_SECURITY\_INFO\_DACL**](/windows/win32/api/iads/ne-iads-ads_security_info_enum) before calling **GetSecurityDescriptor** to only retrieve the DACL without retrieving the other parts of the security descriptor.</span></span>

<span data-ttu-id="fd87e-139">Para obter mais informações e um exemplo de código que usa a interface [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) para adicionar uma ACE a um arquivo, consulte [exemplo de código para adicionar uma ACE a um arquivo](example-code-for-adding-an-ace-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="fd87e-139">For more information and a code example that uses the [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) interface to add an ACE to a file, see [Example Code for Adding an ACE to a File](example-code-for-adding-an-ace-to-a-file.md).</span></span>

<span data-ttu-id="fd87e-140">O código de exemplo a seguir fornece os identificadores de constante para os objetos de arquivo, compartilhamento de arquivo e registro para as propriedades [**AccessMask**](iadsaccesscontrolentry-property-methods.md), **AceType**, **AceFlags** e **Flags** para uso com Visual Basic e Microsoft Visual Basic Scripting Edition.</span><span class="sxs-lookup"><span data-stu-id="fd87e-140">The following example code provides the constant identifiers for file, file share and registry objects for the [**AccessMask**](iadsaccesscontrolentry-property-methods.md), **AceType**, **AceFlags**, and **Flags** properties for use with Visual Basic and Microsoft Visual Basic Scripting Edition.</span></span>


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



 

 